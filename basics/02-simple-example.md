
# ES6 basic example

[react-es6-basic example code](http://github.com/prescottprue/react-es6-basic)

To get started, lets make the most simple React-ES6 app possible. This will look similar to the example from the end of the Primer, but we will be actually rendering the element created through the HelloWorld class.

In order to use ES6 we will need to convert our code to ES5 using Babel. This can be done before running your application or while it is running. For now we are going to go with the simple example and just convert it when the application starts running.

Create an `index.html` with the following code:

```html
<!doctype html>
<html lang='en'>
<head>
  <meta charset='utf-8'>
  <title>React-ES6-Basic</title>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-core/5.8.25/browser.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/react/0.14.0/react-with-addons.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/react/0.14.0/react-dom.js"></script>
  <script type="text/babel">
    class HelloWorld extends React.Component {
      render() {
        return (<div>Hello, world</div>);
      }
    }
    let rootElement = document.getElementById('content');
    ReactDOM.render(<HelloWorld />, rootElement);
  </script>
</head>
  <body>
    <div id="content"></div>
  </body>
</html>
```

When you run your index.html file in a browser you should see Hello, world displayed in the view. This is the most simple form of using React with ES6 to create HTML.

Though this is a useful example, we will need to create more Components in order to make a whole application. With all of the code that comes with that, it is best to organize Components into different files and convert to ES5 before run time. Webpack will help us build all of our classes together while converting them.

Continue to the second primer to learn about how to use Webpack to build a basic application.
