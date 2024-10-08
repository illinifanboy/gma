---
layout: page
title: Cheesecake II
blurb: The recipe says Cheesecake, but it really is more of a cheese pie based on a vanilla custard.
# finalproduct: assets/images/general/noimage.jpg
handwritten: 
  - image: assets/images/handwritten/cheesecakeii-sm.jpg
review: This made a good dessert.  It is more of a vanilla custard pie than a cheesecake.  The cream cheese flavor is very slight.  It needs to be served with fresh (unsweetened) fruit to cut the sweetness and to add some flavor to the vanilla custard.
story: This recipe was one of the few that was typed.  My Grandmother never used a typewriter, so this was probably given to her by a friend. 
# ingredientsimage: assets/images/general/noimage.jpg
ingredients:
  - name: Milk
    amount: 1 cup
    note: 
  - name: Sugar 
    amount: 1 cup
    note: 
  - name: Egg
    amount: 1
    note: 
  - name: Salt
    amount: To taste
    note: 
  - name: Gelatin
    amount: 1 envelope
    note: Recipe says use Knox
  - name: Cold Water
    amount: 1/4 cup
    note: 
  - name: Cream Cheese
    amount: Two 3-ounce packages.
    note: 6 ounces
  - name: Vanilla
    amount: 1 teaspoon
    note: 
  - name: Lemon Juice
    amount: 2 teaspoons
    note: 
  - name: Whipping Cream
    amount: 1/2 pint
    note: 
  - name: Graham Cracker Crumbs
    amount: 1-1/2 cups
    note: For crust
  - name: Sugar
    amount: 1 tablespoon
    note: For crust
  - name: Cinnamon
    amount: To taste
    note: For crust
  - name: Butter, melted
    amount: 3 tablespoons
    note: For crust
    
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

