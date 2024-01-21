---
layout: page
title: Recipe Clips
tagline: TOC
description: Clips of Recipes
clips:
  - header: Apple Dumplings
    link: apple-dumplings
    image: assets/images/clips/appledumplingsclip-sm.jpg
  - header: Gold Cookies
    link: gold-cookies
    image: assets/images/clips/goldcookiesclip-sm.jpg
  - header: Hustle Cake
    link: hustle-cake
    image: assets/images/clips/hustlecakeclip-sm.jpg
---

{% for item in page.clips %}

#### **[ {{item.header}} ](#{{item.link}})**

{% endfor %}


{% for item in page.clips %}

### {{ item.header }}

<img alt="{{ item.header }}" src="https://illinifanboy.github.io/{{ item.image }}">

{% endfor %}

