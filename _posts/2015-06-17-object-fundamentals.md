---
layout: post
title: "Object Fundamentals"
tags:
- Objects
- Inheritance
- Types
excerpt: "Objects, Inheritance, and Types in JavaScript"
---
# Common JavaScript Types

### Primitive Objects

| **Name**  | **Value**              |
| :-------- | :----------------------|
| Undefined | `undefined`            |
| Null      | `null`                 |
| Boolean   | `true`                 |
| String    | `"foo"`                |
| Number    | `3.14159`              |
| Object    | `{ bar: "baz" }`       |
| Function  | `function qux() {...}` |
| Array     | `[ "hoge", 42 ]`       |
| RegExp    | `/piyo/`               |

<!-- <code data-gist-id="ca3cd7e9851b405f934d"></code> -->

### Special Objects

| **Name**  | **Value**               |
| :-------- | :-----------------------|
| Function  | `function qux() {...}'  |
| Array     | `[ "hoge", 42 ]'        |
| RegExp    | `/piyo/'                |

----

### What is a JavaScript Object?
An Object is a set of **name**/**value** pairs, also known as **key**/**value** pairs.

  * A key name must be in the form of a string.
  * Each string can be associated with any type (primitive type or object type)
      * Primitive types are passed by their value.
      * Object types are passed by their reference.
