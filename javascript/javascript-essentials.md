# Javascript Essentials

## What is the difference between var, let and const?

### var
Scope: Function-scoped. If declared inside a function, it is accessible within that function. If declared outside, it is globally scoped.
Hoisting: Variables declared with var are hoisted to the top of their scope and initialized with undefined.
Re-declaration: Can be re-declared within the same scope without errors.

### let
Scope: Block-scoped. It is only accessible within the block (e.g., {}) where it is declared.
Hoisting: Variables declared with let are hoisted but not initialized. Accessing them before declaration results in a ReferenceError.
Re-declaration: Cannot be re-declared within the same scope.

### const
Scope: Block-scoped, similar to let.
Hoisting: Variables declared with const are hoisted but not initialized. Accessing them before declaration results in a ReferenceError.
Re-declaration: Cannot be re-declared within the same scope.
Assignment: Must be initialized at the time of declaration and cannot be reassigned. However, if the variable is an object or array, the contents can be modified.

### Example
```js
function example() {
    var x = 1;
    if (true) {
        var x = 2; // Same variable, re-declared
        console.log(x); // 2
    }
    console.log(x); // 2

    let y = 1;
    if (true) {
        let y = 2; // Different variable, block-scoped
        console.log(y); // 2
    }
    console.log(y); // 1

    const z = 1;
    if (true) {
        const z = 2; // Different variable, block-scoped
        console.log(z); // 2
    }
    console.log(z); // 1
}
```

## Can you explain `Closures` to me?
[Mozilla Developer](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)

  A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function’s scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.

## What is currying?

[Currying Partials](https://javascript.info/currying-partials)

Currying is a transform that makes f(a,b,c) callable as f(a)(b)(c). JavaScript implementations usually both keep the function callable normally and return the partial if the arguments count is not enough.

Currying allows us to easily get partials. As seen in a logging example, after currying the three argument universal `function log(date, importance, message)` gives us partials when called with one argument (like `log(date)`) or two arguments (`like log(date, importance)`).

```javascript
function curry(func) {

  return function curried(...args) {
    if (args.length >= func.length) {
      return func.apply(this, args);
    } else {
      return function(...args2) {
        return curried.apply(this, args.concat(args2));
      }
    }
  };
}

// USAGE

function sum(a, b, c) {
  return a + b + c;
}

let curriedSum = curry(sum);

alert( curriedSum(1, 2, 3) ); // 6, still callable normally
alert( curriedSum(1)(2,3) ); // 6, currying of 1st arg
alert( curriedSum(1)(2)(3) ); // 6, full currying
```

<br><br>

# Memoization

## Given a recursive function call, what could you use in Javascript to optimize this?
MEMOIZATION

## When would you use memoize function?
When computing is very expensive.
Saving time and computing power.
Re-use of already calculated results.

<br><br>

# Compositional

## Can you ecplain me the difference between `compose()` vs `pipe()`?
  [Medium: Pipe and Compose](https://medium.com/free-code-camp/pipe-and-compose-in-javascript-5b04004ac937)
    
`PIPE:`
Multiple functions executed one after another, where the next one is taking the return value of the previous one.

```javascript
pipe = (...fns) => x => fns.reduce((v, f) => f(v), x)
```
Usage: 
```javascript
pipe(
  getName,
  uppercase,
  get6Characters,
  reverse 
)({ name: 'Buckethead' })
// 'TEKCUB'
```

`COMPOSE:` is the same like `pipe`, but the other way around. It starts from the other side.

```javascript
compose = (...fns) => x => fns.reduceRight((v, f) => f(v), x);
```

```javascript
compose(
  reverse,
  get6Characters,
  uppercase,
  getName,
)({ name: 'Buckethead' })
```

<br><br>

# Observables

## What is the difference between flatMap, concatMat and switchMap?

- `flatMap/mergeMap` - creates an Observable immediately for any source item, all previous Observables are kept alive
- `concatMap` - waits for the previous Observable to complete before creating the next one
- `switchMap` - for any source item, completes the previous Observable and immediately creates the next one
- `exhaustMap` - source items are ignored while the previous Observable is not completed

![observables][observables]

[observables]: ./assets/javascript-essentials-observables.png "Observables"
