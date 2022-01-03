# install 
- install node and it comes with it !
- npx create-react-app dir-name
# start app
- cd dir-name
- npm start
# files / folders
- Src/index.js- runs 
- App.js = component  
- see vid
# storing data in component state using ajax call
- make an api call (ajax call using lib)
- use axios instead of jquery 
> add state to constructor 
> componentWillMount()
> DidMount()
> 
- what if we want to mutate the state ??
- review if needed 
- class components are better when u want to bind the states and use lifecycle methods ?
- class compo are called stateful !
- (functional components )
# display data
```jsx
<div className="App">
  {this.state.users.map(user=><div>{user.cell}</div>)}
</div>
```
- curly braces for js ?
# Conditional rendering
- !this.state.loading ? 'data':'loading'
- u can also use && (shortcurcuiting)
> always name components with their starting letter capital 
```js
export const Comp1 = ()=>
export const Comp2 = ()=>
// and then destructure when trying to use 
```
- export default is used only when exporting one component only !

# click events
```js
form onSubmit = {this.func}
  input type = submit val="load users"
```
> bind functions using 
```js
this.func = this.func.bind(this)
```
### merge users state with new data
```js
this.setState({
  users:[...this.state.users,...response.data.results],
  loading : false
})
```
# destructuring inline styling and keys
- const {loading,users} = this.state
### inline style
style={{color:"red"}}
- in react we need to make sure every element has unique id ? why ?
> why do we need key ? & why it should be unique ??
key = {user.id.value}


- we don't want to mutate the state we just want to create a new obj ???
- so the old data is not overwritten okay ??? 
- wrong !!!






