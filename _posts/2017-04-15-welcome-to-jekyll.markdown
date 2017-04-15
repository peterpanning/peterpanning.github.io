---
layout: post
title:  "Welcome to Jekyll!"
date:   2017-04-15 14:40:00 -0700
categories: jekyll update
---

[brew]: https://brew.sh/
[github-pages]: https://pages.github.com/
[jekyll]: https://jekyllrb.com/
[ruby-gems]: https://rubygems.org/pages/download
[github-pages-themes]: https://pages.github.com/themes/
[jekyll-install-theme]: https://jekyllrb.com/docs/themes/#installing-a-theme

For my first post, I thought it would be a great idea to show how I made this
website--using [GitHub Pages][github-pages] and [Jekyll][jekyll].


Jekyll is a Ruby gem which allows for the quick and easy creation and maintenance
of static websites. It is what powers GitHub Pages, so there's a good chance it's
going to stick around with generally good support for quite a long time.

To install Jekyll, you need to be on GNU/Linux, Unix, or macOS.

You also need Ruby 2.0 or above. If you're on macOS, the easiest way to install
this and other packages is with [Brew][brew]. Brew is the package manager that
macOS doesn't have--if you're familiar with the ease of installing packages on
Linux-based operating systems, it's just like that. With Brew, installing ruby
becomes as easy as `brew install ruby`.

You also need [RubyGems][ruby-gems]. Installing it is also pretty easy--just
`cd` to wherever you downloaded the archive and run `ruby setup.rb` (might need to
be root).

You also need GCC and `make` installed. You can see if they're installed with
`gcc -v` and `make -v`.

Once that's all done, you should be able to install Jekyll and bundler with
`gem install jekyll bundler`. Run `jekyll --version` and `gem list jekyll`,
make sure the versions match up. If not, run `gem update jekyll`.

At this point, Jekyll should be installed and ready to go! Now let's use it to
generate a quick homepage.

Navigate to the directory on your computer where you want your new website to live.

Run `jekyll new username.github.io`, where username is your Github username. `cd`
into that directory and run `bundle exec jekyll serve`, and voila! You have a local instance
of your new website! It's not very exciting right now with its filler text, but it
shows that jekyll is working and its power to create an entire website with very
little effort.

All we have to do in order for our new site to go live is add it to our GitHub!
Go to Github.com and start a new repository called username.github.io. Make sure
you DON'T include a README file.

You're still in the username.github.io directory on your local machine, right?
Get there, and run `git init`
`git remote add origin https://github.com/username/username.github.io.git`
`git remove -v` (verifies the new URL)
`git add .`
`git commit -m "First commit"`
And `git push origin master`

And your local build of your website should now be pushed to your Github, and
visible if you visit username.github.io! It might take a couple minutes to go live,
so if it doesn't work, try again in a little bit.

From here, you probably want to jump right into the thick of things and start
using a different theme, writing posts, or creating new pages. Since Jekyll's
whole schtick is that creating and maintaining your website is supposed to be as
easy as possible to allow you to focus on generating content, you might hope that,
for at least the [GitHub Pages supported themes][github-pages-themes] on a
brand-new, zero-content site, something as simple as changing themes would be
just as quick and painless as [their documentation][jekyll-install-theme] suggests.

Unfortunately, this is not the case. The `jekyll new` installation's theme,
minima, comes with more resources than the other GitHub Pages-supported themes.
For example, it comes with a sample post and a layout used to format said post.
If you try to switch themes from minima to any other Pages-supported theme, you
will still have the post, but not the post layout, and your build will fail when
Jekyll tries to format your site with a layout it cannot find.  So if you want
to take the fastest, simplest approach to getting a Jekyll site up and running
but you also want to use a theme other than minima...well, you can't have your
cake and eat it, too. Writing Jekyll layouts may seem like reinventing the wheel
if you already have a good handle on CSS or other similar tools, but if you want
to make hosting a personal website as quick and painless as possible, going
from zero to a hosted page in the span of an afternoon is about as good as it
gets. I'm looking forward to learning more about how to use Jekyll in the future,
and will continue to post more as I do.
