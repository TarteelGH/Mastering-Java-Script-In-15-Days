#  Day3 (5/Jul/2023) 🚀

## Things to do ✔️

1. Watch This Topics from -JavaScript: From First Steps to Professional- course :

  -  Quiz Project .
  -  Quiz Project Functions .
  
2.  Summarize what I learned .
3. Solve some problems from FreeCodeCamp .
  

## Summary of topics 📝

### 1. Quiz Project :

#### So here i did some codes ralatd to the quiz of frontendMaster  :
```

    // TODO 1: Declare & assign variables pointing to the corresponding element(s)
    // statement should be the "statement" div
    const statement = document.getElementById("statement");
    // optionButtons should be all the elements within the "options" div
    const optionButtons = document.queryselector("#options").children;
    // explanation should be the "explanation" div
    const explanation = document.getElementById("explanation");


    // TODO 2: Declare & assign a variable called fact
    // Its value should be an object with a statement, true/false answer, and explanation 
    const fact = {
        statement: "Array ar like obj?",
        answer: true,
        explanation: "Array are kind of object with special properties."
    };

    
    // TODO 3: Set the text of the statement element to the fact's statement
    statement.textContent = fact.statement;
        

    // TODO 4: Declare disable & enable functions to set or remove the "disabled" attribute from a given button element
    // disable(button) should set the button element's attribute "disabled" to the value ""
     
    const disable = (button) => {
    button.setArttribute("diabled","");
     }
    
    // enable(button) should remove the attribute "disabled" from the button element
    const enable = (button) => button.removeAttribute("disabled");
    
    // TODO 5: Declare an isCorrect function that compares a guess to the right answer
    // isCorrect(guess) should return true if the guess matches the fact's answer
    const isCorrect(gues) => guess === fact.answer; 
    // = function isCorrect(guess) {
    //  retrun guess === fact.answer
    // }
```
#### comments
Start with // Help others (and yourself) understand your code Help keep track of things you want to do

### 2. Quiz Project Functions :

#### Functions :

> values are things
 
> variables point to things
 
> functions do things

* declaring (creating) a function: ` function half(x) { return x / 2;} `
* calling (using) a function: ` const one = half(2); `
  
#### Parameters & Arguments : 

* Some functions need more than one value to work ` function add(x, y) { return x + y; } add(2,3); `
* Some functions don't even need any values ` function getRandomNumber() { return Math.random(); } getRandomNumber(); `
* parameters are the inputs a function expects `function add3(x, y, z) { console.log("My parameters are named x, y, z"); console.log("I received the arguments", x, y, z); return x + y + z; } const sum = add3(4,5,6); `
arguments are the actual values the function is called with
* Parameters should be named like variables, and behave like variables within the function body `function doesThisWork("literally a value") {
    return true;
}
function howAboutThis(1weirdVariable!) {
    return true;
} `
 ***What happens if we don't call a function with the intended argument(s)?***
  
 ` add3(1,2) ` = ` NaN `
 
 ` getRandomNumber("unexpected") ` = ` 0.9887074874500856 `

 * JS is pretty "loosey-goosey" about missing/extra arguments 🤩
   
 #### Return values :
 
 * A return statement specifies the function's output value ` function square(x) { return x * x; } const nine = square(3); `
 * Some functions don't return anything ` function sayHello(name) {  console.log("Oh hi, " + name + "!"); } sayHello("Marc"); `
   ` const hm = sayHello("Marc"); = undefined `

#### Arrow functions :

* The => "fat arrow" lets us create an unnamed function without much code ` (x, y) => x + y `
* Since arrow functions are expressions, we can assign them to a variable ` const add = (x, y) => x + y; ` is equivalent to ` function add(x, y) { return x + y; } `
* Arrow functions are great when we just want to return a value ` function square(x) { return x*x;} ` vs. ` const square = (x) => x*x; `
* For one-parameter functions, parentheses are optional ` x => x*x `  ` (x) => x*x `
* For multiple parameters, parentheses are required ` (firstName, lastName) => firstName + " " + lastName `
  
#### Scope : 

```
function declareBankruptcy() {
    let bankruptcy = true;
}
declareBankruptcy();
console.log(bankruptcy); // ReferenceError 🚫
```
* Scopes are nested within the program The widest scope is the **global** scope Each function gets its own new scope within the scope where it was declared.

```
let planet = "Jupiter";
function scopeOut() {
    let planet = "Mars";
    console.log("Inner planet:", planet);
}
scopeOut();
console.log("Outer planet:", planet); // Inner planet: Mars
Outer planet: Jupiter   
```
* Within each scope, you can access variables declared in a wider scope (e.g. global scope) But not those declared in a narrower scope (e.g. function scope).

```
let globalVariable = "I live in global scope"; 
function narrowerScope() {
    console.log(globalVariable);
    let localVariable = "I live in the function scope";
}
narrowerScope();
console.log(localVariable); // I live in global scope , ReferenceError 🚫 .

```
* Variables declared with let can be modified from within a narrower scope This can be useful, but also dangerous!

```
let feeling = "free";
function trap() {
    feeling = "boxedIn";
}
trap();
console.log(feeling); /// undefined ,  boxedIn
```

## Examples 🔍
> I put so many examples at every point ...

## Challenges 💪🏽

1.[Return a Value from a Function with Return](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/return-a-value-from-a-function-with-return)

***Solution***

```
```

2.[Global Scope and Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/global-scope-and-functions)

***Solution***

```
```

3.[Local Scope and Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/local-scope-and-functions)

***Solution***

```
```

4.[Global vs. Local Scope in Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/global-vs--local-scope-in-functions)

***Solution***

```
```

5.[Stand in Line](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/stand-in-line)

***Solution***

```
```


# DONE 😇
