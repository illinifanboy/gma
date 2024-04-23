---
layout: page
title: Oatmeal Cookies
# blurb: A short, one-line introduction
finalproduct: 
  - image: assets/images/recipes/oatmealcookies/oatmealcookiespic-sm.jpg
handwritten: 
  - image: assets/images/handwritten/oatmealcookies-sm.jpg
review: These cookies are good, not great, but I'll likely make this recipe again.<br /><br />I don't eat oatmeal cookies very often, but these seem atypical.  They are not too sweet.  The texture and size remind me of muffin tops.  I also did not add walnuts (yuck!) and used golden raisins.  <br /><br />This makes alot of cookies, so I made two-thirds of a recipe.  That worked out well. <br /><br />The instructions provide by Grandma were slim, "30 mins 375 degrees".  The detailed instructions provided below were dreamed up by my wife and me. 
# story: 
# ingredientsimage: assets/images/general/noimage.jpg
ingredients:
  - name: Oleo (aka marganine)
    amount: 2 sticks
    note: 
  - name: Butter
    amount: 1 stick
    note: 
  - name: Flour
    amount: 3 cups
    note: 
  - name: Old-fashioned Oats
    amount: 3 cups
    note: 
  - name: Sugar
    amount: 1-1/2 cups
    note: 
  - name: Eggs
    amount: 3
    note: Beaten
  - name: Baking Powder
    amount: 1-1/2 teaspoons
    note: 
  - name: Baking Soda
    amount: 1 teaspoon
    note: 
  - name: Salt
    amount: 1/2 teaspoon
    note: 
  - name: Cinnamon
    amount: 3 teaspoons
    note: 
  - name: Raisins
    amount: 1-1/2 cups
    note: 
  - name: Milk
    amount: 1 cup
    note: 
    
steps:
  - header: Preheat oven.
    text: 375 degrees.
  - header: Soften butter and margarine
    text: Soften butter and margarine for creaming.
  - header: Mix Dry Ingredients
    text: Mix oats, flour, baking powder, baking soda, salt and cinnamon in a large bowl.
#    image: assets/images/general/noimage.jpg
  - header: Cream butter, margarine and sugar.
    text: Cream until butter / margarine are combined with sugar.  Use a large bowl. Pick your own tool.  I used a pastry blender.
#  image: 
  - header: Add eggs.
    text: Mix beaten eggs into creamed mixture.
#    image: assets/images/general/noimage.jpg
  - header: Add milk.
    text: Mix milk into creamed mixture.
  - header: Mix dry into wet.
    text: Gradually mix dry ingredients into the wet ingredients.  Gradual mixing decreases the likelihood of clumping.
  - header: Put cookies on baking sheets.
    text: I scooped ping pong ball sized cookies onto parchment paper covered cookies sheets. Parchment avoided any sticking. 
  - header: Bake cookies.
    text: Bake at 350 degrees for thirty minutes until bottoms are light brown.
  - header: Enjoy!
    text: Should create around 3 dozen cookies.  Cool and eat.
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

{{ item.text }}

{{ if (isset item.image ) }}
<img width="480" alt="{{ item.title }}" src="https://illinifanboy.github.io/{{ item.image }}">
{{ end }}
{% endfor %}

{% endif %}

