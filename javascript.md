# JavaScript

[<- Go Back](README.md)

## Definition
> JavaScript often abbreviated as JS, is a `high-level`, `interpreted` programming language. It is a language which is also characterized as `dynamic`, >  `weakly typed`, `prototype-based` and `multi-paradigm`. 

> As a `multi-paradigm` language, JavaScript supports `event-driven`, `functional`, and `imperative (including object-oriented and prototype-based)` > programming styles.

> `Initially only implemented client-side in web browsers`, JavaScript engines `are now embedded in many other types of host software, including server-side in web servers and databases`, and in non-web programs such as word processors and PDF software, and in runtime environments that make > JavaScript available for writing mobile and desktop applications, including desktop widgets.

* This definition comes from [Wikipedia - JavaScript](https://en.wikipedia.org/wiki/JavaScript) document
* Over this course we'll try to figure out what this means and how it works
* By the end of the programing section we should be able to read this definition again and understand it

## JS History
* It's important to know this lenguage history to understand were it comes from and where it's going
* Read [auth0 - A brief history of JavaScript](https://auth0.com/blog/a-brief-history-of-javascript)
* Watch & Read [TXJS 2011 A6 – Brendan Eich – Ecma TC39: The Good, The Bad, and The Ugly.](https://brendaneich.com/2011/08/my-txjs-talk-twitter-remix)
* Watch [Tyler McGinnis - Computing Conversations with Brendan Eich](https://www.youtube.com/watch?v=IPxQ9kEaF8c)
* Watch [ECMAScript, TC39, and the History of JavaScript](https://www.youtube.com/watch?v=gytOcNFV1dM)
* Watch [How to fix the web | Brendan Eich | TEDxVienna](https://www.youtube.com/watch?v=zlcnOr81lPc)
* Watch [Brendan Eich on JavaScript at 17 - O'Reilly Fluent 2012](https://www.youtube.com/watch?v=Rj49rmc01Hs)
* Watch [ECMAScript Harmony: Rise of the Compilers - Brendan Eich keynote](https://www.youtube.com/watch?v=PlmsweSNhTw)

## JS Environments
* JavaScript now runs Client and Server side
* Using a Web Browser is one of the easiest way to execute JS Client side
* Using Node.js we can execute JS Server side
* JavaScript is no longer a scripting lenguage to create interactive browser animations

### Client Side - Browser
* Open Chrome
* Open Devtools
* Select the console tab inside Devtools

![Devtools](./resources/images/js/show_devtools.png)

* Write the following code and press enter to execute it:

```javascript
2 + 2
```

```js
console.log(2 + 2);
```

![Devtools](./resources/images/js/devtools.png)

* Now run the following code:

```javascript
console.log('Congrats!!!, you just ran your firs JS code');
```

### Node.js - Server Side

* [Node.js®](https://nodejs.org/) is a JavaScript runtime built on Chrome's V8 JavaScript engine. Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient. Node.js' package ecosystem, npm, is the largest ecosystem of open source libraries in the world.
* It was created by [Ryan Dahl](https://wikipedia.org/wiki/Node.js) in 2009
* We'll use Node.js from now on to learn the lenguage and run our JavaScript exercises
* Once we know the lenguage core concepts we'll learn about the Browsers API's
* [Download & install Node.js](https://nodejs.org/en/download/)
* [Install Node.js & npm Windows](http://blog.teamtreehouse.com/install-node-js-npm-windows)

* After installing Node.js open a terminar window and run the following command:

```bash
node --version
v8.11.11
```

* Also check that you have npm installed too:

```bash
npm --version
5.6.0
```

* Now that we know that we have installed Node.js & npm we can use it
* Execute the following command:

```bash
node
>
```

* It looks like nothing happened but in reality we are executing Node.js JavaScript console
* The **>** symbol means that we opened the Node.js console and it's wating for us to input JS code
* Now we can write JS code and execute it the same way we did using the browser
* This console is called `REPL("Read-Eval-Print-Loop")`

### Using Node.js REPL
* Open your terminal
* Execute de `node` command
* Write the following sentence once you see the **>** symbol:

```javascript
2 + 2
```
* Press the enter key to see the following result:

```javascript
> 2+2
4
>
```

* Press CTRL + C to quit
* You'll see the following message:

```bash
(To exit, press ^C again or type .exit)
```

* So you need to press CTRL + C twice to exit
* In this exercise we added two numbers and Node.js output the result
* It's nice to be able to try code using Node.js console but for longer programs it's better to use a JS files
* To execute a JS program we'll use the node command and the name of the file that we want to execute

```bash
node program.js
```

* Once we execute this command Node.js will read and interpretate our JS code
* We use the `.js` extension for our JavaScript code

### Using a Node.js file
* Create a folder with the name `js`
* Create a new file `index.js` inside the js folder
* Write the following code into the index.js file

```javascript
2 + 2
```

* Open the console and change directory to the `js` folder
* Execute the program using the node command:

```bash
node index.js
```

* Check out the output!!
* Don't worry if you don't see an output, Node.js executes our code but it's only adding both values together
* To show the result as output we need to use the `console.log()` object and method
* The `log()` method accepts any value to show as output
* Now add `console.log` and execute the program again

```js
console.log(2 + 2);
```

```bash
node progama.js
```

* Now we see the expected output!!!

### Conclusion
* Browser and Node.js internaly use the V8 JavaScript engine to run JavaScript code
* We can use the Browser or Node.js console to try out JavaScript code
* V8 is maintained by Google
* We'll use browser to run JavaScript client side and Node.js for Server side

## Variables declaration & assignment operator

## Variables declaration

* Many times when coding we need to store a value to interact with it
* This value is stored in our computer memory
* As this values might change over time we'll call `variables` to this memory positions
* We can assign variables `name` to identify them
* It's a good practice to use descriptive names to define our variables
* If we use names like a, b, foo they don't add any context about what we're coding
* We can then define that a variables are named memory positions where we can assign different values and override them in case we need to

### ES5
* To define a variable in JavaScript we just need a variable name
* The variable statement **var** declares a variable, optionally initializing it to a value
* Also end each statement with a `;`
* [MDN var doc](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var)

**Example:**
```js
var variableName;
```

* For example we can define a name and age variables to use in our program

**Example:**
```js
var name;
var age;
```

* Not using **var** it's a bad coding practice
* To avoid  unexpected errors use var to declare your variables
* Variable names must start with a letter
* Use descriptive variable names
* In JavaScript it's common to use camel case to define variable names
* In camel case the first word is writen in lower case and the rest of the words start with a capitalize letter

**Example:**
```js
var healthInsuranceNumber;
```

#### Practice
[Exercise 1](./exercises/js/ex_1.md)

## Assignment operator
* Once we defined a variable name we can assign a value
* As we have a memory space reserved we can store a value 
* The **=** assigns a value from right to left

**Example:**
```js
var name;
name = 'Pablo';
```

* We can define all the variables first and then assign the values:

**Example:**
```js
var name;
var age;
name = 'Pablo';
age = 20;
```

#### Practice
[Exercise 2](./exercises/js/ex_2.md)

* Also we can declare all variables using a single line:

**Example:**
```js
var name, age;
name = 'Pablo';
age = 20;
```

#### Practice
[Exercise 3](./exercises/js/ex_3.md)

* We can declare a variable and assign a value in the same line:
* Multiple assignment doesn't work in JavaScript (only one variable and one value)

**Example:**
```js
var name = 'Pablo';
var age = 20;
```

#### Practice
[Exercise 4](./exercises/js/ex_4.md)

* Using `console.log()` we can output the variable value

**Example: index.js (filename)**
```js
var name = 'Pablo';
var age = 20;
console.log(name);
console.log(age);
```

**Execute the program using node.js:**
```bash
node index.js
```

#### Practice
[Exercise 5](./exercises/js/ex_5.md)

* After executing the program we should see pablo & 20 as output
* `console.log()` accepts multiple values comma separated 
* We can show a message and the variable value

**Example: index.js (filename)**
```js
var name = 'Pablo';
var age = 20;
console.log('name: ', name);
console.log('age: ', age);
```

**Execute the program using node.js:**
```bash
node index.js
```

* Now our output looks like: **name: Pablo** y **age: 20**
* This is an easy way to debug our variable values

#### Practice
[Exercise 6](./exercises/js/ex_6.md)

### ES6
* In the lenguage new version we can use **let** to define variables
* This statement declares a **block scope local variable**, optionally initializing it to a value
* Using **let** will help us scope our variables in a better way
* [MDN let doc](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)

**Example:**
```js
let variable = value;
```

#### Practice
[Exercise 7](./exercises/js/ex_7.md)

* When the value of a variable is always the same we can define it as a **constant**
* In ES6 we can declare constants using the reserved word **const** 

**Example:**
```js
const constantVariable = value;
```

#### Practice
[Exercise 8](./exercises/js/ex_8.md)

* We'll get an error if we try to change a constant value

**Example:**
```js
const constantVariable = value;
constantVariable = otherValue;
// TypeError: Assignment to constant variable.
```

#### Practice
[Exercise 9](./exercises/js/ex_9.md)


### var vs let & const
* [Medium - Eric Elliot - JavaScript ES6 var, let or const](https://medium.com/javascript-scene/javascript-es6-var-let-or-const-ba58b8dcde75)
* [StackOverflow - Difference between using let and var](https://stackoverflow.com/questions/762011/whats-the-difference-between-using-let-and-var-to-declare-a-variable-in-jav)
* [JS Tips - Keyword var vs let](http://www.jstips.co/en/javascript/keyword-var-vs-let)

## Data types
* In JavaScript we can use different types of value to represent different things

**Example:**
```js
var name = 'Pablo';
var age = 20;

console.log('name: ', name);
console.log('age: ', age);
```

* In this example we use different types of values:
  * For the name variable we use a value between quotes
  * For age we use a number

* JavaScript has the following different base types that we can use:
  * **string:** this type is used to represent textual data
  * **number:** there is only one number type the `double-precision 64-bit binary format IEEE 754 value`. There is no specific type for integers. In addition to being able to represent floating-point numbers, the number type has three symbolic values: +Infinity, -Infinity, and NaN (not-a-number)
  * **boolean:** represents a logical entity and can have two values: `true or false`
  * **undefined:** A variable that has not been assigned a value has the value `undefined`.
  * **null:** this type has exactly one value: `null`. It represents the intentional absence of any object value

* As programers it's going to be our responsability to choose the right data type for each variable depending the type of value that we need
* The operations that we'll be able to do are going to be related to the data type we choose
* In JavaScript exists many more different types of values and also we can create our own but this are the primitive one
* A primitive (primitive value, primitive data type) is data that is not an object and has no methods
* [MDN primitive doc](https://developer.mozilla.org/en-US/docs/Glossary/Primitive)
* [MDN data structures doc](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures)

### String
* String represente a text value, we can use them for names, last name, address, etc
* String values are inclosed between single or double quotes
* By default we use single quotes for strings but there're some special cases
* [MDN string doc](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

**Example:**
```js
let firstname = 'Juan';
let lastname = "Perez";

console.log(firstname);
console.log(lastname);
```

* In this example we defined two variables (first and lastname) and assigned a string value ('Juan', 'Perez')
* Also we can use this type of value for messages

**Example:**
```js
let message = 'Wellcome to JavaScript!!!';
console.log(message);
```

* We can use primitives without having them assigned to a variable

**Example:**
```js
console.log('Wellcome to JavaScript!!!');
```

* In this example we use a literal **string** as `console.log()` parameter

#### Practice
[Exercise 10](./exercises/js/ex_10.md)

[Exercise 11](./exercises/js/ex_11.md)

### String concatenation
* The `+` operator allows us to concat two or more strings together

**Example:**
```js
let name = 'Juan';
let space = ' ';
let lastname = 'Perez';

console.log(name + space + lastname);
```

* In this example we concat all values using the `+` operator
* We might not need to use a variable for the space and we can use a string literal instead

**Example:**
```js
let name = 'Juan';
let lastname = 'Perez';

console.log(name + ' ' + lastname);
```

* In this example we see how to use a literal value without being assigned to a variable

#### Practice
[Exercise 12](./exercises/js/ex_12.md)

[Exercise 13](./exercises/js/ex_13.md)

[Exercise 14](./exercises/js/ex_14.md)

### Template literals
* In ES6 we have `template literals` that will help us write better string templates
* To write a template literal we use **``** (back-tick)
* Then we use the following syntax to add template values `${variable}`
* Once the code gets executed the JavaScript engine will replace the variable value inside the string one
* Take a look at the following example to better understand this concept
* [MDN template literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)

**Example:**
```js
var name = 'Pedro';
var template = `Wellcome ${name} to this great site`

console.log(template);
```

* In this example we defined a name variable and assigned the Pedro value
* Then we create a template variable with a message and the name variable
* Once we execute this code we'll get Wellcome `Pedro` to this great site
* We can add all the variables that we need to a template
* Also templates are multiline

**Example:**
```js
let mom = 'Marta';
let dad = 'Martín';
let template = `My mother name is ${mom} & my dad name is ${dad}`;

console.log(template);
```

* We'll get as result: My mother name is Marta & my dad name is Martín
* Using string concatenation we can get the same result

**Example:**
```js
let mom = 'Marta';
let dad = 'Martín';
let message = 'My mother name is ' + mom + ' & my dad name is ' + dad;

console.log(message);
```

* We can get the same result using templates or string concat
* Using templates looks like an easier way to do it!!

#### Practice
[Exercise 15](./exercises/js/ex_15.md)

[Exercise 16](./exercises/js/ex_16.md)

[Exercise 17](./exercises/js/ex_17.md)

### Single or double quotes
* In JavaScript we can choose between single or double quotes
* There're some cases where we need to use one or the other

**Example:**
```js
let text = 'text using "double quotes"';
let otherText = "text using 'simple quotes'";

console.log(text);
console.log(otherText);
```

* In this case single or double quotes are part of the value
* When using quotes as part of the value we have to choose between scaping the quotes or just using the quote type that it's not part of the content:
  * Use double quotes if the text has single quote content
  * Use singe quotes if the text has double quote content

#### Practice
[Exercise 18](./exercises/js/ex_18.md)

[Exercise 19](./exercises/js/ex_19.md)

### Numbers
* JavaScript also supports number type
* This type of value doesn't use quotes

**Example:**
```js
let age = 38;
let capacity = 50;

console.log(age);
console.log(capacity);
```

#### Practice
[Exercise 20](./exercises/js/ex_20.md)

[Exercise 21](./exercises/js/ex_21.md)

* A common mistake it's to code numbers as string

**Example:**
```js
let age = 38;
let capacity = "50";
```

> In this example we have two variables that it looks like we are assigning numbers values
> Age has a number type and capacity has a string value with the representation of a number
> Having different types allows us to do different types of operations, for example we can add, substract numbers but not strings

* We'll talk about doing math using number types values

### Boolean
* This type of value only accepts `true or false` as value

**Example:**
```js
let on = true;
let voted = false;
let married = false;

console.log(on);
console.log(voted);
console.log(married);
```

#### Practice
[Exercise 22](./exercises/js/ex_22.md)

### Undefined
* A variable that has not been assigned a value is of type **undefined**
* A method or statement also returns undefined if the variable that is being evaluated does not have an assigned value
* A function returns undefined if a value was not returned
* Also we can assign it as variable value

**Example:**
```js
let variableWithoutDefinition = undefined;

console.log(variableWithoutDefinition);
```

* We might need to assign **undefined** in some special cases

#### Practice
[Exercise 23](./exercises/js/ex_23.md)

### Null
* In JavaScript we also have a **null** value
* We can assign a variable a null value

**Example:**
```js
let nullVariable = null;

console.log(nullVariable);
```

#### Practice
[Exercise 24](./exercises/js/ex_24.md)

* At the begining **null** & **undefined** looks similar but they don't
* We can assign a null value and know that the variable has been defined but it has a null value

### typeof
* The **typeof** operator returns a string indicating the type of the unevaluated operand

**Example:**
```js
let name = 'Marta';
let age = 30;
let married = false;
let undefinedVar = undefined;
let nullVar = null;

console.log(typeof name); // string
console.log(typeof age); // number
console.log(typeof married); // boolean
console.log(typeof undefinedVar); // undefined
console.log(typeof nullVar); // object
```

* In this example we can see that typeof will return different values for different data types
* For **null** it will return object and that is something unexpected
* Object is a different type of JavaScript data value and we'll talk more about it in a different section

#### Practice
[Exercise 25](./exercises/js/ex_25.md)

[Exercise 26](./exercises/js/ex_26.md)

## Arithmetic operators
* Arithmetic operators take numerical values (either literals or variables) as their operands and return a single numerical value
* The standard arithmetic operators are `addition (+), subtraction (-), multiplication (*), & division (/)`

### Addition
* The addition operator **(+)** produces the sum of numeric operands or string concatenation

**Example:**
```js
2 + 2
```

* In this example we add to literal numbers

**Example:**
```js
const myAge = 20;
const myBrotherAge = 15;

console.log(myAge + myBrotherAge);
```

* We can add two or more values using variables

**Example:**
```js
const myAge = 20;
const myBrotherAge = 15;
const result = myAge + myBrotherAge;

console.log(result);
```

* In this example we store the result of adding two values into the result variable

**Example:**
```js
const myAge = 20;
const myBrotherAge = 15;
const result = myAge + myBrotherAge;

console.log(result + 2);
```

* Also we can add variables values and literal numbers too

### Subtraction
* The subtraction operator **(-)** subtracts the two number operands, producing their difference

**Example:**
```js
2 - 2; // We get 0 as result

const myAge = 20;
const myBrotherAge = 15;

// We show the difference between myAge and myBrotherAge
console.log(myAge - myBrotherAge);

// Also we can use a variable to store the subtraction result
const result = myAge - myBrotherAge;

console.log(result);
```

* Also we can combine operations

**Example:**
```js
10 + 2 - 2; 

const myAge = 20;
const myBrotherAge = 15;

// Use variables, literal number and different arithmetic operators
console.log(myAge - myBrotherAge + 10);

const result = myAge - myBrotherAge + 10;

console.log('Result: ' + result);
```

### Multiplication
* The multiplication operator **(*)** produces the product of the operands

**Example:**
```js
2 * 2; // Returns 4 as result

const firstNumber = 10;
const secondNumber = 5;

console.log(firstNumber * secondNumber);

const result = firstNumber * secondNumber;

console.log(result);
```

* In some cases we can use grouping **(operation)** to let the engine know that it need to resolve this operation first
* Read the [MND operator precedence doc](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence) to know more about this subject

**Example:**
```js
2 + 2 * 4; // 10
(2 + 2) * 4; // 16
```

* In the first example it will multiply 2 times 4 and then add 2 to the result
* In the second example as we are grouping 2 plus 2 it will resolve this operation first and then multiply by 4
* This concept works with variables too

**Example:**
```js
const two = 2;
const four = 4;

console.log(two + two * four); // 10
console.log( (two + two) * four ); // 16
```

### Division 
* The division operator **(/)** produces the quotient of its operands where the left operand is the dividend and the right operand is the divisor

**Example:**
```js
20 / 2; // 10

const firstNumber = 20;
const secondNumber = 2;

console.log(firstNumber / secondNumber); // 10

const result = firstNumber / secondNumber;

console.log(result); // 10
```

* With code we can have the same problem that we can have in math when we divide by 0
* JavaScript has a especial number type called **Infinity**
* We get **Infinity** if we try to divide by 0
* [MDN Infinity doc](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Infinity)

### Remainder
* The remainder operator **(%)** returns the remainder left over when one operand is divided by a second operand

**Example:**
```js
20 % 2; // 0

const firstNumber = 20;
const secondNumber = 2;

console.log(firstNumber % secondNumber); // 0

const result = firstNumber % secondNumber;

console.log(result); // 0
```

* We can use this operator to find out if a number is even or odd
[Freecodecamp - Finding a remainder in JavaScript](https://www.freecodecamp.org/challenges/finding-a-remainder-in-javascript)

#### Practice
[Exercise 27](./exercises/js/ex_27.md)

[Exercise 28](./exercises/js/ex_28.md)

[Exercise 29](./exercises/js/ex_29.md)

[Exercise 30](./exercises/js/ex_30.md)

[Exercise 31](./exercises/js/ex_31.md)

[Exercise 32](./exercises/js/ex_32.md)

### Increment & Decrement
* Using the increment and decrement operators we can do addition and substraction by one really easy

#### Increment
* The increment operator **++** increments (adds one to) its operand and returns a value
* If used postfix, with operator after operand (for example, x++), then it returns the value before incrementing
 
**Example:**
```js
let number = 0;

number++;

console.log(number); // 1
```

* If used prefix with operator before operand (for example, ++x), then it returns the value after incrementing

**Example:**
```js
let number = 0;

++number;

console.log(number); // 1
```

* In this case we can use the operator before or after but there might be cases when we need to use one or the other depending if we're using the incremented result or not

#### Decrement
* The decrement operator **--** decrements (subtracts one from) its operand and returns a value
* If used postfix (for example, x--), then it returns the value before decrementing
* If used prefix (for example, --x), then it returns the value after decrementing

**Example:**
```js
let number = 10;

--number;

console.log(number); // 9

number--;

console.log(number); // 8
```

#### Assignment operators
* We can assigna a number to a variable
* Then use this variable to do any arithmetic operation
* Also we can re use the variable to assign the result of the arithmetic operation
* Take a look at the following example:

**Example:**
```js
let number = 1;
number = number + 1
```

* In this example we increment the value of the number variable by one
* We already saw that we can use the increment operator **++** to do this

**Example:**
```js
let number = 1;

number++;
```

* We see in this examples that we increment and assign the result to the variable
* The increment and decrement operators are great but we can only add or substract by one
* We can use different assignment operators to do this task for different operations
* Assignment operators:
  * `+=` Addition assignment
  * `-=` Subtraction assignment
  * `*=` Multiplication assignment
  * `/=` Division assignment
  * `%=` Remainder assignment
* This concept is easier to undestand using code:

**Example:**
```js
let number = 1;

number += 1;

console.log(number); // 2
```

**Example:**
```js
let number = 1;

number = number + 10;

console.log(number); // 11
```

* Using the addition assignment we can do the same operation much easier:

**Example:**
```js
let number = 1;

number += 10;

console.log(number); // 11
```

* We can add 10 to the current number variable value using the addition assignmet operator `+=`
* Then we can use any of the other assignmet operators

**Example:**
```js
let number = 10;

number -= 2;

console.log(number); // 8
```

**Example:**
```js
let number = 10;

number *= 2;

console.log(number); // 20
```

**Example:**
```js
let number = 20;

number /= 2;

console.log(number); // 10
```

**Example:**
```js
let number = 20;

number %= 2;

console.log(number); // 0
```

* The concept is always the same but it only changes the operation that we do over the given variable
* You can learn more about assignment operators on [MDN site](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Assignment_Operators)

#### Practice
[Exercise 33](./exercises/js/ex_33.md)

## Comparison operators

### Equality operators
* We can compare two values using the equality operators **==**
* Using the equality operators we get a **boolean** value as result (true or false)
* This type of equality only compares values by value
* For example using this operator we can compare a number value and string value with a number
* If both values are equals we get **true** as result
* In case they are not the same value we'll get **false** as result

**Example:**
```js
let firstNumber = 20;
let secondNumber = 20;
let thirdNumber = 10;

console.log(firstNumber == secondNumber); // true
console.log(firstNumber == thirdNumber); // false
```

* As we only compare by value:

**Ejemplo:**
```js
console.log(10 == '10'); // This is true even having different values type
```

* Also we can know if the values are differen using the inequality operator **!=**

**Example:**
```js
let firstNumber = 20;
let secondNumber = 20;
let thirdNumber = 10;

console.log(firstNumber != secondNumber); // false
console.log(firstNumber != thirdNumber); // true
```

* Other way to compare values is to know if a value is greater than the other
* The greater than operator **>** returns true if the left operand is greater than the right operand

**Example:**
```js
let firstNumber = 20;
let secondNumber = 10;

console.log(firstNumber > secondNumber); // true

console.log(secondNumber > firstNumber); // false
```

* Also we can compare values by using the less than operator
* The less than operator **<** returns true if the left operand is less than the right operand

**Example:**
```js
let firstNumber = 20;
let secondNumber = 10;

console.log(secondNumber < firstNumber); // true

console.log(firstNumber < secondNumber); // false
```

* We can use the greater than or equal operator 
* The greater than or equal operator >= returns true if the left operand is greater than or equal to the right operand

**Example:**
```js
let firstNumber = 20;
let secondNumber = 10;
let thirdNumber = 20;

console.log(firstNumber >= secondNumber); // true

console.log(firstNumber >= thirdNumber); // true
```

* We can do the same using less than or equal
* The less than or equal operator **<=** returns true if the left operand is less than or equal to the right operand

**Example:**
```js
let firstNumber = 20;
let secondNumber = 10;
let thirdNumber = 10;

console.log(secondNumber <= firstNumber); // true
console.log(secondNumber <= thirdNumber); // true
```

### Strict Equality Comparison 
* The strict equality operators **===** and **!==** use the Strict Equality Comparison Algorithm and are intended for performing equality comparisons on operands of the **same type**

**Example:**
```js
console.log(10 === '10'); // false

console.log(10 !== '10'); // true
```

* Read more about the [comparison operators on MDN site](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators)

#### Practice
[Exercise 34](./exercises/js/ex_34.md)

[Exercise 35](./exercises/js/ex_35.md)

## Logical Operators
* Logical operators are typically used with Boolean (logical) values
* When they are, they return a **Boolean** value
* We can use the **&&** **and operator** to know if both expressions are true
* We can know if the user age is grater than 18 and the password is equal to other value
* In this case we'll get a true value if both expressions are true
* If one of the expressions is **false**, we get false as value too

**Example:**
```js
let age = 20;
let password = 'js1234';
let result = (edad >= 18 && password ==='js1234');
console.log('Result: ', result); // We get true as both expressions are true
```

* In this example we get **true** as both expressions are **true**
* We also have the **&&** **or operator** to check if at least one of the expressions is true
* Using this operator we only need one of the expressions to be true
* If the first expression is true the following one is not evaluated
* If the first expression is false then the following one is evaluated 
* At least one of the expressions needs to be true to get a true value 
* If not we'll get false as result

**Example:**
```js
let age = 20;
let password = 'js12345';
let result = age >= 18 || password ==='js1234';
console.log('Result: ', result); // true
```

* In this case the condition is **true** as the user age is greater than 18 (first expression)
* It doesn't matter if the password is the same or not as the previous expression is true

**Example:**
```js
let age = 10;
let password = 'js1234';
let result = age >= 18 || password ==='js1234';
console.log('Result: ', result); // true
```

* In this case the condition is **true** as the password is correct
* It doesn't matter if the age it's not greated than 18

**Example:**
```js
let age = 10;
let password = 'js12345';
let result = age >= 18 || password ==='js1234';
console.log('Result: ', result); // false
```

* In this case we get **false** as both expressions are false
* [MDN logical operators doc](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_Operators)

## Negation
* Using the not operator **!** we can negate a condition
* If we have a **true** value and we use the not operator we get **false**
* If we have a **false** value and we use the not operator we get **true**

**Example:**
```js
console.log(!true); // false
console.log(!false); // true
```

* We can use the not operator like this: 

**Example:**
```js
let age = 21;
let result = age < 18; 

console.log('User age greater than 18?: ', !result);
```

* The age condition is **false** but as we use the not operator it will be **true**

#### Practice
[Exercise 36](./exercises/js/ex_36.md)

[Exercise 37](./exercises/js/ex_37.md)

## String special characters
* Existen caracteres especiales en los **strings** que agregan un valor extra
* \n  New Line
* \t  Tab
* \r  Carriage back

**Example:**
```js
let message = 'Multiline \n text';

console.log(message); // two lines text

message = '\t \t tab text';

console.log(message); // tab text
```

* Special characters scape:
* \'  Single quote
* \"  Double quote
* \\  Backslash

**Example:**
```js
let message = 'scaping backslash \\ as string content';
console.log(message); // we show \ as string content

message = 'I love to have coffee at Gianu\'s';

console.log(message);

message = "Jets are \"the\" best NHL team";

console.log(message);
```

#### Practice
* Open a browser console and try all the examples to see the output

## String object property and method

### Length
* The **length** property of a **String object** indicates the length of a string
* This property returns the **number** of code units in the string

**Example:**
```js
const text = 'Wellcome to JavaScript!!';
const characterCount = text.length;

console.log(characterCount); // 24
```

**Example:**
```js
const text = 'Wellcome to JavaScript!!';

console.log(text.length);
```

**Example:**
```js
console.log('Wellcome to JavaScript!!'.length);
```

* Strings has a length property that allows us to know the string value length (characters)
* We can use it with string literals
* Also using a string stored in a variable
* Finally we can store the length in a variable too in case we need it
* [MDN length doc](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/length)

#### Practice
[Exercise 38](./exercises/js/ex_38.md)

[Exercise 39](./exercises/js/ex_39.md)

### String methods
* Object methods will allow us to have some functionality for different data types
* In this section we'll explore the String object methods
* JavaScript transform string literals into String objects when calling a method
* [MDN String methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

* Este método retorna un nuevo string con el texto concatenado

**Example:**
```js
const stringVariable = 'string value';

// We can call String methods when we have a string value type. 
// To call the method use a dot before the method name
// After the method name we add () to execute it
stringVariable.method();

// Also we can pass values to the method and they are called parameters
stringVariable.method(methodParameter);

// A method might accept more than one parameter and will depend on the method contract
stringVariable.method(methodParameter, otherMethodParameter);
```

## Concat
* Using the **+** operator we can concat string values
* String object has a **concat** method to do the same using methods instead of operators
* [MDN concat doc](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/concat)

**Example:**
```js
const text = 'My mom name is ';
const name = 'Marta';

// We get one string back as result with both strings concatenated
const message = text.concat(name);

console.log(message); // My mom name is Marta

console.log(text); // My mom name is

console.log(name); // Marta
```

* Some methos might change the object value
* In this case concat only returns a new string without changing the original values
* The concat method also accepts multiple parameters

**Example:**
```js
let text = 'Java';

console.log(text.concat('Script', ' is the best', ' Programming language!!'));
```
* The concat method will return the following string: **JavaScript is the best Programming language!!**
* In this example we used concat with many parameters using literal strings
* We can also use variables

#### Practice
[Exercise 40](./exercises/js/ex_40.md)

### Upper and lower case
* Using the **toUpperCase** & **toLowerCase** we can transform our text to upper and lower case

**Example:**
```js
const upperCaseText = 'HELLO';
const lowerCaseText = 'friends';

console.log(upperCaseText.toLowerCase()); // hello
console.log(lowerCaseText.toUpperCase()); // FRIENDS

console.log(upperCaseText); // HELLO
console.log(lowerCaseText); // friends
```

#### Practice
[Exercise 41](./exercises/js/ex_41.md)

[Exercise 42](./exercises/js/ex_42.md)

### String characters position
* The **charAt** method returns the character at the specified index
* This method accepts a number parameter to specify the index position
* Index in JavaScript starts in 0
* The first character will be at the 0 index position

**Example:**
```js
const text = 'JavaScript rocks!! right?';
const firstCharacter = text.charAt(0); 

console.log(firstCharacter); // J

console.log(text..charAt(0)); // J
```

* To know the last string character we can combine charAt and the length property
* As length will return the amount of characters and the index starts at 0 to know the last character we need to substract one from the length value

**Example:**
```js
const text = 'JavaScript rocks!! right?';
const lastCharacterPosition = text.length - 1;
const lastCharacter = text.charAt(lastCharacterPosition);

console.log(lastCharacter); // ?

console.log( text.charAt(text.length - 1) ); // ?
```

#### Practice
[Exercise 43](./exercises/js/ex_43.md)

[Exercise 44](./exercises/js/ex_44.md)


### String slice
* The **slice** method extracts a section of a string and returns it as a new string
* This method accepts two parameter slice(start, end)
* Use 0 index for the begining of the text
* The end parameter is optional and if we don't pass any value it will return the rest of the text

**Example:**
```js
const text = 'I <3 JavaScript!!';
const result = text.slice(4, 15);

console.log(result); // JavaScript
```

* Counting from the begining we have 4 index before the **J** letter
* Then we slice the string until the 15 index
* The final result is the JavaScript word
* Also we can avoid passing the second slice parameter and get the rest of the text from a starting point until the end

**Example:**
```js
const text = 'I <3 JavaScript!!';
const result = text.slice(4);

console.log(result); // JavaScript!!
```

* The end parameter can be a negative value
* When using negative values it will position at the end of the string and start counting backwards

**Example:**
```js
const text = 'JavaScript and Java are not the same';
const result = text.slice(0, -25); // JavaScript

console.log(result);
```

#### Practice
[Exercise 45](./exercises/js/ex_45.md)

* The **substr** method returns the part of a string between the start index and a number of characters after it
* We can also use 2 parameters (start and end)
* First parameter is the substring start
* Second parameter is the characters length

**Example:**
```js
const text = 'I love JavaScript!!';
const result = text.substr(7, 10);

console.log(result); // JavaScript
```

**Example:**
```js
const text = 'I love JavaScript!!';
const jsText = 'JavaScript';
const result = text.substr(7, jsText.length);

console.log(result); // JavaScript
```

#### Practice
[Exercise 46](./exercises/js/ex_46.md)

* You can learn more about [slice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/slice) and [substr](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/substr) reading the MDN guides

### String split
* The **split** method splits a String object into an array of strings by separating the string into substrings, using a specified separator string to determine where to make each split
* The first method parameter will be the separator value to split the string by
* We'll get an **array** object as result
* For now think about **array** as a list or collection of elements (in this case strings)
* Learn more about the [split](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split) method on the MDN guide

**Example:**
```js
let friends = 'tute, mati, pepe, raul, juan, marta, agus, loli';
let friendsArray = friends.split(',');

console.log(friendsArray);
/* 
[ 
  'tute',
  ' mati',
  ' pepe',
  ' raul',
  ' juan',
  ' marta',
  ' agus',
  ' loli' 
]
*/
```

#### Practice
[Exercise 47](./exercises/js/ex_47.md)

* String object has a lot of methods that we can use
* Read about them on the [MDN string guide -  methods section](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)
* Read about:
  * String.prototype.includes()
  * String.prototype.indexOf()
  * String.prototype.repeat()
  * String.prototype.replace()
  * String.prototype.trim()
  * And more
* Try using this methods on your own code!! `it will be 'fun'.toUpperCase()`
* We don't need to remember all methods, just know that they exist and what they can do for us :)

