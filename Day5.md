#  Day5 (7/Jul/2023) 🚀

## Things to do ✔️

1. Watch This Topics from -JavaScript: From First Steps to Professional- course :
  - Data Fetching & Promises .
  - Destructuring Data .
  - Async .
  - Modules .
  - Wrapping up .
     
2. Summarize what i learned .
3. Solve some problems from FreeCodeCamp .
  

## Summary of topics 📝

### 1. Data Fetching & Promises :

#### Fetching data :

* URLs point to resources on the web *https://images.dog.ceo/breeds/bluetick/n02088632_924.jpg*
* APIs provide URLs that point at data we care about *https://dog.ceo/api/breed/hound/list*
```javascript
  {
    "message": [
      "afghan",
      "basset",
      "blood",
      "english",
      "ibizan",
      "plott",
      "walker"
    ],
    "status": "success"
  }
```
* **fetch()** lets us use JS to load data from APIs ` fetch("https://dog.ceo/api/breed/hound/list") `

#### Promises :

* It takes time to fetch data from the network
```javascript
>> fetch("https://dog.ceo/api/breed/hound/list")
Promise { <state>: "pending" }
```
> So JS writes us an "IOU" for the data value it doesn't have yet aka a Promise of a value

* Promises can be in 3 possible states:

- pending: still waiting for the value, hang tight
- fulfilled (aka "resolved"): finally got the value, all done
- rejected: sorry couldn't get the value, all done
 It takes time for Promises to resolve, so they are "asynchronous"

#### await :

* await lets us tell JS to stop and wait for an asynchronous operation to finish
* In the case of a Promise, it waits for it to resolve before continuing with our code
```javascript
let response = await fetch("https://dog.ceo/api/breed/hound/list");
console.log(response);
```
> The Promise we get from fetch() resolves to a Response object
* It's body contains the data we care about ,But we have to read the body somehow
* Calling the .json() method on the response parses its body as a JSON object ` response.json() ` But that gives us another Promise!
* this time awaiting the JSON Promise too
```javascript
let response = await fetch("https://dog.ceo/api/breed/hound/list");
let body = await response.json();
```

### 2. Destructuring Data :

#### Destructuring :

* Destructuring is a fancy way of declaring multiple variables at once By "extracting" values from an object with their property names
```javascript
let {name, nickname} = spices[0];
```

* If we only care about some of the properties, we can omit the others
```javascript
let {nickname} = spices[2];
```
* We can also destructure Arrays, assigning variables for their items
```javascript
const [baby, ginger, scary, sporty, posh] = spices;
```
* We can ignore the values in the array we don't need
```javascript
const [emma, geri] = spices; 
```
* We can use commas to "skip" values
```javascript
const [,,melB] = spices;
```
* We can use ... to collect remaining values
```javascript
const [babySpice, ...adultSpices] = spices;
```
> The **split()** method takes a pattern and divides a String into an ordered list of substrings by searching for the pattern, puts these substrings into an array, and returns the array.
```javascript
const str = 'The quick brown fox jumps over the lazy dog.';

const words = str.split(' ');
console.log(words[3]);
// Expected output: "fox"

const chars = str.split('');
console.log(chars[8]);
// Expected output: "k"

const strCopy = str.split();
console.log(strCopy);
// Expected output: Array ["The quick brown fox jumps over the lazy dog."]
```
> The **search()** method executes a search for a match between a regular expression and this String object.
```javascript
const paragraph = 'The quick brown fox jumps over the lazy dog. If the dog barked, was it really lazy?';

// Any character that is not a word character or whitespace
const regex = /[^\w\s]/g;

console.log(paragraph.search(regex));
// Expected output: 43

console.log(paragraph[paragraph.search(regex)]);
// Expected output: "."
```
> The trim() method removes whitespace from both ends of a string and returns a new string, without modifying the original string.
  To return a new string with whitespace trimmed from just one end, use trimStart() or trimEnd().
```javascript
const greeting = '   Hello world!   ';

console.log(greeting);
// Expected output: "   Hello world!   ";

console.log(greeting.trim());
// Expected output: "Hello world!";
```

### 3. Async :

#### async functions :

* If we try to await something in a regular function...
```javascript
function fetchResponse(url) {
    const response = await fetch(url);
    return response;
}
```
> JS doesn't allow it
* We need to make it an async function
```javascript
async function fetchResponse(url) {
    const response = await fetch(url);
    return response;
}
```
> This tells JS to expect to await async operations inside the function


### 4. Modules :

#### Modules :

* Modules let us split big codebases across multiple files
* Take a closer look at our script tag:
```javascript
<script type="module">
    //...
</script>
```
> JS modules work differently from JS scripts
* One difference is that we can't use await outside of a function in a script
```javascript
<script>
    await fetch("https://dog.ceo/api/breed/hound/list");
</script>
```
* Module scope Another difference is that modules create their own scope

#### import && export :
* **export** lets us expose variables from our module's scope to the outside world
```javascript
// myModule.js
const veryUsefulFunction = () => "I came from a module";
export { veryUsefulFunction };
```
* import lets us use an exposed variable from another module
```javascript
// otherModule.js
import { veryUsefulFunction } from './myModule.js'

veryUsefulFunction();
```
#### Debugging :

* console.log() (or .warn() or .error()) is one way to understand what's happening when your program runs
```javascript
function whyIsntThisWorking(input) {
    console.log("Well at least we got this far");
    console.log(input);
    return thingThatDoesntWork(input);
}
```
* You can also use the browser's debugger to pause JS and inspect what's happening
```javascript
function whyIsntThisWorking(input) {
    debugger;
    return thingThatDoesntWork(input);
}
```
> The debugger statement creates a breakpoint where JS will pause and let you look around
* Different browsers' debuggers work differently
  - Firefox
  - Chrome
  - Safari

 #### Error handling :

 * Once we've discovered where in our program an error is likely, we can do something about it!
 * Usually errors will cause JS to stop running our code
```javascript
thisThrowsAnError();
console.log("I'll never get here");
```
> Sometimes that's appropriate and what we want JS to do
* try lets us "watch out" for potential errors its friend catch lets us manage errors when they occur
```javascript
try {
    thisMightThrowAnError();
} catch (error) {
    console.error("As if! Error:", error); 
    console.log("Whatever, let's press on anyway");
}
console.log("still rollin' with the homies");
```



## Challenges 💪🏽

1. [Task requirements](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week1-day3-task/task.md)

**Solution**

```
```


# DONE 😇
