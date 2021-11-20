---
title: More setup 
date: 2021-11-20
tags: jekyll git github
---

Organizing domains, subdomains and whatnot.

## CNAME, SRV?
I'm not very familiar with these concepts. I'm aiming to set up my domain and subdomains like this:
- `www.azzco.xyz` - nginx linode host
- `azzco.xyz` - same as above
- `map.azzco.xyz` - planarally, main domain but on port 8000
- `blog.azzco.xyz` - azzco.github.io
	My github page where I upoad this document.
- `dnd.azzco.xyz` - azzco.github.io/dnd-journal
	A second blog but mainly dnd related, specifically session summaries.

I'm encountering problems with the last one when trying to go the CNAME approach like I did with the main github pages. CNAME doesn't do anything other than a domain it seems, subdir not allowed. I think nginx is the way to go, tough I barely know how I managed to get planarally to play nicely earlier.

Honestly I have no idea what I'm doing. I had it working yesterday, didn't change a thing and now it's not working...

## Jekyll - Livereload
With ruby 3 there seems to be some issues with the `jekyll serve --livereload´ option. Been trying a couple of things without any success. Unstalling --platform ruby version of eventmachine didn't work.
Changing requirement to em pure_ruby didn't work.

What actually seesm to work is adding to the Gemfile:
`gem 'eventmachine', '1.2.7', git: 'https://github.com/eventmachine/eventmachine.git', tag: 'v1.2.7'`
and running:
```
bundle install
bundle exec jekyll clean
bundle exec jekyll serve --livereload
```
And it actually seems to work as exepected!

So back to work on the domains.

## Back to domain setup
`map.azzco.xyz` isn't working at the moment. Not sure if it's nginx or if its a DNS thing.

Nginx settings are a bit mysterious to me so I'm going the DNS route, which is alos a mystery... In any case I added A record to point to both IPV4 and IPV6 address with hostname `map`. I also added a srv record pointing to port 8000 and map.azzco.xyz. I just hope that that's enough. I don't know how much time it needs before changes take effect.

I could probably start working on other stuff in the meantime.

## Theme
I have no real idea where to start. The chosen theme seems really nice but I don't know where to begin modifying it. I know I want a navbar with links to 