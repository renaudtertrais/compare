# toTitleCase

A `function` that take a `string` in input and should return all words of the `string` in "Title Case".
```js
toTitleCase("Hello world! WOW it looks awesome :)");
// "Hello World! Wow It Looks Awesome :)"
```

## Haskell
```haskell
import Data.Char
toTitleCase = unwords . map (\s -> (toUpper . head) s : (map toLower . tail) s) . words
```
[demo](https://repl.it/Gfgc/1)

## Javascript
```js
const toTitleCase = s => s
  .split(' ')
  .map(w => w[0].toUpperCase() + w.slice(1).toLowerCase())
  .join(' ');
```
[demo](https://repl.it/Gfhw/1)

## Python

```python
def toTitleCase(s):
  return " ".join(map(lambda s: s[0].upper() + s[1:].lower(), s.split()))
```
[demo](https://repl.it/Gfk4/3)

## Ruby

```ruby
def toTitleCase s
  s.split(' ')
    .map { |x| x[0].upcase + x[1..-1].downcase }
    .join(' ') 
end
```
[demo](https://repl.it/Gwh9/0)

## Swift

```swift
import Foundation

func head(str: String) -> String {
  return str[str.startIndex..<str.index(str.startIndex, offsetBy: 1)]
}

func tail(str: String) -> String {
  return str[str.index(str.startIndex, offsetBy: 1)..<str.endIndex]
}

func toTitleCase(str: String) -> String {
   return str
    .components(separatedBy: " ")
    .map { head(str: $0).uppercased() + tail(str: $0).lowercased() }
    .joined(separator: " ")
}
```

[demo](https://repl.it/GlGL/5)
