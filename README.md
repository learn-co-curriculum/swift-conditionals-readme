# Conditionals

![Shakespeare](http://www.gomoxie.com/wp-content/uploads/Hamlet.jpg)
>To be, or not to be...

## Learning Objectives - The student should be able to..

* Explain that by making parts of their code *conditional*, they can execute different pieces of code based on certain conditions.
* Explain that an *if* statement will execute a set of statements **only** if that condition is *true*. 
* Explain that an *if* statement can provide an alternative set of statements, known as an *else clause*, for situations when the *if* condition is *false*.
* Create/chain multiple *if-else* statements together to consider additional clauses:



## Outline / Notes

In the previous lesson we covered Boolean values (namely ````true```` and ````false````) along with the various operations we can perform that result in a Boolean value (namely ````<, ==, <=, >, >=, !=````).
For example:

````Swift
3 < 5    // false
12 >= 12  // true
let greedoFiredFirst  // true
! greedoFiredFirst  // false
````

At this point you may find Booleans interesting but are wondering what they're actually good for.  If that's the case then you're in luck because that's *exactly* what this lesson is about.

So far you've covered computer code that's of the form of directives and declarations; that is, "do this".  For example:

````Swift
print("hello")   // hello
// directive to print "hello"

var x = 5 * 8
// declaration of variable x

let i = 12 >= 9
// declaration of constant i
````

Most programs, however, need an additional component, and that component is Conditionals.  Conditionals are how you tell the program to take different behavior based upon conditions or results.  The simplest form of Conditional is just to do something if an expression is true.  We can express "if class is hard then study more" like this:

````Swift
if classIsHard {
	studyMore()
}
````

We can also specify an "else" clause.  For example, we can express "if class is hard then study more otherwise catch up on sleep" ike this:

````Swift
if classIsHard() {
	studyMore()
} else {
	catchUpOnSleep()
}
````

Are you begining to see the pattern?  Let's look at another one, maybe something more like an actual program, like "if the file exists then open it, otherwise tell the user it can't be found".  Let's see what it would look like in code:

````Swift
let doesFileExist = findFileNamed("testfile")
if doesFileExist == true {
	openFileNamed("testfile")
} else {
	reportError("testfile not found")
}
````

Every Conditional effectively has both an ````if```` and an ````else```` part but depending upon how we style our code we can leave out the explicit ````else```` (which the compiler interprets as "if the condition is false then don't do anything").  For example, we could re-write the code above as follows:

````Swift
let doesFileExist = findFileNamed("testfile")
if doesFileExist == false {
	reportError("testfile not found")
	return
}
openFileNamed("testfile")
````

Can you see how they'e variations of the same thing?  Let's look at another example.

````Swift
if rainingOutside == true {
	takeUmbrella()
} else {
	// don't worry about taking the umbrella
}
goForAWalk()
````
is the same as...

````Swift
if rainingOutside == true {
	takeUmbrella()
}
goForAWalk()
````

Our ````if```` doesn't have to be followed by a Boolean expression; it can also take Boolean variable or constant, or a function which returns a Boolean.  Here's what that would look like in code:

````Swift
let x = true
if x {
	...
}
````

is the same as

````Swift
let x = true
if x == true {
	...
}
````

And we can use variables:

````Swift
var y = false
if y {
...
}
````

Which is the same as:

````Swift
var y = false
if y == true {
   ...
 }
 ````
 
And here we'll show how to use a function:

````Swift
func test(Bool a, Bool b) -> Bool {
...
}

if test(x, y) {
...
}
````

There is one final bit of magic with Conditionals, and that is that we can chain them together almost indefinitely.  This is something that's actually much clearer to understand in code than written out in English, so let's look at an example:

````Swift
if sallyDressColor == "yellow" {
	wearSomethingGreen()
} else if sallyDressColor == "blue" {
	wearSomethingPurple()
} else if sallyDressColor == "red" {
	wearSomethingOrangle() 
} else if sallyDressColor == "green" {
	wearSomethingBlue()
} else ...
// that's a lot of decision-making!
````

##Review
*You've learned that Boolean expressions return ````true```` or ````false```` based upon the result of the comparison performed (or inverting the value in the case of the spcial operator ````!````).

*Boolean expressions are particularly useful in helping your program take a particular course of action.  For example, ````if the battery is low then alert user to conserve power````.  This is expressed with an ````if```` conditional.

*An alternate course of action can also be specified, such as ````if the battery is low then set battery color to red otherwise set battery color to blue````.   You accomplish this using an ````if / else```` Conditional, such as ````if batteryIsLow { ... } else { ... }````

*You can chain multiple ````if / else```` chunks together to handle more complicated situations where there instead of testing a single value you need to take different actions based upon three or more values.


<a href='https://learn.co/lessons/Conditionals' data-visibility='hidden'>View this lesson on Learn.co</a>
