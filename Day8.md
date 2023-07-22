
#  Day8 (10/Jul/2023) 🚀

## Things to do ✔️

1. Watch This Topics from -JavaScript: The Hard Parts,v2- course :

 - Async JavaScript .
 - Promises .
 
2. Summarize what i learned .   
3. Solve some problems from FreeCodeCamp .
  

## Summary of topics 📝

### 1. Async JavaScript :
javaScript is:
- single threaded (one command run at a time).
- synchronously executed (each line is run in order the code appears).

> we can delay a function using `setTimeOut()`.

#### callback functions
the problems: 
1. our response data is only available in callback functions.
2. maybe it feels a little odd to think of passing of function into another function only for it to run much later.
the benefit:
1. super explicit one we understand how it works under-the-hood.

```javascript
function printHello() {
  console.log('Hello');
}
srtTimeOut(printHello, 1000);
console.log('me first!')

// it will print 'me first' first, then Hello.
 ```

#### Event loop
In JavaScript, the event loop is a fundamental part of the language's concurrency model. It is responsible for managing the execution of asynchronous code and handling events. The event loop ensures that JavaScript remains single-threaded while still allowing non-blocking I/O operations and asynchronous behavior.

explanation of how the event loop works:

1. JavaScript code is executed in a single-threaded environment, meaning that it can only execute one piece of code at a time.

2. When an asynchronous operation, such as a network request or a timer, is encountered, JavaScript doesn't block the execution. Instead, it registers the asynchronous task and continues with the next instructions.

3. Once the asynchronous task is completed, it's placed in a queue called the "task queue" or "callback queue".

4. The event loop continuously checks if the call stack (the place where synchronous code is executed) is empty. If it's empty, it picks the next task from the task queue and moves it to the call stack for execution.

5. This process of moving tasks from the task queue to the call stack is repeated as long as there are tasks in the queue.

By using the event loop, JavaScript can handle multiple asynchronous operations without blocking the execution of other code. It allows for the efficient handling of events, timers, and callbacks in web browsers and other JavaScript environments.

### 2. Promises :
it is an ES6 solution for asunchronous programming in javaScript
- it is initiate backgroung web browser
- work and return a placeholder object (promise) immediately in javaScript

```javascript
function display (data) {
  console.log(data);
}

const futureData = fetch('URL');
futureData.then(display);
console.log('Me first');
```
#### `.then()`
`then()` method is used in combination with promises to handle asynchronous operations and process the results or errors returned by those operations. The `then()` method is part of the Promise API and is used to specify what should happen after a promise is fulfilled (resolved) with a value or rejected with an error.

The `then()` method takes two callback functions as arguments: one for the success case (called when the promise is fulfilled) and one for the failure case (called when the promise is rejected).

#### Microtask queue
The microtask queue is where microtasks are queued for execution. Microtasks are tasks that need to be executed asynchronously but have a higher priority than regular tasks in the event loop. They are typically used for handling promises and other asynchronous operations that need to be resolved as soon as possible.

Problems
- 99% of developers have no idea how they’re working under the hood
- Debugging becomes super-hard as a result
- Developers fail technical interviews

  
Benefits
- Cleaner readable style with pseudo-synchronous style code
- Nice error handling process


## Examples 🔍

## Challenges 💪🏽

1.[Exercises for Async JS & Promises](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day3-tasks/tasks.md))

## Question 1:

You are given a function `executeInSequenceWithCBs` and some code. The task is to
modify the `executeInSequenceWithCBs` function so that it runs and executes all
the tasks inside the asyncTasks array. 

The function should return an array of messages obtained from each task's
execution.

You are only allowed to change the `executeInSequenceWithCBs` function or add new
functions/code. You cannot modify the tasks' functions.

```javascript

const task1 = (cb) => setTimeout(() => {
  const message = "Task 1 has executed successfully!";
  cb(message);
}, 3000)

const task2 = (cb) => setTimeout(() => {
  const message = "Task 2 has executed successfully!";
  cb(message);
}, 0)

const task3 = (cb) => setTimeout(() => {
  const message = "Task 3 has executed successfully!";
  cb(message);
}, 1000)

const task4 = (cb) => setTimeout(() => {
  const message = "Task 4 has executed successfully!";
  cb(message);
}, 2000)

const task5 = (cb) => setTimeout(() => {
  const message = "Task 5 has executed successfully!";
  cb(message);
}, 4000)

const asyncTasks = [task1, task2, task3, task4, task5];

const executeInSequenceWithCBs = (tasks, callback) => {}

```

-------------------------------------------------------------------

## Question 2:

You are given a function called `executeInParallelWithPromises`, which takes an
array of APIs (represented by objects). 

Your task is to write code that fetches the data of each API in parallel using
promises. In Parallel means that the api which resolves first, returns its value
first, regardless of the execution order. 

The output of the `executeInParallelWithPromises` function should be an array
containing the results of each API's execution.

Each result should be an object with three keys: `apiName`, `apiUrl`, and
`apiData`..

```javascript
const apis = [
  {
    apiName: "products", 
    apiUrl: "https://dummyjson.com/products",
  }, 
  {
    apiName: "users", 
    apiUrl: "https://dummyjson.com/users",
  }, 
  {
    apiName: "posts", 
    apiUrl: "https://dummyjson.com/posts",
  }, 
  {
    apiName: "comments", 
    apiUrl: "https://dummyjson.com/comments",
  }
]

const executeInParallelWithPromises = (apis) => {}

```

-------------------------------------------------------------------
## Question 3: 

You are given a function called `executeInSequenceWithPromises`, which takes an
array of APIs (represented by objects). 

Your task is to write code that fetches the data of each API sequentially (one
after the other) using promises. 

In Sequence means that the api which executes first, returns its value
first.

The output of the `executeInSequenceWithPromises` function should be an array
containing the results of each API's execution.

Each result should be an object with three keys: `apiName`, `apiUrl`, and
`apiData`.

```javascript

const apis = [
  {
    apiName: "products", 
    apiUrl: "https://dummyjson.com/products",
  }, 
  {
    apiName: "users", 
    apiUrl: "https://dummyjson.com/users",
  }, 
  {
    apiName: "posts", 
    apiUrl: "https://dummyjson.com/posts",
  }, 
  {
    apiName: "comments", 
    apiUrl: "https://dummyjson.com/comments",
  }
]

//modify and write your code here
const executeInSequenceWithPromises = (apis) => {}

```

# DONE 😇
