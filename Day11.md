#  Day11 (13/Jul/2023) 🚀

## Things to do ✔️

1. Watch This Topics from -JavaScript: - The Hard Parts,v2 - course :

 - Introduction .
 - Types .
 
2. Summarize what i learned .   
3. Solve some problems from FreeCodeCamp .
  

## Summary of topics 📝

### 1. Introduction :

* **firstly we talked abaut ++** :
```javascript
var x = 4 ;

x++;  // 4
x;    // 5

++x;  // 6 
x;    // 6
```

> ( x++ , ++x =  // x = x+1 

* **Course Overview :**
  - Types
    • Primitive Types
    • Abstract Operations
    • Coercion
    • Equality
    • TypeScript, Flow, etc.
  - Objects (Oriented)
    • this
    • class { }
    • Prototypes
    • OO vs. OLOO
  - Scope
    • Nested Scope
    • Hoisting
    • Closure
    • Modules

### 2. Types :

* **Types :** 
   • Primitive Types
   • Abstract Operations
   • Coercion
   • Equality
   • TypeScript, Flow, etc.
> "In JavaScript, everything is an object." // false
* Primitive Types
• undefined = not obj
• string = not obj 
• number = not obj
• boolean = not obj
• object = obj
• symbol = Added recently , ` v = symbol(); typeof v = "symbol"; `
• null = obj
• bigint (future) ` var v = 42n; ` 
• function = not obj , it is not official type.
• array = obj
> typeof return string " ... "
> In JavaScript, variables don't have types, values do.
```
v = "1";
typeof v; // "string"
v = 2;
typeof v; // "number"
v = true;
typeof v; // "boolean"
v = {};
typeof v; // "object"
v = symbol();
typeof v; // "symbol"
var v;
typeof v; // "undefined"
v = 43n;
typeof v; // "biglnt"
typeog notexist ; // "undefined";
v = finction(){};
typeof v = "function";
v = [1,2,3];
typeof v = "array";
```

* **undefined vs. undeclared :** 
- udefined : there is definitely a variable , and at the moment it has no value.
- undeclared : it is neveer been created in any scope that we have access to.
> TDZ : the temoral dead zone .
> block scope : don not get inialization they never initialy get set to undefined.

* **NaN :**  the special what we call sentinal value that indicates an invalid number.
* NaN: Invalid Number
  - don't: undefined
  - don't: null
  - don't: false
  - don't: -1
  - don't: 0
```javascript
var myNextAge = Number("n/a"); //NaN
myAge - "my age"; //NaN
isNaN(myAge); //false
isNaN(myNextAge); //false
isNaN("my age"); //true
Number.isNaN("my age"); //false
```
* so NaN it is a number and it is the invalid nimber and it is for accur

* **Negative Zero :**
* it is the negative reppresentaton of zero
* Object.is() : The Object.is() static method determines whether two values are the same value.
```javascript
console.log(Object.is('1', 1));
// Expected output: false

console.log(Object.is(NaN, NaN));
// Expected output: true

console.log(Object.is(-0, 0));
// Expected output: false

const obj = {};
console.log(Object.is(obj, {}));
// Expected output: false
```javascript
var trend = -0;
trend === 0; //true

trend.toStrinf();      // "0"
trend === 0;           //true
trend < 0;             //false
trend > 0;             //false

Object.is(trend,-0);   //true
Object.is(trend,0);    //false
```












## Examples 🔍

## Challenges 💪🏽

1.[SECTION'S EXERCISES]([[codecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-higher-order-functions-map-filter-or-reduce-to-solve-a-complex-problem](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day3-tasks/tasks.md)](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day1-tasks/tasks.md)https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day1-tasks/tasks.md)

**Solution**

```
```


# DONE 😇
