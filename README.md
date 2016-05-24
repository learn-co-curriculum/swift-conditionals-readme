# Conditionals

![Shakespeare](http://www.gomoxie.com/wp-content/uploads/Hamlet.jpg)
>To be, or not to be...

## Objectives

1. Describe the meaning of *conditional statements*
1. Use the `if` statement to conditionally execute a set of statements
1. Use an `else` clause to provide an alternative set of statements
1. Chain multiple *if-else* statements together

## Conditional statements

You already learned how to use the `Bool` type and various operators to evaluate logical expressions and compare values:

```swift
var age = 19

let isOfDrinkingAge = age > 21 // false, because 19 is not greater than 21
```

As was briefly mentioned in that lesson, those expressions become powerful using *conditional statements* which allow you to write pieces of code which can be executed (or not executed) based on certain conditions. These are called *control flow* constructs, because they allow you to control the execution flow of your program, allowing your program's output to react to conditions, instead of always providing the same output.

## If statement

The `if` statement makes the execution of a set of statements (also called a *block of code*) following it conditional based on a `Bool` value or expression. The given block of code will be executed *only if* the expression evaluates to `true`:

```swift
let age = 19

if age < 21 {
	print("You are not allowed to drink, yet.")
}

// prints "You are not allowed to drink, yet."
```

You can type this block of code in a new Playground file and experiment with giving `age` different values. You will notice that the `print` statement will no longer be executed once you increase the value of `age` to 21 or higher. 

Now try to extend the program by adding a second `if` statement which prints a message if the `age` is greater than or equal to 21. 

You will have ended up with something like this:

```swift
let age = 55

if age < 21 {
	print("You are not allowed to drink, yet.")
}

if age >= 21 {
	print("You are old enough to drink. 🍻")
}

// prints "You are old enough to drink. 🍻"
```

## Else clause

This seems hard to read and will also lead to duplicated work should the condition ever change in the future. Thankfully, Swift provides a better way to provide an alternative block of code to an `if` statement, an *else clause*:

```swift
let age = 55

if age < 21 {
	print("You are not allowed to drink, yet.")
} else {
	print("You are old enough to drink. 🍻")
}

// prints "You are old enough to drink. 🍻"
```

The code block following an `else` statement will only be executed if the condition provided to the corresponding `if` statement is `false`.

## Nested conditionals

Sometimes the execution flow of a program is not as clear cut as an either-or, there may be a third option or a default case. If that happens, you can chain multiple if-else statements together like this:

```swift
let temperatureInFahrenheit = 100

if temperatureInFahrenheit < 32 {
    print("Snow! 🌨")
} else if temperatureInFahrenheit >= 90 {
    print("Very hot! ☀️")
} else {
    print("Just right. 🌻")
}

// prints "Very hot! ☀️"
```

This will print the corresponding message if one of the two conditions are `true` and it will print "Just right. 🌻" when both of them are `false`. You should try typing this into your Playground again and see which statements are executed depending on the value of `temperatureInFahrenheit`.

You should again keep readability in mind and not nest if-statements too deeply. Swift provides an additional conditional statement called `switch` to handle bigger sets of conditionals, this will be introduced in another lesson.

<a href='https://learn.co/lessons/Conditionals' data-visibility='hidden'>View this lesson on Learn.co</a>
