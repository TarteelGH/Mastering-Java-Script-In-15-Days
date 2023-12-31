#  Day2 (4/Jul/2023) 🚀

## Things to do ✔️

1. Watch This Topics from -JavaScript: From First Steps to Professional- course :

- Expressions .
- Arrays .
- Obejcts .
   
2.  Summarize what I learned .
3. Solve some problems from FreeCodeCamp .
  

## Summary of topics 📝

### 1. Expressions :

- #### let : Declaration declares a block-scoped local variable.optionally initializing it to a value .

   * Declaring a variable be like ` let bankruptcy; ` 
   * Assigning a variable be like ` let myDeclaredVariable; myDeclaredVariable = "so value, much wow"; ` .
   * Declaring & assigning at once be like `
let myAssignedVariable = "such efficient, amaze"; ` 

- #### const : declares & assigns a "constant" aka a variable that can't be changed (Declaring & assigning forever)
  ` const myUnchangeableVariable = "Never gonna give you up";` 

- #### Variable names :
  * validVariable
  * also_valid_but_less_common
  * Oddbut_Technicallyfine2
  * ~~0chanceThisWillWork!~~


 - #### Statements vs. Expressions :
    * An expression "asks" JS for a value :
     ` myAssignedVariable
         6 + 4
        document.getElementById("board")
       `
    * A statement "tells" JS to do something (e.g. declare/assign a variable)
` let ten = 6 + 4;
myDeclaredVariable = "new value";
let board = document.getElementById("board"); `

We'll see more kinds of statements later in the course

   ```javascript
 function add(x, y) {
    return x + y;
   }
   let biggest;
   if (5 > 4) {
    biggest = 5;
   } else {
    biggest = 4;
   }
   for (let character of "string") {
    console.log(character);
   }
 ```

### 2. Arrays :

- #### Array : Arrays let us keep multiple values together in a single collection :
  
   `let synonyms = ["plethora", "array", "cornucopia"];`
  
  * Like strings, arrays have a length : ` synonyms.length `
  * And each value has an index : ` synonyms[1] ; synonyms.indexOf("cornucopia") `
  * Also like strings, we can check if an array contains a certain value : ` synonyms.includes("plethora") ; 
   synonyms.includes("variety") `
  * Arrays can be empty, or hold a single item : ` let emptyArray = []; let oneItemArray = ["lonely"]; `
  * Arrays can hold any type of items, or mix and match! : ` let mixedArray = ["pop", 6, "squish", false, document]; `

- #### Functions that i can use with Array :
 
  * **.sort()** : The sort() method sorts the elements of an array in place and returns the reference to the same array, now sorted. The default sort order is ascending, built upon converting the elements into strings, then comparing their sequences of UTF-16 code units values.  ` ["c", "a", "d", "b"].sort() ` output : `  ['a', 'b', 'c', 'd'] `

  * **.join()** : The join() method creates and returns a new string by concatenating all of the elements in an array (or an array-like object), separated by commas or a specified separator string. If the array has only one item, then that item will be returned without using the separator. ` ["lions", "tigers", "bears oh my!"].join(" & ") ` outpot : ` 'lions & tigers & bears oh my!' `

  * **.concat()** : The concat() method is used to merge two or more arrays. This method does not change the existing arrays, but instead returns a new array. ` [1, 2, 3].concat([4, 5, 6]) ` output : ` [1, 2, 3, 4, 5, 6] `
 
  * **.pop()** : The pop() method removes the last element from an array and returns that element. This method changes the length of the array. ` const plants = ['broccoli', 'cauliflower', 'cabbage', 'kale', 'tomato']; plants.pop(); ` output:  ` Array ["broccoli", "cauliflower", "cabbage", "kale"]  `


  * **.push()** : The push() method adds the specified elements to the end of an array and returns the new length of the array. ` let  numbers1 = [1, 2, 3]; let result1 = numbers1.push(4); ` output : ` [1, 2, 3, 4] `

  > ***Do these do the same thing?***
   ```javascript
    let abcArray = ["a", "b", "c"];
     abcArray[1] = "d";
     abcArray;
   ```
   ```javascript
     let abcString = "abc";
     abcString[1] = "d";
     abcString;
   ```
   > So first one **abcArray** will be ["a", "d", "c"]  and the second one **abcString**  will be the same "abc" .

 - #### mutable vs. immutable :
   
   * "Mutable" data can be edited (e.g. Arrays)
   * "Immutable" data always stays the same (e.g. strings & other primitives)
  
   > ***Do these do the same thing?***
   ```javascript
       let numbers1 = [1, 2, 3];
       let result1 = numbers1.push(4);
       numbers1;
   ```
   ```javascript
     let numbers2 = [1, 2, 3];
     let result2 = numbers2.concat([4]);
     numbers2;
   ```
   > So *.puch()* is mutable because **numbers1** = [ 1, 2, 3, 4 ] and *.concat()* is immutable because **numbers2** =  [ 1, 2, 3 ] .
  
   > Some actions "mutate" an array (e.g. oldArray.push(newValue)) ...aka change the array in-place
   > Other actions do not mutate the original array, but instead create a new copy (e.g. oldArray.concat(otherArray)) .

     > ***What will Happen?***
   ```javascript
    const operands = [4, 6];
       const sum = operands[0] + operands[1];
       operands[0] = 5;
       operands = [23,442]; // TypeError: Assignment to constant variable.
       const newSum = operands[0] + operands[1];
       console.log(sum , newSum ,operands);
   ```
   > OutPut ` 10 11 [ 5, 6 ] `

   > ***Other tings***
   > "lonely" == ["lonely"] ✔️
   > "lonely" === ["lonely"] ✖️
   
### 3. Objects :

- #### Object :  The Object type represents one of JavaScript's data types. It is used to store various keyed collections and more complex entities. Objects can be created using the Object() constructor or the object initializer / literal syntax.

```javascript
const js = {
    name: "JavaScript",
    abbreviation: "JS",
    isAwesome: true,
    officialSpec: "ECMAScript",
    birthYear: 1995,
    creator: "Brendan Eich"
};
```
Objects collect multiple values together to describe more complex data Similar to how we can point at different values using variables in our code, objects let us point at related values using properties in the object.

    * Getting property values : ` js.name `  ` js.isAwesome `
    * Using property values : ` js.name.startsWith("Java") `  ` let age = 2022 - js.birthYear; `
    * Setting property values :
```javascript
const indecisive = {
    lunch: "sandwich"
};

indecisive.lunch = "tacos";
indecisive.snack = "chips";

```
>(,)=new property.
>(.)=value to collect | create new proprty.


- #### methods :

    * Properties can point to functions too We call function-properties "methods" on objects
```javascript
const dog = {
    name: "Ein",
    breed: "Corgi",
    speak: function () {
        console.log("woof woof");
    }
}

dog.speak();
```

    * this in a method lets us reference other properties on the object
    
```javascript
anjana.speak = function () {
    console.log("Hi my name is", this.name);
}

anjana.speak();
```
- #### Nested objects :
```javascript
const menu = {
    lunch: {
        appetizer: "salad",
        main: "spaghetti",
        dessert: "tiramisu"
    },
    dinner: {
        appetizer: "samosa",
        main: "saag paneer",
        dessert: "gulab jamun"
    }
};
const tiramisu = menu.lunch.dessert;
```
- #### Objects in Arrays & Objects :
```javascript
const spices = [
    {name: "Emma", nickname: "Baby"},
    {name: "Geri", nickname: "Ginger"},
    {name: "Mel B", nickname: "Scary"},
    {name: "Mel C", nickname: "Sporty"},
    {name: "Victoria", nickname: "Posh"}
];

const spiceGirls = {
    albums: ["Spice", "Spiceworld", "Forever"],
    motto: "Girl Power",
    members: spices
};
```

- #### Built in objects :

  * document :
 ` document.title = "Tic Tac Toe"; document.querySelector("h2").append(" and love"); `
  *  console : 
 ` console.log("hello coder!"); `
 ` console.log(document.querySelector("h1").textContent); `
 ` console.warn("something seems iffy"); `⚠️
 ` console.error("oh no, it broke!"); ` ⛔
 ` console.clear(); ` 🗑️
  * Math :
` let randomNumber = Math.random(); //between 0 & 1 `
` const pi = Math.PI; `
` const five = Math.abs(-5); `
  * strings?
Strings are primitive values (not objects) but JS automatically wraps them in String objects and it,s imutable 
```javascript
const hello = "hello";
console.log(hello.length);
const yello = hello.toUpperCase();
```
>    + var-> functional scope, redecleration✅, reassignment✅, hoisting✅.
      
>    + let-> block scope, redecleration❎, reassignment✅, hoisting❎.
     
>    + const-> block scope, redecleration❎, reassignment❎, hoisting❎.

 
## Examples 🔍

> I put so many examples at every point ... 

## Challenges 💪🏽

1.[Profile Lookup](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/profile-lookup)

***Solution***

```javascript
// Setup
const contacts = [
  {
    firstName: "Akira",
    lastName: "Laine",
    number: "0543236543",
    likes: ["Pizza", "Coding", "Brownie Points"],
  },
  {
    firstName: "Harry",
    lastName: "Potter",
    number: "0994372684",
    likes: ["Hogwarts", "Magic", "Hagrid"],
  },
  {
    firstName: "Sherlock",
    lastName: "Holmes",
    number: "0487345643",
    likes: ["Intriguing Cases", "Violin"],
  },
  {
    firstName: "Kristian",
    lastName: "Vos",
    number: "unknown",
    likes: ["JavaScript", "Gaming", "Foxes"],
  },
];

function lookUpProfile(name, prop) {
  // Only change code below this line
  for (let i = 0; i < contacts.length; i++) {
    if (contacts[i].firstName === name) {
      if (contacts[i].hasOwnProperty(prop)) //The hasOwnProperty() method returns a boolean indicating whether the object has the specified property as its own property (as opposed to inheriting it). {
        return contacts[i][prop];
      } else {
        return "No such property";
      }
    }
  }
  return "No such contact";
  // Only change code above this line
}

lookUpProfile("Akira", "likes");

```

2.[Copy Array Items Using slice()](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/copy-array-items-using-slice)

***Solution***

```javascript
function forecast(arr) {
  // Only change code below this line
let forecast = ['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms'] //The slice() method returns a shallow copy of a portion of an array into a new array object selected from start to end (end not included) where start and end represent the index of items in that array. The original array will not be modified. 
 arr = forecast.slice(2,4);
  return arr;
}

// Only change code above this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```

3.[Combine Arrays with the Spread Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/combine-arrays-with-the-spread-operator)

***Solution***

```javascript
function spreadOut() {
  let fragment = ['to', 'code'];
  let sentence = ['learning', ... fragment ,'is',  'fun']; // Change this line
  return sentence;
}

console.log(spreadOut());

//The spread (...) syntax allows an iterable, such as an array or string, to be expanded in places where zero or more arguments (for function calls) or elements (for array literals) are expected. In an object literal, the spread syntax enumerates the properties of an object and adds the key-value pairs to the object being created.


```

# DONE 😇
