# Mixin pattern
A mixin is an object that we can use in order to add reusable functionality to another object or class, without using inheritance. We can't use mixins on their own: their sole purpose is to add functionality to objects or classes without inheritance.

If we have a class:
```
class Dog {
    constructor(name) {
        this.name = name
    }
}
```

we create a set of functionality that we want to add to the class:

```
const animalFunctionality = {
    walk: () => {...}
    sleep: () => {...}
}
```
Then we add to the prototype:
```
Object.assign(Dog.prototype, animalFunctionality)
```

Although we can add functionality with mixins without inheritance, mixins themselves can use inheritance.

```
const dogFunctionality = {
    bark: () => {...}
    wagTail: () => {...}
    play: () => {...}
    walk() {
        super.walk();
    },
    sleep() {
        super.sleep();
    }
}

Object.assign(dogFunctionality, animalFunctionality)
```
or 
```
const dogFunctionality = {
    __proto__: animalFunctionality,
    ...
```
Example:
`window` object has applied two mixins that extend functionalities `WindowOrWorkerGlobalScope` and `WindowEventHandlers`.

