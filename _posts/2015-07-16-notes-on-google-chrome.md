---
layout: post
title: "Tweaking Google Chrome: Chrome URLs"
categories: []
tags: ['Chrome', 'Google', 'Browsers', 'Chromium', 'Flags']
published: true
excerpt: "Chrome URLs and Tweaks"
---

### Resources
A number of tweaks can be accessed by typing `chrome://<some-option>` in
Chrome's address bar. Many of these options were previously accessed using `about:<some-option>`.
The list is available [here](chrome://chrome-urls).

I've yet to find an official page documenting these options; however, you can
find outdated information on the Chromium [AboutLinks](https://code.google.com/p/chromium/wiki/AboutLinks)
and Wikipedia [about URI scheme](https://en.wikipedia.org/wiki/About_URI_scheme)
pages.

Arch Linux has notes on many of these in their [Chromium Tweaks](https://wiki.archlinux.org/index.php/Chromium_tweaks)
post.

### Flags
* Peter Beverloo - [List of Chromium Command Line Switches](http://peter.sh/experiments/chromium-command-line-switches/)
* Christian Cantrell - [All About Chrome Flags](https://blogs.adobe.com/cantrell/archives/2012/07/all-about-chrome-flags.html)

### [List of Chrome URLs](chrome://chrome-urls)
* [about](chrome://about/)
* [accessibility](chrome://accessibility/)
* [appcache-internals](chrome://appcache-internals/)
* [apps](chrome://apps/)
* [blob-internals](chrome://blob-internals/)
* [bookmarks](chrome://bookmarks/)
* [cache](chrome://cache/)
* [chrome](chrome://chrome/)
* [chrome-urls](chrome://chrome-urls/)
* [components](chrome://components/)
* [copresence](chrome://copresence/)
* [crashes](chrome://crashes/)
* [credits](chrome://credits/)
* [device-log](chrome://device-log/)
* [devices](chrome://devices/)
* [dns](chrome://dns/)
* [downloads](chrome://downloads/)
* [extensions](chrome://extensions/)
* [flags](chrome://flags/)
* [flash](chrome://flash/)
* [gcm-internals](chrome://gcm-internals/)
* [gpu](chrome://gpu/)
* [help](chrome://help/)
* [histograms](chrome://histograms/)
* [history](chrome://history/)
* [indexeddb-internals](chrome://indexeddb-internals/)
* [inspect](chrome://inspect/)
* [invalidations](chrome://invalidations/)
* [local-state](chrome://local-state/)
* [media-internals](chrome://media-internals/)
* [memory](chrome://memory/)
* [memory-internals](chrome://memory-internals/)
* [memory-redirect](chrome://memory-redirect/)
* [nacl](chrome://nacl/)
* [net-internals](chrome://net-internals/)
  * [capture](chrome://net-internals/#capture)
  * [export](chrome://net-internals/#export)
  * [import](chrome://net-internals/#import)
  * [proxy](chrome://net-internals/#proxy)
  * [events](chrome://net-internals/#events)
  * [waterfall](chrome://net-internals/#waterfall)
  * [timeline](chrome://net-internals/#timeline)
  * [dns](chrome://net-internals/#dns)
  * [sockets](chrome://net-internals/#sockets)
  * [http2](chrome://net-internals/#http2)
  * [quic](chrome://net-internals/#quic)
  * [sdch](chrome://net-internals/#sdch)
  * [httpCache](chrome://net-internals/#httpCache)
  * [modules](chrome://net-internals/#modules)
  * [hsts](chrome://net-internals/#hsts)
  * [bandwidth](chrome://net-internals/#bandwidth)
  * [prerender](chrome://net-internals/#prerender)
* [newtab](chrome://newtab/)
* [omnibox](chrome://omnibox/)
* [password-manager-internals](chrome://password-manager-internals/)
* [plugins](chrome://plugins/)
* [policy](chrome://policy/)
* [predictors](chrome://predictors/)
* [print](chrome://print/)
* [profiler](chrome://profiler/)
* [quota-internals](chrome://quota-internals/)
* [serviceworker-internals](chrome://serviceworker-internals/)
* [settings](chrome://settings/)
* [signin-internals](chrome://signin-internals/)
* [suggestions](chrome://suggestions/)
* [sync-internals](chrome://sync-internals/)
* [system](chrome://system/)
* [terms](chrome://terms/)
* [thumbnails](chrome://thumbnails/)
* [tracing](chrome://tracing/)
* [translate-internals](chrome://translate-internals/)
* [user-actions](chrome://user-actions/)
* [version](chrome://version/)
* [view-http-cache](chrome://view-http-cache/)
* [voicesearch](chrome://voicesearch/)
* [webrtc-internals](chrome://webrtc-internals/)
* [webrtc-logs](chrome://webrtc-logs/)

### For Debug
** The following pages are for debugging purposes only. Because they crash or hang the renderer, they're not linked directly; you can type them into the address bar if you need them. **

* chrome://crash
* chrome://crashdump
* chrome://kill
* chrome://hang
* chrome://shorthang
* chrome://gpuclean
* chrome://gpucrash
* chrome://gpuhang
* chrome://ppapiflashcrash
* chrome://ppapiflashhang
* chrome://quit/
* chrome://restart/
