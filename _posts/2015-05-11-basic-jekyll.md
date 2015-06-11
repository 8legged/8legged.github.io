---
layout: post
title: "Basic Tasks: Jekyll"
tags:
- jekyll
published: true
---
<br />
You can update your site name, avatar and other options using the
_config.yml file in the root of your repository<br />
![_config.yml]({{ site.baseurl }}/images/config.png)

### Highlighting Code
To find the appropriate identifier to use for the language you want to
highlight, look for the “short name” on Pygments’
[lexers page](http://pygments.org/docs/lexers/) or the Rouge
[wiki](https://github.com/jneen/rouge/wiki/List-of-supported-languages-and-lexers).

##### Highlighted Code Example
{% highlight ruby %}
# ruby
def foo
  puts 'foo'
end
{% endhighlight %}

##### An embeded Gist
{% gist 8legged/ed0ed64ddd02a71c1883 tiny-gist-example.js %}
<br />

##### Highlighted Code Example
{% highlight javascript %}
// javascript
var num = 1;
var newNum = ++num;

newNum;
2

num;
2
{% endhighlight %}

For more information head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.
