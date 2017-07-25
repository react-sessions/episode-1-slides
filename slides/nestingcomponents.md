#### Nesting components

```js
const App = () => {
  return (
    // When putting multiple tags in a return statement,
    // they must be wrapped with a div
    <div>
      <AppHeader />
      <AppBody />
      <AppFooter />
    </div>
  )
}

const AppHeader = () => {
    return (
        <h1>My amazing app</h1>
    )
}

const AppBody = () => {
  return (
    <p>Some stuff in the body</p>
  )
}

const AppFooter = () => {
    return (
        <a href="#">Some more amazing stuff that Ive linked to</a>
    )
}
```

[CodePen](https://codepen.io/berkmolla/pen/wqByGx)
