# Conditionals

![Shakespeare](http://www.gomoxie.com/wp-content/uploads/Hamlet.jpg)
>To be, or not to be...

## Learning Objectives - The student should be able to..

* Explain that by making parts of their code *conditional*, they can execute different pieces of code based on certain conditions.
* Explain that an *if* statement will execute a set of statements **only** if that condition is *true*. 

```swift
var age = 19

if age < 21 {
    print("You're not allowed to drink!")
}

// prints "You're not allowed to drink!"
```

* Explain that an *if* statement can provide an alternative set of statements, known as an *else clause*, for situations when the *if* condition is *false*.

```swift
var myHeight = 50

if myHeight > 60 {
    print("You're free to go on the ride, enjoy!")
} else {
    print("I'm sorry, you're too short to go on this ride today.")
}

// prints "I'm sorry, you're too short to go on this ride today."
```

* Create/chain multiple *if* statements together to consider additional clauses:

```swift
var temperatureInFahrenheit = 100

if temperatureInFahrenheit < 32 {
    print("Snow! 🌨")
} else if temperatureInFahrenheit >= 90 {
    print("Very hot! ☀️")
} else {
    print("Just right. 🌻")
}
```



## What the student can do at this point 

* Create variables and constants
* Is familiar with type annotations, type inference and string interpolation.
* Can create functions with return types.
* Is familiar with the `String`, `Int`, `Double` and `Bool` type.
* Just learned about `Bool` prior to this reading.
* Just learned about *comparison operators* but has YET to see what an if statement looks like. 


## Outline / Notes

*  You can run with the the narrative/examples I provided above if you so desire.
* I like the idea of having them open a playground file and get used to typing in the syntax.
* Maybe challenge them to type code off of a sentence or two (put them in a position where they have to evaluate what you wrote and turn that into code).

<a href='https://learn.co/lessons/Conditionals' data-visibility='hidden'>View this lesson on Learn.co</a>
