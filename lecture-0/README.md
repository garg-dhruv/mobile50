# CS50 lecture-0 notes
## variables and array
```js
const varName = "value"

const arr = [
	'string',
	42,
	function() {console.log('hi')},
]
arr[2]()
```

## Coercion = Typecasting
```js
const explicit = String(42) // explicit === "42"
```

## == vs ===
== coerces the types, means implicitly changes the type
=== requires equivalent types
