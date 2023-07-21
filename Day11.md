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
```javascript
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
* **Math.sign() :** 
The Math.sign() static method returns 1 or -1, indicating the sign of the number passed as argument. If the input is 0 or -0, it will be returned as-is.
```javascript
Math.sign(-3)   //-1
Math.sign(3)    //1
Math.sign(-0)   //-0
Math.sign(0)    //0

//"fix" Math.sign(..)
function sign(v) {
return v !== 0 ? Math.sign(v) : object.is(v,-0) ? -1 : 1;
}
```
> 1/-♾ = -0 
* **Fundamental Objects :** 
aka: Built-In Objects
aka: Native Functions

```javascript
var yesterday = new Date("March 6 , 2019");
yesterday.toUTCString();
// "Wed, 06 Mar 2019 06:00:00 GMT"

```

## Examples 🔍

> I wrote !! 

## Challenges 💪🏽

* [SECTION'S EXERCISES](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day1-tasks/tasks.md)

1. Question 1:
Write a function called convertStringToNumber that converts a string to a number using the unary plus operator.
If the input is not a string, return an object of the input's value and type.
```javascript
function convertStringToNumber(input) {
  if (typeof input !== 'string') {
    return { value: input, type: typeof input };
  }

  const convertedNumber = +input;

  if (Number.isNaN(convertedNumber)) {
    return { value: input, type: 'NaN' };
  }

  return { value: convertedNumber, type: 'number' };
}

// is a string, it tries to convert it to a number using the unary plus operator (+). This operator converts a string to a numeric value.
}
```
2. Question 2:
Write a function called checkNaN that takes a single argument and returns true if the argument is NaN and false otherwise.
```javascript
const checkNaN = (value) => {
  return Number.isNaN(value); 
} 
```
3. Question 3:
Write a function called isEmptyValue that checks if a given input is an empty value (undefined, null, or empty string).
```javascript
 function isEmptyValue(value) {
  return value === undefined || value === null || value === '';
}
```
4. Question 4:
Write a function called compareObjects that takes 2 arguments of type "object" and compares them. If both arguments are equal, return true. If not, return false.

If either argument is not of type "object", the function should return an array of the arguments.
```javascript
const compareObjects = (input1, input2) => {
if ( typeof input1 === typeof input2 ) {
if ( input1 === input2 ) {
return true;
    }
  }
}
```
5. Question 5:
Write a function called complexCoercion that takes a single argument and checks if its type is primitive, and if so returns a coerced value according to the rules below.

coercion rules:

- if input is primive and:
- if input is a number, convert to string and then return a boolean.
- if input is a string, return a boolean.
- if input is null or undefined, return false.
- If input is not a primitive type, return the argument.
```javascript
const complexCoercion = (input) => {
  //write your own code here
}
```

# DONE 😇
