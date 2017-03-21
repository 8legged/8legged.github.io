---
layout: post
title: 'Using the :target pseudo-selector in Jekyll'
categories: ['Jekyll', 'JavaScript', 'CSS']
tags: ['Jekyll', 'JavaScript', 'Tooltips', 'Popovers', 'CSS', 'pseudo-selectors', ':target']
published: true
excerpt_separator: <!-- excerpt -->
---
A test post to get my glossary working.
<!-- excerpt -->

include

{% include show-hide-input.html param="turkey" %}

{{ include.param }}

hider

{{ hider | lstrip }}

I want posts to include links to definitions in my site's `terms.yml` file.
This points to a single entry about [Jekyll](#info).

{% include info.html %}

{% include dictionary.html %}
