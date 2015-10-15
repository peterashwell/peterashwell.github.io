If you're trying to access an array element for a computed value in handlebars, like @index inside a loop, use lookup

`{{lookup <array_ref> @index}}`

Remember that inside a loop you may need to refer to the higher level scope, so say your model is

{
  myArray: ['a', 'b', 'c', 'd']
  toIterate: ['x', 'y', 'z']
}

{{#each toIterate}}
	<div>
		{{lookup ../myArray @index}} {{this}}
	</div>
{{/each}}

Gives you
a x
b y
c z

Why are hipsters so bad at documenting things? It's like a rule of thumb about hip JS frameworks that the documentation is never updated
with obvious tricky cases that arise as soon as the thing isn't being used like a toy.
