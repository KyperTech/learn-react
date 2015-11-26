# Primer

Before we get into building anything, lets discuss why we will be using the tools that we will be using.

## React

React provides a simple and organized way to build "Reactive" HTML, which basically means HTML that can change based on something going on within an application. This is useful to keep from having to make tons of similar HTML files, as well as for general code organization.

## ES6

ES6 is a new version of Javascript that is actually so new that not all browsers support it yet. The good thing is that there are tools like [Babel]() that allows you to convert ES6/ES7 code to ES5 so that it will run in every browser.

Among other things, ES6 has the capability to create Classes. A class is a way to organize creating objects of a the same type. Below we will create a Car class:

Car Class:

```javascript
class Car {
  //Runs when calling new
  constructor(carData) {
    //Set Car's attributes from passed data
    this.color = carData.color;
    this.make = carData.make;
  }
  //Method to get color and make together
  get colorAndMake() {
    return this.color + ' ' + this.make;
  }
}
```

Creating new Car:

```javascript
let myCar = new Car({color: 'Black', make: 'Tesla'});
let myFriendsCar = new Car({color: 'White', make: 'Audi'});

console.log('My car is a ' + myCar.colorAndMake);
//Output: My car is a Black Tesla

console.log('My friends car is a ' + myFriendsCar.colorAndMake);
//Output: My friends car is a White Audi

```

This example is some what simple, but it shows how using a class can organize functionality in an Object Oriented manor.

## React and ES6 combined
Classes become particularly useful when combined with React because you actually create a Class for a set of HTML. That means you can change what is displayed based on data that changes within an application while still keeping to the object oriented organization.

Here is an example of a simple ES6 class that uses React to become an HTML element.

```javascript
//Basic React class that becomes an HTML element by extending React.Component
class HelloWorld extends React.Component {
  render() {
    return (<div>Hello, world</div>);
  }
}
```

The simple-example uses this same code to create an HTML element that is then rendered.

## NodeJS and NPM
[NodeJS](nodejs.org) is server side or "backend" javascript. NodeJS comes with a package managing tool called NPM that is a useful library/dependency management tool even for websites or "frontend".

NPM organizes dependencies into a `package.json` file and allows you to add libraries, such as [Lodash]() to your project by running `npm install --save lodash`.

#### References
