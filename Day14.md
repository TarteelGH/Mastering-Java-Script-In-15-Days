#  Day14 (16/Jul/2023) 🚀

## Things to do ✔️

1. Watch This Topics from -JavaScript: - The Hard Parts,v2 - course :

 - Advanced Scope - the remaining 30 mins .
 - Closure .
 
2. Summarize what i learned .   
3. Solve some problems from FreeCodeCamp .
  

## Summary of topics 📝

### 1. Advanced Scope - the remaining 30 mins :


### 2. Closure :

## Examples 🔍



## Challenges 💪🏽
[SECTION'S EXERCISES]([https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day2-tasks/tasks.md?plain=1](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day4-tasks/tasks.md?plain=1))

## ADVANCED SCOPE:

### QUESTION #1

Given the following code snippet and **explain what's happening**.

```javascript
for (var i = 0; i < 5; i++) {
    setTimeout(function() {
      console.log("value of [i] is: ", i);
    }, 100);
}
```

The current output is: "value of [i] is: 5" five times.

The output should be: 

"value of [i] is: ", 0 "value of [i] is: ", 1 "value of [i] is: ", 2 "value of
[i] is: ", 3 "value of [i] is: ", 4

Without changing anything in the for loop's code itself, provide a solution to
fix it.

-------------------------------------------------------------------

## ADVANCED SCOPE:

### QUESTION #2

Given the following code snippet and **explain what's happening**. 

```javascript

for (let i = 0; i < 5; i++) {
   let array = [];
   array.push(i);
   console.log("Current array is: ", array)
}

```

The current output is: 

"Current array is: [ 0 ]" "Current array is: [ 1 ]" "Current array is: [ 2 ]"
"Current array is: [ 3 ]" "Current array is: [ 4 ]".

The output should be: "Current array is: [0, 1, 2, 3, 4]".

Provide a solution to fix it. 

-------------------------------------------------------------------

## ADVANCED SCOPE:

### QUESTION #3

Given the following code snippet and **explain what's happening**. 

```javascript

let functions = [];

for (var i = 0; i < 5; i++) {
  functions.push(() => {
    console.log("Current value of i is:", i);
  });
}

functions.forEach((func) => func());

```

The current output is: 

"Current value of i is: 5" "Current value of i is: 5" "Current value of i is: 5"
"Current value of i is: 5" "Current value of i is: 5"

The output should be: 

"Current value of i is: 0" "Current value of i is: 1" "Current value of i is: 2"
"Current value of i is: 3" "Current value of i is: 4"

Provide a solution to fix it. 

-------------------------------------------------------------------

## CLOSURE:

### QUESTION #1

Create a function called `privateCounter()` that behaves like a private counter.
The function should not have any public variables, and the count should only be
accessible through a closure. It should have two methods: `increment()` and
`getCount()`. The `increment()` method should increment the count, and
`getCount()` should return the current count.

-------------------------------------------------------------------

## CLOSURE:

### QUESTION #2

Write a JavaScript function called `generateFibonacci(count)` that returns a
closure. The closure should generate the next number in the Fibonacci sequence
each time it is called. The `generateFibonacci` function should take a parameter
`count` that determines how many times the closure will generate the next
number, and it should use recursion for this purpose.


# DONE 😇
