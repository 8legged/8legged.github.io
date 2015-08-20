---
layout: post
title: "CSS Selectors"
categories: []
tags: ['CSS', 'Selectors']
published: true
excerpt: "Notes & Resources on CSS Selectors"
---
[CSS 3 Selectors](http://www.w3.org/TR/css3-selectors/)

## Selectors
A Selector represents a structure. This structure can be used as a condition
(e.g. in a CSS rule) that determines which elements a selector matches in the
document tree, or as a flat description of the HTML or XML fragment
corresponding to that structure.

Selectors may range from simple element names to rich contextual representations.

For future searchers, there is a way to escape without plugins, use the code below:

<!-- `{{ "{% this " }}%}` -->
<!-- and for tags, to escape `{{ this }}` use: -->
<!-- `{{ "{{ this " }}}}` -->

it is possible to disable liquid processing engine using the raw tag:
<!-- {% raw  %}
{% this %}
{% endraw %} -->
will display




###### The following table summarizes the Selector syntax:

| **Pattern** | **Meaning** | **Described in section** |
| :------ |:-------:| --------------------:|
| * | any element | [Universal selector](http://www.w3.org/TR/selectors/#universal-selector)
| `E` | an element of type E | [Type selector](http://www.w3.org/TR/selectors/#type-selectors)
| `E[foo]` | an E element with a "foo" attribute | [Attribute selectors](http://www.w3.org/TR/selectors/#attribute-selectors)
| `E[foo="bar"]` | an E element whose "foo" attribute value is exactly equal to "bar" | [Attribute selectors](http://www.w3.org/TR/selectors/#attribute-selectors)
| `E[foo~="bar"]` | an E element whose "foo" attribute value is a list of whitespace-separated values, one of which is exactly equal to "bar" | [Attribute selectors](http://www.w3.org/TR/selectors/#attribute-selectors)
| `E[foo^="bar"]` | an E element whose "foo" attribute value begins exactly with the string "bar" | [Attribute selectors](http://www.w3.org/TR/selectors/#attribute-selectors)
| `E[foo$="bar"]` | an E element whose "foo" attribute value ends exactly with the string "bar" | [Attribute selectors](http://www.w3.org/TR/selectors/#attribute-selectors)
| `E[foo*="bar"]` | an E element whose "foo" attribute value contains the substring "bar" | [Attribute selectors](http://www.w3.org/TR/selectors/#attribute-selectors)
| `E[foo|="en"]` | an E element whose "foo" attribute has a hyphen-separated list of values beginning (from the left) with "en" | [Attribute selectors](http://www.w3.org/TR/selectors/#attribute-selectors)
| `E:root` | an E element, root of the document | [Structural pseudo-classes](http://www.w3.org/TR/selectors/#structural-pseudos)
| `E:nth-child(n)` | an E element, the n-th child of its parent | [Structural pseudo-classes](http://www.w3.org/TR/selectors/#structural-pseudos)
| `E:nth-last-child(n)` | an E element, the n-th child of its parent, counting from the last one | [Structural pseudo-classes](http://www.w3.org/TR/selectors/#structural-pseudos)
| `E:nth-of-type(n)` | an E element, the n-th sibling of its type | [Structural pseudo-classes](http://www.w3.org/TR/selectors/#structural-pseudos)
| `E:nth-last-of-type(n)` | an E element, the n-th sibling of its type, counting from the last one | [Structural pseudo-classes](http://www.w3.org/TR/selectors/#structural-pseudos)
| `E:first-child` | an E element, first child of its parent | [Structural pseudo-classes](http://www.w3.org/TR/selectors/#structural-pseudos)
| `E:last-child` | an E element, last child of its parent | [Structural pseudo-classes](http://www.w3.org/TR/selectors/#structural-pseudos)
| `E:first-of-type` | an E element, first sibling of its type | [Structural pseudo-classes](http://www.w3.org/TR/selectors/#structural-pseudos)
| `E:last-of-type` | an E element, last sibling of its type | [Structural pseudo-classes](http://www.w3.org/TR/selectors/#structural-pseudos)
| `E:only-child` | an E element, only child of its parent | [Structural pseudo-classes](http://www.w3.org/TR/selectors/#structural-pseudos)
| `E:only-of-type` | an E element, only sibling of its type | [Structural pseudo-classes](http://www.w3.org/TR/selectors/#structural-pseudos)
| `E:empty` | an E element that has no children (including text nodes) | [Structural pseudo-classes](http://www.w3.org/TR/selectors/#structural-pseudos)
| `E:link`<br>`E:visited` | an E element being the source anchor of a hyperlink of which the target is not yet visited (:link) or already visited (:visited) | [The link pseudo-classes](http://www.w3.org/TR/selectors/#link)
| `E:active`<br>`E:hover` <br>`E:focus` | an E element during certain user actions | [The user action pseudo-classes](http://www.w3.org/TR/selectors/#useraction-pseudos)
| `E:target` | an E element being the target of the referring URI | [The target pseudo-class](http://www.w3.org/TR/selectors/#target-pseudo)
| `E:lang(fr)` | an element of type E in language "fr" (the document language specifies how language is determined) | [The :lang() pseudo-class](http://www.w3.org/TR/selectors/#lang-pseudo)
| `E:enabled`<br>`E:disabled` | a user interface element E which is enabled or disabled | [The UI element states pseudo-classes](http://www.w3.org/TR/selectors/#UIstates)
| `E:checked` <!--<br>`E:indeterminate`--> | a user interface element E which is checked<!-- or in an indeterminate state--> (for instance a radio-button or checkbox) | [The UI element states pseudo-classes](http://www.w3.org/TR/selectors/#UIstates)
| `E::first-line` | the first formatted line of an E element | [The ::first-line pseudo-element](http://www.w3.org/TR/selectors/#first-line)
| `E::first-letter` | the first formatted letter of an E element | [The ::first-letter pseudo-element](http://www.w3.org/TR/selectors/#first-letter)
| `E::before` | generated content before an E element | [The ::before pseudo-element](http://www.w3.org/TR/selectors/#gen-content)
| `E::after` | generated content after an E element | [The ::after pseudo-element](http://www.w3.org/TR/selectors/#gen-content)
| `E.warning` | an E element whose class is "warning" (the document language specifies how class is determined). | [Class selectors](http://www.w3.org/TR/selectors/#class-html)
| `E#myid` | an E element with ID equal to "myid". | [ID selectors](http://www.w3.org/TR/selectors/#id-selectors)
| `E:not(s)` | an E element that does not match simple selector s | [Negation pseudo-class](http://www.w3.org/TR/selectors/#negation)
| `E F` | an F element descendant of an E element | [Descendant combinator](http://www.w3.org/TR/selectors/#descendant-combinators)
| `E > F` | an F element child of an E element | [Child combinator](http://www.w3.org/TR/selectors/#child-combinators)
| `E + F` | an F element immediately preceded by an E element | [Adjacent sibling combinator](http://www.w3.org/TR/selectors/#adjacent-sibling-combinators)
| `E ~ F` | an F element preceded by an E element | [General sibling combinator](http://www.w3.org/TR/selectors/#general-sibling-combinators)


**The meaning of each selector is derived from the table above by prepending
"matches" to the contents of each cell in the "Meaning" column.**

