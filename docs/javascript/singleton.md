# Singleton

Classes that can be instantiated once, and can be accessed globally.

```
let instance;
let counter = 0;

class Counter {
    constructor() {
        if (instance) {
            throw new Error("You can only create one instance!")
        }
        instance = this;
    }

    getInstance() {
        return this;
    }

    getCount() {
        return counter;
    }

    increment() {
        return ++counter;
    }

    decrement() {
        return --counter;
    }
}

const singletonCounter = Object.freeze(new Counter());
export default singletonCounter;
```

However, in Javascript, they can be created using a simple objects.
```
let count = 0;

const counter = {
    increment() {
        return ++counter;
    }
    decrement() {
        return --counter;
    }
};
Object.freeze(counter);
export { counter };
```

## Pros
Can potentially save a lot of memory space.

## Cons
They are considered an anti-pattern:
- Testing: all tests rely on the modification to the global instance of the previous test, the order of the tests matter. After testing we need to reset the entire instance.
- Dependency Hiding: it's not obvious that module is a Singleton during importing of it. Can be imported from many times and updated in multiple places.
- Global behaviour: it's actually a global variables, which can lead to a lot unexpected behavior.
