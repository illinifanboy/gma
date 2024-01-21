---
layout: page
title: Coconut Islands
# blurb: A short, one-line introduction
# finalproduct: assets/images/general/noimage.jpg
handwritten: 
  - image: assets/images/handwritten/coconutislands-sm.jpg
review: Trying today.
# story: 
# ingredientsimage: assets/images/general/noimage.jpg
ingredients:
  - name: Flour
    amount: 2 cups
  - name: Baking Soda
    amount: 1/2 teaspoon
  - name: Salt
    amount: 1/2 teaspoon
  - name: Unsweetened Chocolate
    amount: 3 ounces
  - name: Coffee
    amount: 1/4 cup
    note: Hot and strong.
  - name: Butter 
    amount: 1/2 cup
  - name: Brown Sugar
    amount: 1 cup
  - name: Egg
    amount: 1
  - name: Sour Cream
    amount: 1/2 cup
  - name: Coconut
    amount: 1/3 cup
    note: Finely cut.  Canned\(?\).
#  - name: Ingredient 2
#    amount: Amount 2
#    note: 
    
steps:
  - header: Sift Dry Ingredients Together
    text: Sift together the flour, baking soda, and salt.
  - header: Melt Chocolate and Coffee
    text: Melt the chocolate and coffee in a small saucepan over low heat.  Allow the mixture to cool.
  - header: Cream Butter and Sugar
    text: Gradually add brown sugar to butter creaming well.
  - header: Add Egg and Chocolate Mixture
    text: To the creamed butter, add unbeaten egg and chocolate mixture.  Beat well.
  - header: Add Dry Ingredients and Sour Cream
    text: Alternately mix in dry ingredients and sour cream beginning and ending with dry ingredients.  Blend thoroughly after each addition.
  - header: Add Coconut
    text: Stir in the coconut.
  - header: Bake
    text: Bake at 375 degrees for 12 to 15 minutes.  Yield 3-1/2 dozen cookies.


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

