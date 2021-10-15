{::options parse_block_html="true" /}



# React Introduction


*Covered introduction to React some more. Elements & Components & some state*
 Today I learned that this is what an element in react could look like:

```javascript
const Element = <h1>This is JSX {this.isJS}</h1>
``` 
Elements in react are what is used to generate the virtual document object 
model. React uses these elements and the vdom they create to update the real 
DOM structure as is needed. This is done via a diffing algorithm that figures 
out the best way to do so. 
 Components are either functions or classes that are used to create React 
Elements. Here is an example of each: 

```javascript
//function component
function Hello(props) {
    return (<h1>Hello, {props.name}</h1>);
}

//class component
class Hello extends React.Component {
    render() {
        return <h1>Hello, {this.props.name}</h>
    }
}

//implementation of component
ReactDOM.render(
    <app>
        <Hello name='Lennart'/>
    </app>
    , 
    document.selectElementByID('root')
    )
```
Using this allows us to separate concerns. Button elements can become their own
Javascript functions tying how they need to look in the moment to the function that
renders them.

Another thing I learned was the implementation of useState.

```Javascript
    function Counter() {
        const [count, setCount] = useState(0);
        return (
            <div>
                <h1>The counter is reading {count}</h1>
                <button onClick={ () => setCount(++count)}/>
            </div>
        )
    }

```
