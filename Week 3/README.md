# Week 3

## Week 2 Summary

We talked about nested viewgroups, how to take apart a view using a view hierarchy, and then we started learning some basics of programming such as variables and methods. We ended off last week with explanation of how to find views via code and setting up a Click listener.

We learned:

- Adding button code to your app
- Updating views
- Properly scoping variables
- Finding views by their ID

## Object Oriented Programming

We can take our basic programming experience and start thinking about how we can be more object oriented with our approach.

## Public vs. Private

Public - Can be seen by anything else (Think of a for sale sign outside your house)

Private - Can only be seen within itself (Think of an envelope addressed to you)

## Defining a Method (Part 2)

{Access Modifier} {Return Data Type} {Method Name}({Parameter 1 Data Type} {Parameter 1 Variable Name})

- Access Modifier - Public/Private
- Return Data Type - void/int/String
- Method Name - Descriptive of what the method does
- Parameter Name - Descriptive of what the input is

EX:

```
public int calculatePrice(int totalCost) {
    return totalCost * 5;
}
```

**Note:** You can have 0 or more input parameters if you want. With no parameters, you do not define anything. With multiple, you separate with a comma.

EX:

```
public int calculatePriceBasedOnQuantity(int totalCost, int quantity) {
    return totalCost * quantity;
}
```

## Calling a Method

Depending on your access modifier and the scope of your method definition, calling a method is as simple as calling the method name in code and passing enough arguments(if any) to the method.

EX:

```
int totalPrice = calculatePrice(60);
```

## Creating an Object

```
public class Circle {        // class name
   double radius;            // variables
   String color;
   
   double getRadius() { ...... }  // methods
   double getArea() { ...... }
}
```

```
public class SoccerPlayer {  // class name
   int number;               // variables
   String name;
   int x, y;
   
   void run() { ...... }     // methods
   void kickBall() { ...... } 
}
```

How to instantiate these objects?

```
Circle redCircle = new Circle();

SoccerPlayer newPlayer = new SoccerPlayer();
```

How to set variables?

```
redCircle.color = "Red";

newPlayer.number = 99;
```

How to call methods?

```
double redCircleRadius = redCircle.getRadius();

newPlayer.kickBall();
```

## Accessing Resources

There's many different types of resources that we can access in Android.

- Image - R.drawable
- String - R.string
- Layout - R.layout
- ID - R.id
- Color - R.color

## Defining Resources in XML

- Image - @drawable/
- String - @string/
- Layout - @layout/
- ID - @id/
- Color - @color/

## Boolean Data Type

The boolean data type is a **true or false** data type. This data type is especially important for cases where you might need to ensure a condition is met before continuing.

EX:

Java
```
boolean isQuestionCorrect = false;
```

C#
```
bool isQuestionCorrect = false;
```

## Why learn about different Data Types?

In Android, we have many controls that can give us different values.

EX: 

We define a `Checkbox` control which has a `Checked State` of either true or false. This can indicate to us that an option is selected or not.

## Conditional Code

Conditionals are how we can make decisions in our applications. We can use language features such as `if / else` to create conditionals in our code.

## If Statement

The if statement simply checks whether the condition is true or false.

EX:
```
if (isClassOver) {
    //What code runs when class is over?
}
```

## If / Else Statement

But what about if the statement does not meet the condition? We don't always want to execute code sometimes. We can use an if/else statement:

EX:
```
if (isClassOver) {
    //What code runs when class is over?
} else {
    //What code runs if class is not over?
}
```

## If / Else If / Else Statement

What if we need to cover multiple conditions though? We can use an `else if` to match on conditions before the `else` hits.

EX:
```
if (isClassOver) {
    //What code runs when class is over?
} else if (isClassOver && classStudents > 20) {
    //What code runs if class is over and there's more than 20 students?
} else {
    //What code runs if class is not over?
}
```

## Equality and Relational Operators

There are many equality operators you can use:

```
==      equal to
!=      not equal to
>       greater than
>=      greater than or equal to
<       less than
<=      less than or equal to
```

## Intents

An intent is a "Intention to hand off work to something else". For example, you might want to delegate some hard work to another application to handle.

EX:
You might want to take a picture in your application but you haven't coded a camera in your app. However you can send an intent for the Android OS to find an application that can take a picture for you.

## What's inside an Intent?

- Action
- Data / Data URI
- Category
- Component
- Extras

## Using an Intent to pass data/extras

```
Intent i = new Intent(this, ActivityTwo.class);
i.putExtra("Value1", "This value one for ActivityTwo ");
i.putExtra("Value2", "This value two ActivityTwo");
```

As value you can use the primitive data types (int, float, …​) plus objects of type String, Bundle, Parcelable and Serializable.

## Retrieving an Intent's extras

```
Bundle extras = getIntent().getExtras();
if (extras == null) {
    return;
}
// get data via the key
String value1 = extras.getString(Intent.EXTRA_TEXT);
if (value1 != null) {
    // do something with the data
}
```

## Quiz #1

Object Oriented program mocks real life examples of objects?

- True
- False

## Quiz #2

How many arguments/parameters must a method have?

- 0 or more
- 1 or more
- 2 or more

## Quiz #3

The boolean data type returns a value of true or false?

- True
- False

**Note:** Yes this is a confusing question, I'm asking if it returns either true or false.

## Quiz #4

What is the equality operator for not equal to?

- ==
- !=
- not =
- <=

## Quiz #5

What is an intent useful for?

- Delegating work
- Communicating with another app
- Sending extra information
- All of the above

## App #3: Quiz App

Design and implement a quiz app with your favorite quiz questions!
