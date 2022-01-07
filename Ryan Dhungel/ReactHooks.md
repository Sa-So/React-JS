# hooks
- u can use states inside functional components using hooks !
- using hook called useState 
- for side effects : useEffect
- no need to write lifecycle methods 
# why class components 
- keep data in state
- use lifecycle methods
- to pass props from classes to func compo
# counter app using class
- bootstrap material ui
# using func compo
- useState returns 2 things
- current state value and a function to update that state.
```js
import React , {Component , useState , useEffect } from 'react';
const App = () => {
  const [count,setCount] = useState(0); 
  const increment = ()=>{
    setCount(count+1);
  };
  return {
    <div>
      <h3> {count} </h3>
      button.onClick={increment}
    </div>
  }
}
```
# useEffect
- as state changes useEffect will run 
- 


```js

```
