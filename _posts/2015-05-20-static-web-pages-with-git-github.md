---
layout: post
title: "Static Sites and GitHub (or Gist)"
tags:
- Jekyll
- GitHub
- Gist
- GitHub Pages
- Static Sites
published: true
excerpt: "Quickly and easy ways to view your code as a web page"
---
#### Resources
- [RawGit](http://rawgit.com/)
- [GitHub & BitBucket HTML Preview](https://htmlpreview.github.io/)
- [bl.ocks.org](http://bl.ocks.org/)
- [Jekyll](http://jekyllrb.com/)

The code in [this repository](https://github.com/github/choosealicense.com)
has been helpful when working with Jekyll and GitHub Pages.

Ben Balter's post ["Explain like I’m five: Jekyll collections"](http://ben.balter.com/2015/02/20/jekyll-collections/)
has also been very useful.

The data for my blog is automatically transformed by Jekyll into a static site
whenever I push its repository to GitHub.

# Installing Jekyl
I used the [github-pages](https://github.com/github/pages-gem) Ruby Gem to do this.

### Health check
Checks your GitHub Pages site for common DNS configuration issues.

`github-pages health-check`

# Running Jekyll
* Run `bundle exec jekyll serve`
* Your site should be available at [http://localhost:4000](http://localhost:4000)

Find out about installing Jekyll, keeping it updated (with GitHub Pages), configuration settings, e.t.c. [here](https://help.github.com/articles/using-jekyll-with-pages/).

# Turning Jekyll off
You can completely opt out of Jekyll processing by creating a file named .nojekyll in the root of your Page repository and pushing that file to GitHub. This should only be necessary if your site uses directories that begin with an underscore, as Jekyll sees these as special directories and does not copy them to the final destination.

# License
The following directories and their contents are Copyright Jason Niemi. You may not reuse anything therein without my permission:
* _drafts/
* _includes/
* _layouts/
* _posts/
* _site/
* about/
* images/
* javascripts/
* stylesheets/
