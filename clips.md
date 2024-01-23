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
  - header: Christmas Cookies
    link: christmas-cookies
    image: assets/images/clips/christmascookies-sm.jpg
  - header: Crusty Italian Bread
    link: crusty-italian-break
    image: assets/images/clips/crustyitalianbread-sm.jpg
  - header: Homemade Bread
    link: homemade-bread
    image: assets/images/clips/homemadebread-sm.jpg
  - header: Hustle Cake
    link: hustle-cake
    image: assets/images/clips/hustlecakeclip-sm.jpg
  - header: Lemon Cake
    link: lemon-cake
    image: assets/images/clips/lemoncake-sm.jpg
  - header: Lemon Meringue Pie
    link: lemon-meringue-pie
    image: assets/images/clips/lemonmeringuepie.jpg
  - header: Mandarin Orange Cake
    link: mandarin-orange-cake
    image: assets/images/clips/mandarinorangecake-sm.jpg
  - header: Orange Loaf
    link: orange-loaf
    image: assets/images/clips/orangeloaf-sm.jpg
  - header: Swans Down Pancakes and Biscuits
    link: swans-down-pancakes-and-biscuits
    image: assets/images/clips/swansdown-sm.jpg
    review: I tried the pancakes.  They are pancakes - nothing special.  I'll stick to Bisquick.
  - header: White Mountain Frosting
    link: white-mountain-frosting
    image: assets/images/clips/whitemountainfrosting-sm.jpg

---

{% for item in page.clips %}

#### **[\> {{item.header}} ](#{{item.link}})**

{% endfor %}


{% for item in page.clips %}

### {{ item.header }}

{% if item.review != nil %}
> Steve's Review: {{ item.review }}
{% endif %}

<img alt="{{ item.header }}" src="https://illinifanboy.github.io/{{ item.image }}">

{% endfor %}

