### Props


---

#### Props

- An object passed through the parent, received as an argument
- Added as *attributes* on the component


```
ReactDOM.render(
    <Button title="Submit" />
    document.getElementById('root')
);
```

---

#### Props

- Our component definition now looks like this
- Attribute name specified corresponds to property on props object

```
const Button = (props) => {
    return (
        <button type="submit">{props.title}</button>
    )
}
```
[Example](https://codepen.io/berkmolla/pen/LjEzVb)

---

- Class-based components use the *`this`* keyword to access props
```
class Button extends React.Component {
    render() {
        <button type="submit">{this.props.title}</button>
    }
}
```

[Example](https://codepen.io/berkmolla/pen/zdxEpB)
