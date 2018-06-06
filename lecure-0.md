# CS50 lecture-0 notes
## Basic Syntex
### Variables and Array
```js
const varName = "value"

const arr = [
	'string',
	42,
	function() {console.log('hi')},
]
arr[2]()
```

### For loop
```js
for (let i = 0; i < arr.length; i++) {
	console.log(arr[i])
}
```
### Function defination
Method 1:
```js
function foo() {
	console.log("Hello, world")
}
```
Method 2: Not a proper method(just declaring a variable and stores the pointer to the function)
```js
const foo = function() {
	console.log("Hello, world")
}
```
## Types
### Premitive types
* undefined
* null
* boolean
* number 
* string
* (symbol)

### Coercion = Typecasting
```js
const explicit = String(42) // explicit === "42"
```
### == vs ===
== coerces the types, means implicitly changes the type  
=== requires equivalent types
Note: always use ===

### typeof
gives the type of variable
```js
console.log(typeof 42)
```
### Ambugity
```js
typeof null
```
**output**: object

### Flasy values
* undefined
* null
* false
* +0, -0, NaN
* ""

### Truthy values
* {}
* []
* Everything else (e.g. Array)

### Primitives vs Objects
* Primitives are immutable
* objects are mutable and stored by reference

* Passing by reference vs passing by value

### Objects
**methods to define object:**  
Old
```js
const o = new Object()
```
New
```js
const 0 = {}
```
**method to insert variables**  
Method 1
```js
o.Name = 'Dhruv'
o.greet = function() {
	consile.log('hi!')
}
```
Method 2
```js
o[Name] = 'Dhruv'
```
**Another method to definer objects**
```js
const o = {
	varname: 'value',
	foo: function() {
		console.log('hi')
}
```
objects can also be nested
```js
obj1 = {
	obj2: {
		//contents	
	}
}
```
**Method to access objects**  
obj.varName or obj["varName"] or obj[key]

#### Examples
* Object names are pointers and hence if we copy one object into another using assignment operator and then change something in new object, same change will be reflected in original object as well. 
* **cloning an object**
	* Method one (shelow copy)
	```js
	const o2 = Object.assign({}, o}
	```
	this function takes multiple objects, combines them into one, and returns the pointer to the new object
	hence we are creating a new empty object and combining it with original object
	Problem: when objects are nested
	* Method Two (deep copy)
	```js
	function deepCopy(obj) {
		// check if vals are objects
		// if so, copy that object (deep copy)
		// else retuen the value
		const keys = Object.keys(obj) // keys are the names of the variables of an object

		const newObject = {}

		for (let i = 0; i < keys.length; i++) {
			const key = keys[i]
			if (typeof obj[key] === 'object') {
				newObject[key] = deepVopy(obj[key])
			}
			else {
				newObject[key] = obj[key]
			}
		}
		return Object.assign({}, obj) // if we are gerented that no objects will be inside the object, we can just return a copy
	}
	```
	if we want this to work with array or other type of datatypes, we wll need to add them as well

### Prototype Inheritance
* Non-primitive types have properties/methods attached to them
example: push function in arrays
```js
const arr = []
arr.push('value')
```
* The function declared on the highest level is given priority over one with same name but deeper in the tree (this even reduces confusion)

### scope
#### Variable lifetime
* **Lexical Scoping**(var): from when they're declared until when their function ends
* **Block scoping**(const, let): untill the next } is reached
	* const: value can't be changed
	* let: value can be changed
* if we declare a variable without specifing type then it is declared as global variable
* **Hoisting**
	* Hoisted:
		* function defination
	* Not hoisted:
		* lexically0scoped initializations 
