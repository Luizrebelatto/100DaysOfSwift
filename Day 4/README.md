## For Loops
- Run some code repeatedly until a condition evaluates as false
```
let count = 1..10
for number in count {
    print("Number is \(number)")
}
```

- If you don’t use the constant that for loops give you, you should use an underscore instead so that Swift doesn’t create needless values:
`_`
```
let names = ["Sterling", "Cyril", "Lana", "Ray", "Pam"]

for name in names {
    print("\(name) is a secret agent!")
}
```

## While Loops
- On the other hand, while loops can loop until any arbitrary condition becomes false, which allows them until we tell them to stop.
- That’s where a while loop comes in handy: we can keep the loop going around until we’re ready to exit
```
var number = 1

while number <= 20 {
    print(number)
    number += 1
}

print("Ready or not, here I come!")
```

## Repeat loops
- when we need to execute the code once before checking it.

```
var number = 1

repeat {
    print(number)
    number += 1
} while number <= 20

print("Ready or not, here I come!")
```

## Exiting loops
- you can leave the loop whenever you want, just add the condition of your choice inside the loop with the word break
```
while countDown >= 0 {
    print(countDown)

    if countDown == 4 {
        print("I'm bored. Let's go now!")
        break
    }

    countDown -= 1
}
```

## Exiting multiple loops
```
outerLoop: for i in 1...10 {
    for j in 1...10 {
        let product = i * j
        print ("\(i) * \(j) is \(product)")

        if product == 50 {
            print("It's a bullseye!")
            break outerLoop
        }
    }
}
```

## Skipping items
```
for i in 1...10 {
    if i % 2 == 1 {
        continue
    }

    print(i)
}
```

## Infinite loops
- To make an infinite loop, just use true as your condition.
- That allows you to end the loop when you’re ready, so they aren’t truly infinite. 
```
var counter = 0

while true {
    print(" ")
    counter += 1

    if counter == 273 {
        break
    }
}
```

## Looping Summary
- Loops let us repeat code until a condition is false.
- The most common loop is for, which assigns each item inside the loop to a temporary constant.
- If you don’t need the temporary constant that for loops give you, use an underscore instead so Swift can skip that work.
- There are while loops, which you provide with an explicit condition to check.
- Although they are similar to while loops, repeat loops always run the body of their loop at least once.
- You can exit a single loop using break, but if you have nested loops you need to use break followed by whatever label you placed before your outer loop.
- You can skip items in a loop using continue.
- Infinite loops don’t end until you ask them to, and are made using while true. Make sure you have a condition somewhere to end your infinite loops!