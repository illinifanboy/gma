---
layout: page
title: Cheesecake II
blurb: The recipe says cheesecake, but it really is more of a cheese pie based on a vanilla custard. 
finalproduct: assets/images/recipes/cheesecakeii/ck2slice-sm.jpg
handwritten: 
  - image: assets/images/handwritten/cheesecakeii-sm.jpg
review: This made a good dessert.  It is more of a vanilla custard pie than a cheesecake.  The texture is very light.  The cream cheese flavor is very slight.  It needs to be served with fresh (unsweetened) fruit to cut the sweetness and to add some flavor to the vanilla custard.
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
    note: 6 ounces softened
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
    
steps:
  - header: Mix the shell. 
    text: Mix the graham crack crumbs, 1 tablespoon of sugar and cinnamon (I used 1/2 teaspoon).
    image: assets/images/recipes/cheesecakeii/ck2crumbs-sm.jpg
  - header: Put crumbs in pan.
    text: Put crumb mixture into a pie pan. The recipe says to use an 8 inch pan.  I used a 9 inch pie pan.  The recipe also says to save half of the crumbs to use as a topping.  I only saved one quarter and still had too much. Chill the shell.
    image: assets/images/recipes/cheesecakeii/ck2crust-sm.jpg
  - header: Mix custard ingredients.
    text: In a small saucepan, mix the milk, sugar, egg and salt.
    image: assets/images/recipes/cheesecakeii/ck2custardingreds-sm.jpg
  - header: Cook custard.
    text: Cook until thick stirring constantly [this only thickens slightly].
    image: assets/images/recipes/cheesecakeii/ck2custardcooking-sm.jpg
  - header: Soak the gelatin.
    text: In a small bowl, mix the gelatin and water and sit aside.
    image: assets/images/recipes/cheesecakeii/ck2gel-sm.jpg
  - header: Add gelatin to custard.
    text: Add the soaked gelatin to the hot custard.
    image: assets/images/recipes/cheesecakeii/ck2gel-sm.jpg
  - header: Cool the custard.
    text: Custard needs to cool until no longer warm. 
  - header: Mix the cream cheese. 
    text: Mix the softened cream cheese, vanilla, and lemon juice.
  - header: Whip the cream.
    text: Whip the whipping cream until thick.  Using a freezing-cold bowl helps.
    image: assets/images/recipes/cheesecakeii/ck2freezer-sm.jpg
  - header: Fold-in the cream.
    text: Fold the whipped cream into the custard.
    image: assets/images/recipes/cheesecakeii/ck2fold-sm.jpg
  - header: Fill the shell.
    text: Pour the cream cheese mixture into the pie shell.
    image: assets/images/recipes/cheesecakeii/ck2shell-sm.jpg
  - header: Add topping.
    text: Sprinkle reserved crumbs onto the pie.
    image: assets/images/recipes/cheesecakeii/ck2finalpie2-sm.jpg
  - header: Chill.
    text: Chill the pie until good and firm.  Enjoy!
    image: assets/images/recipes/cheesecakeii/ck2finalpie-sm.jpg
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

