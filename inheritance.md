## What is inheritance?

In OOP, inheritance is the concept that allows us to define a class like Person, Car, Animal, etc. Then take all the properties and all that functionality then use it in child classes. The goal with inheritance is to make the parent(s) classes as broad as they can be and then extend the functionality of the parent class by adding specific properties or methods within the child class. <p>Take an Animal class for example. As a parent, it might have name, type, and a few other really generic properties that all animals have in common. Then we can create a child class called Mammal that will extend the Animal class while maybe adding a few properties and methods of its own. We take this idea one step further and create two child classes from Mammal, Cats and Dogs. Each child class gets all the functionality of the Parent that it <em>inherits</em> from. The previously defined class or “the Parent” will pass down everything to “the Child”. Let’s look at an example.

Imagine we define a class Person like this. We give this class some properties (name, email, age) and some functionality (greeting or farewell).

```javascript
class Person { 
    constructor(name, age) {
        this.name = name; 
        this.age = age; 
        greeting() { console.log(`Hi! I'm ${this.name.first}`); };
        goodbye() { console.log(`${this.name.first} said goodbye.`); 
    }; 
}
``` 

Now we want to build a child class "Dad" that inherits from our parent class Person. Let’s make a Dad class.

```javascript
class Dad extends Person { 
    // inherits all the functionality of Person
    // like name, gender and the functions greeting and goodbye
    constructor(name, age, interests) {
        // interests is specific to Dad
        this.interests = interests
    };
    // we can also add functionality
    dadjoke() { console.log('Insert corny dad joke here')}
}
```

Then we can simply use our classes whenever we need to throughout our code base.
```javascript
let julie = new Person('Julie Smith', 25);
julie.greeting()
```
or
```javascript
let dad1 = new Dad('Rick Smith', 52, ['sports', 'beer', 'fishing']);
console.log(dad1.interests) // should return our array of interests ['sports', 'beer', 'fishing']
dad1.dadjoke()
```

### Assessment 
Write a parent and a child class on your own  with 2-3 properties and methods in each and then use NodeJs to console.log a property and a method from both the parent and the child class.

### Additional Resources
[Brad Traversy - YouTube on OOP in Javascript](https://www.youtube.com/watch?v=vDJpGenyHaA)
[You Don't Know JS - Chapter on Objects](https://github.com/getify/You-Dont-Know-JS/blob/1st-ed/this%20%26%20object%20prototypes/ch4.md)