# Prototype with JavaScript

In javascript, an object has a property called prototype which refers to another object (this iso object is called the prototype object). Each creation of a new object has a property called `__proto__` which are the functions or the properties inherited by the object instance. 

A class itself also has a property called `prototype` which represents what properties will be inherited by new instances of the class. 
- These includes variables, functions, and other properites defined in the class.

# Prototype chain

We can directly add methods or functions to the `prototype` itself which will be inherited by all instances of the object class with the syntax `Object.prototype.{name of the function} = function(){...};`. E.g. `Object.prototype.hello = function () {console.log("hello world");};`.
- Every instances of Object can then call the function `hello` using the dot notation.

Prototype Chain
- This is a set of objects defined by `__proto__`. 
  - Think of it like a linked list. Each time you traversed through a object using `__proto__` you reach another prototype object. At the end of the list is the `null` value. The `Object.prototype.__proto__` defined as `null`.
- We can use `Object.create()` to assigned a prototype object to another object. 
  - For example, let say we defined an object `let dessert = {....};`. We then created a new object called `cake` and assign the `dessert` object as a prototype object to cake like so: `let cake = Object.create(dessert)`. The prototype chain will then look like `cake -> dessert -> Object.prototype -> null`. When we call a function or property using the dot notation for `cake` such as `cake.name` it will first look for the `name` property in `cake` object before looking for it in `dessert` object, and it if does not exist in `dessert` it will look for it in `Object.prototype` before finally reaching the end of the chain and return `null` if it does not find the `name` property anywhere in its prototype chain. 
    - We can confirm the prototype object within a prototype chain as follow: 
      - `cake.__proto__ === dessert` returns `true`
      - `cake.__proto__.__proto__ === Object.prototype` returns `true`
    - We can add more properties to the `cake` object directly or to one of its prototype and it will still be able to access them.
      - `cake.name = chocolate`
        - Can access via `cake.name`
      - `Object.prototype.calories = 100`
        - Can access via `cake.calories`
    - We can also use `isProtoypeOf()` to check if an object is a prototype of another object
      - `dessert.isPrototypeOf(cake)` returns true; `dessert` is a prototype object of `cake` or `cake` contains a prototype object called `dessert`.

Note: functions are objects in JavaScript so we can add properties to a function
- If `foo` is a function defined as `let foo = function () {....};`:
  - We can add a property called `prop` to `foo` as so `foo.prop = "hi"`. We can then called the property using dot notation such as `console.log(foo.prop)`
    - A property can be anything (e.g. function, object, variable, etc.)

