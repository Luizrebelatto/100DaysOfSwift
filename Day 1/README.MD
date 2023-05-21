## Variables

#### how to create a variable?
- To create a variable we add the word **var** before the variable name
Example:
  ```
  var str = "Hello World"
  ```

#### How to edit a variable?
- you need to call the variable name and assign the name value, to edit you don't need the word **var** because it has already been created.
Example:
  ```
  str = "Hello Swift"
  ```


## Strings and integers
- Swift is what’s known as a type-safe language, which means that every variable must be of one specific type.
- **Int** –> short for “integer”.
- **str** –> short for "string".

- to create a variable to type integer we do like this:
```
var int = 40
```

- When we are going to deal with large numbers, we can use **underscore(_)** as separators for thousands. This makes it easier to read the value, For example:
```
var int = 75_000_000
```


## Multi-line strings
- swift default uses double quotes to define a string
- Multi-line strings must start and end with three double
- if you want multi-line strings, follow the example below:
"""
my code
test swift 
ios developer 
"""

- if you just want to format your code without breaking the line, use the **backslash(\)**
"""
my code \
test swift \
ios developer \
"""

## Doubles and booleans
- **Double** -> short for “double-precision floating-point number”
- when you create a variable with a fractional number, the language already sets your variable to type double:
```
var pi = 3.141
```

- Type boolean is just false or true
```
var a = false
var b = true
```

## String interpolation
- If you want to put some variable inside a string you can use string interpolation
- You can place any type of variable inside your string – all you have to do is write a backslash, \, followed by your variable name in parentheses.
```
var experience = 3 
var str = "My experience with mobile developer is \(experience)"
```


## Constants
- In some cases you want to assign a value and not change it anymore, so we use the constants
```
let taylor = "swift"
```

## Type annotations
- swift sets the types of your data according to the value assigned, this is called type interference
- You can be explicit about the type of your data rather than relying on Swift’s type inference, for example:
```
let album: String = "Reputation"
let year: Int = 1989
let height: Double = 1.78
let taylorRocks: Bool = true
```

## Simple types: Summary
- You make variables using var and constants using let. It’s preferable to use constants as often as possible.
- Strings start and end with double quotes, but if you want them to run across multiple lines you should use three sets of double quotes.
- Integers hold whole numbers, doubles hold fractional numbers, and booleans hold true or false.
- String interpolation allows you to create strings from other variables and constants, placing their values inside your string.
- Swift uses type inference to assign each variable or constant a type, but you can provide explicit types if you want.