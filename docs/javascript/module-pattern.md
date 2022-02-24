# Module Design Pattern

It is a Design Pattern used to wrap a set of variables and functions together in a single scope, defining objects and specify the variables and the functions that can be accessed from outside the scope of the function and others that can be private.

```
var makeCounter = function() {
  var privateCounter = 0;
  function changeBy(val) {
    privateCounter += val;
  }
  return {
    increment: function() {
      changeBy(1);
    },

    decrement: function() {
      changeBy(-1);
    },

    value: function() {
      return privateCounter;
    }
  }
};

var counter1 = makeCounter();
var counter2 = makeCounter();

```

In the example, `counter1` and `counter2` share the same definition but they have distinct lexical scope.

ES2015 introduced built-in JavaScript modules. A module is a file containing JavaScript code, with some difference in behavior compared to a normal script.
If you want use code in another file you have to `export` it and then `import` in the file you want to use it.

## Dynamic import
When importing all modules on the top of a file, all modules get loaded before the rest of the file. In some cases, we only need to import a module based on a certain condition:

```
import("module_name").then(module => {
  //do stuff
})

(async () => {
  const module = await import("module_name");
  //do stuff
})

```

## Benefits:
- Maintainability: Module Patterns enable better maintainability since all the related code can be encapsulated inside a single logical block. These logically independent blocks are relatively easier to update.
- Reusability: We single unit of code can be reused across the entire application. Functionality enclosed as a module can be reused and we do not need to define the same functions at multiple points.