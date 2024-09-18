---
layout: page
title: Chocolate Fudge Drops
# blurb: A short, one-line introduction
# finalproduct: assets/images/general/noimage.jpg
handwritten: 
  - image: assets/images/handwritten/chocfudge1-sm.jpg
  - image: assets/images/handwritten/chocfudge2-sm.jpg
  - image: assets/images/handwritten/chocfudge3-sm.jpg
  - image: assets/images/handwritten/chocfudge4-sm.jpg
review: I have not tried this recipe yet.<br /><br />As you can see below, this recipe was not in great shape.  The paper was brown and the pencil marks were faded.  Because of this, I scanned it twice.  The first two images, below, are the "original" scan.  The secord two images are the same pages put through the "magic" filter to enhance readability.<br />I have put my own comments in parenthesis.
# story: 
# ingredientsimage: assets/images/general/noimage.jpg
ingredients:
  - name: Semi-sweet Chocolate
    amount: 1 package
    note: Melted
  - name: Flour 
    amount: 1-1/2 cups
    note: Sifted
  - name: Baking Powder
    amount: 1/2 tsp. (I think)
    note: Was hard to read.
  - name: Salt
    amount: 1/2 tsp. (I think)
    note: Was hard to read.
  - name: Shortening 
    amount: 1/2 cup
    note: 
  - name: Brown Sugar 
    amount: 1/2 cup
    note: 
  - name: Eggs
    amount: 2
    note: Slightly beaten (I think)
  - name: Vanilla
    amount: 1/2 tsp.
    note: 
  - name: Chopped Nuts
    amount: 1/2 cup
    note: 
    
steps:
  - header: Melt Chocolate
    text: Melt the chocolate over hot water (I guess she means in a double boiler).
#    image: assets/images/general/noimage.jpg
  - header: Sift Dry Ingredients 
    text: Sift together the flour, baking powder, and salt.  Set aside.
#    image: assets/images/general/noimage.jpg
  - header: Mix Shortening and Sugar
    text: Blend shortening and sugar (does blend mean cream?).
#    image: assets/images/general/noimage.jpg
  - header: Add Eggs
    text: Add (slightly beaten?) eggs to the shortening mixture.
#    image: assets/images/general/noimage.jpg
  - header: Add Remaining Ingredients
    text: Add the melted semi-sweet chips, vanilla, and chopped nuts.
#    image: assets/images/general/noimage.jpg
  - header: Drop on Cookie Sheet
    text: Drop the dough by teaspoon onto a cookie sheet.
#    image: assets/images/general/noimage.jpg
  - header: Bake
    text: Bake and 375 degrees for 15 minutes.
#    image: assets/images/general/noimage.jpg
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

