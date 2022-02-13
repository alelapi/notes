# Immutability in JS

In Javascript only Object and Array are mutable, primitives values are not immutable; you can make a variable name point to a new value, but the previous value is still held in memory. Hence the need for garbage collection.

## const
Block scope variable which value can not be reassigned or redeclared.
If applied to an object, prototype and properties can still be modified.

## Object.freeze()
When applied to an object, it returns the same object with prototype and properties frozen. You can not add or delete any properties and can not modify value properties; object properties can still be modified, unless they are also frozen.

## Object.seal()
When applied to an object, it seals the object blocking every modify to its prototype. No properties can be added or deleted but existing ones can still be modified.