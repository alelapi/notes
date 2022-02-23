# Observer pattern

With the observer pattern, we can subscribe certain objects, the observers, to another object, called the observable. Whenever an event occurs, the observable notifies all its observers.
An observable object usually contains 3 important parts:
- subscribe(): a method in order to add observers to the observers list
- unsubscribe(): a method in order to remove observers from the
observers list
- notify(): a method to notify all observers whenever a specific event occurs

For example:
```
class Observable {
    constructor() {
        this.observers = [];
    }

    subscribe(func) {
        this.observers.push(func)
    }

    unsubscribe(func) {
        this.observers = this.observers.filter(observer => observer !== func)
    }

    notify(data) {
        this.observer.forEach(observer => observer(data))
    }
}
```

## Pro
It is a great way to enforce separation of concerns and the single-responsiblity principle.

## Cons
Can cause performance issues when notifying all subscribers, if subscribers are too complex.

