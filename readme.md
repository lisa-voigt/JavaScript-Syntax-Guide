
# Java Script Syntax Guide by: Lisa Voigt

![alt text](lola.png)

### Brace yourself for a Syntax guide themed on my loyal dog, Lola. :dog:

## Variables

Variables store and manage data in your code and they can be declared in 4 ways: 
1. Automatically
2. Using var
3. Using let
4. Using const

All JavaScript variables must be identified with unique names. Here are the general rules for constructing names for variables:

- Names can contain letters, digits, underscores, and dollar signs.
- Names must begin with a letter.
- Names can also begin with $ and _.
- Names are case sensitive.
- Reserved words cannot be used as names.

Creating a variable in JavaScript is called declaring a value. This is how you declare values:

```
let a = 11;
let name = 'Lola';
let lastName = 'Voigt';
let fullName = 'name' + ' ' + 'lastName';
```

You can declare many variable in one statement by separating them with a comma. Here's an example:

```
let dog = "Lola", breed = "Husky", age = 11;
```

## Comparison Statements

A comparison statement evaluates an expression to determine whether it is true or false by using comparison operators:

| Operator 	| Name                                 	|
|----------	|--------------------------------------	|
| ==       	| Equal to                             	|
| ===      	| Equal value and equal type           	|
| !=        | Not equal                             |
| !==       | Not equal value or not equal type     |
| >         | Greater than                          |
| <         | Less than                             |
| >=        | Greater than or equal to              |
| <=        | Less than or equal to                 |


Comparison operators can be used in conditional statements to compare values and take action depending on the result. Like this:

```
if (dogAge > 10) text = "Officially a senior dog, requires many treats";
```

Let's try to guess Lola's age using (x == 11) as a comparison statement in an if/else statement:

```
let x = 11;

if (x == 11) {
  alert("That's right!");
} else {
  alert("That's wrong.");
}
```

Here we will use a comparison statement (lolaAge < amosAge) to compare Lola's age to her friends (Amos) age. 

```
let lolaAge = 11;
let amosAge = 5;

if (lolaAge < amosAge) {
  alert('Wrong. Lola is older than Amos.')
} else {
  alert('Yes! But she looks very young for her age.')
}
```

![alt text](lola_amos.png)

## Boolean Statements

A JavaScript Boolean represents one of two values: **TRUE or FALSE** . 

Here's a simple example of a boolean statement:

```
let lolaAge = 11;
let amosAge = 5;
let isLolaOlder = lolaAge > amosAge;

```

Boolean statements are used to test conditions, make decisions, and control the flow of a program and they are created using comparison operators. Boolean statements are at the heart of comparison stataments.


In conditional statements, a Boolean statement is tested, and the associated code block is executed if the statement evaluates to true. 

The basic syntax of an if statement is as follows:

```
if (condition) {
  // Code to be executed if the condition is true
}
```

Let's see an example trying to guess Lola's most dominant breed type: 

```
let lolaBreed = 'Husky';

if (lolaBreed == 'Husky') {
  alert('Yes! She's a husky mix.')
} else {
  alert('Nope, try again.')
}
```

## Arrays

An array is a special variable that can hold more than one value.

This is an array [1, 2, 3]
So is this ["one", "two", "three"]

```
let lolasFaveTreats = ["Bacon", "Salmon", "Liver"];
```

Indexing an array allows you to acces accurately in your code. We Index an array like this:

```
lolasFaveTreats[1] // Starts at 0, then 1, 2, 3. This represents 'Salmon'. 
lolasFaveTreats[0] // This represents 'Bacon'.
```

The length property returns the length of an array:

```
<p id="demo"></p>

<script>
let treats = ["Bacon", "Salmon", "Liver", "Cheese", "Steak"];
let totalTreats = treats.length;
document.getElementById("demo").innerHTML = totalTreats;
</script>
```

## Objects

Objects can contain many values. They can represent complex data structure, entities or models in your code, making them a key element of the language. 

Objects are dynamic in nature - you can add, modify or remove properties and methods at any time. 

This code assigns many values to a variable named dogOfTheYear:

```
let dogOfTheYear = {
    dogName: 'Lola',
    nickName: 'Lulu',
    breed: 'Husky',
    age: 11,
    faveTreat: 'Bacon',
};
```

This could also be represented like this:

```
let dogOfTheYear = {dogName: 'Lola', nickName: 'Lulu', breed: 'Husky', age: 11, faveTreat: 'Bacon'};

```

These are the properties: dogName, nickName, breed, age, faveTreat

And these are the property values: Lola, Lulu, Husky, 11, Bacon

How do we access these properties? We call on them like this: 

```
dogOfTheYear.dogName // This would return Lola. 
dogOfTheYear.breed // This would return Husky.

```

or this: 

```
dogOfTheYear["dogname"] 
```

Objects can also have mthods which are actions that can be performed on objects. Methods are stored in properties as function definitions.

| Property  	| Property Value                       	|
|------------ |--------------------------------------	|
| firstName	  | Lola                                	|
| breed    	  | Husky                                	|
| age         | 11                                    |
| faveTreat   | Bacon                                 |
| funFacts    | function() { return this.firstName + "is a good " + this.breed + " who loves " + this.faveTreat; }                          |

Example: 

```

let dogOfTheYear = {
  firstName: "Lola",
  breed: "Husky",
  age: 11,
  faveTreat: "Bacon",
  funFacts: function() {
    return this.firstName + " is a good " + this.breed + " who loves " + this.faveTreat;
  }
};
```

By using "this", you can access the object's properties and include them in the returned string generated by the "funFacts" method. "This" is not a variable, it is a keyword and the value cannot be changed.

Objects promote encapsulation by grouping related data and behaviour together. This helps with code organization and complexity. Objects are fundamental in JavaScript, serving as the building blocks for data modeling, data storage, and code organization. 

![alt text](beach_lola.png)

## Functions

A JavaScript function is a block of code that is designed to perform a particular task. How do we execute that function after it is written? We call it! Also known as "invoking" the function. We use the () operator to invoke the function.

Here is the basic structure of a simple function: 

```
function name(parameter1, parameter2, parameter3){
    //code to be executed
}
```

Function arguments are the values received by the function when it is invoked. An example of invoking a function is having a user click a button.When JavaScript reaches a return statement, the function will stop executing.

Example:

```
function treatsPerWeek(){
  let treats = 8; // Treats per day. Don't judge me, they're small treats!
  let week = 7; // Self explanatory - number of days in a week.

  return treats * week;

  console.log(treatsPerWeek()); // Outputs 56
}
```

Variables declared within a JavaScript function are local to that function and can only be accessed from within the function.

Example: 

```
// code here can NOT use dogName

function myFunction() {
  let dogName = "Lola";
  // code here CAN use dogName
}

// code here can NOT use dogName
```

## Parameters

Functions can have parameters, which are the names listed in the function definition. Function arguments are the valued passed througn the function. When declaring a function, specify the parameter names in the functions parameter list. For example:

```
function Lola(parameter1, parameter2, parameter3) {
  // code to be executed
  alert("Lola is the best!");
}
```
Named parameters allow you to pass values to the funtion and use those values with meaningful names within the functions body. 

## Loops

JavaScript loops can execute a block of code a number of times. They are especially helpful when you want to run the same code over and over again, each time with a difference value (which is often the case when working with arrays).

There are several kinds of JavaScript loops to learn:

**for loops** loop through a block of code a number of times. 

```
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

**for/in loops** loop through the properties of an object. 

```
let dog = {
  name: 'Lola',
  age: 11
}
for (let key in dog) {
  console.log(key + ": " + dog[key]);
} 
```

**for/of loop** is used to iterate over the elements of an iterable object, such as an array. 

```
let treats = ['bacon, 'salmon', 'turkey'];
for (let treat of treats) {
  console.log(treat);
}
```

**while loops** loop through a block of code as long as a specified condition is true.

```
let count = 0;
while (count < 3) {
  console.log("Hello!");
  count++;
}
```

**do/while loops** also loop through a block of code while a specified condition is true and they guarantee that the block of code runs at least once. 

```
let x = 0;
do {
  console.log("One lap around the block of code");
  x++;
} while (x < 0);
```

![alt text](amos_lola2.png)

## Data Types

To access variables, you need to know the data type. JavaScript data types are dynamic ans one variable can hold several different data types!  

```
let L;       // Undefined
x = 11;       // Number
x = "Lola";  // String
```

There are 6 data types in JavaScript.  

1. **String** 

JavaScript string are written in quotes, and they are for storing and manuipulating text. When you add a numbers and strings together, JavaScript treats the number as a string.

```
// Strings:
let breed = "Husky";
let firstName = "Lola";
let  = "Treats " + 4 + " A Good Girl"; // "Returns Treats 4 A Good Girl"
```

2. **Number**

Numbers can be written with or without decimals. 

```
// Numbers:
let age = 11;
let weight = 65.25;
let height = 40.00;
```

3. **BigInt**

BigInt is a new datatype that is like a super-sized container for storing really big whole numbers in your JavaScript code. It's useful when you need to work with numbers that are too large for regular numbers to handle.
```
let lolaNapsPerDay = BigInt("123456789012345678901234567890");
```

4. **Boolean**

Booleans can only have two values: **true** or **false** which can be used to make decisions and control program flow.
```
let goodDog = true;
let badDog = false;
```

5. **Undefined**

A variable without value is undefined. An empty value isn't necessarily undefined, it is simply empty data value. 
```
let lola; // Undefined. 
let lola = ""; // The value is "", the type is "string".
```

6. **Null**

Null has only one value - NULL, which means that there hasn't been any value assigned to it. 

```
let emptyValue = null;

if (emptyValue === null) {
  console.log("The value is intentionally empty (null).");
} else {
  console.log("The value is not empty.");
}
```

7. **Symbol**

A symbol is a data type introduced to represent a unique and immutable value. They are used to ensure that property names do not clash with other properties in an object. Use the Symbol() function to create a symbol, function takes an optional string parameter, which can be used to give the Symbol a description. Symbols can also be used to create constants, which are useful for creating APIs.

```
// Creating a symbol for a property key
const specialKey = Symbol("special");

// Creating an object with a "regular" property
const myDog = {
  name: "Lola",
  age: 11
};

// Adding a property using the symbol as the key
myDog[specialKey] = "This is a special property";

// Accessing properties
console.log(myDog.name); // Outputs: Lola
console.log(myDog[specialKey]); // Outputs: This is a special property
```

8. **Object**

Objects are written with the curly brackets {}. They are variables, but they can contain many values separated by commas. Object values are defined as **name : value**. 

```
// Object:
let dog = {firstName: 'Lola', breed: 'Husky'};

```

## Comments

Comments are so helpful in JavScript! Keeping organized, concise comments in your code is a best practice to follow. 

```
// Single line comments should look like this.

/** This is what multiple line comments look like. 
Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. */
```

###I hope you have enjoyed this informative Syntax Guide!

I recognize that I have merely covered the essentials in here for now, but I look forward to adding a more comprehensive guide to JavaScript as I become more fluent in this language. I have enjoyed this project, and Lola got a lot of love! :heart: