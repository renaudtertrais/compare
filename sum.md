# Sum

The function `sum` should take an` array` of `numbers` and return their sum.
Even if there should be some native functions to do it in some languages, 
it is interssting to compare the difference when implenting it.

```js
sum([1, 2, 3]); // -> 6
```

## Javascript

**using reduce**
```js
const add = (x, y) => x + y;
const sum = xs => xs.reduce(add);
```

**recursive**
```js
const sum = xs => xs.length > 0 ? xs[0] + sumRec(xs.slice(1)) : 0;
```

[demo](https://repl.it/HCV3/0)
