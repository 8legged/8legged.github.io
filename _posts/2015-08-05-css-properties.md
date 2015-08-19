---
layout: post
title: "CSS Properties and Selectors"
categories: []
tags: ['CSS']
published: true
excerpt: "Dumbed down for me"
---
## Properties
[<code>outline</code>](https://developer.mozilla.org/en-US/docs/Web/CSS/outline)

{% highlight javascript linenos %}
/* width | style | color */
outline: 1px solid white;

/* Global values */
outline: inherit;
outline: initial;
outline: unset;
{% endhighlight %}

The outline property in CSS draws a line around the outside of an element.
It's similar to border except that:
  - You can't specify particular sides
  - It's not a part of the box model, so *it won't effect the position of
    the element or adjacent elements*
  - It doesn't respect border-radius (makes sense - it's not a border)
  - It isn't always rectangular. If the outline goes around an inline element
    with different font-sizes, for instance, Opera will draw a staggered box
    around it all.

Often used for accessibility reasons, to emphasize a link when tabbed to without
affecting positioning and in a different way than hover.

## Selectors
Pseudo class selectors are CSS selectors with a colon preceding them.

{% highlight css %}
a:hover {

}
{% endhighlight %}

## Tools
- [Autoprefixer CSS Online](https://autoprefixer.github.io/)
