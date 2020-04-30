# Version 2 - Functions

Created: Apr 30, 2020 2:14 PM
Source: https://watchandcode.com/courses/60264/lectures/929349

# Goal Overview

Understand the concept of the function:

- interpret a sandwich recipe into JavaScript way
- interpret customizing the recipe into JavaScript way

Build an web app that has:

- a function to display todos
- a function to add todos
- a function to change todos
- a function to delete todos
- Interpret

    explain, elucidate, clarify, explicate

    translate, transcribe

# References

- ***function is a recipe*** [https://www.codeanalogies.com/javascript-functions-explained](https://www.codeanalogies.com/javascript-functions-explained)

# Process

## Pre-Step 1: A Sandwich Recipe

Understand the concept of ***functions as a recipe of food.***

The whole point of the recipe is giving a piece of information to someone to get expected outcome with benefits like saving time to explain, minimizing the chance of error, and increase reusability.

Here is a recipe to make a turkey sandwich. Imagine that you're writing the instruction step-by-step for the most unexperienced staff.

> ***Make a turkey sandwich***
1. Get one slice of bread.
2. Add turkey.
3. Put a slice of bread on top.

Let's convert this to JavaScript function.

```jsx
// start with 'function' keyword followed by the name of the function

function makeTurkeySandwich
1. Get one slice of bread.
2. Add turkey.
3. Put a slice of bread on top.
```

```jsx
// add parenthese right next to the name of function

function makeTurkeySandwich()
1. Get one slice of bread.
2. Add turkey.
3. Put a slice of bread on top.
```

```jsx
// wrap all steps with curly braces

function makeTurkeySandwich() {
	1. Get one slice of bread.
	2. Add turkey.
	3. Put a slice of bread on top.
}
```

```jsx
// Instead of '.', Javascript uses ';' to end the each line.
// And we don't need the order of step because JavaScript natually read the line by line in order.

function makeTurkeySandwich() {
	Get one slice of bread;
	Add turkey;
	Put a slice of bread on top;
}
```

Now we have a recipe of the turkey sandwich. You may put that in your kitchen so every staff of the restaurant can find. When customer comes in and ask for the turkey sandwich, ***you can simply say "Make a turkey sandwich!"***

Whoever is in the kitchen, will find and follow the same recipe, you and customer can expect what to get. Because, what you're really asking is ***'to make a turkey sandwich according to the steps of the recipe'.***

> "Make a turkey sandwich!"

We need to convert this to JavaScript, so computer also can understand what to do.

```jsx
// the name of the function with parenthese to tell the computer to find the function and execute.

makeTurkeySandwich();
```

**Speaking JavaScript**
"a recipe" > ***a function***
"a step" > ***each line inside of `{...}`***
"make it!" > ***functionName()***
"." > `***;***`

## Pre-Step 2: Tweak the Recipe

Understand the concept of ***parameters*** and ***arguments*** as ***customizing the recipe***.

Now imagine your shop is expanding and you are adding a few more menus to serve. You can keep adding new recipes such as 'ham sandwich recipe', 'tuna sandwich', and 'peanut butter and jelly sandwich'.

In another hand, we can tweak the recipe to be customizable. So we can simply keep single recipe and provide a way to customize the sandwich with it. This might be a good idea because all steps of 'sandwich making' process are same accept the 'filling'.

So if we can make it to guide kitchen staff to use whatever 'filling' from customer's order, we'll be just fine with the single recipe for different sandwich outcomes. We will avoid repetitiveness of process that might caused by the numbers of recipes.

- repetitive

    monotonous, tedious, boring

The precess used be like:

***Restaurant has a recipe for the turkey sandwich.***

> ***Make a turkey sandwich***
1. Get one slice of bread.
2. Add turkey.
3. Put a slice of bread on top.

***Customer orders "One turkey sandwich please."***

> "Make a turkey sandwich!"

- Find and follow turkey sandwich recipe

    1. Get one slice of bread.
    2. Add turkey.
    3. Put a slice of bread on top.

***Outcome from the kitchen "One turkey sandwich served!"***

Now we can improve that like:

***Restaurant has a recipe for the sandwich with ______ that can place possible fillings.***

> ***Make a sandwich with _____***
1. Get one slice of bread.
2. Add _____.
3. Put a slice of bread on top.

***Customer orders "One [ham](https://codeburst.io/parameters-arguments-in-javascript-eb1d8bd0ef04) sandwich please."***

> "Make a [ham](https://codeburst.io/parameters-arguments-in-javascript-eb1d8bd0ef04) sandwich!"

- Find and follow a sandwich recipe with filling customer choose ([ham](https://codeburst.io/parameters-arguments-in-javascript-eb1d8bd0ef04))

    1. Get one slice of bread.
    2. Add [ham](https://codeburst.io/parameters-arguments-in-javascript-eb1d8bd0ef04).
    3. Put a slice of bread on top.

***Outcome from the kitchen "One [ham](https://codeburst.io/parameters-arguments-in-javascript-eb1d8bd0ef04) sandwich served!"***

Now let's do this in JavaScript.

We can do ***'____'*** by using a ***placeholder*** called ***parameter*** in JavaScript. And that can be filled with what every customer asked for - for example, 'ham.'

***Parameters*** are ***variables*** listed as a part of the function definition.
***Arguments*** are ***values*** passed to the function when it is invoked.

```jsx
// We have function **makeTurkeySandwich** provided

function makeTurkeySandwich() {
	Get one slice of bread;
	Add turkey;
	Put a slice of bread on top;
}

// Ivoke the function here
makeTurkeySandwitch();

// This will execute the function

// ------------- modify the function to customize sandwich ----------

// We have function **makeSandwichWith** provided
// and add a parameter **filling**

function makeSandwitchWith(***filling***) {
	Get one slice of bread;
	Add ***filling***;
	Put a slice of bread on top;
}

// Ivoke the function with the 'ham' as an argument
makeSandwitchWith('ham');

// This will execute the function with specific filling 'ham'
```

### Parameters vs. Arguments in JavaScript

[https://codeburst.io/parameters-arguments-in-javascript-eb1d8bd0ef04](https://codeburst.io/parameters-arguments-in-javascript-eb1d8bd0ef04)

### A Parameter as a Variable, An Argument as a Value

```jsx
funtion sayHiTo(person) {
	console.log('Hi', person);
}

sayHiTo('Han');
```

![Version%202%20Functions/Untitled.png](Version%202%20Functions/Untitled.png)

The code executed as expected.

Let's break this down.

Remember the ***parameters*** are variables that part of the function? ***When we define a function with a parameter***, it's like ***declaring a variable***.

```jsx
function sayHiTo(person) { // at this point, it's like declaring a variable: var person;
	console.log('Hi', person);
}
```

And ***when you invoke*** the function with a ***argument***, it's like ***assigning a value*** to the variable.

```jsx
function sayHiTo(person) { // var person;
	console.log('Hi', person);
}

sayHiTo('Han'); // person = 'Han'; which allows the function to deal with this data
```

**Speaking JavaScript**
"a placeholder" > ***a parameter***
"a real value to pass to steps" > ***an argument***

## Step 1: Have a function to display todos

TBD