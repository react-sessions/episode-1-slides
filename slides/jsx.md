### JSX

**J**ava**S**cript **X**ML

------

### What is JSX?

JSX is an inline markup that looks like HTML and gets transformed to JavaScript

You write JSX in the same file as you write JavaScript code

---

A JSX expression starts with an HTML-like open tag, and ends with the corresponding closing tag

```js
const element = <h1>Hello, world!</h1>;
const component = <ProfileTitle>Hello, world!</ProfileTitle>;
```

---

JSX tags support the XML self close syntax so you can optionally leave the closing tag off

```js
const element = <img src="" />;
const component = <ProfileImage src="" />;
```

------

### Specifying Attributes

---

Use quotes when adding attributes

```js
const element = <div id="my-id"></div>;
```

---

JSX uses a camelCase convention for attributes with more than a single word e.g. `tabindex` becomes `tabIndex`.

```js
const element = <div tabIndex="0"></div>;
```

---

Use curly braces to embed an expression in an attribute

```js
const element = <img src={user.avatarUrl}></img>;
```

Do not wrap expressions in quotes otherwise they will be treated as strings

---

To apply the `class` and `for` attributes in JSX you have to use `className` and `htmlFor` respectively.

This is because `class` and `for` are reserved keywords in JavaScript

------

### Embedding Expressions

---

You can embed any JavaScript expression in JSX by wrapping it in curly braces

```js
const formatHeading = () => "Hello, World";

const app = (
    <h1>
        {formatHeading()}!
    </h1>
);
```

note: https://goo.gl/wfNfxc - Use the "View compiled JS" option to show how the code is transformed

---

JSX expressions evaluate to ReactElements. Think of them as shorthand for calling React.createElement()

The last example compiles to this

```js
var formatHeading = function formatHeading() {
    return "Hello, World";
};

var app = React.createElement(
    "h1",
    null,
    formatHeading(),
    "!"
);
```

---

#### Ignored expressions

`false`, `null`, `undefined`, `and` true are valid children. They simply don't render. These JSX expressions will all render to the same thing

```js
<div />

<div></div>

<div>{false}</div>

<div>{null}</div>

<div>{undefined}</div>

<div>{true}</div>
```

------

### JSX is an Expression Too

---

After compilation, JSX expressions become regular JavaScript objects

This means that you can use JSX inside of `if` statements and `for` loops, assign it to variables, accept it as arguments, and return it from functions

---

```js
const formatGreeting = username => {
    // JSX assigned to variables
    const DefaultGreeting = <h1>Hello, World!</h1>;

    return username
        // JSX returned from function
        ? <h1>Hello, {username}!</h1>
        : DefaultGreeting;
};

// JSX passed as argument
const app = formatGreeting(<em>Desmond</em>);
```

note: https://goo.gl/VJuKuP

------

### Child Elements

---

JSX can contain child elements

When adding multiple children to a JSX element you must wrap those elements with a single parent element as React components can only return a single element

---

Here, the JSX code is spread over multiple lines for readability and wrapped in parenthesis to avoid automatic semicolon insertion

```js
const app = (
    <main>
        <h1>React Sessions</h1>
        <h2>is cool!</h2>
    </main>
);
```

note: https://goo.gl/TsLFgh

------

### Exercise

Identify and fix the issues in this code example

https://goo.gl/ERWcfj
