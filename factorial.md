# Factorial
Implement the factorial function.

```js
factorial(4); // 24 = 1 * 2 * 3 * 4
```
## Javascript

Using a range:
```js
const factorial = n => Array
  .from({ length: n <= 1 ? 1 : n })
  .map((_, i) => i + 1)
  .reduce(Math.imul);
```

Recusive:
```js
const factorialR = n => n <= 1 ? 1 : n * factorial(n - 1);
```

[demo](https://repl.it/HgDr/1)
