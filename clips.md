---
layout: page
title: Recipe Clips
tagline: TOC
description: Clips of Recipes
clips:
  - header: Apple Dumplings
    link: apple-dumplings
    image: assets/images/clips/appledumplingsclip-sm.jpg
  - header: Blue Ribbon Lemon Pie
    link: blue-ribbon-lemon-pie
    image: assets/images/clips/blueribbonlemonpie-sm.jpg
  - header: Christmas Cookies
    link: christmas-cookies
    image: assets/images/clips/christmascookies-sm.jpg
  - header: Coconut Peach Ice Cream
    link: coconut-peach-ice-cream
    image: assets/images/clips/coconutpeachicecream-sm.jpg
  - header: Crusty Italian Bread
    link: crusty-italian-bread
    image: assets/images/clips/crustyitalianbread-sm.jpg
  - header: Cream Cheese Cookies
    link: cream-cheese-cookies
    image: assets/images/clips/creamcheesecookies-sm.jpg
  - header: Cream Puffs
    link: cream-puffs
    image: assets/images/clips/creampuffs-sm.jpg
  - header: Gold Cookies
    link: gold-cookies
    image: assets/images/clips/goldcookiesclip-sm.jpg
  - header: Hershey Cake
    link: hershey-cake
    image: assets/images/clips/hersheycake-sm.jpg
  - header: Homemade Bread
    link: homemade-bread
    image: assets/images/clips/homemadebread-sm.jpg
  - header: Hustle Cake
    link: hustle-cake
    image: assets/images/clips/hustlecakeclip-sm.jpg
  - header: Lady Baltimore Cake
    link: lady-baltimore-cake
    image: assets/images/clips/ladybaltimorecake-sm.jpg
  - header: Lemon Cake
    link: lemon-cake
    image: assets/images/clips/lemoncake-sm.jpg
  - header: Lemon Cheese Cake Pie
    link: lemon-cheese-cake-pie
    image: assets/images/clips/lemoncheesecakepie-sm.jpg
    reviewimage: assets/images/clips/lemoncheesecakepie-review.jpg
    reviewtext: Not bad.  Lots of lemon flavor.  The cracker crumb pie shell is also not bad.  The pie is not good enough to serve to company, but I would try again.  Next time, I will just throw everything into a food processor.  All of these micro steps are not necessary.
  - header: Lemon Meringue Pie
    link: lemon-meringue-pie
    image: assets/images/clips/lemonmeringuepie-sm.jpg
  - header: Orange Loaf
    link: orange-loaf
    image: assets/images/clips/orangeloaf-sm.jpg
  - header: Speedie Rolls
    link: speedie-rolls
    image: assets/images/clips/speedierollsclip-sm.jpg
  - header: Swans Down Pancakes and Biscuits
    link: swans-down-pancakes-and-biscuits
    image: assets/images/clips/swansdown-sm.jpg
    review: I tried the pancakes.  They are pancakes - nothing special.  I'll stick to Bisquick.
  - header: Sweet Coffee Cake
    link: sweet-coffee-cake
    image: assets/images/clips/sweetcoffeecake-sm.jpg
    review: I tried the pancakes.  They are pancakes - nothing special.  I'll stick to Bisquick.
  - header: White Mountain Frosting
    link: white-mountain-frosting
    image: assets/images/clips/whitemountainfrosting-sm.jpg

---

> The reason I call this a "scrapbook" and not a "cookbook" is because of clippings.  The scrapbooks contain both handwritten recipes and other recipes cut out from newspaper and magazines.  In fact, there are far more clippings than handwritten recipes.<br /><br />Since there were so many clippings to pick through, I had to decide what to include or leave out.  I picked clips because they were interesting, either interesting to cook or interesting to look at.

<img alt="Lady Cooking" src="https://illinifanboy.github.io/assets/images/general/ladycooking-vs.jpg">

{% for item in page.clips %}

#### **[\> {{item.header}} ](#{{item.link}})**

{% endfor %}


{% for item in page.clips %}

### {{ item.header }}

<img alt="{{ item.header }}" src="https://illinifanboy.github.io/{{ item.image }}">

{% if item.reviewimage != nil %}
<img alt="{{ item.header }}" src="https://illinifanboy.github.io/{{ item.reviewimage }}">
{% endif %}

{% if item.reviewtext != nil %}
> Steve's Review: {{ item.reviewtext }}
{% endif %}

{% endfor %}

