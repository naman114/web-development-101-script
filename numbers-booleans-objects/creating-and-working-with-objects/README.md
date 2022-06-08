# Script

In this lesson, we will learn about JavaScript Objects. 
In JavaScript, an object is a very powerful concept, and you are going to work with them all the time. So, let's get started.

### Overview 
A JavaScript object is a collection of named values. Like many other programming languages, it can be compared to objects in real life. Compare it with a *cup*, for example. A *cup* is an object that has various properties. A cup has a color, a design, weight, the material it is made of etc. In the same way, JavaScript objects can have properties, which define their characteristics.

### Objects & Properties
The properties of an object define the characteristics of the object. Object properties are basically the same as ordinary JavaScript variables, except their attachment to the objects. You access the properties of an object with a simple dot-notation:

```js
objectName.propertyName
```

Like all JavaScript variables, both the object name and property name are case-sensitive. You can define a property by assigning it a value. 

For example, let's create an object named `myComputer` and give it properties like `name`, `processor`, `ram` and `price` etc.

#### Creating Objects
Now, there are two different ways to create a JavaScript object.

> Action: Open browser console or VS Code to create this code and also explain on the go

1. **Using object initializer**
```js
const myComputer = {
  property_1: 'value_1',
  name: 'Macbook Air',
  processor: 'Intel i5',
  ram: '8GB',
  price: 65000
}
```
Here **myComputer** is the name of the new object, with properties like: `name`, `processor`, `ram` etc.

One important point to note here, assigning an **object** to a variable (Ex. here it's assigned to **myComputer**) is totally optional. You can define this object without giving it a name.

A property of an object can contain another object too, for example:
```js
const myComputer = {
  name: 'Macbook Air',
  processor: 'Intel i5',
  ram: '8GB',
  price: 65000,
  storage: {
    type: "SSD",
    size: "512 GB",
    brand: "WD"
  }
}
```

2. **Using a constructor function**

Alternatively, you can create an object with these two steps:

  - Define the **object type** by writing a **constructor** function.
  - Create an instance of the object with new.

To define an **object type**, create a function that specifies its name, properties, and methods. 

For example, suppose you want to create an **object type** for *cars* with properties like: make, model, and year. To do this, you would write the following function:

```js
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}
```
Here, `this` is used to assign values to the object's properties. Now you can create an object called myCar as follows:
```js
  const myCar = new Car('Honda', 'Civic', 2018);

  // Try it out
  console.log(myCar)

  // You can create any number of **Car** objects by calls to `new`. For example,
  const magnite = new Car('Nissan', 'Magnite', 2021);
  const seltos = new Car('Kia', 'Seltos', 2020);
```

### To conclude
That's it for this lesson, see you in the next one.