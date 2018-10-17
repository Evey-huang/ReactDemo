This is a collection of simple demos of React.js.

These demos are purposely written in a simple and clear style. You will find no difficulty in following them to learn the powerful library.

## How to use

First copy the repo into your disk.

```bash
$ git clone https://github.com/Evey-huang/ReactDemo.git
```

Then play with the source files under the repo's demo* directories.

## HTML Template

```html
<!DOCTYPE html>
<html>
  <head>
    <script src="../build/react.js"></script>
    <script src="../build/react-dom.js"></script>
    <script src="../build/browser.min.js"></script>
  </head>
  <body>
    <div id="example"></div>
    <script type="text/babel">

      // ** Our code goes here! **

    </script>
  </body>
</html>
```

## Index

1. [Render JSX](https://github.com/Evey-huang/ReactDemo/blob/master/demo/helloworld.html)
1. [Use JavaScript in JSX](https://github.com/Evey-huang/ReactDemo/blob/master/demo/hello.html)

---

## Demo01: Render JSX

[source](https://github.com/Evey-huang/ReactDemo/blob/master/demo/helloworld.html)

The template syntax in React is called [JSX](http://facebook.github.io/react/docs/displaying-data.html#jsx-syntax). It is allowed in JSX to put HTML tags directly into JavaScript codes. `ReactDOM.render()` is the method which translates JSX into HTML, and renders it into the specified DOM node.

```js
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('example')
);
```

Attention, you have to use `<script type="text/babel">` to indicate JSX codes, and include `browser.min.js`, which is a [browser version](https://babeljs.io/docs/usage/browser/) of Babel and could be get inside a [babel-core@5](https://www.npmjs.com/package/babel-core) npm release, to actually perform the transformation in the browser.

Before v0.14, React use `JSTransform.js` to translate `<script type="text/jsx">`. It has been deprecated ([more info](https://facebook.github.io/react/blog/2015/06/12/deprecating-jstransform-and-react-tools.html)).

## Demo02: Use JavaScript in JSX

[demo](http://ruanyf.github.io/react-demos/demo02/) / [source](https://github.com/ruanyf/react-demos/blob/master/demo02/index.html)

You could also use JavaScript in JSX. It takes angle brackets (&lt;) as the beginning of HTML syntax, and curly brackets (`{`) as the beginning of JavaScript syntax.

```js
function formatName(user) {
    return user.firstName + '' + user.lastName;
}
function getGreeting(user) {
    if(user) {
        return <h1>Hello, {formatName(user)}!</h1>;
    }
    return <h1>Hello, Stanger.</h1>
}
const user = {
   firstName: 'Harper',
   lastName: ' Perez'
};
const element = (
   getGreeting(user)
);

ReactDOM.render(
   element,
   document.getElementById('example')
);
```



## Useful links

- [React's official site](http://facebook.github.io/react)
