# What I learned in Week 5 at Code Immersives

### About

This readme file contains notes from concepts I learned in week 5 at [Code Immersives](https://www.codeimmersives.com) - The best total immersion programmer training in NYC. 

---

### Topics Covered

1. Flowcharts in programming logic
2. Conditional Statements Continuation
3. Switch Statement
4. Running Node Applications

---

### Flowcharts in Computer Programming Logic

* Flowcharts can be useful when programming computers to help explain logic flow.
* Flowcharts can be used to explain small components of an app such as a function or the big picture.
* **Circles** are used to indicate when there in an input or output occurring.
* **Diamonds** are used to indicate when a decision is occurring.
* **Boxes** are used to indicate if the decision was yes (`true`), no (`false`), or done.
* If you decide your done too early, your not going to hit every potential logical flow.

##### Flowchart **FizzBuzz** example

![](https://i.imgur.com/DLWtYBF.png)

---

### Conditional Statements Continuation

* When using the `if` and `else if` keywords the block of code within the curly brackets will execute only if the statement is `true`.
* The `else` statement will only execute if the statements before it are `false`.
* The && represents AND.
* The || represents OR.


##### Syntax example:
```javascript
if(/* condition 1 */ && /* condition 2 */){
    // Code to be executed if true here
}else if(/* condition 1 */ || /* condition 2*/){
    // Code to be executed if true here
}else{
    // Code to be executed if other conditions are false here
}
```

---

### Switch Statement

* Switch keyword is followed by parenthesis and curly brackets.
* Case keyword is followed by the potential value and a colon.
* After the case line, return keyword followed by value to return.
* After all cases have been written, default keyword following by a colon then a return.
* default keyword is like else keyword. It does not need a condition.
* Switch statement is good for when expecting a specific value.

##### Example:

```javascript
switch(num){
    case 1:
        return 'Sunday'
    case 2:
        return 'Monday'
    case 3:
        return 'Tuesday'
    case 4:
        return 'Wednesday'
    case 5:
        return 'Thursday'
    case 6:
        return 'Friday'
    case 7:
        return 'Saturday'
    default:
        return 'Wrong number, please enter a number between 1 and 7.'
}
```

---

### Running Node Applications

* Node applications can be ran on the command line interface.
* To run Node CLI apps, on the terminal type `node` followed by the filepath where the file is located.
* If the Node app is expecting arguments, typed them after the filename.
* When writing a node app, you can receive an input by using process.argv() function.
* You can create methods from function definitions that are located on a separate file with the require() function.