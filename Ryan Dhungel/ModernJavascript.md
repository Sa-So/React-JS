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
- use a comma to seperate values
- let [ , , See] = ['a',5,3] 
- console.log(See)

### Restructuring
- Object Literal enhancemment ?
```js
var a='a'
var b = 845
va comb = {a,b};
```
- object methods ?
- okay so we can assign prop of obj to be a function !
- when we declared a function outside it's this value was window 
- when we asssigned it to obj then (this value changed ?)
```js
let a = {
  b:'b',
  c: 'c',
  d() {
    console.log(`hey $(this.a)`);
  }
  // ES^6
};
```
# Spread the rest operators
- ... 3 dots
### combine objects / arrays !
- when you combine it doesn't modify / mutate the original source 
- we create new instance !
```js
var nepal = ['Everest','Fish Tail'];
var jap = ['fuji'];
var comb = [...nepal,...jap];

```
### rest
```js
var a = ['a','b'];
var [f,...rest] = a;

```
### useful in 
state - that contains certain data then u might get additional data from the api , so u might want to combine both data and render into app


# Classes
- create func and add methods ? on the functionibj using the prototype ??
- js - func are obj - a prototype obj is always created when u create an obj
```js
// func a(b){this.b = b}
// a.prototype.display = func(){clg(this.b);}
// var c = new a("this is b")
// clg(c.display());


```
### ES6
```js
class a { // this is also a function and so an obj so has a prototype obj.
  constructor(b,c){
    this.b= b;
    this.c = c;
   }
}
clg(a.prototype) // constructor ?
// if constructor is a part of the prototype obj then y do we get 
// only a constr when we clg prototype ?
// constructor sets prop of class => this makes obj like prop of class (make sense)!!

```
### Extends 
```js
class ExtA extends a { 
  constructor(destination,days,gear){
    super(dest,days)// passing to parent for handling 
    this.gear= gear ;
  }
  display(){
    super.info();
    clg("bring your ${this.gear.join("and your")}")
  }
}
```





