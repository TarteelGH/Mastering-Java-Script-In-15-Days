#  Day4 (6/Jul/2023) 🚀

## Things to do ✔️

1. Watch This Topics from -JavaScript: From First Steps to Professional- course :

 - Events & Handlers .
 - Conditionals .
 - Map & Filter .
 - Doggos Quiz Game .

2. Summarize what i learned .   
3. Solve some problems from FreeCodeCamp .
  

## Summary of topics 📝

### 1. Events & Handlers :

#### Events & Handlers :

* The web browser fires events when certain things happen on the page ,For example, when the user clicks somewhere on the page, a click event is fired .
* We can detect events with JS using an event listenerThe **.addEventListener()* method lets us listen for events on a DOM element
```
document.addEventListener("click", () => {
    console.log("clicked")
});
```
* .addEventListener() takes 2 parameters:
  - The name of the event to listen to (e.g. "click")
  - A handler function that JS calls when that event is fired on this element

* JS passes an event object to the handler function with information about the event ,If we accept this as a parameter, we can use it to get details
```
document.addEventListener("click", (event) => {
    console.log(event);
});
```
* event.target is the element the event fired on (in this case, which element was clicked)
```
document.addEventListener("click", (event) => {
    console.log(event.target);
});
```
* "click" isn't the only type of event we can handle
   - "dblclick"
   - "mouseover"
   - "mouseout"
   - ...and lots more!

#### Loops :

* Loops let us run the same chunk of code multiple times
```
for (let rep = 0; rep < 10; rep += 1) {
    console.log("now doing rep", rep);
}
console.log("do you even lift bro");
```
> this is called iteration
* for loops require us to:
  - declare & initialize a loop counter
  - give a condition for the loop to keep running
  - describe how to change (usually increment) the counter each time
```
for (let count = 0; count <= 100; count += 10) {
    console.log(count);
}
```
* for ... of loops let us more easily iterate over items in a collection
```
const numbers = [1,2,3];
for (let i = 0; i < numbers.length; i++) {
    console.log(numbers[i]);
}
for (let n of numbers) {
    console.log(n);
}
```
* We can use for...of to iterate over characters in a string
```
for (let char of "ALOHA") {
    console.log(char);
}
```
or items in an array
```
for (let item of ["pop", 6, "squish"]) {
    console.log(typeof item);
}
```
> because strings & arrays are "iterables"
     
### 2. Conditionals :

* if statements let us execute code under a certain condition
```
const you = {wannaBeMyLover: true};
if (you.wannaBeMyLover) {
    you.gottaGetWithMyFriends = true;
}
```
> code in the if block only runs if the (condition) is true

* we can use else to run other code if (condition) is false
```
if (you.reallyBugMe) {
    console.log("Goodbye");
} else {
    console.log("Hello");
}
```
* We can chain else and if blocks to account for multiple conditions
```
function compare(x, y) {
    if (x > y) {
        console.log(x, "is greater than", y);
    } else if (x < y) {
        console.log(x, "is less than", y);
    } else {
        console.log(x, "is equal to", y);
    }
}
```
* The (condition) is usually an expression that evaluates to a boolean
```
if (forecast === "rain") {
    console.log("bring an umbrella");
}
```
* If it's given some other value, JS will convert it to a boolean and decide based on its "truthiness"
```
if ("nonempty strings are truthy") {
    console.log("this line will run");
}
```
```
if (0) {
    console.log("zero is truthy");
} else {
    console.log("zero is falsy");
}
// (0)="falsy" , ([])="truthly" , ("")="falsy" , (null)="falsy" , (undefined)="falsy" 
```

#### Boolean (logical) operators :

* Sometimes we care about the opposite of a value
```
let someoneIsAroundYou = false; 
if (!someoneIsAroundYou) {
    console.log("baby I love you");
}
```
> The ! operator negates a boolean (gives its opposite)

* Sometimes we care about the truthiness of more than one value
```
if (you.happy && you.knowIt) {
    you.clapHands();
}
```
* Logical operators let us make two boolean values become one
* Logical "and" (&&) requires both values to be truthy

  **A && B**

  |   A    |   B    | A AND B| 
  | ------ | ------ | ------ |
  |  true  |  true  |  true  |
  |  true  |  false | false  |
  |  false |  true  | false  |
  |  false |  false | false  |

* Logical "or" (||) requires only one value to be 

  **A || B**

  |   A    |   B    | A OR B |  
  | ------ | ------ | ------ |
  |  true  |  true  |  true  |
  |  true  |  false |  true  |
  |  false |  true  |  true  |
  |  false |  false | false  |


#### Conditional ternary operator :

* JS also has a "shortcut" operator for writing quick conditionals it needs 3 values to work: ` condition ? valueIfTrue : valueIfFalse; `
```
let mood = forecast === "sunny" ? "happy" : "sad";
```
is equivalent to
```
let mood;
if (forecast === "sunny") {
    mood = "happy";
} else {
    mood = "sad";
}
```

### 3.  Map & Filter :

#### map & filter :
* The map & filter methods also let us process all the items in an array .
* **map** calls a function on each item in an array to create a new array
```
    const spices = [
    {name: "Emma", nickname: "Baby"},
    {name: "Geri", nickname: "Ginger"},
    {name: "Mel B", nickname: "Scary"},
    {name: "Mel C", nickname: "Sporty"},
    {name: "Victoria", nickname: "Posh"}
];

const nicknames = spices.map(s => s.nickname + " Spice

```

* String templates are useful too! Make them with backticks and ${}, e.g. *string to insert ${variable} into* ` s => ${s.nickname} Spice; ` is equivalent to ` s => s.nickname + " Spice" `
* **filter** calls a true/false function on each item and creates a new array with only the items where the function returns true
` const mels = spices.filter(s => s.name.includes("Mel")); `
#### Spread (...) : 
* Is another neat trick for iterating over arrays
* It lets us take all the items in an array and spread 'em around
* We can use it to put all the items from one array inside another array
```
const oldBurns = ["square", "wack"];
const newBurns = ["basic", "dusty", "sus"];
const burnBook = [...oldBurns, ...newBurns];
```
equivalent to
```
const burnBook = oldBurns.concat(newBurns);
```
* We can also use it to pass all the items from an array as arguments to a function or method
```
const skills = ["HTML", "CSS", "JS"];
const newSkills = ["React", "TypeScript", "Node"]
skills.push(...newSkills);
console.log(...skills);
let mood = forecast === "sunny" ? "happy" : "sad";
```
is equivalent to
```
let mood;
if (forecast === "sunny") {
    mood = "happy";
} else {
    mood = "sad";
}
```

### 4. Doggos Quiz Game :

#### Loops ...continued :

##### while loops:

* let us run a chunk of code over & over if a (condition) is true
```
let fiveRandomNumbers = [];
while (fiveRandomNumbers.length < 5) {
    fiveRandomNumbers.push(Math.random());
}
```
* Don't use while (true) unless you want to see your computer burn!
```
while (true) {
    console.log("I am wasting resources infinitely");
}
```
#### (A)synchronous code :

* Usually, our JS code does things that are very quick
```
console.log("This will print in a New York minute");
console.log("This will print one New York minute later");
```
> So JS can usually run straight through our program "synchronously"
* But when we need to do something that takes a long time we still want the web browser to keep working
* JS can only do one task at a time ("single-threaded") JS says: I cannot text you with a drink in my hand, eh 😂
* So when we give JS a task that takes a while, it doesn't stop and wait
```
console.log("This will print first"); // 1
setTimeout(() => console.log("This will print third"), 1000); // 3
console.log("This will print second"); // 2
```
it adds the slow task to a "TODO list" and keeps on running our program
The task runs some time later, "asynchronously"
* Some things that take time:
 - Waiting for user events
 - Asking a user to pick a file
 - Getting permission to access the camera/mic
 - Loading data from the interwebs

## Examples 🔍

``` // TODO 1: Declare & assign variables pointing to the corresponding element(s)
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
     // const isCorrect (guess) => guess === fact.answer; 
      function isCorrect(guess) {
      return guess === fact.answer
     }

    // TODO 6A: Use a for loop to add a click event listener to each of the optionButtons
    for(let button of optionButtons) {
        button.addEventListener("click", (event) => {

      
    
    // TODO 6B: Within the event handler function, display the fact's explanation by setting the text of the explanation element
      explanation.textContent = fact.explanation;        

            // TODO 7: Within the event handler function, 
            // Use a for loop to disable all the option buttons
            
            for (let button of optionButtons){
              disable(otherButton);
            }

            // TODO 8: Within the event handler function,
            // Get the guessed value from the clicked button
            // Use a conditional to compare the guess to the fact's answer
            // and add the "correct"/"incorrect" class as appropriate

            if (isCorrect(button.value)) {
                //TODO if correct answer
                button.classList.add("correct");
            } else {
                //TODO if wrong answer
                button.classList.add("incorrect");
            }

    
    })
    }
```

## Challenges 💪🏽

1.[Use Multiple Conditional (Ternary) Operators](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-multiple-conditional-ternary-operators)

**Solution**

```
function checkSign(num) {

  return ( num > 0) ? "positive" : ( num < 0) ? "negative" : "zero" ;

}

checkSign(10);
```

2.[Golf Code](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/golf-code)

**Solution**

```
```

3.[Use the map Method to Extract Data from an Array](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-the-map-method-to-extract-data-from-an-array)

**Solution**

```
```

4.[Use the filter Method to Extract Data from an Array](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-the-filter-method-to-extract-data-from-an-array)

**Solution**

```
```

# DONE 😇
