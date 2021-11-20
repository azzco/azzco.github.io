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