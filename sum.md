# Sum

The function `sum` should take an` array` of `numbers` and return their sum.
Even if there should be some native functions to do it in some languages, 
it is interesting to compare the difference when implenting it.

```js
sum([1, 2, 3]); // -> 6
```

## Clojure
```clojure
(def sum (partial reduce +))
```
[demo](https://repl.it/HITM/1)

## F#

```f#
let sum = List.reduce (+)
```
[demo](https://repl.it/HFbJ/1)

## Haskell

```haskell
sum = foldl1 (+)
```
[demo](https://repl.it/HECN/0)

## Javascript

**using reduce**
```js
const sum = xs => xs.reduce((x, y) => x + y);
```

**recursive**
```js
const sum = ([head, ...tail]) => tail.length ? head + sum(tail) : head;
```
[demo](https://repl.it/HCV3/0)

## Python
```py
from functools import reduce
from operator import add

def sum (xs): return reduce(add, xs)
```
[demo](https://repl.it/HH1F/2)

## Ruby
```rb
def sum (xs)
  xs.reduce(:+)
end
```
[demo](https://repl.it/HH3k/0)
