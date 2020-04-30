# Version 1 - Arrays

Created: Apr 17, 2020 11:31 AM
Source: https://watchandcode.com/courses/60264/lectures/900191

# Goal Overview

Build an web app that has:

- a place to store todos
- a way to display todos
- a ways to add new todos
- a way to change a todo
- a way to delete a todo

While you understand the concept of 'Arrays'

# References

- ***`var`*** [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var)
- ***method*** [https://developer.mozilla.org/en-US/docs/Glossary/Method](https://developer.mozilla.org/en-US/docs/Glossary/Method)
- ***property accessors*** [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Property_accessors](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Property_accessors)
    - [https://codeburst.io/javascript-quickie-dot-notation-vs-bracket-notation-333641c0f781](https://codeburst.io/javascript-quickie-dot-notation-vs-bracket-notation-333641c0f781)
- ***parameters vs arguments*** [https://codeburst.io/parameters-arguments-in-javascript-eb1d8bd0ef04](https://codeburst.io/parameters-arguments-in-javascript-eb1d8bd0ef04)
- ***single vs double quotation*** [https://medium.com/javascript-in-plain-english/the-real-difference-between-single-quotes-and-double-quotes-in-javascript-3d00bf720bcd](https://medium.com/javascript-in-plain-english/the-real-difference-between-single-quotes-and-double-quotes-in-javascript-3d00bf720bcd)
    - [https://staxmanade.com/2018/03/should-i-use-javascript-single-or-double-quotes/](https://staxmanade.com/2018/03/should-i-use-javascript-single-or-double-quotes/)
- ***array*** [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
    - `***push()***` [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push)
    - `***splice()***` [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)

# Process

Understand the concept of ***arrays***

- Go through the natural workflow to create a list in the interaction with computer
- Interpret the flow in JavaScript way to understand concepts:
    - ***String and data type***
    - ***Variables***
    - ***Initialization: Declare a variable and assign a data to that***

## Step 1: Have a place to store todos

Discover and understand the common factors from real life todo note (pen and paper) and JavaScript ***arrays***.

An ***Array*** is a programming term for a ***list*** in JavaScript.

Write down a list of 3 items

- item 1
- item 2
- item 3

Now, let's convert this to Javascript code. Open up the browser console and type these 3 items with ***comma*** `,` to break instead of ***line-break*** and ***bullets***.

```jsx
// without `,`, below line would be treated like a single word.
item 1, item 2, item 3
```

In JavaScript, computer will look for `'...'` to find ***text*** information. Which we call ***string data type***.

```jsx
'itme 1', 'item 2', 'item 3' 
```

Group them with the bracket `[...]` to make them as a ***set*** of datas. Not this is a list the computer can understand in JavaScript, which called an ***array***.

```jsx
['item 1', 'item 2', 'item 3']
```

Try this in the browser console. We are asking a browser to make this list.

![Version%201%20Arrays/Untitled.png](Version%201%20Arrays/Untitled.png)

A browser will return the ***array*** which says 'we have created and printed your list in JavaScript ***array***'.

Now, we have this array of items printed. But it like someone just speaks up. Once the words's spoken, we can hear and once we hear, we can remember.

**Note:** browser does ***store*** the data we entered to have, try up arrow to see the proof.

But there no way we can ***bring them back to hear again*** at this point, unless we ***record*** them. This is a problem, we can create an ***array***, but then we have no way to get ahold of it again.

But there's a way we can ***record*** them in JavaScript, so that we can reference it later.

Start with giving a ***nickname*** to the data we want to ***record.*** Let's try `todos`.

```jsx
todos ['item 1', 'item 2', 'item 3'];
```

And add the syntax `var` to ***declare statement*** as a ***variable***. And add `=` ***to*** ***assign*** the ***array*** as a ***value*** of the ***variable***.

```jsx
var todos = ['item 1', 'item 2', 'item 3'];
```

![Version%201%20Arrays/Untitled%201.png](Version%201%20Arrays/Untitled%201.png)

When you enter this line into console, browser will spit `undefined`.  We'll revisit this later. For now, go ahead and try to print the todo list by entering `todos`.

![Version%201%20Arrays/Untitled%202.png](Version%201%20Arrays/Untitled%202.png)

Bingo! Now as long as your browser remembers this, you will be able to ***access*** to the list by using the ***variable***.

**Speaking JavaScript**
"a list" > ***an array (surrounded with open and closing brackets)***
"a list item" > ***each values that separated by `,`***
"text" > ***string (surrounded with quotation marks)***
"record data" > ***assign a data(value)***
"bring the data back to reuse" > ***access data***
"giving a nickname to the data" > ***initialize a variable***

- get ahold of

    (Use it in a sentence as an idiom 'get ahold of') having made contact, verbally or physically.

    get through, acquaint, advice, apprise

    - acquaint

        familiarize

    - apprise

        inform, notify, tell

## Step 2: Have a way to display todos

Use browser console(JavaScript console) to display the data by using `console.log` to ask ***printing it in the console*** to show us. `console.log` is like a ***recipe for computer to follow what to do***.

```jsx
console.log;
```

And we need to tell browser what item to print in ***parentheses*** right after the syntax.

```jsx
console.log(todos);
```

![Version%201%20Arrays/Untitled%203.png](Version%201%20Arrays/Untitled%203.png)

**Note:** we can use `,` for multiple items, and `'...'` for text item as well.

We can add some ***string*** to explain what this is. We can print out some helpful text `'My Todos'` followed by `todos` ***variable.***

```jsx
console.log("My Todos: ", todos);
```

![Version%201%20Arrays/Untitled%204.png](Version%201%20Arrays/Untitled%204.png)

Note: a space in the ***string*** takes a place as one character.

***A browser has a short term memory*** unless we force them to do so for longer term.
Every time we close and reopen the new tab(or window) it would refresh the memory.
With that said, if we are using new tab of the browser, we may need to create the nickname with the data of a list again.

![Version%201%20Arrays/Untitled%205.png](Version%201%20Arrays/Untitled%205.png)

**Speaking JavaScript**
"print something in the console" > `console.log(...)`
"a recipe for computer to follow what to do" > ***a function***

## Step 3: Have a way to add new todos

We have this list call by a nickname `todos`. In other words, we have a `todos` ***variable*** that is pointing to the assigned data of an ***array***.

And we want to tell to ***add new item(s) to the list*** by using a ***command*** `push`. It's called `push` because because we can think of it as ***pushing something to the end*** of the ***array***.

Start by ***pointing the list*** we want to deal with and followed by the ***command*** `.push()`. We can use ***the nickname*** as well.

**What does the `.` do?**
There are numbers of commands as the out-of-box features of given data. And the `.` helps us to access to the commands that belong to the data so we can pick and  use a valid command by the characteristic of the data.

```jsx
todos.push();
```

Now we can put the item to add inside of the ***parentheses***. Let's try `'item 4'`.

```jsx
todos.push('item 4');
```

**Note:** we need ***quotation marks*** to keep them as ***text***.

![Version%201%20Arrays/Untitled%206.png](Version%201%20Arrays/Untitled%206.png)

JavaScript will tell us how many items we have in the array after adding the new item.

![Version%201%20Arrays/Untitled%207.png](Version%201%20Arrays/Untitled%207.png)

Add one more item and type the ***variable*** name to see what the result looks like.

Can I `push` to something to a ***string***?
No. Because `push` is working only on an ***array***.

![Version%201%20Arrays/Untitled%208.png](Version%201%20Arrays/Untitled%208.png)

**Speaking JavaScript**
"add new item(s) to the list" > `push`
"a command" > ***a method***

## Step 4: Have a way to change a todo

Since our `todos` is an ***array***, we should be able to specify which item to change.

We can do that by calling out the list by the ***nickname*** and add ***a set of brackets*** to access to the item***.***

```jsx
todos[];
```

And put ***a number*** inside of the brackets that tells JavaScript which item you want to specify.

Let's add `0` to get the ***first item*** of the ***array***.

```jsx
todos[0];
```

Note: Computer is counting the number from `0` and we don't need the quotation marks for ***numbers***.

![Version%201%20Arrays/Untitled%209.png](Version%201%20Arrays/Untitled%209.png)

What if we try `todos[6]`?
That will say `undefined` that's because we don't have an item in the sixth position.

![Version%201%20Arrays/Untitled%2010.png](Version%201%20Arrays/Untitled%2010.png)

Now we know how to pick a specific item from an ***array***, we should try to change it.

Let's try the first item, and ***update the value using equal sign***.

```jsx
todos[0] = "item 1-1";
```

**Note:** A single equal sign `=` is an ***assignment operator*** not an 'equal to' `==`  as a ***comparison operator***.

![Version%201%20Arrays/Untitled%2011.png](Version%201%20Arrays/Untitled%2011.png)

JavaScript will return the updated ***value.***

![Version%201%20Arrays/Untitled%2012.png](Version%201%20Arrays/Untitled%2012.png)

The first item of an ***array*** has updated.

**Speaking JavaScript**
"pick the first item of an array" > ***array[0]*** 
"a set of brackets to access to the item" > ***bracket notation (property accessor)***
"update the value using equal sign" > ***assign a value***

## Step 5: Have a way to delete a todo

In JavaScript, we can ***ask a computer to*** delete an item(s) in an array by ***specifying the range of items*** to deal with as the ***clues for the command***.

We can start by calling out the ***nickname*** of the list, and add a ***command*** `splice` with a `.` to ***access to the out-of-box featured commands***. We need ***parentheses*** as well to provide ***the clues for the range of items*** to delete.

```jsx
todos.splice();
```

We can set the ***range of items*** by providing 2 numbers. For the first number,  we want the ***order of the item that the range start with.*** And for the second number, we need the ***number of how many items we want to delete***. Let's try to tell computer to remove the first item of the list.

```jsx
todos.splice(0, 1);
```

![Version%201%20Arrays/Untitled%2013.png](Version%201%20Arrays/Untitled%2013.png)

This returns the item.

Check how many items remain, and try to remove the last item this time.

```jsx
todos.splice(3, 1);
```

![Version%201%20Arrays/Untitled%2014.png](Version%201%20Arrays/Untitled%2014.png)

Note that the order has changed.

What will happen if we tell to delete that there's nothing? Like we try `todos.splice(3, 1)` again?
- It will return an ***empty array*** since there nothing has been deleted.

![Version%201%20Arrays/Untitled%2015.png](Version%201%20Arrays/Untitled%2015.png)

Note that there's no change.

**Speaking JavaScript**
"ask a computer to do(a command)" > ***function***
"clues for the command" > ***arguments, arguments of the function***
"out-of-box features" > ***property (since an array is an object)***
"use a `.` to access to the out-of-box featured commands" > ***dot notation (property accessor)***

# Review

Build an web app that has:

- a place to store todos

    ```jsx
    var todos = ['item 1', 'item 2', 'item 3']
    ```

- a way to display todos

    ```jsx
    console.log('My Todos: ', todos)
    ```

- a way to add new todos

    ```jsx
    todos.push('new todo')
    ```

- a way to change todo

    ```jsx
    // Access and change the first item
    todos[0] = 'changed todo'
    ```

- a way to delete a todo

    ```jsx
    // Delete the first item
    todos.splice(0, 1)
    ```