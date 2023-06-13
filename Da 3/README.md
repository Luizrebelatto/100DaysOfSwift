## Arithmetic operators

```
- + * / %
```

## Operator overloading
- we can add two integers using +, we can append one string to another using +, we can join two arrays using +

```
let fakers = "Fakers gonna "
let action = fakers + "fake"
```

```
let firstHalf = ["John", "Paul"]
let secondHalf = ["George", "Ringo"]
let beatles = firstHalf + secondHalf
```

## Compound assignment operators
- Operator abbreviation when you need to do an operation with a variable created by itself and another element 

```
var quote = "The rain in Spain falls mainly on the "
quote += "Spaniards"
```
```
var score = 95
score -= 5
```
```
var score = 95
score *= 5
```
```
var score = 95
score /= 5
```

## Comparison operators

```
==
!=
< >
<= >=
```

- In string swift follows alphabetical order
```
"Luiz" > "Gabriel" -> true
```

- That will print “true”, because small comes before large in the enum case list.
```
enum Sizes: Comparable {
    case small
    case medium
    case large
}

let first = Sizes.small
let second = Sizes.large
print(first < second)
```

## Conditions
```
if firstCard + secondCard == 2 {
    print("Aces – lucky!")
} else if firstCard + secondCard == 21 {
    print("Blackjack!")
} else {
    print("Regular cards")
}
```

## Combining conditions
- && and
- || or
- ! not

```
let age1 = 12
let age2 = 21

if age1 > 18 && age2 > 18 {
    print("Both are over 18")
}
```

## The ternary operator
```
firstCard == secondCard ? "Answer 1" : "Answer 2"
```

## Switch conditions
- if you want the condition continue in next case use keyword `fallthrough`
- When you use switch to check a value for multiple possible results, that value will only be read once, whereas if you use if it will be read multiple times. 

```
switch weather {
case "rain":
    print("Bring an umbrella")
case "snow":
    print("Wrap up warm")
case "sunny":
    print("Wear sunscreen")
    fallthrough
default:
    print("Enjoy your day!")
}
```

## Range operators
- For example, the range 1..<5 contains the numbers 1, 2, 3, and 4, whereas the range 1...5 contains the numbers 1, 2, 3, 4, and 5.
```
    let score = 85

switch score {
case 0..<50:
    print("You failed badly.")
case 50..<85:
    print("You did OK.")
default:
    print("You did great!")
}
```

## Operators and conditions summary
- Swift has operators for doing arithmetic and for comparison; they mostly work like you already know.
- There are compound variants of arithmetic operators that modify their variables in place: +=, -=, and so on.
- You can use if, else, and else if to run code based on the result of a condition.
- Swift has a ternary operator that combines a check with true and false code blocks. Although you might see it in other code, I wouldn’t - recommend using it yourself.
- If you have multiple conditions using the same value, it’s often clearer to use switch instead.
- You can make ranges using ..< and ... depending on whether the last number should be excluded or included.