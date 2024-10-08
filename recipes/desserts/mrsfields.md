---
layout: page
title: Mrs. Fields Cookies
# blurb: A short, one-line introduction
finalproduct: assets/images/recipes/mrsfields/mrsfieldsfinalproduct-sm.jpg
handwritten: 
  - image: assets/images/handwritten/mrsfields-sm.jpg 
review: I tried this.  Makes a perfectly decent chocolate chip cookie - my wife says they are excellent. 
story: The steps from the original, handwritten recipe are labeled with 'Gma-'.  My own versions of the steps are labeled with 'Steve-'. 
ingredientsimage: assets/images/recipes/mrsfields/mrsfieldsingreds-sm.jpg
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
  - name: Flour
    amount: 2-1/2 to 3 cups
    note: 
  - name: Chocolate
    amount: 8 ounces
    note: Chips or broken bar
    
steps:
  - header: Gma - Mix Everything
    text: Mix all ingredients together.  Use a mixer for smooth texture.
#    image: assets/images/general/noimage.jpg
  - header: Gma - Shape
    text: Shape into golf ball size balls.  Place on greased cookie sheet.
#    image: 
  - header: Gma - Flatten
    text: Push down slightly.
#    image: 
  - header: Gma - Bake
    text: Bake 6-8 minutes at 400 degrees.
#    image: 
  - header: Steve - Cream
    text: Soften the butter.  Cream the butter with the sugars.
    image: assets/images/recipes/mrsfields/mrsfieldscream-sm.jpg
  - header: Steve - Eggs
    text: Lightly beat the eggs and add them to the creamed mixture.
    # image: assets/images/recipes/mrsfields/mrsfieldscream-sm.jpg
  - header: Steve - Add the Rest
    text: Mix in everything else except the oats, flour, nuts and chocolate.
    # image: assets/images/recipes/mrsfields/mrsfieldscream-sm.jpg
  - header: Steve - Add the Oats
    text: Mix in the oats.
    # image: assets/images/recipes/mrsfields/mrsfieldscream-sm.jpg
  - header: Steve - Add the Flour
    text: Mix in the flour a little at a time.
    # image: assets/images/recipes/mrsfields/mrsfieldscream-sm.jpg
  - header: Steve - Nuts and Chocolate
    text: Fold in the nuts and the chocolate chips/pieces.
    # image: assets/images/recipes/mrsfields/mrsfieldscream-sm.jpg
  - header: Steve - Shape
    text: Shape into golf ball size balls.  Place on greased cookie sheet.
    image: assets/images/recipes/mrsfields/mrsfieldsready-sm.jpg 
  - header: Steve - Flatten
    text: Push down slightly.
    # image: assets/images/recipes/mrsfields/mrsfieldsready-sm.jpg 
  - header: Steve - Bake
    text: Bake 6-8 minutes at 400 degrees.
    image: assets/images/recipes/mrsfields/mrsfieldsintheoven-sm.jpg
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

