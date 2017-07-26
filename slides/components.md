### Components

---

#### A component

At the most basic level, a component is simply a Javascript function

```js
function HelloWorld() {
    return <h1>Hello, world!</h1>
}
```

---

#### Using ES6 arrow functions

```js
const HelloWorld = () => (
    <h1>Hello, world!</h1>
);
```

<small>(stateless functional components)</small>

---

#### Class-based components

```js
class HelloWorld extends React.Component {
    render() {
        return (
            <h1>Hello, world!</h1>
        )
    }
}
```

------

### Nesting components

```js
const App = () => (
    // When putting multiple tags in a return statement,
    // they must be wrapped with a div
    <div>
        <AppHeader />
        <AppBody />
        <AppFooter />
    </div>
);

const AppHeader = () => (
    <h1>My amazing app</h1>
);

const AppBody = () => (
    <p>Some stuff in the body</p>
);

const AppFooter = () => (
    <a href="#">Some more amazing stuff that Ive linked to</a>
);
```

[CodePen](https://codepen.io/berkmolla/pen/wqByGx)
