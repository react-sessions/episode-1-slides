### JSX

**J**ava**S**cript **X**ML

---

### What is JSX?

JSX is an inline markup that looks like HTML and gets transformed to JavaScript

You write JSX in the same file as you write JavaScript code, then Babel transforms these expressions into actual JavaScript code

---

A JSX expression starts with an HTML-like open tag, and ends with the corresponding closing tag

```js
const element = <h1>Hello, world!</h1>;
const component = <ProfileTitle>Hello, world!</ProfileTitle>;
```

JSX tags support the XML self close syntax so you can optionally leave the closing tag off

```js
const element = <img src="" />;
const component = <ProfileImage src="" />;
```

---

### Specifying Attributes

Use quotes when adding attributes

```js
const element = <div tabIndex="0"></div>;
```

JSX uses a camelCase convention for attributes with more than a single word e.g. tabindex becomes tabIndex.

```js
const element = <div tabIndex="0"></div>;
```

---

### Specifying Attributes

Use curly braces to embed an expression in an attribute

```js
const element = <img src={user.avatarUrl}></img>;v
```

Be careful not to wrap expressions in quotes as JSX will treat the attribute as a string

---

### Specifying Attributes

To apply the `class` and `for` attributes in JSX you must use `className` and `htmlFor` respectively, this is because `class` and `for` are reserved keywords in JavaScript

---

### Embedding Expressions

You can embed any JavaScript expression in JSX by wrapping it in curly braces

JSX expressions evaluate to ReactElements. Think of them as shorthand for calling React.createElement().

note: https://goo.gl/wfNfxc - Use the "View compiled JS" option to show how the code is transformed

---

### JSX is an Expression Too

After compilation, JSX expressions become regular JavaScript objects

This means that you can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions

note: https://goo.gl/VJuKuP

---

### Children

JSX can contain child elements

When adding multiple children to a JSX element you must wrap those elements with a single parent element as React component can only return a single element

note: https://goo.gl/TsLFgh

---

### Exercise

Identify and fix the issues in this code example

https://goo.gl/ERWcfj
