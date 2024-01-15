# JavaScript-Refresher for React and also for begginers 

# Table of content ( click to navigate )
- [let & const](#let & const)


</br>

# let & const

let  and const  basically replace var . You use let  instead of var  and const  instead of var  if you plan on never re-assigning this "variable" (effectively turning it into a constant therefore). </br>
<p style="color:red">let :</p> 
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
