


# More React 


Not a lot of time today. But I covered more information about React today regarding
Lifecycle and State. 

## State

State can be done via classes and functions. 

Classes implement state via:
<ol>
<li> A call to Constructor that takes props as the argument </li>
<li> Super(props);  followed by this.state = {object containing the state(s)}</li>
<li> A function call anywhere of this.setState() that updates the state. </li>
</ol>

Functions are a lot simpler: let [nameOfState, setnameOfState] = UseState(initial value);
nameOfState contains the state value. setnameOfState is used to update it.


## LifeCycle

React lifecycle can be divided in a 2*3 array. 

|   | Mounting | Update | Unmounting | 
|---|-----------|-------|------------|
|Render| constructor</br>render | new props<br/>setState()<br/> forceUpdate() | nothing here |
| Commit | Update DOM <br/>componentDidMount() | Update DOM <br/>componentDidUpdate() | componentWillUnmount() |
