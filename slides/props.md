### Props

------

#### Props

- An object passed through the parent, received as an argument
- Added as *attributes* on the component
- Props are **read-only**


```js
ReactDOM.render(
    <Button title="Submit" />
    document.getElementById('root')
);
```

---

#### Props

- Our component definition now looks like this
- Attribute name specified corresponds to property on props object

```js
const Button = (props) => {
    return (
        <button type="submit">{props.title}</button>
    )
}
```
[Example](https://goo.gl/pvjQoH)

---

#### Props

Class-based components use the `this` keyword to access props

```js
class Button extends React.Component {
    render() {
        <button type="submit">{this.props.title}</button>
    }
}
```

[Example](https://goo.gl/bnjR3E)

------

### Exercise

Write a component that says hello to you and tells you the current date

https://goo.gl/5Sc6xp

---

[Solution](https://goo.gl/vr1EWP)

------

#### `props.children`

There is a special prop called `children` which can be used to pass in content.

```js
const Menu = props => (
    <ul>
        {props.children}
    </ul>
);

const App = () => (
    <Menu>
        <li>Welcome!</li>
        <li>Hi!</li>
    </Menu>
);
```

[Example](https://goo.gl/wppjLN)

note: Children in React don’t have to be components, they can be anything

---

JSX automatically removes whitespace at the start and end of a line as well as blank lines. It also converts blank lines in the middle of string literals into one space.

---

All of these examples will render the same thing

```js
<Container>Hello world!</Container>

<Container>
  Hello world!
</Container>

<Container>
  Hello
  world!
</Container>

<Container>

  Hello world!
</Container>
```

---

Children can be of multiple different types

```js
<Container>
  Here is a divider:
  <Divider />
  Here is another divider:
  <Divider />
</Container>
```
