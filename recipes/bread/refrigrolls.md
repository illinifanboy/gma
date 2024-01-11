---
layout: page
title: Refrigerator Rolls
# blurb: A short, one-line introduction
# finalproduct: assets/images/general/noimage.jpg
handwritten: 
  - image: assets/images/handwritten/refrigrolls1-sm.jpg
  - image: assets/images/handwritten/refrigrolls2-sm.jpg
  - image: assets/images/handwritten/refrigrolls3-sm.jpg
# review: Not yet reviewed.
# story: 
# ingredientsimage: assets/images/general/noimage.jpg
ingredients:
  - name: Ingredient 1
    amount: Amount 1
    note: Note 1
  - name: Ingredient 2
    amount: Amount 2
    note: 
    
steps:
  - header: Step 1
    text: The text that says what to do 1.
    image: assets/images/general/noimage.jpg
  - header: Step 2
    text: The text that says what to do 2.
    image: 
  - header: Step 3
    text: The text that says what to do 3.
    image: assets/images/general/noimage.jpg
---

{::comment}========================={:/comment}

{{ if (isset page.blurb ) }}
> Blurb: {{ page.blurb }}
{{ end }}

Jump to **[\<Recipe\>](#recipe)**.

<!--- ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ --->

page.finalproduct is {% if page.finalproduct == blank %}blank{% else %}"{{ page.finalproduct }}"{% endif %}

page.finalproduct is {% if page.finalproduct == "" %}empty string{% else %}"{{ page.finalproduct }}"{% endif %}

page.finalproduct is {% if page.finalproduct == nil %}nil{% else %}"{{ page.finalproduct }}"{% endif %}


<!--- {{ if (isset page.finalproduct ) }}  --->
{{ if (!empty(page.finalproduct)) }} 

<img alt="Final Product" src="https://illinifanboy.github.io/{{ page.finalproduct }}">

{{ end }}

{{ if (isset page.review ) }}
### Steve's Review  
{{ page.review }}    
{{ end }}

### Grandma's Handwritten Recipe

{% for item in page.handwritten %}

<img alt="Grandma's Handwritten Recipe" src="https://illinifanboy.github.io/{{ item.image }}">

{% endfor %}

{{ if (isset page.review ) }}

{{ page.story }}

{{ end }}

## Recipe

### Ingredients


{{ if (isset page.ingredientsimage ) }}
<img alt="Ingredients" src="https://illinifanboy.github.io/{{ page.ingredientsimage }}">
{{ end }}


{{ if (isset page.ingredients ) }}
Ingredient | Measurement, Weight | Notes
---|---|----
{% for item in page.ingredients %}{{ item.name }} | {{ item.amount }} | {{ item.note }}
{% endfor %}
{{ end }}



### Steps

#### <ins>Step 1</ins>

Step 1 text.

<img width="480" alt="Step 1" src="https://illinifanboy.github.io/assets/images/general/noimage.jpg">

### Step Looping

{% for item in page.steps %}

### <ins>{{ item.header }}</ins> 

{{ item.text }}

{{ if (isset item.image ) }}
<img width="480" alt="{{ item.title }}" src="https://illinifanboy.github.io/{{ item.image }}">
{{ end }}
{% endfor %}



