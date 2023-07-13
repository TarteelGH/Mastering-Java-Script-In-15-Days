#  Day1 (3/Jul/2023) 🚀

## Things to do ✔️

1. Watch This Topics from -JavaScript: From First Steps to Professional- course :
  - Intrudoction .
  - Dom .
  - Value & Data Types .
  - Operators .
2.  Summarize what I learned .
3. Solve some problems from FreeCodeCamp .
  

## Summary of topics 📝

 ### 1. Introduction :

 - JavaScript is a dynamic programming language used usually in websites .
 - Created in 1995 by Brendon Eich.
 - Used to modify and interact with HTML.

***How Where do we write JS?***

 The browser's JS console
 Local text file in editor, e.g. TextEdit, VS Code
 Online playground e.g. CodePen, CodeSandbox

 ***How to do it?***
 
Open 1-tictactoe.html in your browser
(File > Open file...)
Inspect the page to open DevTools
(Right click > Inspect)
Click on Console tab

### 2. DOM (Document Object Model) :

#### Reading the DOM with JS
Let's dig into this document!

- `document` = the entire HTML document
- `document.title` = the page (document) title
- `document.body` = the body element
- `document.body.children` = all the elements within the body
- `document.getElementById("board")` = the (first) element with id="board"
- `document.getElementsByTagName("h1")` = all the h1 elements
- `document.getElementsByClassName("player")` = all the elements with class="player"
- `document.getElementsByClassName("player").length` / `document.querySelectorAll(".player").length` = the number of elements with class="player"
- `document.getElementById("p1-name").textContent` = the text inside the element with id="p1-name"

#### Editing the DOM with JS

- `document.title = "My Page"` = change the page title = change the page title/note the double-quotes
- `document.getElementById("p1-name").textContent = "Sofia"` = replace the text of the #p1-name element
- `document.getElementById("p1-name").append(" & friends")` = add to the end of the element's current text

### 3. Values & Data Types :

- Values : chunks of information we want to work with that information (data) can be of different types
- typeof : tells you the type of a value
- JS has two kinds of data:
    - Primitive types :
        - string
        - number
        - boolean
        - undefined = accidental nothing
        - null = deliberate nothing
    - Objects (e.g. document & friends)

### 4. Operators :
- Arithmetic operators
  - ( + )add
  - ( - )subtract
  - ( * )multiply
  - ( / )divide
- Comparison operators
  - ( > ) greater than
  - ( < )less than
  - ( >= )greater than or equal to
  - ( <= )less than or equal to
    
## Examples 🔍
1.
```javascript
<body>
    <header>
    <h1>Tic Tac Toe</h1>
    <h2>A game you know</h2>
    <div id="players">
        <p id="p1" class="player">Player <span id="p1-symbol">X</span>: <span id="p1-name">Anjana</span></p>
        <p id="p2" class="player">Player <span id="p2-symbol">O</span>: <span id="p2-name">Marc</span></p>
    </div>
    </header>
    <div id="board">
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
        <div class="square"></div>
    </div>
</body>
document.getElementsByTagName("p")                       = will return all p elements which are p1 & p2
document.querySelectorAll(".square").length              = will return the number of elements that have the class square which are 9
document.querySelector("h2").textContent                 = will return the text inside the element h2 which is "A game you know"
document.getElementById('p2-name').textContent = "Majd"  = will change the second player name to Majd
document.getElementById('p2-name').append(" & Sara")     = will add sara to the sacond player
document.querySelector("header h2").append(" and love")  = will append "and love" to the second header  
```
__________________________________________________________
2.
```
"super".length                 OutPut = 5
"ALOHA"[2]                     OutPut = O
"ALOHA".indexOf("L")           OutPut = 1
"ALOHA".indexOf("Q")           OutPut = -1
"ALOHA".includes("HA")         OutPut = 3
"ALOHA".startsWith("AL")       OutPut = True
"ALOHA" + "!"                  OutPut = ALOHA!
"ALOHA".toLowerCase()          OutPut = aloha
typeof document.title          OutPut = String
typeof "some string".length    OutPut = Number
typeof null                    OutPut = Object
```


## Challenges 💪🏽

1.[Compound Assignment With Augmented Multiplication](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/compound-assignment-with-augmented-multiplication)

***Solution***
```javascript
let a = 5;
let b = 12;
let c = 4.6;

// Only change code below this line
a *= 5;
b *= 3;
c *= 10;
```

2.[Concatenating Strings with the Plus Equals Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/concatenating-strings-with-the-plus-equals-operator)

***Solution***

```javascript
let myStr;
myStr = "This is the first sentence.";
myStr += " This is the second sentence.";
```

3.[Use Bracket Notation to Find the Nth-to-Last Character in a String](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-bracket-notation-to-find-the-nth-to-last-character-in-a-string)

***Solution***

```javascript
// Setup
const lastName = "Lovelace";

// Only change code below this line

const secondToLastLetterOfLastName = lastName[lastName.length - 2]; // Change this line

```

# DONE 😇







