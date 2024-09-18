---
layout: page
title: Mrs. Fields Cookies
# blurb: A short, one-line introduction
# finalproduct: assets/images/general/noimage.jpg
handwritten: 
  - image: assets/images/handwritten/mrsfields-sm.jpg
# review: Not yet tried.  This recipe is typed, but I am calling this handwritten.
# story: 
# ingredientsimage: assets/images/general/noimage.jpg
ingredients:
  - name: Sugar
    amount: 1 cup
    note: 
  - name: Brown Sugar
    amount: 1 cup
    note: 
  - name: Salt
    amount: 1/2 tsp.
    note: 
  - name: Baking Soda
    amount: 1 tsp.
    note: 
  - name: Butter
    amount: 1 cup
    note: Not margarine.
  - name: Eggs
    amount: 2
    note: 
  - name: Baking Powder
    amount: 1 tsp.
    note: 
  - name: Vanilla
    amount: 1 tsp.
    note: 
  - name: Oatmeal
    amount: 1-1/2 cups
    note: 
  - name: Nuts
    amount: 3/4 cup
    note: 
  - name: Flout
    amount: 2-1/2 to 3 cups
    note: 
  - name: Chocolate
    amount: 8 ounces
    note: Chips or broken bar
    
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

