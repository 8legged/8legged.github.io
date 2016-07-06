---
layout: post
title: 'Popovers and Tooltips with Vanilla JS'
categories: ['Jekyll', 'JavaScript']
tags: ['Jekyll', 'JavaScript']
published: true
excerpt_separator: <!-- excerpt -->
---

Using JavaScript for popovers and tooltips in Jekyll.

<!-- excerpt -->

<h2>Popover</h2>
{% include popovers.html %}
<br />


The example above uses `_includes/popovers.html`:

```html
<div>
    Regular text <span class="tip" onclick="return vanillaTip.click(this);">popover trigger</span>.
    <div class="popover top">
        <div class="arrow"></div>
        <div class="popover-content">
            {{site.data.glossary.jekyll}}
        </div>
    </div>
</div>
```

Here's the resulting html:

```html
<div>
    Regular text <span class="tip" onclick="return vanillaTip.click(this);">popover trigger</span>.
    <div class="popover top">
        <div class="arrow"></div>
        <div class="popover-content">
            Jekyll is a static site generator that builds sites using most modern web technologies. <a href="https://www.techopedia.com/definition/1320/canonical">source</a>
        </div>
    </div>
</div>
```

Finally, our JavaScript appends the popover and its content to the bottom of the page:

```html
<!-- Note: Style and Class data was written by popover.js -->
<div class="popover top popover-clone popover-clone" style="display: block; position: absolute; left: 10px; top: 238px;">
    <div class="arrow" style="left: 107.547px;"></div>
    <div class="popover-content">
        Jekyll is a static site generator that builds sites using most modern web technologies. <a href="https://www.techopedia.com/definition/1320/canonical">source</a>
    </div>
</div>
```

The resulting popover is styled according to instructions our `.css` file.

---

{% include tooltips.html %}
