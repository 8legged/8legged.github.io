---
layout: post
title: "Obeject-Oriented vs. Functional Programming"
categories: []
tags: ['OOP', 'Object-Oriented Programming', 'Functional Programming']
published: true
excerpt: "A stripped down version of Bill Gathen's article on CodeNewbie"
---

> This is a stripped down version of [Bill Gathen](http://billgathen.com/)'s
article, which is meant to highlight points that I'm most interested in. The
original is
[here](http://www.codenewbie.org/blogs/object-oriented-programming-vs-functional-programming).

Programs have two primary components:

* Data - stuff a program knows
* Behaviors - stuff a program can do to/with the data

Object-Oriented Programming and Functional Programming use different approaches
for how to best create understandable and flexible programs.

* **OOP says that bringing together data and its associated behavior in a single
location (called an “object”) makes it easier to understand how a program
works**.

* **FP says that data and behavior are distinctively different things and should
be kept separate for clarity**.

Our examples will use Ruby to look at the two approaches -- other languages
also support both *,e.g., JavaScript and Scala*.

Let’s say you run a company and you’ve just decided to give all your employees a
$10,000.00 raise. How could we write a command-line script to make this change?

You most likely have all your employee records in a database with two
attributes: the **employee’s name** and a **current salary**. We’ll ignore the
part where you transfer the data to and from the database, focusing on the
“giving a raise” feature.

### An approach using OOP:

{% highlight ruby %}
class Employee
  def initialize(name, salary)
    @name = name
    @salary = salary
  end

  def change_salary(amt)
    @salary = @salary + amt
  end

  def description
    "#{@name} makes #{@salary}"
  end
end
{% endhighlight %}

This is our class, which we’ll use to generate new `Employee` objects. Most OOP
languages use classes to generate objects in the same way a cook uses recipes to
create meals -- the **classes tell us how to construct the object, how it should
behave, what it looks like, etc**.

The `@`-sign before a variable makes it an “instance” variable: a variable that
lives inside the object (aka instance) and can be used in its methods without
having been passed in as an argument, the way `change_salary` uses `@salary`.
The `initialize` method takes the name and salary we passed to new and stores
them in the `@name` and `@salary` instance variables.

All the methods except for `initialize` are “instance methods” which also live
inside the object (aka instance) and can be called on the object itself.

Now we’ll generate some objects to work with.

{% highlight ruby %}
employees = [
  Employee.new("Bob", 100000.0),
  Employee.new("Jane", 125000.0)
]
{% endhighlight %}

Each `Employee.new(...)` call creates an object with data (`@name` and
`@salary`) and behavior (`change_salary` and `description`). We call `new`
twice, which gives us a pair of objects representing Bob and Jane stored in an
array we are calling “employees”. In a normal app, this array of objects is
typically returned by the database.

Now let’s give out those raises.

{% highlight ruby %}
employees.each do |emp|
  emp.change_salary(10000.0)
end
{% endhighlight %}

We call the `each` method on our array of employees, which hands us each
employee in turn and stores it in a local variable called emp. We call the
“change_salary” method we defined in our class, passing in a value of 10000.0.
This adds our $10K to the employee’s salary and stores the sum in `@salary`,
overwriting the existing value.

{% highlight ruby %}
employees.each do |emp|
  puts emp.description
end
{% endhighlight %}

Finally we can generate some output to make sure the results are what we
intended, using the `description` method to build our output string instead of
trying to access the data fields (`@salary` and `@name`) directly. This is
called “data hiding” and it allows us to change the names of our instance
variables without forcing the users of our object to change how they use it.

We use `each` again to output the results. This time, we use `puts` (`put` *`string`*)
and call the `description` method for each of our objects to print their
description, as we defined in our class.

**Important things to notice about the OOP implementation:**

* Data is supplied to an object at the time the object is created (when we
called the ‘new’ method)

* Then we use methods on that object (`change_salary` and `description`) to
interact with our stored data

* We have a good place for the behaviors associated with our objects,
making them easy to find if we’re unfamiliar with the code or refreshing our
memory

* Method names document object behavior, familiarizing us with the code

* The object is an obvious location to add behaviors as complexity increases

### Using an FP approach:

{% highlight ruby %}
employees = [
  [ "Bob",  100000.0 ],
  [ "Jane", 125000.0 ]
]
{% endhighlight %}

**This time our data structure is an array of arrays instead of an array of
objects containing the values**. FP prefers to keep data in plain arrays and/or
hashes and not “complicate” data by mixing it with behavior.

Instead of converting the data to an object and then calling methods on it, we
write a pair of standalone methods called `change_salaries` (plural) and
`change_salary` (singular). We pass `change_salaries` two arguments: the array
of arrays representing our data and the change amount. `change_salaries` uses
`map` instead of the `each` method we used for OOP.

**FP leans very heavily on tiny methods that do one small part of a larger job,
delegating the details to other tiny methods**. Combining small methods into a
larger task is called “composition”.

In our example...

* `change_salaries` has one job: call `change_salary` for each employee in the
employees array and return the values as a new array. `change_salaries`
delegates the calculation of the new salary to `change_salary`, allowing
`change_salaries` to focus entirely on handling the set of employees.

* `change_salary` also has one job: return a copy of a single employee with the
salary field updated.

A benefit of this approach is if we had a single employee we wanted to change the
salary for, we could call `change_salary` directly!

While OOP also uses it, **composition is a cornerstone of the FP mindset**.


{% highlight ruby %}
happier_employees = change_salaries(employees, 10000.0)
{% endhighlight %}

Because we don’t have objects, `change_salaries` requires that we pass in not
just the amount, but also the data we want to modify. This method returns the
updated data, which we'll store in `happier_employees`.

{% highlight ruby %}
happier_employees.each do |emp|
  puts "#{emp[0]} makes #{emp[1]}"
end
{% endhighlight %}

Finally, we use ‘each’ to go through every record in `happier_employees` and
generate the output message. This fits the FP model because FP likes to view
everything as a data transformation: you start some data, apply transformations
(in this case, adding $10K) and generate a new data.

Notice there are fewer lines of code, mainly because we don’t build the class
for creating our objects.

Another important thing to note is that in the OOP version `change_salary` used
`each` to process each employee, but the FP version uses `map`. Instead of
changing the original value, ’map’ creates a copy of the array containing the
return value of each pass. When all elements have been processed, `map` hands us
the copy with all the new values, which we store in `happier_employees`. The
original array is untouched!

**The idea of not changing the contents (or “state”) of a variable once it’s
been created is called immutability and is another key aspect of FP**.

In our OOP example, the contents of the employees array changes over time:

* Before `change_salary` is applied the salaries are 100K and 125K
* Afterwards salaries are 110K and 135K!

This means we won't know which value we’ll have at any given point. The program
must walk through the flow to see if `change_salary` has been called, which can
be difficult as complexity increases.

* The FP version avoids this as `employees` represent the “before” state and
  `happier_employees` represents the “after” state. Their values never change.

### Which one should you use?
[Michael Fogus](http://blog.fogus.me/), author of “Functional JavaScript”,
[suggests](http://blog.fogus.me/2013/07/22/fp-vs-oo-from-the-trenches/) a simple two-point guideline:

* When dealing with data *about* people, FP works well
* When trying to *simulate* people, OOP works well

Our example is “data about people” -- since we’re changing the salary directly
-- so FP is shorter and simpler.

If we had a feature like “employee requests time off”, requiring a more complex
interaction with the data -- likely creating a “time-off request” object
attached to the employee -- then OOP might be a better fit.
