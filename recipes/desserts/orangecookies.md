---
layout: page
title: Orange Cookies
# blurb: A short, one-line introduction
# finalproduct: assets/images/general/noimage.jpg
handwritten: 
  - image: assets/images/handwritten/orangecookies-sm.jpg
review: I have not yet tried this recipe.
# story: 
# ingredientsimage: assets/images/general/noimage.jpg
ingredients:
  - name: Butter or Margarine
    amount: 1/2 cup
    note: 
  - name: Sugar
    amount: 1/2 cup
    note: 
  - name: Grated Orange Zest
    amount: 1 teaspoon
    note: 
  - name: Orange Juice
    amount: 2 tablespoons
    note: 
  - name: Flour
    amount: 1 cup
    note: Sifted
  - name: Baking Soda
    amount: 1/2 teaspoon
    note: 
  - name: Egg
    amount: 1
    note: 
  - name: Chopped Nuts
    amount: 1/2 cup
    note: 
  - name: Dates
    amount: 1/2 cup
    note: 
     
steps:
  - header: Prepare Pan
    text: Grease a 9x9x2 inch square cake pan.
  - header: Melt Butter
    text: Melt butter in a saucepan.  Remove from heat.
  - header: Add Sugar and Orange
    text: Add sugar, orange zest, and orange juice to the melted butter.  Blend.
  - header: Add Dry Ingredients
    text: Sift flour and baking soda together.  Stir into butter mixture.
  - header: Add Egg
    text: Add egg and blend well.
  - header: Bake
    text: Pour into pan.  Bake for 25 minutes \[No temperature given!\].  Cool in pan.
  - header: Frost and Serve
    text: Frost with Orange Frosting and cut into 16 bars.  Enjoy.




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

#### <ins>{{ item.header }}</ins> 

<font size="4">{{ item.text }}</font>

{{ if (isset item.image ) }}
<img width="480" alt="{{ item.title }}" src="https://illinifanboy.github.io/{{ item.image }}">
{{ end }}
{% endfor %}

{% endif %}

