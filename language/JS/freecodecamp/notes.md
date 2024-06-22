# JAVASCRIPT

## __**Print:**__
---
The console allows us to print and view JavaScript output. we can send information to the console using **console.log()**.

For example, this code will print "Naomi" to the console:

```
console.log("Naomi");
```

```
let developer = "Naomi";
console.log(developer);
```
---

## __**Variable :**__
---
JavaScript is the programming language that powers the web. Unlike the HTML and CSS you have learned previously, JavaScript is most commonly used to write logic instead of markup.

One of the most important concepts in programming is variables. A variable points to a specific memory address that stores a value. Variables are given a name which can be used throughout your code to access that value.

Declaring a variable means giving it a name. In JavaScript, this is often done with the **let** keyword.

For example, here is how we would declare a hello variable:

`let hello;`

we can assign a value using the assignment operator **=**.

For example:

`let character = "Hello";`

When a variable is declared with the **let** keyword, we can reassign (or change the value of) that variable later on.

In this example, the value of programmer is changed from "Naomi" to "CamperChan".

```
let programmer = "Naomi";
programmer = "CamperChan";
```
The default value of an uninitialized variable is **undefined**. This is a special data type that represents a value that does not have a definition yet.

You can still assign a value to an uninitialized variable.

Here is an example:

```
let uninitialized;
uninitialized = "assigned";
```
We can also assign the value of a variable to another variable.

For example:

```
let first = "Hello";
let second = "Hello World";
let first = second;
```
Declaring a variable with the ***let*** keyword allows it to be reassigned. This means we can change it later to be a completely different value.

If we are sure that the declared variable will not gonna be changed then we then use ***const*** keyword to declare them. ***const*** variable are special.

`const variable = value;`

A ***const*** variable cannot be uninitialized. This example code will throw error.

`const firstname;`

A ***const*** variable cannot be reassigned like a ***let*** variable. This code example would throw an error:

```
const firstname = "Naomi"
firstname = "CamperChan";
```
Variables in JS are available in a specific *scope*. In other words, where a variable is declared determines where in our code it can be used.

___Global Scope :___ The first scope is the global scope. Variable that are declared outside of any "block" like a function and for loop are in the *global scope*.

When a variable is in the global scope, a function can access it in its definition. Here is an example of a function using a global *title* variable.

```
const title = "Professor ";
function demo(name) {
  return title + name;
}
demo("Naomi")
```
___Local Scope or Block Scope :___ Variable can also be declared inside a function. These variables are considered to be in the *local scope*, or *block scope*. A variable declared inside a function can only be used inside that function. If we try to access it outside of the function, we got a reference error.

---
## __**Data Types**__
---
JavaScript has seven primitive data types, with **String** being one of them. In JavaScript, a string represents a sequence of characters and can be enclosed in either single (') or double (") quotes.

**Number :** With number datatype, we can perform mathematical operations, like addition and multiplication. When using a number value, we do not use quotes.

For example:

`let num = 10;`

**Objects :** Objects are very important data type in JS. Objects are non primitive data types are mutable data types that are not *undefined*, *null*, *boolean*, *number*, *string* or *symbol*.

For example:
```
{
  key: value
}
```
Objects are similar to arrays, except that instead of using indexes to access and modify their data, you access the data in objects through properties.

Properties consist of a key and a value. The key is the name of the property, and the value is the data stored in the property.

For Example:
```
const obj = {
  name: "Quincy Larson"
};
```
If the property name (key) of an object has a space in it, you will need to use single or double quotes around the name.

Here is an example of an object with a property name that has a space:

For example:
```
const spaceObj = {
  "Space Name": "Kirk",
};
```
If we tried to write a key without the quotes, it would throw an error:

For example:
```
const spaceObj = {
  // Throws an error
  Space Name: "Kirk",
};
```
There are two ways to access the properties of an object: dot notation (.) and bracket notation ([]), similar to an array.

Dot notation is what we use when we know the name of the property you're trying to access ahead of time.

For example:
```
object.property;
```
Here is a sample of using dot notation (.) to read the name property of the developer object:
```
const developer = {
  name: "Jessica",
}

// Output: Jessica
console.log(developer.name);
```
The second way to access the properties of an object is bracket notation ([]). If the property of the object we are trying to access has a space in its name, you will need to use bracket notation.

For example:
```
objectName["property name"];
```
Here is a sample of using bracket notation to read an object's property:
```
const spaceObj = {
  "Space Name": "Kirk",
};

spaceObj["Space Name"]; // "Kirk"
```

---

## __**Data Structure**__
---

In programming, we will often need to work with lots of data. There are many data structures that can help you organize and manage your data. One of the most basic data structures is an array.

**Array :** An array is a non-primitive data type that can hold a series of values. Non-primitive data types differ from primitive data types in that they can hold more complex data. Primitive data types like strings and numbers can only hold one value at a time. Arrays are denoted using square brackets (**[...]**).

Here is an example of a variable with the value of an empty array:

`let array = [];`

When an array holds values, or element, those value are separated by commas.

Here is an array that holds two strings:

`let array = ["first", "second"];`

We can access the values inside an array using the *index* of the value. An index is a number representing the position of the value in the array, starting from 0 for the first value. We can access the value using *bracket notation*, such as **array[0]**.

Arrays are special in that they are considered *mutable*. This means you can change the value at an index directly.

For example, this code would assign the number 25 to the second element in the array:

~~~
let array = [1, 2, 3];
array[1] = 25;
console.log(array); // prints [1, 25, 3]
~~~

Notice how the value inside our array has been changed directly? This is called *mutation*.

Currently, our code accesses the last element in the array with last index. But we may not know how many elements are in an array when we want the last one.

We can make use of __*.length*__ property of an array. This returns the number of elements in the array. To get the last element of any array, we can use the following syntax:

`array[array.length -1];`

#### ___array.methods___

- __*array.length*__ returns the number of elements in the array. By subtracting1, we get the index of the last element in the array. <br> `array.length`

- __*array.push()*__ allows us to **"push"** a value to the end of an array. <br> `array.push(12);`

- ***array.pop()*** remove the last element from an array and returns that element. <br> `array.pop();`

- ***array.unshift()*** method of an array allows us to add a value to the beginning of the array, unlike *.push()* which adds the value at the end of the array. <br> `array.unshift(12);`

- ***array.shift()*** method remove the first element of the array, unlike .pop() which removes the last element. <br> `array.shift();`

- ***array.includes()*** method determines if an array contains an element and will return either *true* or *false*. <br> `array.includes(12)`

**String :**

#### ___string.methods___
- ___.repeat___ method accepts a number as a an argument, specifying the number of times to repeat the target string. <br> For example, using *.repeat()* to generate the string *"code! code! code!"*: <br> `const activity = "code! ";` <br> `activity.repeat(3);`

---
## __**Conditional Statement**___
---

 conditional statement, also known as a selection statement, facilitates the making of decisions on the basis of particular conditions. Furthermore, such a statement executes in a sequential manner when there is no condition around the statement. In case some condition is put for a block of statements, change may occur in the execution flow on the basis of the result evaluated by the condition

 #### <u>__***if Statement :***__</u>
An *if statement* allows you to run a block of code only when a condition is met.

```
if (condition) {
  logic
}
```

A ***truthy value*** is a value that is considered true when evaluated as a boolean. Most of the values you encounter in JavaScript will be truthy.

Example
```
if ("false") {
  console.log("Condition is true");
}
```

A ***falsy value*** is the opposite - a value considered false when evaluated as a boolean. JavaScript has a defined list of falsy values. Some of them include false, 0, "", null, undefined, and NaN.

Example
```
if (false) {
  console.log("Condition is true");
}
```

 #### <u>__***if...else if...else Statement :***__</u>
*if...else if...else statements* allow you to check multiple conditions in a single block of code.

```
if (condition1) {
  // code to run if condition1 is true
} else if (condition2) {
  // code to run if condition2 is true
} else if (condition3) {
  // code to run if condition3 is true
} else {
  // this code will run
  // if the first and second conditions are false
}
```
If the first condition is **false**, JavaScript will check the next condition in the chain. If the second condition is **false**, JavaScript will check the third condition, and so on. An else block will only evaluate if the conditions in the *if* and *else if* blocks are not met.

---
## __**Loops**__
---

Loops are used to execute a block of code repeatedly for a specified number of times.

### <u>__***for loop :***__</u>

```
for (iterator; condition; iteration) {
  logic;
}
```

- ***Iterator -*** The iterator is a variable we can declare specifically in your *for* loop to control how the loop iterates or gos through our logic. <br> It is common convention to use *i* as out iterator variable in a loop. A *for* loop allows us to declare this in the parentheses ().<br>For example, here is a *for* loop that declares an *index* variable and assigns it the value *100*.<br>
`for (let index = 100; "second"; "third") {}`

- ***Condition -*** The *condition* of a *for* loop tells the loop how many times it should iterate. When the *condition* becomes false, the loop will stop.

- ***Iteration -*** Our *iteration* statement tell our loop what to do with the iterator after each run.

### <u>__***for...of loop :***__</u>

```
for (const value of iterable) {

}
```

A *for...of* loop iterates over each item in an iterable object and temporarily assign it to a variable.

Note that we can use *const* because the variable only exists for a single iteration, not during the entire loop.

### <u>__**while loop**__</u>
A *while* loop will run over and over again until the *condition* specified is no longer true.

~~~
while (condition) {
  logic;
}
~~~

If we change *condition* to true, our *while* loop will run forever. This id called *infinite loop*, and we should be careful to avoid these. An *infinite loop* can lock up our system, requiring a full restart to escape.

---
## __**Functions**__
---

A *function* is a block of code that can be reused throughout your application. Functions are declared with the following syntax:

~~~
function name(parameter) {

}
~~~

The *function* keyword tells JS that the *name* variable is going to be a function. *parameter* is a variable that represents a value that us passed into the function when it is used. A function may have as many , or as few, parameters as we like. Like a *for* loop, the space between the curly braces is the function body.

In order to use a function, we need to call it. A *function* call tells our application to run the code from the function whenever we choose to call it. The syntax for a function call is the function name followed by parentheses.

For example, this code defines and calls a *test* function.

```
function test() {

}

test();
```

___Parameter:___ Parameters are special variables that are given a value when you call the function, and can be used in the function's code.

To add a parameter to our function, we need to add a variable name inside the parentheses.

For example, this *demo* function has a *name* parameter:

```
function demo(name) {

}
```

When we pass a value to a function call, that value is referred to as an *argument*. Here is an example of calling *demo* function and passing *"Naomi"* as the argument for the name parameter.

```
function demo(name) {
  return name;
}
demo("Naomi");
```

Values returned out of a function are used by calling the function. you can use the function call directly as the value it returns, or capture the returned value in a variable. This way, we can use the value assigned to a locally scoped variable, outside the function it was created in.

```
function getName() {
  const name = "Camper cat";
  return name;
}

console.log(getName()); // "Camper cat"

const capturedReturnValue = getName();
console.log(capturedReturnValue); // "Camper cat"

console.log(name); // reference error
```
An important thing to know about the *return* keyword is that it does not just define a value to be returned from your function, it also stops the execution of your code inside a function or a block statement. This means any code after a *return* statement will not run.