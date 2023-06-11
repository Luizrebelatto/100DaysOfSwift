## Arrays

`let fruits = ["apple", "orange", "banana", "papaya"]`

#### read an array position
- you type inside the square brackets the number of the index you are interested in
- if index does not exist, the array crashes

`fruits[0]`

- a example type annotation with arrays
`var cities: [String] = ["London", "Paris", "New York"]`

## Sets
- Collections of values

#### Sets characteristics
- Items aren’t stores in any order
- It is not really a random order, it is unordered
- No item can appear twice in a set
- All items must be unique
- If you enter a duplicate item, swift will ignore it
- You can’t read values from a set using numerical positions like you can with arrays

`let colors = Set<String>(["red", "green", "blue"])`

#### Why use Set?
- Because it has no specific order and no duplicates when you need to search if an item exists, it is more performant
- They can instead store them in a seemingly random order that optimizes them for fast retrieval

## Tuples
- Allow you to store several values in a single value
- You can’t add or remove items from a tuple, they are fixed in size
- You can’t change the type of items in a tuple 
- They always have the same types they were created with.
- Can access items in a tuple using numerical positions or by naming them, if that exist

#### Create a tuple
`let test: (name: String, city: String) = (name: "Luiz", city: "Cachoeirinha")`

#### Access a tuple
- by number
`name.0`
- by name
`name.first`

## Arrays vs Sets vs Tuples

#### Tuple
- If you need a specific, fixed collection of related values where each item has a precise position or name, you should use a tuple.
- If you want to hold precisely two strings, or precisely two strings and an integer, or precisely three Booleans, or similar, you should use a tuple.
```
let address = (house: 555, street: "Taylor Swift Avenue", city: "Nashville")
```

#### Sets
- If you need a collection of values that must be unique or you need to be able to check whether a specific item is in there extremely quickly, you should use a set:
- If you want to store a list of all words in a dictionary for a game, that has no duplicates and the order doesn’t matter so you would go for a set.
```
let set = Set(["aardvark", "astronaut", "azalea"])
```

#### Arrays
- If you need a collection of values that can contain duplicates, or the order of your items matters, you should use an array:
- If you want to store a list of high scores for a video game, that has an order that matters and might contain duplicates (if two players get the same score), so you’d use an array.

```
let pythons = ["Eric", "Graham", "John", "Michael", "Terry", "Terry"]
```

## Dictionaries
- Dictionaries are collections of values just like arrays, but rather than storing things with an integer position you can access them using anything you want.

```
let numbers: [String: Int] = [
    "one": 1,
    "two": 2,
    "three": 3
]
```

#### Access Dictionaries
- Access by your keys
`numbers["one"]`


## Dictionary default values
- When fetching an unknown value from the dictionary, to keep the program from breaking, we add the following term.

```
let favoriteIceCream:[String: String] = [
    "Paul": "Chocolate",
    "Sophie": "Vanilla"
]
```

- But if we tried reading a value that not exist, we’d get back nil, meaning that Swift doesn’t have a value for that key.
- We can fix this by giving the dictionary a default value of “Unknown”, so that when no ice cream is found we get back “Unknown” rather than nil:
`favoriteIceCream["Charlotte", default: "Unknown"]`

## Creating empty collections
- Arrays, sets, and dictionaries are called collections

- Dictionaries
```
var name = [String: String]()
var names = Dictionary<String, Int>()
```

- Array
```
var teams = [Int]()
var team = Array<Int>()
```

- Set
```
var numbers = Set<Int>()
```

## Enumerations
- usually called just enums – are a way of defining groups of related values in a way that makes them easier to use.
```
enum Result {
    case success
    case failure
}
```
- Call enum
`let result4 = Result.failure`

## Enum associated values
- Enum associated values let us add those additional details:

```
enum Weather {
    case sunny
    case windy(speed: Int)
    case rainy(chance: Int, amount: Int)
}
```

## Enum raw values
- call enum by its value
- You can set value and swift set the rest
```
enum Planet: Int {
    case mercury = 1
    case venus
    case earth
    case mars
}
```

## Complex types: Summary
- Arrays, sets, tuples, and dictionaries let you store a group of items under a single value. They each do this in different ways, so which you use depends on the behavior you want.
- Arrays store items in the order you add them, and you access them using numerical positions.
- Sets store items without any order, so you can’t access them using numerical positions.
- Tuples are fixed in size, and you can attach names to each of their items. You can read items using numerical positions or using your names.
- Dictionaries store items according to a key, and you can read items using those keys.
- Enums are a way of grouping related values so you can use them without spelling mistakes.
- You can attach raw values to enums so they can be created from integers or strings, or you can add associated values to store additional information about each case.