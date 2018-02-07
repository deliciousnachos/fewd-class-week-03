# Control Flow and Pseudocode
-----------------------------
## Learning Objectives
    - What is control flow?
    - Understand how/why programs don’t follow regular control flow
    - What is pseudocode?
    - Understand how/why we use pseudocode
    - Write a program together that controls a thermostat
---------------------------------------------------------

## Javascript As A Programming language

**What is programming to you?**

Programming is essentially solving problems step-by-step by using code

**Programming Terms**

Variables

- Declared using `var x = 3`
- Unlike in math, `=` is an assignment, it doesn't mean that there is an equality between the two values
- Variable names can't start with a number
- Variables with multiple words are written in camel case. Ex: myVariableName

Numbers

- With numbers you can use a lot of the operators that you're familiar with in math (+, -, /, *, >, <, >=, <=, !==)
- Here is where you can use equals the way that you might expect with `===`. 
    + Let's say you set a variable earlier in your code and you want to double-check what the current variable is. You can use `===` to find out
- You can also use `%` - the modulo. This will return the remainder of the two numbers used
    + Ex: 5 % 2 
    + Ex: 13 % 5

Strings

- Lines of text.
    + Ex: "apple", "computer", "book", etc
- What do you think would happen if I tried to use arithmetic operators on a string? Let's say "apple" + "computer"?
    + Automatic Type Conversion
- Here I'll show you why I said not to use `==`. What do you think I would get if I wrote `3 == "3"`?

Boolean

- `true`, `false`
- There's a difference between "true" and `true`

Array

- When you want to make a list of related elements you use an array
- Ex: `var groceryList = ["milk", "eggs", "bread"]`
- We target an item by putting the array name followed by an index surrounded by a bracket
- How would we select the second item from the groceryList array?

Functions

- Functions are a way to group a specific set of actions and give it a name.
- You can later call that name to run those actions
- This is helpful in following the D.R.Y. philosophy in coding (Don't Repeat Yourself)
- You can also give a function paramaters
- There are two ways commonly used to call functions:
    + `var functionName = function() {...}`
    + `function functionName () {...}`

**Pair Practice:** 

1. Create a function that will log the result of the input number squared
2. Create a function that takes a name and location as an input. When ran, this function will log "Hello, I'm *name* and I'm from *location*".

Objects

- Objects are a way to group related information. We do this using something called key/value pairs.
- You can have different values in an object like strings, numbers, even functions!
- One of the weird quirks about Javascript is that *technically* everything is an object. This is helpful though because it means that other data types like strings and arrays have methods too!
    + Array.length
    + Array.push(), Array.pop(), Array.shift(), Array.unshift()
    + String.toUpperCase()
- Syntax:
    + `var objName = {key1:"string", key2:5, key3: false, key4: functionName()}`
- You can select a property in an object similarly to how you can do it with arrays. To select "string" we would do `objName.key1`

Undefined
- The value a variable holds before it has been assigned a value

Null 
- Is a value that you can assign to a variable that represents [the absence of value](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/null)

## What is control flow?

The *control flow* is the order in which the computer executes statements in a script.

Similar to how CSS cascades in a stylesheet, Javascript runs from left to right and from top to bottom...most of the time. Sometimes you need flexibility in how your code is run. In those situations, you would manipulate the control flow.

What are some examples that you can think of where you would want to change the control flow?

### Methods of Control Flow Manipulation

**Conditionals**

    - A method of having certain lines of code run based on a certain condition
    - This is extremely useful and you'll see this in most codebases
    - We use conditionals by using the "if" and "else" keywords

**For Loop**

    * A way to have lines of code repeat a certain number of times

**While Loop**

    * A way to have lines of code repeat when you're not sure how many times you want to iterate
    * MAKE SURE THAT YOUR CONDITION WILL BE MET! You don't want to have to deal with an infinite loop and a browser crash

Things can get confusing when jumping around in code. That’s why we have pseudocode!

## Pseudocode

**What is pseudocode?**

Pseudocode is a non-technical, high-level step-by-step outline for your code
Pseudocode helps you plan out the control flow and fix mistakes before you start typing it out

Think about it as being similar how we draw out our HTML element mockups before we start working. It helps us avoid headaches when we start typing

Pseudocode should be written as close to possible as plain English. 
Examples: [http://www.unf.edu/~broggio/cop2221/2221pseu.htm](http://www.unf.edu/~broggio/cop2221/2221pseu.htm)

**Group Practice**

Describe how to make PBJ

**Group Practice:**

Let’s pseudo code a program that can control the thermostat

Our code will:

- Check for the current temperature. 
- If the current temperature is more than or equal to the target temperature, turn off the heater. 
- If current temperature is less than our target temperature, we want our code to turn on the heater. 

**Ex**: 

If the current temperature is 80 degrees and the target temperature is 75, we want the heater to turn off

If the current temperature is 75 degrees and the target temperature is 75, we want the heater to turn off

If the current temperature is 65 degrees and the target temperature is 75, we want the heater to turn on 

**Pair Practice:**

Pseudo code a rock paper scissors game. Remember to work out all possibilities!
Bonus: Have your “program” declare a winner if someone wins 2 out of 3 rounds

## Reintroducing the DOM with Javascript

Earlier we talked about the "family tree" nature of the DOM and how it helps us visualize HTML elements but it also comes into play with Javascript. The way that we use JS in our web pages is by using JS to target elements or *nodes* and changing their properties.

## Understanding Code

Read through the Color Switcher file [here](https://github.com/ga-students/FEWD-NYC-1.17.18/tree/master/week_03/07-intro-programming/color_scheme_switcher). Go into the "scripts/main.js" file and read the code. What do you think that it is doing?

The Color Switcher file uses "getElementByID" to target HTML elements but there are other ways to target nodes on the DOM with Javascript. Here are some other options:

**getElementByClassName()**

    document.getElementByClassName("my-div");

**getElementByTagName()**

    document.getElementByTagName("my-div");

**querySelector()**

    document.querySelector("#my-div");

**querySelectorAll()**

    document.querySelectorAll("#my-div.my-class");     

## Editing Code

**Pair Practice:**
[Here](https://codepen.io/Dtaitt/pen/zRoEJO?editors=0010) is a traffic light created in codepen but it doesn't work correctly. Edit it so that the light turns yellow when a user clicks "slow" and so that the light turns green when a user clicks "go".

## Helpful Links

[Dot Notation vs Bracket Notation](https://codeburst.io/javascript-quickie-dot-notation-vs-bracket-notation-333641c0f781)

[Document Object Properties and Methods](https://www.w3schools.com/jsref/dom_obj_document.asp)

[Mouse Events](https://www.w3schools.com/jsref/dom_obj_event.asp)