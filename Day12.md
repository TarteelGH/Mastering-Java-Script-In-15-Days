#  Day12 (14/Jul/2023) 🚀

## Things to do ✔️

1. Watch This Topics from -JavaScript: - The Hard Parts,v2 - course :

 - Static Typing .
 - Scope .
 
2. Summarize what i learned .   
3. Solve some problems from FreeCodeCamp .
  

## Summary of topics 📝

### 1. Static Typing :

#### Static Types:

Static typing is a type system feature where the type of a variable is checked at compile-time. It means that the types of variables are explicitly declared and enforced during the compilation phase. The type of a variable remains fixed throughout its lifetime, and any attempt to assign a value of an incompatible type will result in a compilation error.

*Static typing offers several advantages, including:*

- Early detection of type-related errors during compilation.
- Improved code quality and maintainability.
- Enhanced tooling support, such as autocompletion and refactoring assistance.
- Potential performance optimizations, as the compiler can make assumptions based on the static types.
- Examples of programming languages with static typing include Java, C++, C#, and TypeScript.

#### Value Types:

Value types are a classification of data types based on how they are stored and passed around in memory. In a value type, the actual value is directly stored in the memory location associated with the variable. In other words, when you assign a value type variable to another variable or pass it as a function argument, a copy of the value is made.

*Value types have the following characteristics:*

- The value is stored directly, without the need for additional memory allocations.
- Copies of value type variables are independent of each other.
- Operations on value types typically involve manipulating the values directly.
- Common examples of value types are integers, floating-point numbers, characters, and boolean values. In some programming languages, - - structures and enumerations are also considered value types.

### 2. Scope :

#### Lexical scope :

* is the ability for a function scope to access variables from the parent scope. We call the child function to be lexically bound by that of the parent function. The diagram below outlines the supposed hierarchy that the lexical scope maintains in JavaScript.

```javascript
var a = 10; // variable a assigned to 10

var func = function (){ // outermost function
    var b = 20;
    console.log("a and b is accessible (outer):", a, b);
    var innerFunc= function (){ // innermost function
        var c = 30;
        console.log("a and b and c is accessible (innner):", a, b, c);
    }
    innerFunc();
    return;
}
func(); // invoke function func 
console.log("only a is accessible (global):", a);
```
* In the above code, the value of variable a is accessible by all function scopes since it is in the global scope. Meanwhile, variable b is not accessible outside the function assigned to func. This is because the variable is of local scope for the function assigned to variable func. Another thing to note is that the function assigned to the innerFunc variable can access variable b and c. This is because the inner functions are lexically bound by the outer functions.

#### strict mode :
* is a way to opt in to a restricted variant of JavaScript, thereby implicitly opting-out of "sloppy mode". Strict mode isn't just a subset: it intentionally has different semantics from normal code. Browsers not supporting strict mode will run strict mode code with different behavior from browsers that do, so don't rely on strict mode without feature-testing for support for the relevant aspects of strict mode. Strict mode code and non-strict mode code can coexist, so scripts can opt into strict mode incrementally.

*Strict mode makes several changes to normal JavaScript semantics:*

1. Eliminates some JavaScript silent errors by changing them to throw errors.
2. Fixes mistakes that make it difficult for JavaScript engines to perform optimizations: strict mode code can sometimes be made to run 3. faster than identical code that's not strict mode.
4. Prohibits some syntax likely to be defined in future versions of ECMAScript.
   
> note -> In JavaScript, a reference error occurs when you try to access a variable or function that is not defined or not accessible in the current scope. This type of error is quite common and can occur for various reasons, such as misspelling a variable name, accessing a variable outside its scope, or trying to use a function that hasn't been declared yet.

## Examples 🔍



## Challenges 💪🏽
[SECTION'S EXERCISES](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day2-tasks/tasks.md?plain=1)

## STATIC TYPING QUESTIONS:

### QUESTION #1

Given the following `promisesArray`, convert the array into an object using the
`convertToObj` function.

You should apply typescript types to every promise, the input of `convertToObj`,
and the output of `convertToObj`. 

Build interfaces and types as needed.

```javascript

const sayHelloWorld = new Promise(resolve, reject => {
  resolve("Hello world!");
});

const checkBoolean = (boolean) => new Promise(resolve, reject => {
  if (boolean) {
    resolve(boolean);
  } else {
    reject(`Input is false :(`)
  }
})

const returnObj = new Promise(resolve, reject => {
  resolve({
    x: "meow",
    y: 45,
  })
})

const promisesArray = [sayHeloWorld, checkBoolean, returnObj];

const convertToObj = (array) => {
  //write your code here;
  return obj;
}

```

-------------------------------------------------------------------

## SCOPE & HOISTING QUESTIONS:

### QUESTION #1:

What will be the output of the following code snippet? Pick the right choice
then **justify your answer with an explanation**.

```javascript
function testScope1() {
  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;
  }
  console.log(a);
  console.log(b);
  console.log(c);
}

testScope1();

```
**Choices:**

1. `undefined`, `undefined`, `undefined`  ✖️   
2. `1`, `undefined`, `ReferenceError`  ✔️
3. `1`, `ReferenceError`, `ReferenceError`  ✖️ 
4. `1`, `ReferenceError`  ✖️

-------------------------------------------------------------------

### QUESTION #2:

What will be the output of the following code snippet? Pick the right choice
then **justify your answer with an explanation**.

```javascript
function testScope2() {
  console.log(a);
  console.log(b);
  console.log(c);
  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;
  }
}

testScope2();

```

**Choices:**

1. `undefined`, `ReferenceError`  ✔️   
2. `1`, `undefined`, `ReferenceError`  ✖️
3. `undefined`, `undefined`,
`ReferenceError`  ✖️
4. `1`, `ReferenceError`  ✖️

-------------------------------------------------------------------

### QUESTION #3:

What will be the output of the following code snippet? Pick the right choice
then **justify your answer with an explanation**.

```javascript

function testScope3() {
  var a = 36;
  let b = 100;
  const c = 45;

  console.log([a, b, c]);

  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;

    console.log([a, b, c]);
  }

  console.log([a, b, c]);
}

testScope3();

```

**choices:**

1. `[ 36, 100, 45 ]` | `[ 1, 2, 3 ]` | `[ 36, 2, 3 ]`   ✔️
2. `[ 36, 100, 45 ]` | `[1, 2, 3 ]` | `[ 36, 100, 45 ]`   ✖️
3. `[ 36, 100, 45 ]` | `[ 1, 2, 3 ]` | `[ 1,100, 45 ]`  ✖️ 
4. `[ 36, 100, 45 ]` | `[ 1, 2, 3 ]` | `[ 1, 2, 3 ]`  ✖️




# DONE 😇
