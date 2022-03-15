# Symbol
Symbol is a built-in object whose constructor returns a `symbol` primitive that's guaranteed to be unique. 
Symbols are often used to add unique property keys to an object that won't collide with keys any other code might add to the object, and which are hidden from any mechanisms other code will typically use to access the object. That enables a form of weak encapsulation, or a weak form of information hiding.

Every Symbol() call is guaranteed to return a unique Symbol.
Every Symbol.for("key") call will always return the same Symbol for a given value of "key". When Symbol.for("key") is called, if a Symbol with the given key can be found in the global Symbol registry, that Symbol is returned. Otherwise, a new Symbol is created, added to the global Symbol registry under the given key, and returned.

## Create
```
const sym1 = Symbol()
const sym2 = Symbol('foo') //optional string, description of the symbol
```

This will create unique symbols and not global. If you want create Symbols available across files or realm you can use:
- `Symbol.for(key)` : search an existing symbol with given key or create new one.
- `Symbol.keyFor(symbol)` : search an existing symbol and return the key.

`Object.getOwnPropertySymbols()` will return an array of symbols of the given object.

