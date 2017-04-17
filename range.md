# Range

The idea here is to generate an array/list of numbers fom 1 to 10.

```js
a = range(1, 10)
// [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

## Clojure

**native `range` function**
```clojure
a = range(1, 11)
```

**recursive implementation**
```clojure
(defn range-rec [from, to] (
  if (> from to) '() (cons from (range-rec (+ from 1) to))
))
```
[demo](https://repl.it/HKZ5/3)

## Haskell
```haskell
a = [1..10]
```
[demo](https://repl.it/GyvT/0)

## Javascript
**using `Array.from()`:**
```js
const range = (from, to) => Array
  .from({ length: Math.max(to - from + 1, 0) })
  .map((_, i) => i + from);

const a = range(1, 10);
```

**recursive:**
```js
const rangeRec = (from, to) => from > to ? [] : [from, ...rangeRec(from + 1, to)];
    
const b = rangeRec(1, 10);
```
[demo](https://repl.it/GtnU/3)

## Python
```py
a = [x for x in range(1, 11)]
b = list(range(1, 11))
```

[demo](https://repl.it/Gyui/0)

## Ruby
```rb
a = *(1..10)
b = (1..10).to_a
c = Array (1..10)
```
[demo](https://repl.it/GtbQ/5)
