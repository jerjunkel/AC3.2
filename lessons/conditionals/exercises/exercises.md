/* My answers are */

//: Playground - noun: a place where people can play

import UIKit

var str = "Hello, playground"
/*
Question1
Reasons to use switch instead of if
1. when you have multiple conditions that need to be met with the same data type.
2.

Question 2
C.

Question 3

*/

//Question 3
var temperatureInFahrenheit = 72

switch temperatureInFahrenheit {

case -20..<40:
print("It's freezing out!")
case 85..<200:
print("It's really warm.")
default:
print("Weather is moderate.")
}

//Question 4

let cardNum = 12

switch cardNum {
case 11:
print("Jack")
case 12:
print("Queen")
case 13:
print("King")
default:
print(cardNum)
}

//Question 5

var numGrade: Int = 101
let msg = "Your grade is "

switch numGrade {
case 100:
print("\(msg) A+")
case 90...99:
print("\(msg) A")
case 80...89:
print("\(msg) B")
case 70...79:
print("\(msg) C")
case 65...69:
print("\(msg) D")
case 0...64:
print("\(msg) F")
default:
print("This is not a legit grade!")
}

/*Question 6

It currently prints out "The answer to life, the universe and everything"
365 will print "Days in year"
1024 will print "Bytes in a Kilobyte"
65 will print default "Some uninteresting number"
If the default is rremoved there will be an error

*/

//Question 7

var population: Int = 10001
var message = String()

if population > 10000 {
message = "\(population) is a large town"
}else if population < 10000 && population > 5000{
message = "It's a medium size town"
}else{
message = "it's a mid sized town"
}

switch population{
case 0..<5000:
message = "it's a mid sized town"
case 5000...10000:
message = "It's a medium size town"
default:
message = "\(population) is a large town"
}


//Question 8

let myTuple: (Int, Int) = (5,10)
let sum = myTuple.0 + myTuple.1

if sum >= 15 {
print("The sum is at least 15")
}
else {
print("The sum is less than 15")
}


switch sum{
case 0..<15:
print ("The sum is less than 15")
default:
print("The sum is at least 15")

}

//Question 9
let studentNameAndClass = ("Ben", 3.2)

var myTupleTwo = studentNameAndClass


switch myTupleTwo{
case(_,3.2):
print("Welcome \(myTupleTwo.0) to the \(myTuple.1) class")
default:
break

}

//Question 10
var myTupleThree = (x: 2,y: 5)

switch myTupleThree {
case let (x,y) where x==y :
print("x is equal to y")
case let (x,y) where y==2*x:
print("y is double the value of x")
case let (x,y) where y==3*x:
print("y is triple the value of x")
case let (x,y):
print("Nothing is special about this tuple")
default:
break
}


# Conditionals

### Question 1.
What are some reasons to use a __switch__ instead of an __if__?

### Question 2.
What's missing from the switch statement below?
- a. The case statement needs to say month == 1
- b. The code is valid and not missing anything
- c. The below code will not compile because switch statements need case statements for all expected values or a default statement.

```swift
let monthNum = 3
switch monthNum {
case 1:
    print("January")
}
```

### Question 3.
Convert the if/else statement below into a switch statement.

```swift
temperatureInFahrenheit = 72

if temperatureInFahrenheit <= 40 {
    print("It's cold out.")
} else if temperatureInFahrenheit >= 85 {
    print("It's really warm.")
} else {
    print("Weather is moderate.")
}
```

### Question 4.
Change the below if/else statement into a switch statement.
```swift
let cardNum = 12
if cardNum == 11 {
    print("Jack")
} else if cardNum == 12 {
    print("Queen")
} else if cardNum == 13 {
    print("King")
} else {
    print(cardNum)
}
```

### Question 5.
Create a switch statement that will convert a number grade into a letter grade as shown below:
* 100 -> A+
* 90 - 99 -> A
* 80 - 89 -> B
* 70 - 79 -> C
* 65 - 69 -> D
* Below 65 -> F

### Question 6.
Consider the below switch statement. What should your system currently print? What happens when you change _number_ to 365? 1024? 65? What happens when you remove the __default__ clause?
```swift
let number = 42

switch number {
case 365:
    print("Days in year")
case 1024:
    print("Bytes in a Kilobyte")
case 0:
    print("Where arrays start")
case 42:
    print("The answer to life, the universe and everything")
default:
    print("Some uninteresting number")
}
```

### Question 7.
Consider the variable below called _population_ and the if-condition.
1. Add an else-if-condition that states if _population_ is less than 10000 but greater than 5000, the message changes to say it's "a medium size town".
2.  Add an else-condition where the message changes to say it's a mid-size town.
3. Convert your final if-else statement to a switch statement.

```swift
var population: Int = 10000
var message = String()

if population > 10000 {
    message = "\(population) is a large town"
}
```

### Question 8.
Complete the code below so that it prints out and tells the user if the sum of the two numbers in the tuple is at least 15.
a) Using a conditional
b) Using a switch statement

```swift
let myTuple: (Int, Int) = (5, 10)
```

### Question 9.
Complete the switch statement below.  We want it to output a personalized greeting to the student based on their name and class.

```swift
let studentNameAndClass = ("Ben", 3.2)
switch myTupleTwo{
   
}

```

### Question 10.
Consider the below switch with a tuple.
* Add a case for when _y_ is __double__ the value of _x_
* Add a case for when _y_ is __triple__ the value of _x_

```swift
switch (x,y) {
case let (x,y) where x==y :
    print("x is equal to y")
case let (x,y):
    print("Nothing is special about this tuple")
}
```

###Question 11
Write an if statement that checks to see what quadrant a point is in, then prints that quadrant.
Then write it as a switch statement
```swift
let myPoint: (Double, Double)
```

###Question 12
Write an if statement that prints out what decade of life someone is in (e.g "You are in your twenties).
Then write it as a switch statement
```swift
let nameAndBirthDate: (String, Int)
```

###Question 13
Write a switch statement that switches on a tuple with two Bools and prints what logical operators (&&, ||) could be applied to make a true expression.
```swift
let pAndQ: (Bool, Bool)
```

Next, write a switch statement that switches on a tuple with 3 Bools and prints what logical operators (&&, ||) could connect all Bools with to make a true expression.
```swift
let pAndQAndR: (Bool, Bool, Bool)
```

###Question 14
Write a switch statement that prints out the type of what it's switching on

###Question 15
Write a conditional statement that prints out whether a number is a whole number

### Question 16
 You're walking in Manhattan. Write a switch statement that switches
 on a variable named "direction" having one of the values "North", "East",
 "West", or "South" and tells you if you're on a street or avenue
 
### Question 17
 You're in the Battery and you're heading for C4Q AND you can walk on water.
 Write a switch using fallthrough to tell you you're getting warmer or colder
 based on "direction" again. It should also report if you're going
 "uptown" or "downtown" (but shouldn't report about east or west).



 
