---
layout: page
title: Almond Frosting
# blurb: A short, one-line introduction
# finalproduct: assets/images/general/noimage.jpg
handwritten: 
  - image: assets/images/handwritten/almondfrosting-sm.jpg
review: This was a flop.  Adding hot butter to powder sugar creates something that turns into a rock.  Frosting was hard, not fluffy, and not enough volume to frost a batch of cupcakes.
# story: 
# ingredientsimage: assets/images/general/noimage.jpg
ingredients:
  - name: Butter or Margarine
    amount: 1/4 cup
    note: 
  - name: Evaporated Milk
    amount: 2 tablespoons
    note: 
  - name: Powdered Sugar
    amount: 2 cups
    note: Sifted
  - name: Toasted Almonds 
    amount: 1/2 cup
    note: Chopped
     
steps:
  - header: Melt Butter
    text: Melt butter or margarine and keep on low heat until bubbly.
  - header: Mix in Some Sugar
    text: Remove butter from heat and mix in 1/3 of the sugar.
  - header: Mix in Rest of Sugar and Milk
    text: Add milk and remaining sugar and beat until smooth.
  - header: Add almonds.
    text: Stir in the almonds.
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

