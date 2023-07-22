#  Day7 (9/Jul/2023) 🚀

## Things to do ✔️

1. Watch This Topics from -JavaScript: The Hard Parts,v2- course :

 - Closures .
   
2. Summarize what i learned .   
3. Solve some problems from FreeCodeCamp .
  

## Summary of topics 📝

### 1. Closures : 

* when functions returned other function, we call it *closure*.
```javascript
//
function createFunction() {
  functon multiplyBy2(num) {
    return num*2;
  }
  return multiplyBy2;
}
const gererateFunction = creataFunction();
const result = generateFunction(3); //6
```
* when we execute a function, all local data memory will deleted after we exit the function, so closure is to save this data memory.

* calling the function outside of the function call in witch it was defined.

```javascript
function outer() {
  let counter = 0;
  function increamentCounter() {
    counter++;
  }
return increamentCounter;
}
const myNewFunction = outer();
myNewFunction();
myNewFunction();
```
* in previous example, we can not access the value of counter unless we run the function `myNewFunction()`

```javascript
const anotherFunction = outer();
anotherFunction();
anotherFunction();
```
> the value of counter will be one two one two.

* this is because the backpack for `myNewFunction` and the backpack for `anotherFunction` are two different backpacks.

* closures give our function persistent memories and entirely new toolkit for writing professional c0de.
 

## Examples 🔍

I wrote it !

## Challenges 💪🏽

1.[Exercises for closures]([[codecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-higher-order-functions-map-filter-or-reduce-to-solve-a-complex-problem](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day2-tasks/tasks.md)https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day2-tasks/tasks.md](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day2-tasks/tasks.md))

**Solution**


1. Question 1:
Write a closure named createCounter that takes an initial value start and returns a function. The returned function, when invoked, should increment the counter by 1 and return the updated value.
```javascript

function createCounter (initValue) {
    let counter = initValue;
    function increamentCounter() {
        counter++;
        return counter;
    }
    return increamentCounter;
}
```

2. Question 2:
Write a closure named calculateAverage that takes an array of numbers, nums, and returns a function. The returned function, when invoked, should calculate and return the average of the numbers in the array.
```javascript

function calculateAverage (arr) {
    let sum = arr.reduce((a,b) => a + b, 0)
    function avg() {
        return sum / arr.length;
    }
    return avg;
}
```

3. Question 3:
Write a closure named powerOf that takes a base number base and returns a function. The returned function, when invoked with an exponent exp, should calculate and return the result of base raised to the power of exp.
```javascript

function powerOf(n) {
    function calculatePower(x) {
        return Math.pow(n, x);
    }
    return calculatePower;
}
```


# DONE 😇

