---
layout: post
title: 'Jekyll Tooltip and Popover Resources'
categories: ['Jekyll', 'JavaScript']
tags: ['Jekyll', 'JavaScript', 'Tooltips', 'Popovers']
published: true
excerpt_separator: <!-- excerpt -->
---
[This site](http://andeon.github.io/askey/apps/gimp/) by
[Anderson Prado](https://github.com/andeon/) inspired me to use tooltips
and popovers to quickly look up things that I often forget.

<!-- excerpt -->

## Resources
* [Tooltip](https://chrisbracco.com/a-simple-css-tooltip/)
* [Popup](http://www.sevensignature.com/blog/code/pure-css-popup-without-javascript/)
* [Organize a multi-language Jekyll site](http://benoitpatra.com/2014/08/24/organize-a-multilanguage-jekyll-site/)

Notes from the popup post:

* This popup has various divisions
  * A popup box after clicking a button
  * A close button within the popup window
    * An `<a>` tag is used for the close button

### HTML
```html
Regular text <span class="box"><a class="button" href="#thepopup">popup link</a></span> regular text

<!-- Only show the content below when the popup is clicked -->
<div id="thepopup" class="overlay">
	<div class="popup">
		<h2>H2 Heading</h2>
		<a class="close" href="#">close</a>
		<div class="content">
			Popup content.
		</div>
	</div>
</div>
```

### CSS
```css
.button, .close {
  color: #000;
  text-decoration: none;
}

.button { background-color: yellow; }

.overlay {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background: rgba(0, 0, 0, 0.7);
  transition: opacity 500ms;
  visibility: hidden;
  opacity: 0;
}

.overlay:target { visibility: visible; opacity: 1; }

.popup {
  margin: 70px auto;
  background: pink;
  border-radius: 3px;
  width: 30%;
  position: relative;
}

.close {
  position: absolute;
  top: 0.5rem;
  right: 0.5rem;
}

.popup .content {
  max-height: 30%;
  overflow: auto;
}
```
