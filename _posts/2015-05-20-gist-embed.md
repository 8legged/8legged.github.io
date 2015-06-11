---
layout: post
title: "gist-embed: Better Embedded Code Snippets"
tags:
- Gist
- GitHub
published: true
---
An example of an embedded Gist using gist-embed
<section>
  <code data-gist-id="9e907ead1ad5f0440a8d" data-gist-file="ruby-example.rb" data-gist-hide-footer="true" data-gist-highlight-line="1,3,5"></code>
</section>

Include jQuery and gist-embed src

{% highlight html %}
<head>
  <script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
  <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/gist-embed/2.1/gist-embed.min.js"></script>
</head>
{% endhighlight %}

Add an HTML element to your page with a data attribute in the following format, where `<gist-id>` should be replaced with the id of your gist

    <code data-gist-id="<gist-id>"></code>

There's also a [RubyGem](https://github.com/itsNikolay/gist-embed-rails) and an [AngularJS library](https://github.com/pasupulaphani/angular-gist-embed)

#### Examples
* Including a single gist
* Including individual files from a gist
* Including specific line numbers from a gist
* Removing all line numbers from a gist
* Removing the footer from a gist
* Highlight lines from a gist

Check out the [gist-embed website](http://blairvanderhoof.com/gist-embed/) and the [gist-embed project on GitHub](https://github.com/blairvanderhoof/gist-embed)

#### Loading a gist
<code data-gist-id="5457595"></code>

#### Loading a gist with all line numbers removed
<code data-gist-id="5457605" data-gist-hide-line-numbers="true"></code>

#### Loading a gist with footer removed
<code data-gist-id="5457619" data-gist-hide-footer="true"></code>

#### Loading a gist with both footer and line numbers removed
<code data-gist-id="5457629" data-gist-hide-footer="true" data-gist-hide-line-numbers="true"></code>

#### Loading a gist with multiple files
<code data-gist-id="5457635"></code>

#### Loading a single file from a gist (example-file2.html)
<code data-gist-id="5457644" data-gist-file="example-file2.html"></code>

#### Loading a single line number from a gist (line 2)
<code data-gist-id="5457662" data-gist-line="2"></code>

#### Loading a range of line numbers from a gist (line 2 through 4)
<code data-gist-id="5457652" data-gist-line="2-4"></code>

#### Loading a single line and a range of line numbers from a gist (line 1 and line 3 through 4)
<code data-gist-id="5457665" data-gist-line="1,3-4"></code>

#### Loading a list of line numbers from a gist (line 2, 3, 4)
<code data-gist-id="5457668" data-gist-line="2,3,4"></code>

<!-- #### Highlighting a list of line numbers from a gist (line 1, 3, 5) -->
<code data-gist-id="7922593" data-gist-highlight-line="1,3,5"></code>

#### Loading a private gist
<code data-gist-id="a85770344febb8e30935"></code>

#### Loading a gist without the loading text
<code data-gist-id="f847e6866e13ed607f49" data-gist-show-loading="false"></code>

#### Loading a gist after the page has loaded
<code id="after-page-load-test"></code>

#### Loading a code element without a gist id data attribute
<code>
  This is the content of a code element.  It has no gist id data attribute, so it's not parsed.
</code>
