# Object-Oriented Programming in JavaScript

JavaScript is a versatile programming language that can be used to implement object-oriented programming (OOP) concepts. OOP is a programming paradigm that focuses on organizing code into objects that have properties and methods. Here's a breakdown of how OOP works in JavaScript:

## Object Creation

Objects in JavaScript can be created in several ways:

### Object Literals

The simplest way to create an object is using an object literal, which is a comma-separated list of name-value pairs enclosed in curly braces:

`const myObject = {   
	`property1: value1,   
	`property2: value2,   
	`method1: function() {     
		``// code for method1   
	``} 
``};`

### Constructor Functions

Another way to create objects in JavaScript is to use constructor functions, which are special functions that are used to create and initialize objects. To define a constructor function, you use the `function` keyword, followed by the name of the function and the arguments that the function should accept. Within the constructor function, you use the `this` keyword to refer to the current object.

`function Person(name, age) {   
	`this.name = name;   
	`this.age = age;   
	`this.greet = function() {     
		`console.log("Hello, my name is " + this.name + " and I am " + this.age + " years old.");   
		``}; 
	``}  
`const person1 = new Person("John", 30); 
`person1.greet(); // Output: "Hello, my name is John and I am 30 years old."`

### ES6 Classes

ES6 introduced a new syntax for defining classes, which is similar to the syntax used in other object-oriented programming languages. You use the `class` keyword to define a class, and the `constructor` method to initialize the object. Within the class, you define methods using regular functions.

`class Person {   
	`constructor(name, age) {     
		`this.name = name;     
		`this.age = age;   
	``}    
		
		`greet() {     
			`console.log("Hello, my name is " + this.name + " and I am " + this.age + " years old.");   
		} 
	}  
	
`const person1 = new Person("John", 30); 
`person1.greet(); // Output: "Hello, my name is John and I am 30 years old."`

## Inheritance

Inheritance is the process of creating new objects that are similar to existing objects, but with some modifications or additions. In JavaScript, you can achieve inheritance using either prototypes or classes.

### Prototypal Inheritance

Prototypal inheritance works by creating an object and setting its prototype to another object. When you call a method or property on the object, JavaScript checks the object itself for the method or property. If it can't find it, it checks the object's prototype, and continues up the prototype chain until it either finds the method or property or reaches the top of the chain.

```
const animal = {   
	type: "unknown",   
	sound: function() {     
		console.log("Unknown sound.");   
	} 
};  

const dog = Object.create(animal); 
dog.type = "dog"; 
dog.sound = function() {   
	console.log("Woof!"); 
};  

dog.sound(); // Output: "Woof!"`
```

### Class Inheritance

ES6 classes also support inheritance through the use of the `extends` keyword. When you define a class that extends another class, the new class inherits all the properties and methods of the parent class.

```
`class Animal {  
	`constructor(type) {     
		`this.type = type;   
	``}    
	
	sound() {     
		console.log("Unknown sound.");   
	} 
``}  

`class Dog extends Animal {   
	`constructor() {     
		`super("dog");
	``}
	
	sound() { console.log("Woof!"); 
	} 
``}

`const dog = new Dog(); dog.sound(); // Output: "Woof!"
```
## Encapsulation
Encapsulation is the process of hiding the internal details of an object and only exposing a public interface. In JavaScript, you can achieve encapsulation using closures.

```
function Person(name, age) {
  let privateName = name;
  let privateAge = age;

  this.getName = function() {
    return privateName;
  };

  this.getAge = function() {
    return privateAge;
  };

  this.greet = function() {
    console.log("Hello, my name is " + privateName + " and I am " + privateAge + " years old.");
  };
}

const person1 = new Person("John", 30);
console.log(person1.getName()); // Output: "John"
console.log(person1.getAge()); // Output: 30
person1.greet(); // Output: "Hello, my name is John and I am 30 years old."

```

In the above example, the privateName and privateAge variables are only accessible within the Person constructor function. The getName, getAge, and greet methods are public methods that can be accessed outside the constructor function.

## Polymorphism
Polymorphism is the ability of an object to take on many forms. In JavaScript, you can achieve polymorphism through method overriding. Method overriding is the process of defining a method in a subclass that has the same name and parameters as a method in the parent class.

```
class Animal {
  constructor(type) {
    this.type = type;
  }

  sound() {
    console.log("Unknown sound.");
  }
}

class Dog extends Animal {
  constructor() {
    super("dog");
  }

  sound() {
    console.log("Woof!");
  }
}

class Cat extends Animal {
  constructor() {
    super("cat");
  }

  sound() {
    console.log("Meow!");
  }
}

const dog = new Dog();
const cat = new Cat();
const animals = [dog, cat];

animals.forEach(animal => {
  animal.sound();
});
```

In the above example, the Dog and Cat classes both override the sound method of the Animal class. When you call the sound method on the dog and cat objects, they output "Woof!" and "Meow!" respectively.