---
layout: page
title: Table of Contents
tagline: TOC
description: Clips of Recipes
clips:
  - header: Apple Dumplings
    image: assets/images/clips/appledumplingsclip-sm.jpg
  - header: Gold Cookies
    image: assets/images/clips/goldcookiesclip-sm.jpg
---

## Clips

{% for item in page.clips %}

### {{ item.header }}

<img alt="{{ item.header }}" src="https://illinifanboy.github.io/{{ item.image }}">

{% endfor %}

