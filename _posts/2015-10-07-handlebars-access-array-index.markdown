---
layout: post
title:  "Handlebars access array by loop index"
date:   2015-10-07 10:00:00
categories: handle bars access array element computed value loop index
---

If you're trying to access an array element for a computed value in handlebars, like `@index` inside a loop, use `lookup`.

Inside a loop, use lookup along with the special index variable, like this

    {% raw %}
    {{lookup <array_ref> @index}}
    {% endraw %}

Remember that inside a loop you may need to refer to the higher level scope, so say your model is

    {someArray: ['a', 'b', 'c', 'd'], toIterate: ['x', 'y', 'z']}

And your template

    {% raw %}
    {{#each toIterate}}
	<div>
	  {{lookup ../someArray @index}} {{this}}
	</div>
    {{/each}}
    {% endraw %}

Then you get

    a x
    b y
    c z

Why are hipsters so bad at documenting things? It's like a rule of thumb about hip JS things that the documentation never covers
 obvious tricky cases that arise as soon as the thing isn't being used like a toy.
