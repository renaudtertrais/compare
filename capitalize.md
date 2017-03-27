# Capitalize

A `function` that take a `string` in input and should return all words of the `string` in capitalize case.
```js
capitalize("Hello world! WOW it looks awesome :)");
// "Hello World! Wow It Looks Awesome :)"
```
## Javascript
```js
const capitalize = s => s.split(' ')
  .map(w => w[0].toUpperCase() + w.slice(1).toLowerCase())
  .join(' ');
```
[demo](https://repl.it/Gfhw/0)

## Haskell
```haskell
import Data.Char
capitalize = unwords . map (\s -> (toUpper . head) s : (map toLower . tail) s) . words
```
[demo](https://repl.it/Gfgc/0)
