# modern js
- JS is based on Ecmascript specs
- European Comp manufacturing association
- ES6 - 2016
# var using const
- old school
```js
var name = 'Ryan'
```
- ES6 introduced const and let
# let
- var : it becomes part of the window object
- js was made for the browser - window !
- if an object doesn't have a prop named x then obj.name would return "" ?
# template strings
- f strings
- better than string concat
- 
```js
let name = 'Ryan';
let age = prompt('Guess age');
let res = `${name} is ${age}`;
alert(res)
```
- useful when making api calls
# default parameters
```js
function welcome(user="Mystery person",message="goodday"){
  alert(`Hello ${user}, ${message}`);
}
```
# Arrow functions
```js
function greet(user="Mystery person",message="goodday"){
  return alert(`Hello ${user}, ${message}`);
}
let gr = msg => alert(`${msg}`);
let createBlog = (title,body) => {
  if(!title){
    throw new Error("title req");
  }
  if(!body){
    throw new Error("body req");
  }
  return alert(`hello`)
}
let greeeting = () =>{alert(`hello`)}
greeting()
```
# this keyword 
- even function become part of the window obj
- so this keyword refers to the window obj
- in js function can be used as the value 
- so i am guessing this means that var in c++ = function,var in js
```js
let nepal = {
  mt : ['Everest','Fish Tail'];
  printDash : function(){
    setTimeout(function(){
      console.log(this.mt.join(" - "))
    },3000)
  }
}
alert(nepal.mt)// this will work
nepal.printDash() // won't work
// so use arrow functions !!
// arrow functions don't have their own enclosing context ?
```
# Destructuring 
```js
let a = {
  b:'b',
  c: 'c',
  d:'d'
}
let {b,c} = ä;
```
### destructuring function paramaters
({b,c}) => {console.log(a)}

### destructuring arrays






