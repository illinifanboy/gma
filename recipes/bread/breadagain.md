---
layout: page
title: Bread I
# blurb: A short, one-line introduction
# finalproduct: assets/images/general/noimage.jpg
handwritten: 
  - image: assets/images/handwritten/breadagain-sm.jpg
review: I tried this recipe and it did not work out.  The dough seemed very dry.  I used a stand mixer with a dough hook to knead.  However, the dough was too dry for this to work, so I added some milk.  I also think the proofing wasn't long enough.  The bread did not rise enough.  Bottom line, I made bricks.
story: My Grandmother made so much bread that she kept a medium garbage can in her kitchen just to hold flour. 
# ingredientsimage: assets/images/general/noimage.jpg
ingredients:
  - name: Yeast
    amount: 2 cakes
    note: 4-1/2 teaspoons dry yeast?
  - name: Water
    amount: 1/4 cup
    note: lukewarm
  - name: Flour
    amount: 5 cups
    note: Sifted.  I will try bread flour.
  - name: Butter
    amount: 4 tablespoons
  - name: Sugar
    amount: No amount given.
    note: Trying 1-1/2 tablespoons.
  - name: Salt
    amount: 1 tablespoon
  - name: Top Milk
    amount: 1/4 cup
    note: Top milk is not homogenized.  I'll use half and half.
  - name: Eggs
    amount: 3
    note: Beaten

steps:
  - header: Dissolve the Yeast
    text: Mix the yeast into the lukewarm water.
  - header: Sift the Flour
  - header: Create Warm Milk Mixture
    text: Heat the following to lukewarm - butter, sugar, salt, milk.
  - header: Add Eggs, Yeast, Milk to Flour
    text: Add the lukewarm milk, the yeast mixture, and the beaten eggs to the flour.  Beat with a wooden spoon.
  - header: Knead
    text: Turn mixture onto a floured board.  Knead for 8 to 10 minutes.
  - header: Let Rise
    text: Put dough in a clean large bowl.  Cover and let rise about 2 hours.  
  - header: Knead Again
    text: Not too much.
  - header: Shape
    text: Make into two loaves.  Place in greased pans.  What size pans?
  - header: Rise Again
    text: Cover and let rise another hour.
  - header: Bake
    text: 350 degrees for 1 hour.
  

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

#### <ins>{{ item.header }}</ins> 

{% if item.text != nil %}
{{ item.text }}
{% endif %}

{% if item.image != nil %}
<img width="480" alt="{{ item.title }}" src="https://illinifanboy.github.io/{{ item.image }}">
{% endif %}

{% endfor %}

{% endif %}

