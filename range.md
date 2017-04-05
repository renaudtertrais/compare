# Range

The idea here is to generate an array/list of numbers fom 1 to 10.

```js
a = range(1, 10)
// [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

## Javascript

```js
// using Array.from()
const range = (from, to) => Array
  .from({ length: Math.max(to - from + 1, 0) })
  .map((_, i) => i + from);

const a = range(1, 10);

// recusive
const rangeRec = (from, to) => from > to 
  ? []
  : from === to
    ? [from]
    : [from, ...rangeRec(from + 1, to)];
    
const b = rangeRec(1, 10);
```

## Ruby
```rb
a = *(1..10)
b = (1..10).to_a
c = Array (1..10)
```
[demo](https://repl.it/GtbQ/5)
