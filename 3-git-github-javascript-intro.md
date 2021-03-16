# What I Learned in Week 3 at Code Immersives

### About

In this README file I try to simply explain the concepts I learned in week 3 at Code Immersives.

---

### Topics Covered

1. Introduction to Git & GitHub
2. Steps for Creating a New Repository
3. Introduction to JavaScript
4. Linking JavaScript to a HTML file
5. Creating Variables in JavaScript
6. Math in JavaScript
7. Concatenating in JavaScript
8. Introduction to Jest

---

### Introduction to Git & GitHub

Version control systems, VCS, are used to help keep track of changes that are made to a project over a period of time. It is used by groups of people working on spreadsheets, word documents, photo editors, computer code, and more. 

*GIT* is one of many version control systems that is used in software development. With GIT, computer programmers can send a version of their code to Git servers. Once their code is on a Git server, with Git and GitHub other computer programmers can get a copy of that code. The action of sending code to the cloud is called **push** and the action of downloading a version of code from a server to a personal computer is called **clone**. *GitHub* is a web application that computer programmers use *to manage versions of their code on Git servers*.

Almost all computer programmers use a local computers command line interface to perform Git actions. This is because of how quick and easy it is to do compared when using a graphical user interface. To start a repository within a local machine, they must first perform the **git init** command within the directory they choose to work on within a computer. In example, on a terminal:

```shell
a-directory-name$ git init

Initialized empty Git repository in /Users/Documents/new-directory/.git/
```

With the git init command, a folder named .git will be created in the computers storage. This is the local repository. In software development, a **repository** is a storage location for storing files with computer code and the different versions of that code. 

It is important for computer programmers to track code changes that are made over a period of time. This is because when new features are added to the code, it is possible to come across issues that cause the code to not function properly or at all. Saving different versions of that code allows computer programmers to not only start from scratch but possibly even identify what went wrong when adding a new feature.

When a computer programmer wants to send new changes to their code to a Git server, the remote repository, they will first have to use the **git add** command. For example, on a terminal: 

```shell
a-directory-name$ git add main.js
```
> To see if the changes were added use the **git status** command.

This metaphorically adds the file with new changes in "a box". Once, the computer programmer is done adding files with changes to "the box" with the git add command, they need to use the **git commit** command to, metaphorically, package the file and "label it". For example, on a terminal:

```shell
a-directory-name$ git commit -m "Adds friends list"
```

Where **-m** gives them the ability to add a message - or "label".

The "git package", which is now in the .git folder that was created earlier with the git init command, is now ready to be moved to the Git server. To finally move the new changes, or send "the box", to the Git server, a computer programmer must use the **git push** command. Simply, on a terminal:

```shell
a-directory-name$ git push
```
> To see a log of all Git activity, use the **git log** command.

The new changes have been moved to the server. Every time a computer programmer wants to add changes to a Git server, they would repeat this process. 

With the code now on the Git server, other computer programmers have the ability to get a copy of that code. They can get a copy of the code by logging onto GitHub's web application and going onto the webpage with the repository of that code, then fork it. **Fork** is when a copy of code is made onto a Git account from another Git account. Once the forked version is on their account, they can clone the code onto their computer with the **git clone** command and the repositories URL. In example, on a terminal:

```shell
a-directory-name$ git clone https://github.com/timothynegron/make-variables-not-war
```

> Also with GitHub, computer programmers can compare previous versions of their code with the current and vice versa.

When the command above is entered, a copy will be made under the directory where the command was entered and the code can now be edited on that computer.

If a computer programmer is invited to **collaborate** on the project, they can use the **git pull** command to get the latest copy of any code that has been pushed to the git servers by other programmers working on the same code. In example, on a terminal:

```shell
a-directory-name$ git pull
```

If a programmers pushes changes to a file that a co-programmer was working on and then that co-programmer pulls the new changes, a **conflict** would occur. The co-programmer that pulled the code from the git server could then choose to **merge** both files, decline any changes, or accept the new changes and not keep the changes they've made. To avoid conflicts, programmers must communicate and plan out stages of development.


##### Here is a pictorial representation of the Git version control system: 

![alt Git revision control system](https://i.imgur.com/3pQlZ1L.png)


---

### Steps for Creating a New Repository

On a terminal:

1. Go to a directory you want to work from.
2. Enter the `git init command`.
3. Create any files you want. *Good time to create a `README.md`*
4. Enter the `git add command` and add the files.
5. Enter the `git commit -m "a message"` command and enter a good message.

Next, on a web browser:

1. Log into your GitHub account.
2. Create a new repository.

Finally, on a terminal within the same directory:

1. Enter `git branch -M main`
2. Enter `git remote add origin https://github.com/username/new_repo_name`
3. Enter `git push -u origin main`

---

### Introduction to JavaScript

JavaScript is a programming language that was originally designed to build interactive web pages. Later, it was made possible to run outside of a web browser with a technology called Node. Node gave developers the ability to program mobile applications, command-line tools, and more with JavaScript. Today, JavaScript is one of the most, if not the most, popular programming language.

---

### Linking JavaScript to a HTML file

To link a JavaScript, .js, file to a HTML file, .html, the following line of code needs to be within the `<body>` tag or the `<header>` tag of the .html file:

```html
<script src="script.js"></script>
```

In the quotes would be the name of the JavaScript file with the .js extension. In this case the name of the .js file is script.

---

### JavaScript Variable Types

With JavaScript, variable names can be created and each variable can be set with a value. The value can be of many different types. Here is a list of JavaScript variable types:

* **String:** an array of characters and symbols in quotations.
* **Number:** integer, decimals, negative numbers.
* **Boolean:** either a true or false value.
* **NaN:** not a number.
* **Null:** a value does not exist.
* **Undefined:** a variable that has not been set with a value.

---
### Creating Variables in JavaScript

Creating variables in JavaScript is more straight forward than other computer programming languages. To create a variable in JavaScript, you must use the `let` keyword before the name of the variable. The variable name cannot contain spaces. In example:

```javascript
let myFirstVariable = 1;
```
The line of JavaScript code above creates a variable with a type of number. Where the `let` keyword tells the computer to create a variable, `myFirstVariable` is the variable name, and `= 1` sets the value of the variable `myFirstVariable` to one *and tells the computer that the variable has a type of number*. 

Here is an example of creating a string variable type:

```javascript
let myFirstString = 'Hello World';
```

The single quotes before and after the text, *tells the computer that the variable has a type of String*.

Here is an example of creating a boolean variable:

```javascript
let myFirstBoolean = true;
```
True and false, without quotations, is a value and keyword in JavaScript that *tells the computer that the type of the variable is boolean*.

---
### Math in JavaScript

Math in JavaScript can be done with the following symbols as the basic math operators:

* Addition operator: +
* Subtraction operator: -
* Multiplication operator: \*
* Division operator: /

Here is an example in code:

```javascript
let sum = 4 * 4;

console.log(sum);
```

Output:

```javascript
16
```

---
### Concatenating in JavaScript

In JavaScript you can link, or concatenate, two String variables with the addition symbol. For example:

```javascript
let myFirstName = 'Timothy';
let myLastName = 'Negron';

let myFullName = myFirstName + ' ' + myLastName;

console.log(myFirstName);
```

Output:

```javascript
Timothy Negron
```

Where the value of `myFirstName`, the space in between the single quotes, and the value of `myLastName` is assigned to `myFullName`. The result is a **concatenation** of all three values.

---

### Introduction to Jest

*Jest* is a JavaScript unit testing tool that gives computer programmers instant feedback on the test they create for their code. **Unit Testing** is important in software development for ensuring that all components of a program is working properly. On a terminal, to start the Jest program, enter:

```shell
a-director$ jest --watch-all
```

> To install Jest, on a terminal enter: npm install --global jest

---

### Summary

To summarize, Git is a powerful version control system that helps software developers maintain a history of revisions that they make to their code. GitHub is a website that helps manage Git repositories. JavaScript is a computer programming language that was originally design to create interactive web applications and is now also used to create interactive mobile and desktop applications. Finally, Jest is a JavaScript unit testing tool that helps build stable computer applications.