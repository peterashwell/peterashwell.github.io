---
layout: post
title:  "Handlebars access array by loop index"
date:   2015-10-07 10:00:00
categories: handle bars access array element computed value loop index
---

If you're trying to access an array element for a computed value in handlebars, like @index inside a loop, use `lookup`.

Inside a loop, use lookup along with the special index variable, like this `{{lookup <array_ref> @index}}`

Remember that inside a loop you may need to refer to the higher level scope, so say your model is

<pre lang="javascript"><code>{
  myArray: ['a', 'b', 'c', 'd']
  toIterate: ['x', 'y', 'z']
}
</code></pre>

<pre lang="javascript"><code>\{\{\#each toIterate\}\}
	\<div\>
		\{\{lookup ../myArray @index\}\} \{\{this\}\}
	\</div\>
\{\{/each\}\}
</code></pre>

Gives you
<pre><code>
a x
b y
c z
</code></pre>

Why are hipsters so bad at documenting things? It's like a rule of thumb about hip JS frameworks that the documentation is never updated
with obvious tricky cases that arise as soon as the thing isn't being used like a toy.
