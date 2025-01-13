---
layout: page
title: Cake-n-Cheesecake
# blurb: A short, one-line introduction
finalproduct: assets/images/recipes/cakencheesecake/cncfinal-sm.jpg
handwritten: 
  - image: assets/images/handwritten/cakeandcheesecake-sm.jpg
# review: Not yet reviewed.
story: I had to find something on the internet (https://www.food.com/recipe/cake-n-cheesecake-147937) to flesh out this recipe especially the cooking steps.  They say this recipe is from 1954. 
ingredientsimage: assets/images/recipes/cakencheesecake/cncingreds-sm.jpg
ingredients:
  - name: Cream Cheese
    amount: One eight ounce package
    note: For topping.
  - name: Sour Cream
    amount: 1/2 cup
    note: For topping.
  - name: Vanilla
    amount: 1 teaspoon
    note: For topping.
  - name: Unbeaten eggs.
    amount: 2 eggs
    note: For topping.
  - name: Sugar
    amount: 2/3 cup
    note: For topping.
  - name: All purpose flour
    amount: 1 cup
    note: For cake.
  - name: Baking Powder
    amount: 1 teaspoon
    note: For cake.
  - name: Salt
    amount: 1/2 teaspoon
    note: For cake.
  - name: Margarine
    amount: 1/2 cup
    note: For cake.
  - name: Sugar
    amount: 2/3 cup
    note: For cake.
  - name: Eggs
    amount: 2 eggs
    note: For cake.
  - name: Milk
    amount: 1 tablespoon
    note: For cake.
  - name: Vanilla
    amount: 1 teaspoon
    note: For cake.
    
steps:
  - header: Topping Step 1
    text: Beat cream cheese and sugar together until well blended.
  #    image: assets/images/general/noimage.jpg
  - header: Topping Step 2
    text: Mix in sour cream and vanilla.
    # image: 
  - header: Topping Step 3
    text: Beat in eggs one at a time then set the topping mixture aside.
    # image: assets/images/general/noimage.jpg
  - header: Cake Step 1
    text: Sift together flour, sugar, salt, and backing powder.  Set aside.
    # image: assets/images/general/noimage.jpg
  - header: Cake Step 2
    text: Cream butter and sugar.
    # image: assets/images/general/noimage.jpg
  - header: Cake Step 3
    text: Beat in eggs.
    # image: assets/images/general/noimage.jpg
  - header: Cake Step 4
    text: Stir in milk and vanilla.
    # image: assets/images/general/noimage.jpg
  - header: Cake Step 5
    text: Stir in dry ingredients.
    # image: assets/images/general/noimage.jpg
  - header: Cake Step 6
    text: Grease and flour a 9-inch pie plan or 9 by 9 square pan.
    # image: assets/images/general/noimage.jpg
  - header: Cake Step 7
    text: Spread cake batter over bottom and sides of pan.  Spread thinner on the sides.
    image: assets/images/recipes/cakencheesecake/cncfillable-sm.jpg
  - header: Cake Step 8
    text: Spoon cheesecake topping over the batter.
    image: assets/images/recipes/cakencheesecake/cncready-sm.jpg
  - header: Cake Step 9
    text: Bake at 325 degrees for 50 minutes.
    # image: assets/images/general/noimage.jpg
  - header: Cake Step 10
    text: Cool then refrigerate for 4 hours.
    # image: assets/images/general/noimage.jpg
  - header: Cake Step 11
    text: Enjoy!
    image: assets/images/recipes/cakencheesecake/cncslice-sm.jpg
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

