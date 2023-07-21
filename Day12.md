#  Day12 (14/Jul/2023) 🚀

## Things to do ✔️

1. Watch This Topics from -JavaScript: - The Hard Parts,v2 - course :

 - Static Typing .
 - Types .
 
2. Summarize what i learned .   
3. Solve some problems from FreeCodeCamp .
  

## Summary of topics 📝

### 1. Static Typing :


### 2. Scope :

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

A) `undefined`, `undefined`, `undefined`   
B) `1`, `undefined`, `ReferenceError`  
C) `1`, `ReferenceError`, `ReferenceError`   
D) `1`, `ReferenceError`

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

A) `undefined`, `ReferenceError`   
B) `1`, `undefined`, `ReferenceError`   
C)`undefined`, `undefined`,
`ReferenceError`  
D) `1`, `ReferenceError`

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

A) `[ 36, 100, 45 ]` | `[ 1, 2, 3 ]` | `[ 36, 2, 3 ]`   
B) `[ 36, 100, 45 ]` | `[1, 2, 3 ]` | `[ 36, 100, 45 ]`   
C) `[ 36, 100, 45 ]` | `[ 1, 2, 3 ]` | `[ 1,100, 45 ]`   
D) `[ 36, 100, 45 ]` | `[ 1, 2, 3 ]` | `[ 1, 2, 3 ]`




# DONE 😇
