---
layout: post
title: "Responsive Web Pages"
categories: []
tags: ['Responsive', 'RWD']
published: true
---
I'm not sure where I was when I took these notes on responsive web design - need
find out what book/exercise the chapters are referencing.

----

Media queries...

- Modify css based on
  + width
  + orientation
  + media 'type'
  + color
  + resolution
  + aspect-ration
  + etc.

###### Post about video
1. Create a post identifying an interesting topic or fact that you learned by watching these videos.
2. Link to external content related to your topic.
3. Place the link on the post and a description of what may be found there.

**Post a meaningful response to the submission of one other person.**  Be sure to
contribute something to the conversation - display thought on your part.

----

## Chapter 1
- Exploring the need for responsive design
- Responsiveness impacts how people experience and use sites across devices
- The telephone URL format allows mobile devices to make calls or add numbers to contact lists

----

## Chapter 2
Two mechanisms for overriding the user agent's default view port

- **Viewport Meta Tag**
  - Appears in the head, has 2 parts: name and content
    - Doesn't use px
    - Device width value lets you set your size based on the device's viewport
      size (less popular)

- **@ viewport CSS rule**
  - Appears anywhere in CSS - recommended placement is prior to any media
    queries because it can affect these queries. Most designers put it near the
    top of their styles as one of, if not their first rule.

###### Reference pixel (css pixel) = 1/96th of an in.
device-pixel-ratio

###### Reduce bitmap graphics by using
* SVG
  * Often larger in size than bitmaps
  * Graphics are redrawn with each screen change

* CSS
  * Complex artwork is difficult
  * Often require non-semantic markup
  * Property support isn't universal

* Icon Fonts
  * Have to include unnecessary characters in your markup
  * Can cause accessibility confusion

* Raster Graphics
  * Larger in size
  * Have to account for largest size needed

#### Recommendations:
* CSS
  * Background images: use media queries to target specific device ratios.
    Change out image for high res versiion and use background-size to properly
    size image.

* Javascript
  * Query user agent's device pixel ratio and pass a request to use higher res images over lower res images. Make sure script doesn't download un-necessary assets.

{% highlight css %}
@ media [not | only ] screen [and] (expression) {
}
{% endhighlight %}


using a comma separator is seen as an "or"

scottjehl's respond.js helps with older IE versions (github)

#### Mobile
480 and smaller

#### Tablet
481 to 768

#### Desktop
769 and greater

*You can divide screen width by 16px to get the "em".*

* Filament Group's <s>Responsive-Images</s> **No longer recommended.** Use[Picturefill](https://github.com/scottjehl/picturefill).
  * <s>[Source code](https://github.com/filamentgroup/Responsive-Images)</s>
  * Client side solution
  * The script determines the context, parses the page, and then serves the
    appropriate image
    * Replacement image may be downloaded after the initial image is downloaded
    * Prefetching

##### 3 factors to consider when using responsive images
* Screen size
* Screen density
* Bandwidth

* Combine files at runtime into single requests
  * Quickconcat (*Filament Group*)
  * Enhance.js (*Filament Group*)

----------------------------------------

## Chapter 3
- Create a content inventory and a hierarchy
- New products
- Images of products
- Contact information
- Order status
- Login information
- *e.t.c...*

#### Breakpoints
- Design towards screen sizes (groups) instead of devices

#### Tweakpoints
- More granular breakpoints
- Used when you know a specific size needs to be accounted for

Ask if you can make the site in a single document structure, if no, you may want
to redefine goals, modify content, or create an app or separate mobile site.

#### Wireframe and prototyping tools for sites:
* Ai (Illustrator)
* Responsive sketch books and sheets
* Keynote and PowerPoint
* HTML and CSS Frameworks
  * Skeleton

- Consider which features (location, camera, e.t.c.) will best serve the user

- Explore micro-formats

#### CSS (follow developments)
* Box Model
* Template Layout Module

#### Other
* Benjamin Keen
  * Bookmarklet to show multiple sizes
* Responsive.is
* Screenqueri.es


* Mobitest (load times and waterfall chart breaking out resources individually)
* Testiphone.com
* Opera Mini
* Opera Mobile
* Apple and Android SDKs
mobiforge on emulators - guide to mobile emulators

#### Remote debugging
* Opera Dragonfly
* Weinre

## Goals
* Emphasize important content (stack rank [involve others in this process])
* Make relationships clear
* Make it accessible on small screens

## Conclusion

### Fluid grid frameworks:
* Keeps consistent code
* Solid starting code base
* Adds unnecessary code

#### More stuff
* goldengridsystem.com
* simpleGrid.info
* columnal.com
* responsivegridsystem.com
* gridsetapp.com
* foundation.zurb.com (Foundation 3)
* twitter.github.com/bootstrap/
* html5boilerplate.com/mobile (mobile boilerplate)
* getskeleton.com

#### Additional Tools:
* jeremypalford.com/arch-journal/responsive-web-design-sketch-sheets
* tinyfluidgrid.com
* csswizardry.com/fluid-grids
* brettjankfor.com/2012/01/16/categorizr-a-modern-device-detection-script
* modenizr.com (current standard in feature detection)
* fitvidsjs.com
* github.com/scottjehl/Respond
* filamentgroup.com/lab/overthrow
* github.com/filamentgroup/southstreet
* responsejs.com (response.js)
* github.com/zmoazeni/csscss
* github.com/geuis/helium-css

#### More
* From Google video I randomly found (slides on [wildermuth.com](wildermuth.com))
* [AdaptJS](adapt.960.gs/)
* [EnhanceJS](https://code.google.com/p/enhancejs)
  - Cons: cookies determine screen size, not recently worked on
* [ResponseJS](responsejs.com)

#### Important Bookmarks
* [Filament Group Articles](filamentgroup.com/lab/)
* [LukeW](lukew.com)
* [Ethan Marcotte's Blog](unstoppablerobotninja.com)
* [Brad Frosts's Blog](bradfrostweb.com/blog/)
