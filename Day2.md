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

   ``` function add(x, y) {
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


  * **.push()** : The push() method adds the specified elements to the end of an array and returns the new length of the array. ` let numbers1 = [1, 2, 3]; let result1 = numbers1.push(4); ` output : ` [1, 2, 3, 4] `

  > ***Do these do the same thing?***
   ``` let abcArray = ["a", "b", "c"];
     abcArray[1] = "d";
     abcArray;
   ```
   ```
     let abcString = "abc";
     abcString[1] = "d";
     abcString;
   ```
   > So first one **abcArray** will be ["a", "d", "c"]  and the second one will be the same **"abc"** 

 - #### mutable vs. immutable :
   
   * "Mutable" data can be edited (e.g. Arrays)
   * "Immutable" data always stays the same (e.g. strings & other primitives)
  
       > ***Do these do the same thing?***
   ``` let numbers1 = [1, 2, 3];
       let result1 = numbers1.push(4);
       numbers1;
   ```
   ```
     let numbers2 = [1, 2, 3];
     let result2 = numbers2.concat([4]);
     numbers2;
   ```
   > So *.puch()* is mutable because **numbers1** = [ 1, 2, 3, 4 ] and *.concat()* is immutable because **numbers2** =  [ 1, 2, 3 ] .
  
   > Some actions "mutate" an array (e.g. oldArray.push(newValue)) ...aka change the array in-place
   > Other actions do not mutate the original array, but instead create a new copy (e.g. oldArray.concat(otherArray)) .

     > ***What will Happen?
   ``` const operands = [4, 6];
       const sum = operands[0] + operands[1];
       operands[0] = 5;
       operands = [23,442]; // TypeError: Assignment to constant variable.
       const newSum = operands[0] + operands[1];
       console.log(sum , newSum ,operands);
   ```
   > OutPut ` 10 11 [ 5, 6 ] `    
### 3. Objects :

## Examples 🔍

## Challenges 💪🏽

1.[Profile Lookup](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/profile-lookup)

***Solution***

```
```

2.[Copy Array Items Using slice()](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/copy-array-items-using-slice)

***Solution***

```
```

3.[Combine Arrays with the Spread Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/combine-arrays-with-the-spread-operator)

***Solution***

```
```

# DONE 😇
