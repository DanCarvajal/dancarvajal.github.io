---
title: Breaking My Site and Fixing It Again
date: 2016-11-23 00:00:00 Z
layout: post
author: Dan Carvajal
---

Wow this is embarrassing but it’s been six months since my last blog post. A lot has happened since then, but before I play catch up on let me explain why I haven’t been blogging.

My site was broken the entire time. This website is hosted on [Github](https://github.com/) using the blog tool [Jekyll](https://jekyllrb.com/). Github began using a new version of Jekyll which broke my site since it was built for an old version. Every few weeks I would spend an hour or two trying to fix the site but nothing seemed to work. After a while I just took a break from my site.

This past weekend I decided to give my site another try. **I was successful!**

It turns out that my main issues were:

* Github has very little detail in its error reports. When I would try to fix my site I would get an email that said little about how it [broke](https://help.github.com/articles/page-build-failed-date-is-not-a-valid-datetime/).
* Bundler, a tool that I use to help build the site, was also having an error. This error stopped me from learning about why my site broke. While I thought I had the right tool, it was lying to me. Other people have also have had [this problem](https://github.com/github/pages-gem/issues/351).
* After I [fixed](https://github.com/github/pages-gem/issues/351#issuecomment-258647085) Bundler, I was able recreate the same error that Github had. Except the error code was better than Github's. A quick Google search and then I found the exact [answer](http://stackoverflow.com/questions/21098566/jekyll-invalid-date-is-not-a-valid-datetime) I needed.
* My site broke because the Jekyll tried to use draft blog posts in my site's "main" folder instead of the "posts" folder. It looked in the wrong place, got screwy dates on the posts, and just said “I give up.”

Other factors into why this was a hard fix for me:
* I sold my Mac and moved to Windows. Jekyll is a little easier on Macs.
* The whole reason I use Jekyll for my site is that it's free, but it's not that simple. This has been learning process.

That’s the story of how my site broke for six months because I put files in the wrong place.
