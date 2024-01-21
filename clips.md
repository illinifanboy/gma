---
layout: page
title: Table of Contents
tagline: TOC
description: Table of Contents
clips:
  - header: Gold Cookies
    image: assets/images/clips/goldcookiesclip-sm.jpg
---

## Clips

{% for item in page.clips %}

### {{ item.header }}

<img alt="{{ item.header }}" src="https://illinifanboy.github.io/{{ item.image }}">

{% endfor %}

