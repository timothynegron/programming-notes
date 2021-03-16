# Programming Foundations

### Topics Covered

1. JavaScript Functions
2. Global Variables Vs Local Variables
3. Passing Values to Functions
4. Using a Function to Return a Value
5. JavaScript Comparison Operators
6. Intro to Conditional Statements: if and else keywords

---

### JavaScript Functions

In computer programming, functions are blocks of code that can execute
at any instances *when called on*. In JavaScript, a function is created, also referred to as *defined*, with a keyword called `function` followed by the function name with a set of parenthesis and curly brackets. In example: 

```javascript
function sayHello () {
    console.log('Hello, World!');
}
```
**Keywords** are reserved words that have special meaning to a computer. 
In this case, the keyword `function` tells the computer that the following 
line or lines of code is defining a function. In between the curly brackets 
is where the definition is written. The function above was defined, *created*,
to display the string "Hello, World!"

Defining, a function  does not execute any code. It only gives
the functions name meaning to the computer. To execute a function, you need 
to write the variable name followed by the parenthesis, outside of the
function. This is called **invoking** the function by **calling** the
function. In example, in JavaScript:

```javascript
sayHello(); // Executes the function
```

Output:

```
Hello, World!
```

Where `sayHello();` calls, and therefore executes, the function definition that has the function name `sayHello`. The function definition is the lines, or line, of code in between the curly brackets. The code in between the curly brackets is also know as the function body or the code block. 

Functions help make code easier to read. Giving a function a good name can immediately indicate to a programmer what the code within the function does. Functions also help make it *easier to make code changes* while building applications, adding features in the future, or fixing issue with code, also known as bugs.

As an example as to how functions are helpful, say a computer programmer wants to make a change to the lines of code in between a function. If an application uses the function defined above, `sayHello()`, at many different instances within the application, **any changes made to the 
definition of** `sayHello()` **would also affect the many other instances 
where** `sayHello()` **is executed**. So, if a computer programmer changes 
`sayHello()` to output "Ugh, Trolls!" instead of "Hello, World!" *where the definition is the defined*, then each instance that `sayHello()` is executed within the application would now output "Ugh, Trolls!" 

In contrast, if the lines of code in between `sayHello()` was entered at each instance of the application instead of using the function itself, than the computer programmer would have to change the text "Hello, World!" to "Ugh, Trolls!" at each instance. Consequently, this method is more time consuming and more error prone.

---

### Global Variables Vs Local Variables

**Global variables** are variables declared outside of a function. If a variable is declared outside of a function, then code in between the curly brackets of *all* function can give that variable a new value. For example, in JavaScript:

```javascript
let classSize = 20; // Global variable

function addOneToClassSize() {
    classSize = classSize + 1;
}

function removeOneFromClassSize() {
    classSize = classSize - 1;
}

addOneToClassSize(); // Calls the function
console.log(classSize);

removeOneFromClassSize(); // Calls the function
console.log(classSize);
```

Output:

```
21

20
```

Where the variable `classSize` is declared outside of both functions and, therefore, is a global variable. Global variables have **global scope**. Since `classSize` was declared outside of the function, both functions were able to change the value of `classSize` because of its global scope.

If a variable is declared inside of a function, the variable is a **local variable** to that function and has **local scope** to that function. For example, in JavaScript:

```javascript
function declareClassSize() {
    let classSize = 20; // Initializes classSize within the function
}

console.log(classSize);
```

Output:

```
classSize is not defined
```

The variable `classSize` was defined *within the function*, **in between the curly brackets**, of `declareClassSize` and, as a result, `console.log()` could not output the value of `classSize`. In other words, the variable `classSize` does not exist outside of the function.

---

### Passing Values to Functions

Functions can be defined with parameters. **Parameters** are variable names of values that are passed to the function. They are defined in between the parenthesis of a function separated by a comma. For example, in JavaScript:

```javascript
function nameOfFunction(parameter1, parameter2, parameter3){
    // You can access the parameters in here.
}
```

As another example:

```javascript
let sum = 0;

function sumOfThreeNumbers(num1, num2, num3){
    sum = num1 + num2 + num3;
}

sumOfThreeNumbers(2, 5, 3); // calling the function and passing values
console.log(sum);
```

Output:

```
10
```

**Where the values of the parameters were passed to the function when calling the function**. The passed in value can be of any data type.

---

### Using a Function to Return a Value

A function can **return** a value by using the `return` keyword within the curly brackets of a function. For example, in JavaScript:

```javascript
function helloString(){
    return 'Hello!'; // return the string Hello!
}
```

The function above is defined to `return` the hello `string`.

To retain the value that the function returns, *you must assign it to a variable*. For example, with the function above, in JavaScript:

```javascript
let str = helloString();

console.log(str);
```

Output:

```
Hello!
```

Where the variable `str` will be given the value returned from the function `helloString()`.

##### Here is an image breaking down the components of a JavaScript function:

![alt JavaScript function components](https://www.frontamentals.com/static/function-breakdown-e46e54ec2e0de641547f63411acb1d84-bf43a.png)

> Here is a good article for JavaScript functions: [JavaScript Functions]((https://www.frontamentals.com/functions/))

---

### JavaScript Comparison Operators

In JavaScript, you can give a variable a value with a type of Boolean. For example, in JavaScript:

```javascript
let myBoo = true;

console.log(myBoo);
```

Output:

```
true
```

Where `true` is a keyword that lets the computer know that the variable is a type of boolean and has a value of true.

JavaScript has a set of comparison operators that when used, returns a `true` or `false` boolean value. Here is a list of the comparison operators:

* Greater Than: >
* Greater Than or Equals to: >=
* Less Than: <
* Less Than or Equals to: <=
* Equals to: ===
* Not Equals to: !==

In example, if we compare two numbers say is 10 greater than 20 when the computer executes that line of code, it will return false. Here is how that looks in JavaScript:

```javascript
let myBoo = 10 > 20;

console.log(myBoo);
```

Output:

```javascript
false
```

Where the variable `myBoo` was initialized with the value of `false` after the computer computed `10 > 20`.

---

### Intro to Conditional Statements: if and else keywords

In JavaScript, the `if` and `else` keywords can be used to execute code depending on certain conditions. The `if` keyword is written with a set of parenthesis and usually followed by a set of curly brackets. Within the parenthesis is where the condition needs to be written and within the curly brackets is where the code to be executed, if the condition is true, will be written. If the condition is false, the code will not execute. For example, in JavaScript:

```javascript
if(10 < 20){
    console.log('Trolls are among us. Cyberharassment is common on the internet.'):
}
```

Output:

```
Trolls are among us. Cyberharassment is common on the internet.
```

Since the condition between the parenthesis in the `if` statement is `true`, the code in between the curly brackets of the `if` statement was executed.

The `else` keyword is written after the closing curly bracket of the `if` statement. It is not followed by a set of parenthesis but by a set of curly brackets. The code within the curly brackets of the `else` statement will execute only when the statements before it are false. For example, in JavaScript:

```javascript
if (50 === 100){
    console.log('Trolls are among us. Cyberharassment is common on the internet.');
}else{
    console.log('Shamers are among us. They feel a need to gain power over others.');
}
```

Output:

```
Shamers are among us. They feel a need to gain power over others.
```
Since the condition between the parenthesis of the `if` statement is `false`, the code in between the curly brackets of the `else` statement was executed.

---

### Summary

In summary, functions are blocks of code that execute when call on. They can be helpful for making clean code and making it easier to make changes to code during future developments. Global variables can be accessed within a function because it has global scope while variables declared inside a function can only be accessed within the function it was declared on. When defining a function, you can also define parameters within the parenthesis of a function to receive values outside of the function. The `return` keyword can be used inside of a function to pass a value outside of the function. The JavaScript language has a set of operators that can be used to compare value. Finally, `if` and `else` keywords are used to execute code depending on certain conditions.