---
layout: page
title: French Bread
# blurb: A short, one-line introduction
# finalproduct: assets/images/general/noimage.jpg
handwritten: 
  - image: assets/images/handwritten/frenchbread1-sm.jpg
  - image: assets/images/handwritten/frenchbread2-sm.jpg
review: Not yet tried.  
story: I am putting in ingredients / instructions for a 1/2 batch (one loaf) 
# ingredientsimage: assets/images/general/noimage.jpg
ingredients:
  - name: Dry Yeast
    amount: 1/2 package (1/4 oz., 7 grams, or 1 1/8 teaspoons)
    note: 
  - name: Warm Water 
    amount: 3/4 cups
    note: 
  - name: Salt
    amount: 1 teaspoon
    note: 
  - name: Sugar
    amount: 1 tablespoon
    note: 
  - name: Soft Shortening
    amount: 1 cup
    note: 
  - name: Sifted Flour
    amount: 3 cups
    note: 
    
steps:
  - header: Bloom the yeast.
    text: Sprinkle yeast into 1/4 cup water water.  Add 1 teaspoon of sugar.  Stir.
#    image: assets/images/general/noimage.jpg
  - header: Mix all by Flour.
    text: In large bowl, add remaining sugar, remaining water, and salt.  Add shortening and yeast mixture and mix well.
    # image: 
  - header: Add flour. 
    text: Add flour and mix well.
  - header: Intermittently stir the flour.
    text: With a spoon, work through the dough 5 times.  What a 10 minute interval between each time you work the dough.  The Internet says this process allows the flour to absorb water and allows starches to become sugars. 
  - header: Rest the dough.
    text: Roll the dough into a ball and let it rest 10 minutes.
  - header: Roll the dough.
    text: Roll the ball of dough into a 12 by 9 rectangle.
  - header: Shape the bread.
    text: Roll the rectangle as if you were creating a jelly roll.  Seal the edges.  <br />The Internet says sealing edges entails moistening the edge, pinching and pressing, folding in the piched edge, and resting the dough for a few minutes.
  - header: Place and score.
    text: Place the bread on a cookie sheet and score the top diagnally 6 times.
  - header: Rise
    text: Let rest for 1 1/2 hours.
  - header: Bake.
    text: Back at 400 degrees for 35 to 40 minutes.
---

{::comment}========================={:/comment}

{% if page.blurb != nil %}
> {{ page.blurb }}
{% endif %}

{% if page.ingredients != nil or page.steps != nil %}
Jump to **[\<Recipe\>](#recipe)**.
{% endif %}

<!--- ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ --->

<!--- 
page.finalproduct is {% if page.finalproduct == blank %}blank{% else %}"{{ page.finalproduct }}"{% endif %}

page.finalproduct is {% if page.finalproduct == "" %}empty string{% else %}"{{ page.finalproduct }}"{% endif %}

page.finalproduct is {% if page.finalproduct == nil %}nil{% else %}"{{ page.finalproduct }}"{% endif %}
--->

<!--- {{ if (isset page.finalproduct ) }}  --->
{% if page.finalproduct != nil %}

<img alt="Final Product" src="https://illinifanboy.github.io/{{ page.finalproduct }}">

{% endif %}

<!--- ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ --->

{% if page.review != nil %}
### Steve's Review  
{{ page.review }}    
{% endif %}

<!--- ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ --->

### Grandma's Handwritten Recipe

{% for item in page.handwritten %}

<img alt="Grandma's Handwritten Recipe" src="https://illinifanboy.github.io/{{ item.image }}">

{% endfor %}

{% if page.story != nil %}

{{ page.story }}

{% endif %}

<!--- ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ --->

{% if page.ingredients != nil or page.steps != nil %}
## Recipe
{% endif %}

{% if page.ingredients != nil %}
### Ingredients

{% if page.ingredientsimage != nil %}
{{ if (isset page.ingredientsimage ) }}
<img alt="Ingredients" src="https://illinifanboy.github.io/{{ page.ingredientsimage }}">
{% endif %}

Ingredient | Measurement, Weight | Notes
---|---|----
{% for item in page.ingredients %}{{ item.name }} | {{ item.amount }} | {{ item.note }}
{% endfor %}

{% endif %}

{::comment}========================={:/comment}
{% if page.steps != nil %}
### Steps

{% for item in page.steps %}

### <ins>{{ item.header }}</ins> 

{{ item.text }}

{{ if (isset item.image ) }}
<img width="480" alt="{{ item.title }}" src="https://illinifanboy.github.io/{{ item.image }}">
{{ end }}
{% endfor %}

{% endif %}

