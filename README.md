# JavaScript-Refresher

# Table of content ( click to navigate )
- [let & const](#let-&-const)
- [ES6 Arrow Functions](#ES6-Arrow-Functions)


</br>

# let & const

<code>let</code>  and <code>const</code> basically replace var . You use <code>let</code>  instead of var  and <code>const</code>  instead of var  if you plan on never re-assigning this "variable" (effectively turning it into a constant therefore). </br>
</br>
<code>let</code> : The <code>let</code> declaration declares re-assignable, block-scoped local variables, optionally initializing each to a value.

```js
let x = 1;

if (x === 1) {
  let x = 2;

  console.log(x);
  // Expected output: 2
}

console.log(x);
// Expected output: 1

```
<code>const</code> : The <code>const</code> declaration declares block-scoped local variables. The value of a constant can't be changed through reassignment using the assignment operator, but if a constant is an object, its properties can be added, updated, or removed.

```js
const number = 42;

try {
  number = 99;
} catch (err) {
  console.log(err);
  // Expected output: TypeError: invalid assignment to const 'number'
  // (Note: the exact output may be browser-dependent)
}

console.log(number);
// Expected output: 42
```
# ES6 Arrow Functions

An arrow function expression is a compact alternative to a traditional function expression, with some semantic differences and deliberate limitations in usage:

- Arrow functions don't have their own bindings to this, arguments, or super, and should not be used as methods.
- Arrow functions cannot be used as constructors. Calling them with new throws a TypeError. They also don't have access to the new.target keyword.
- Arrow functions cannot use yield within their body and cannot be created as generator functions.

Arrow function syntax may look strange but it's actually simple.

```js
function callMe(name) { 
    console.log(name);
}
```
which you could also write as:

```js
const callMe = function(name) { 
    console.log(name);
}
```
becomes: 

```js
const callMe = (name) => { 
    console.log(name);
}
```
Important: 

When having no arguments, you have to use empty parentheses in the function declaration:

```js
const callMe = () => { 
    console.log('Max!');
}
```
When having exactly one argument, you may omit the parentheses:

```js
const callMe = name => { 
    console.log(name);
}
```
When just returning a value, you can use the following shortcut:

```js
const returnMe = name => name
```

That's equal to:

```js
const returnMe = name => { 
    return name;
}
```
