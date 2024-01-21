---
layout: page
title: Recipe Clips
tagline: TOC
description: Clips of Recipes
clips:
  - header: Apple Dumplings
    image: assets/images/clips/appledumplingsclip-sm.jpg
  - header: Gold Cookies
    image: assets/images/clips/goldcookiesclip-sm.jpg
  - header: Hustle Cake
    image: assets/images/clips/hustlecakeclip-sm.jpg
---

## Apple Dumplings x

<img alt="{{ item.header }}" src="https://illinifanboy.github.io/assets/images/clips/appledumplingsclip-sm.jpg">

## Gold Cookies x

<img alt="{{ item.header }}" src="https://illinifanboy.github.io/assets/images/clips/goldcookiesclip-sm.jpg">

## Hustle Cake x

<img alt="{{ item.header }}" src="https://illinifanboy.github.io/assets/images/clips/hustlecakeclip-sm.jpg">



{% for item in page.clips %}

### {{ item.header }}

<img alt="{{ item.header }}" src="https://illinifanboy.github.io/{{ item.image }}">

{% endfor %}

