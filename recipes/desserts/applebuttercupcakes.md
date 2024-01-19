---
layout: page
title: Apple Butter Cupcakes
# blurb: A short, one-line introduction
# finalproduct: assets/images/general/noimage.jpg
handwritten: 
  - image: assets/images/handwritten/applebuttercupcakes1-sm.jpg
  - image: assets/images/handwritten/applebuttercupcakes2-sm.jpg
# review: Not yet reviewed.
# story: 
# ingredientsimage: assets/images/general/noimage.jpg
ingredients:
  - name: Butter or Margarine
    amount: 1/2 cup
    note: 
  - name: Sugar
    amount: 1 cup
    note: 
  - name: Egg
    amount: 1
    note: 
  - name: Apple Butter 
    amount: 1 cup
    note: 
  - name: Vanilla
    amount: 1 teaspoon
    note: 
  - name: Flour
    amount: 1-3/4 cups
    note: Sifted
  - name: Baking Soda
    amount: 1 teaspoon
    note: 
  - name: Salt
    amount: 1/2 teaspoon
    note: 
  - name: Baking Powder
    amount: 1-1/2 teaspoon
    note: 
  - name: Lemon Juice
    amount: 2 tablespoons
    note: 
  - name: Evaporated Milk
    amount: 2/3 cup
    note: 
     
#steps:
#  - header: Step 1
#    text: The text that says what to do 1.
#    image: assets/images/general/noimage.jpg
#  - header: Step 2
#    text: The text that says what to do 2.
    # image: 
#  - header: Step 3
#    text: The text that says what to do 3.
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

