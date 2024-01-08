---
layout: page
title: Template Title
blurb: A short, one-line introduction
finalproduct: assets/images/general/noimage.jpg
handwritten: assets/images/general/noimage.jpg
review: Not yet reviewed.
story: 
ingredientsimage: assets/images/general/noimage.jpg
ingredients:
  - name: Ingredient 1
    amount: Amount 1
    note: Note 1
  - name: Ingredient 2
    amount: Amount 2
    note: 
    
steps:
  - header: Step 1
    text: The text that says what to do 1.
    image: assets/images/general/noimage.jpg
  - header: Step 2
    text: The text that says what to do 2.
    image: 
  - header: Step 3
    text: The text that says what to do 3.
    image: assets/images/general/noimage.jpg
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

<img alt="Ingredients" src="https://illinifanboy.github.io/{{ page.ingredientsimage }}">


Ingredient | Measurement, Weight | Notes
---|---|----
Item Name | Amount | Notes
Item Name | Amount | Notes
Item Name | Amount | Notes
Item Name | Amount | Notes
{% for item in page.ingredients %}{{ item.name }} | {{ item.amount }} | {{ item.note }}{% endfor %}

### Steps

#### <ins>Step 1</ins>

Step 1 text.

<img width="480" alt="Step 1" src="https://illinifanboy.github.io/assets/images/general/noimage.jpg">

### Step Looping

{% for item in page.steps %}

### <ins>{{ item.header }}</ins> 

{{ item.text }}

{{ if (isset item.image ) }}
<img width="480" alt="{{ item.title }}" src="https://illinifanboy.github.io/{{ item.image }}">
{{ end }}
{% endfor %}




