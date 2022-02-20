# Proxy pattern

Proxy is an object that represents the handler for an object. In the handler object, we can define specific behavior based on the type of interaction. 

```
const proxy1 = new Proxy(target, handler);
```

There are many methods that you can add to the Proxy handler:

- apply(): A trap for a function call.
- construct(): A trap for the new operator.
- defineProperty(): A trap for Object.defineProperty. 
- deleteProperty(): A trap for the delete operator.
- get(): A trap for getting property values.
- getOwnPropertyDescriptor(): A trap for Object.getOwnPropertyDescriptor.
- getPrototypeOf(): A trap for Object.getPrototypeOf.
- has(): A trap for the in operator.
- isExtensible(): A trap for Object.isExtensible.
- ownKeys(): A trap for Object.getOwnPropertyNames and Object.getOwnPropertySymbols.
- preventExtensions(): A trap for Object.preventExtensions.
- set(): A trap for setting property values.
- setPrototypeOf(): A trap for Object.setPrototypeOf.

