---
layout: page
title: Template Title
blurb: A short, one-line introduction
finalproduct: assets/images/general/noimage.jpg
handwritten: assets/images/general/noimage.jpg
review: Not yet reviewed.
story: 
ingredients: assets/images/general/noimage.jpg
steps:
  - header: Step 1
    text: The text that says what to do.
    image: assets/images/general/noimage.jpg
  - header: Step 2
    text: The text that says what to do.
    image: 
  - header: Step 3
    text: The text that says what to do.
    image: 
---

> {{ page.blurb }}

Jump to **[\<Recipe\>](#recipe)**.

<img alt="Final Product" src="https://illinifanboy.github.io/{{ page.finalproduct }}">


### Steve's Review  
{{ page.review }}    

### Grandma's Handwritten Recipe

<img alt="Final Product" src="https://illinifanboy.github.io/{{ page.handwritten }}">

{{ page.story }}

## Recipe

### Ingredients

<img alt="Ingredients" src="https://illinifanboy.github.io/{{ page.ingrediants }}">


Ingredient | Measurement, Weight | Notes
---|---|----
Item Name | Amount | Notes
Item Name | Amount | Notes
Item Name | Amount | Notes
Item Name | Amount | Notes

### Steps

#### <ins>Step 1</ins>

Step 1 text.

<img width="480" alt="Step 1" src="https://illinifanboy.github.io/assets/images/general/noimage.jpg">

### Step Looping

{% for item in page.steps %}

### <ins>{{ item.title }}</ins> 

{{ item.text }}

{{ if (isset item.image ) }}
<img width="480" alt="{{ item.title }}" src="https://illinifanboy.github.io/{{ item.image }}">

{{ end }}


{% endfor %}




