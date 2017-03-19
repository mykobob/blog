---
layout: post
title: Subdomain woes
---

The sad adventures of me learning about how subdomains actually work.

## Background

My website is actually hosted on a [heroku](www.heroku.com) with a CNAME with Google Domains. I am CNAME'ing this blog to a subdomain of my main website. To make things a bit harder for unexperienced me, all of the tutorials that I found online were not tailored for a person in my situation, so I frequently gave up on trying to fix my issues.

## Problem + Solution

My subdomain of blog and 'www' were causing problems in almost every configuration that I was trying out. Here are some things that I figured out/got more clarity on while addressing this issue. 

The 'www' in a url is actually a subdomain. I've actually known that you could go to a website without using www, but I never figured out why until now. Typically, people redirect 'www' urls to the main address without the 'www'. With this knowledge, it is super important to realize that an address of '`www.blog.limichael.com`' doesn't make sense if I am just trying to create a simple subdomain of 'blog' under my 'limichael.com' website. This was the key insight that I figured out while trying to understand the structure of standard internet websites.

## End Thoughts

While it was cool to figure out the intricacies of subdomains and domains, I was more annoyed that it caused me to think about how to fix this technical issue instead of thinking of different topics that I want to write about.
