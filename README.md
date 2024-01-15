# JavaScript-Refresher for React and also for begginers 

# Table of content ( click to navigate )
- [let & const](#let-&-const)


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
