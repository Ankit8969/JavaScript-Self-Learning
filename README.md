## About JavaScript
- JavaScript was initially created to  ***make web pages alive.***
- Today, JavaScript can execute not only in the browser-
-  but also on the server actually on any device that has a special program called the JavaScript engine.

## How do engines work?
  - The engine (embedded if it’s a browser) reads (“parses”) the script.
  -  Then it converts (“compiles”) the script to the machine language.
  - And then the machine code runs, pretty fast.

## Learn About Script Tag
***In <script> </script> tag we also have two more attribute "language" and "type" but we are not using now-a-days***
```
If you want to use the multitple "js" file in your html file you can use multitple script
<script src="/js/script1.js"></script>
<script src="/js/script2.js"></script>
```

## If src is set, the script content is ignored.
> A single <script> tag can’t have both the src attribute and code inside.
This won’t work:

```
  <script src="file.js">
  alert(1); // the content is ignored, because src is set
</script>
We must choose either an external <script src="…"> or a regular <script> with code.

The example above can be split into two scripts to work:

<script src="file.js"></script>
<script>
  alert(1);
</script>
```
  
# Data Types in JavaScript
- Number
- BigINt
- Boolean
- Null
- Undefined
- Object
- String
  
 
# Modals in JavaScript
  - Alert ***It is used to only show the message***
  - Prompt ***It is used to ask some question***
  - Confirm ***It contains two button ok and cancel if user clikc on OK it return true otherwise false***
 
# Object in JavaScript
  ```
  > Object is not-Premitive data type
> An object can be created with figure brackets {…} with an optional list of properties. 
    A property is a “key: value” pair, where key is a string (also called a “property name”), and value can be anything.

/* Creating an empty object, we have to ways */

let user = new Object(); // "object constructor" syntax
let user = {};  // "object literal" syntax

/* You can also add a new key value pair like this */
let a = {
  name: "ankit",
  roll: "23",
};
a.school = "makaut";


/* you can also delete a key value pair */
let a = {
  name: "ankit",
  roll: "23",
};
a.school = "makaut";
delete a.name;

  ```
  
  
#Square Bracket in Object
  ```
    >For accesing the multivalue property
    > By using dot we can't access the the multivalue property

    let user = {};
    // set
    user["likes birds"] = true;
    // get
    alert(user["likes birds"]); // true
    // delete
    delete user["likes birds"];

    ###Computed Properties in Object 

    let x = "name";

    let obj = {
      [x]: "ankit",
    };

    console.log(obj);
  ```
  
  # Check Existing property or not
    - We have to ways to check the propery is present or not 
  ```
      let x = {};

      if (x.ankit === undefined) {
        console.log("Not present");
      } else {
        console.log("Present");
      }
  ```
  ## you can also check like this
  ```
    let x = {};
    if ("age" in x) {
      console.log("present");
    } else {
      console.log("not Present");
    }
  ```
  ## you can also run the loop
  ```
    let user = {
      name: "ankit",
      age: 20,
      school: "Makaut",
    };

    for (let key in user) {
      console.log(key);
      console.log(user[key]);
    }

  ```
  
  ## you also add the new value in the object like this
  ```
    let x = {
    name: "Ankit",
    };
    Object.assign(x, { age: 20, lapto: "Air" });
    console.log(x);
  ```
  ## copy the value of object we have two way
  - let temp = [...obj]
  - JSON.parse(JSON.stringify(x));
  - ***but the difference is those value undefined that value it don't copy***
  
  ## you can also write the function in the object
  ```
    let obj = {
      xyz() {
        console.log("check");
      },
      name: "Ankit",
    };
  ```
  
  # 'this' in object
  ```
      let user = {
      name: "John",
      age: 30,

      sayHi() {
        alert(this.name);
      },
    };

    user.sayHi();
  ```
  
# Optional Chaining in Object
  ```
  const user = {};
  console.log(user.name); ***it give undefined***
  ```
  ```
  console.log(user.name.something); ***it give error***
  console.log(user.name?.age);
  ```
  
# MAP and SET in Java Script
   ## Map is a collection of keyed data items, just like an Object. But the main difference is that Map allows keys of any type.
    - Methods and properties are:
    - new Map() – creates the map.
    - map.set(key, value) – stores the value by the key.
    - map.get(key) – returns the value by the key, undefined if key doesn’t exist in map.
    - map.has(key) – returns true if the key exists, false otherwise.
    - map.delete(key) – removes the value by the key.
    - map.clear() – removes everything from the map.
    - map.size – returns the current element count.

************************************
  ```
  let map = new Map();
  map.set(2, 1);
  map.set(3, 1);
  map.set(4, 1);
  map.set(5, 1);
  map.set(7, 2);
  map.set(7, map.get(7) === undefined ? 1 : map.get(7) + 1);
  console.log(map);
  ```

**************************************************************************
## FOR MAP VALUES ITERATION
```
  let recipeMap = new Map([
    ['cucumber', 500],
    ['tomatoes', 350],
    ['onion',    50]
  ]);

  // iterate over keys (vegetables)
  for (let vegetable of recipeMap.keys()) {
    alert(vegetable); // cucumber, tomatoes, onion
  }

  // iterate over values (amounts)
  for (let amount of recipeMap.values()) {
    alert(amount); // 500, 350, 50
  }

  // iterate over [key, value] entries
  for (let entry of recipeMap) { // the same as of recipeMap.entries()
    alert(entry); // cucumber,500 (and so on)
  }
```
********************************************************************************

  # Set 
  ***A Set is a special type collection – “set of values” (without keys), where each value may occur only once.***
  
  - Its main methods are
  - new Set(iterable) – creates the set, and if an iterable object is provided (usually an array), copies values from it into the set.
  - set.add(value) – adds a value, returns the set itself.
  - set.delete(value) – removes the value, returns true if value existed at the moment of the call, otherwise false.
  - set.has(value) – returns true if the value exists in the set, otherwise false.
  - set.clear() – removes everything from the set.
  - set.size – is the elements count.
  ```
  It store the unique value but not in sorted order
  Iteration over set
  for (let x of set) console.log(x);
  ```
  
# Array Method
  ```
  let arr = []
  arr.push(45);
  arr.pop();
  arr.shift()  it remove the first element, and also shrink the array size.

  arr.unshift("Ankit") it add the data at the beginning
  ```
  ### You can also write like this
  ```
  let arr = new Array(1, 2, 3);
  console.log(arr);
  ```
  
  *****************************************************************************************
  ```
  let arr = [1, 2, 3, 4];

  // delete arr[2];
  arr.splice(1, 2); // it remove the item from the array starting position from 1 and erase 2 item

  // it remove the items and push these three string
  arr.splice(1, 1, "ankit", "kumar", "yadav");

  arr.splice(1, 0); // it don't remove any element

  console.log(arr);
  ```

********************************************************************************************************
  ```
  let arr = [1, 2, 3, 4];
  // for each method for array traversing
  arr.forEach((value) => console.log(value));
```
****************************************************
##Searching Property( All three searching property takes 2 argument second one was optional)
1. indexOf()
  
  - let arr = [1,2,3,4];
  - const t = arr.indexOf(3);
  - if value is present in the array it give the index otherwise it give -1

2. arr.lastIndexOf(item, from) – same, but looks for from right to left.
3. arr.includes(item, from) – looks for item starting from index from, returns true if found.

*********************************************************************************************
##Find Method in Array
  ```
  // If not present it gives undefined

  let arr = [
    { name: "Ankit", id: 2 },
    { name: "sonu", id: 1 },
    { name: "MAnish", id: 3 },
  ];

  let user = arr.find((data) => data.name === "Ankit");
  console.log(user);
  ```

*********************************************************************************************
##Filter Method 
  ```
  let arr = [
  { name: "Ankit", id: 2 },
  { name: "sonu", id: 1 },
  { name: "MAnish", id: 3 },
  ];

  let temp = arr.filter((value) => value.id >= 2);
  console.log(temp);
  ```

***********************************
# Sorting in array
  ```
  let arr = [ 1, 2, 15 ];

  // the method reorders the content of arr
  arr.sort();

  alert( arr );  // 1, 15, 2
  ```
  
# Destructing in Object
  let arr = ["ankit", "kumar"];

let [first, second, third] = arr;
console.log(first, second, third);

In COnsole -> ankit kumar undefined

*********************
  ## Actually, we can use it with any iterable, not only arrays:
  ```
  let [a, b, c] = "abc"; // ["a", "b", "c"]
  let [one, two, three] = new Set([1, 2, 3]);
  ```
*********************************
```
let obj = {
  name: "Ankit",
  roll: "2",
};

for (let [key, value] of Object.entries(obj)) console.log(key, value);
```

******************************************************
  ```
let arr = [1, 2, 3, 4, 5, 6];

let [first, second, ...third] = arr;
console.log(first, second, third);
```

********************************************
  ```
let obj = {
  names: "Ankit",
  roll: 20,
};

const { names, roll } = obj;
console.log(names, roll);
  ```

****************************************


## "..." is rest operator ***Spread Operator***
  ### For Time Method
  - let obj = new Date();
  - console.log(obj.getFullYear());
  - console.log(obj.getMonth());
  - console.log(obj.getDate());
  - console.log(obj.getHours());
  - console.log(obj.getMinutes());
  - console.log(obj.getSeconds());

 
# JSON in java-script
  - IF we want to send some data to the server then we convert it to "JSON"
  - JSON.stringify to convert objects into JSON.
  - JSON.parse to convert JSON back into an object.
  ```
    let student = {
      name: "John",
      age: 30,
      isAdmin: false,
      courses: ["html", "css", "js"],
      wife: null,
    };

    let obj = JSON.stringify(student);
    console.log(obj);

    obj = JSON.parse(obj);
    console.log(obj);
  ```

  # How to sort object in javascript 
***We can sort the array of object like this***
  ```
let arr = [
  {
    name: "Ankit",
    roll: 2,
  },
  {
    name: "Sonu",
    roll: 1,
  },
  {
    name: "Aankit",
    roll: 5,
  },
  {
    name: "Rohan",
    roll: 2,
  },
];

arr.sort((a, b) => (a.name > b.name ? 1 : -1));

console.log(arr);
  ```
  ```
let arr = [];
arr.push(2);
arr.push(3);
arr.push(2, 3, 4);
// Size will be 5
```
  
***************************************************
```
function sum(x,y,...z){
    console.log(x);
    console.log(y);
    console.log(z); // z will print the array which contain [4,5,6,4]
};

sum(2,3,4,5,6,4)
  ```
****************************************************

## Blocks for let and const

## If a variable is declared inside a code block {...}, it’s only visible inside that block.
```
function sum() {
  let x = 2;
  return function () {
    let z = 2;
    return x + z;
  };
}

let z = sum();
console.log(z());

It prints 4 because of closure
```
***********************************************************************

# setTimeout() in JS
  ```
    function sum(x, y) {
      console.log(x + y);
    }

    let t = setTimeout(sum, 5000, 2, 3);

    let t2 = setTimeout(sum, 5000, 2, 4);

    clearTimeout(t2);

    console.log(t, t2);
  ```

- set time out returns a timerId
- you can also clear that Timer, once you clear that id than that funciton will not call in future 

***********************************************************************************************************
## Using setTimeout and setInterval together
```
// repeat with the interval of 2 seconds
let timerId = setInterval(() => console.log("start"), 2000);

// after 5 seconds stop
setTimeout(() => {
  clearInterval(timerId);
  console.log("stop");
}, 5000);
```
****************************************************************************

## Zero delay setTimeout
  - setTimeout(func, 0), or just setTimeout(func).


# Inheritance in Object
  ```
let animal = {
  eats: true,
};
let fox = {
  jumps: true,
};

fox.__proto__ = animal;

console.log(fox.eats);
```
*******************************************
  ```
let animal = {
  eats: true,
  walk() {
    alert("Animal walk");
  }
};

let rabbit = {
  jumps: true,
  __proto__: animal
};

// walk is taken from the prototype
rabbit.walk(); // Animal walk
```
  
****************************************************
  ```
You can also write Like this 
let animal = {
  eats: true,
  walk() {
    /* this method won't be used by rabbit */
  },
};

let rabbit = {
  __proto__: animal,
};

rabbit.walk = function () {
  alert("Rabbit! Bounce-bounce!");
};

console.log(rabbit);
```
***************************************************************
  
# Classes in JavaScript

***The “class” syntax***
- The basic syntax is:
```
class MyClass {
  // class methods
  constructor() { ... }
  method1() { ... }
  method2() { ... }
  method3() { ... }
  ...
}
  ```

************************************************
```
class User {
  constructor(name) {
    this.name = name;
  }
  sayHi() {
    console.log(this.name);
  }
}

let user = new User("Ankit");
user.sayHi();
```
**************************************************************************************************

## Inheritance in Class
```
class Animal {
  constructor(name) {
    this.speed = 0;
    this.name = name;
  }
  run(speed) {
    this.speed = speed;
    console.log("Run Function " + this.speed);
  }
  stop() {
    this.speed = 0;
    console.log("Stop Function " + this.name);
  }
}

let animal = new Animal("My animal");

class Rabbit extends Animal {
  hide() {
    console.log("hides Function");
  }
}
let rabbit = new Rabbit("White Rabbit");

rabbit.run(5); // White Rabbit runs with speed 5.
rabbit.hide(); // White Rabbit hides!
```

## Try and Catch block
  ```
  
try {
    console.log("Start of try runs");
    dfdfdf;
    console.log("End of try runs");
  } catch (err) {
    console.log(err.name); // ReferenceError
    console.log(err.message); // lalala is not defined
    console.log(err.stack);
  }
  ```

  # Callback in JS
  ***Passing a function to another function as an argument this is known as Callback***
  ```
  
const post = [
  { title: "First Post" },
  { title: "Second Post" },
  { title: "Third Post" },
];

function getPosts() {
  let t = "";
  setTimeout(() => {
    post.forEach((item) => {
      t += `<li>${item.title}</li>`;
    });
    document.body.innerHTML = t;
  }, 2000);
}

// getPosts();

function createPost(temp, callback) {
  setTimeout(() => {
    post.push(temp);
    callback();
  }, 3000);
}
createPost({ title: "forth post" }, getPosts);
  ```
 
# Promise in JS
```
  const post = [
  { title: "First Post" },
  { title: "Second Post" },
  { title: "Third Post" },
];

function getPosts() {
  let t = "";
  setTimeout(() => {
    post.forEach((item) => {
      t += `<li>${item.title}</li>`;
    });
    document.body.innerHTML = t;
  }, 1000);
}

function createPost(temp) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      post.push(temp);
      reject("error something goes wrong");
    }, 2000);
  });
}

createPost({ title: "forth post" })
  .then(() => {
    getPosts();
  })
  .catch((e) => console.log(e));
```
  
# PROMISE AND FETCH 
  ```
  const promise1 = Promise.resolve("Hello World");
const promise2 = 10;
const promise3 = new Promise((resolve, reject) => {
  setTimeout(resolve, 2000, "How are you!");
});

const promise4 = fetch("https://jsonplaceholder.typicode.com/users").then(
  (res) => res.json()
);

Promise.all([promise1, promise2, promise3, promise4]).then((values) =>
  console.log(values)
);
  ```
  
# Async Await
  ```
  const post = [
  { title: "First Post" },
  { title: "Second Post" },
  { title: "Third Post" },
];

function getPosts() {
  let t = "";
  setTimeout(() => {
    post.forEach((item) => {
      t += `<li>${item.title}</li>`;
    });
    document.body.innerHTML = t;
  }, 1000);
}

function createPost(temp) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      post.push(temp);
      resolve();
    }, 2000);
  });
}

async function init() {
  await createPost({ title: "Fourth" });
  getPosts();
}
init();
  ```
  
  ***********************************************
### WE CAN ALSO WRITE LIKE THIS

```
async function fetchUsers() {
  const res = await fetch("https://jsonplaceholder.typicode.com/users").then(
    (res) => res.json()
  );
  console.log(res);
}

fetchUsers();
  
  ```
  
  # Hoisting in JS
    - Hoisting is a phenomena where you can access the variable and function before its initialization.
```
  console.log(x);
console.log(add(2, 4));

var x = 4;
function add(x, y) {
  return x + y;
}
```
```
  Output - 
  undefined
  6
```

### but in case of "let" and "const" If you are trying to access the varibale it gives you "Reference" Error

## Scope Definition
  - The part of the code where you can access the specific variable 
  
## Scope Chain
- In this code first second() will find b inside the scope of second function, and then it find the scope of first function then it will find the global memory scope
- this is callled as scope chaining
  ```
    function first() {
      function second() {
        console.log(b);
      }
      second();
    }
    var b = 20;
    first();
  ```

## Block in JS
- We can use block by using {} these curly braces
- Definition ***block are used to combine  multiple statement such that JavaScript runs all the command assuming to be a single statement.***

## Shadowing in JS
  - shadowing is the concept where the vaule of variable is changed in the global memory scope
  - But it won't work in case of let and const
  ```
  var a = 20;
  {
    var a = 1;
    let b = 2;
    const c = 3;

    console.log(a, b, c);
  }
  console.log(a);
  ```

# Closure
  - Function bundled with its lexical environment is known as a closure. Whenever function is returned, 
  even if its vanished in execution context but still it remembers the reference it was pointing to. 
  - Its not just that function alone it returns but the entire closure and that's where it becomes interesting.
  ```
    function x() {
        let a = 20;
        function y() {
          console.log(a);
        }
        return y;
      }

      let z = x();
      z();
  ```
## Anonemous Function
  ### Function without name are called Anonemous Function
```
  (function () {
  console.log("Check");
})();

```

# Function Statement
  ```
  function a(){
    console.log("Check")
  }
  ```
# Function Expression
  ```
  const b = function (){
    console.log("Check")
  }
  ```
- The main difference b/w function statement and function expression is the hoisting

# Named Function Expression
  ```
  var b = function xyz(){
      console.log("Check")
  }
  b();
  xyz()// it gives you error
  ```

# Parameter and Argument
  ```
  function sum(a, b)  // parameter
  {
  }
  sum(2,4)  // argument
  ```
  
# First Class Function / First class citizen
  - the ability of function to be used as value and passed to a function and return from a function is known as first class function.

```
  var b = function (param) {
  function xyz() {
    param();
    console.log("Check");
  }
  return xyz;
};

function sum() {
  console.log("Sum function");
}

b(sum)();
```
  
# Arrow Function 
```
  const x = ()=>{};
```
  
## JavaScript is synchronous single threaded language it means it runs one command at a time in specific order.
  
#CallBack
- when you pass a function to a another function as an argument this is called as Callback function
- Sum function is called as CallBack function
```
  function b(param) {
  param();
}

function sum() {
  console.log("Sum function");
}

b(sum);

```
  
- then why the name is callback because we call that function sometime letter in our code that's why named is CallBack function.
  

## Axios Call get and post
  ```
  import axios from "axios";
import React from "react";

const baseURL = "https://jsonplaceholder.typicode.com/posts";

export default function App() {
  const [post, setPost] = React.useState(null);

  React.useEffect(() => {
    axios.get(`${baseURL}/1`).then((response) => {
      setPost(response.data);
    });
  }, []);

  function createPost() {
    axios
      .post(baseURL, {
        title: "Hello World!",
        body: "This is a new post.",
      })
      .then((response) => {
        setPost(response.data);
      });
  }

  if (!post) return "No post!";

  console.log(post);
  return (
    <div>
      <h1>{post.title}</h1>
      <p>{post.body}</p>
      <button onClick={createPost}>Create Post</button>
    </div>
  );
}

  ```
  
  
# call, apply and bind method

## Call() Method
  - In call() method we pass the argument by seprating with comma ','
  ```
      let obj1 = {
      fname: "Ankit",
      lname: "Yadav",
      giveFull: function () {
        console.log(this.fname, this.lname);
      },
    };

    let externals = function (home, city) {
      console.log(`My name is ${this.fname}`);
      console.log(`My hometown is ${home} ${city}`);
    };

    obj1.giveFull();

    let obj2 = {
      fname: "sonu",
      lname: "kumar",
    };
    
    *** Function Borrowing***
    obj1.giveFull.call(obj2);
    
  externals.call(obj2, "Bihar", "forbesganj");

  ```
  
  
## apply() method 
  - In apply() method we pass the argument in the array
  
  ```
      let obj1 = {
      fname: "Ankit",
      lname: "Yadav",
      giveFull: function () {
        console.log(this.fname, this.lname);
      },
    };

    let externals = function (home, city) {
      console.log(`My name is ${this.fname}`);
      console.log(`My hometown is ${home} ${city}`);
    };

    obj1.giveFull();

    let obj2 = {
      fname: "sonu",
      lname: "kumar",
    };

    obj1.giveFull.apply(obj2);
    externals.apply(obj2, ["Bihar", "forbesganj"]);

  ```
  
  
 ## bind() method
  - the basic difference b/w call() and bind() method is in bind() method it returns a function and we can use that function later.
  
  ```
      let obj1 = {
      fname: "Ankit",
      lname: "Yadav",
      giveFull: function () {
        console.log(this.fname, this.lname);
      },
    };

    let externals = function (home, city) {
      console.log(`My name is ${this.fname}`);
      console.log(`My hometown is ${home} ${city}`);
    };

    obj1.giveFull();

    let obj2 = {
      fname: "sonu",
      lname: "kumar",
    };

    obj1.giveFull.call(obj2);
    externals.apply(obj2, ["Bihar", "forbesganj"]);

    let temp = obj1.giveFull.bind(obj2, "Bihar", "Forbesgaj");
    console.log(temp);
    temp();
  ```
  ## It gives you undefined holes in the array
  ```
  const fruits = ["Banana", "Orange", "Apple"];
  fruits[6] = "Lemon";  // Creates undefined "holes" in fruits
```

## Creating the empty array 
  ```
  // Create an array with 40 undefined elements:
const points = new Array(40);  
  ```
  
## Warning !
Array elements can be deleted using the JavaScript operator delete.

Using delete leaves undefined holes in the array.

Use pop() or shift() instead.
```
  const fruits = ["Banana", "Orange", "Apple", "Mango"];
delete fruits[0];
  ```
##Merging Two Arrays
  ```
  const myGirls = ["Cecilie", "Lone"];
  const myBoys = ["Emil", "Tobias", "Linus"];

  const myChildren = myGirls.concat(myBoys);
  ```

  ```
  const myChildren = arr1.concat(arr2, arr3);
  ```
##The slice() method slices out a piece of an array into a new array.

```
  const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(1, 3);
  ```
```
  let arr = [1,2,3,4,5,6];

// For each is only to used for iteration
let t = arr.forEach((data)=>{
    return data;
});
console.log(t);

// In map method it creates the new array
let t2 = 2;
arr.map((data, index, arr)=>{
    console.log(data, index, arr)
})
console.log(arr);
console.log(t2);


// It gives the new array
let t3 = arr.filter((data)=>{
    return data>4;
})
console.log(t3);

```
## RegExp 
- In JavaScript, regular expressions are often used with the two string methods: search() and replace().
- The search() method uses an expression to search for a match, and returns the position of the match.
- The replace() method returns a modified string where the pattern is replaced.

  
```
  let text = "Visit W3Schools";
  let n = text.search(/w3schools/i);
```

## We can also use try and catch like this
  ```
  <p id="demo"></p>

<script>
try {
  adddlert("Welcome guest!");
}
catch(err) {
  document.getElementById("demo").innerHTML = err.message;
}
</script>
  ```
  
##The throw Statement
***The throw statement allows you to create a custom error***
  
```
throw "Too big";    // throw a text
throw 500;          // throw a number
```
  
##The finally Statement
```
  try {
  Block of code to try
}
catch(err) {
  Block of code to handle errors
}
finally {
  Block of code to be executed regardless of the try / catch result
}
```
  

## Scope
- Js have three type of scope
- Block Scope  {}
- Function Scope
- Global Scope



## "use strict"; Defines that JavaScript code should be executed in "strict mode".
  
## Modules

- JavaScript modules allow you to break up your code into separate files.
- This makes it easier to maintain the code-base.
- JavaScript modules rely on the import and export statements.
  

  ## more about JSON

- JSON stands for JavaScript Object Notation
- JSON is a lightweight data interchange format
- JSON is language independent *
- JSON is "self-describing" and easy to understand

  ```
  {
"employees":[
  {"firstName":"John", "lastName":"Doe"},
  {"firstName":"Anna", "lastName":"Smith"},
  {"firstName":"Peter", "lastName":"Jones"}
]
}
  ```
  
## The debugger Keyword

- The debugger keyword stops the execution of JavaScript, and calls (if available) the debugging function.
- we are making dubug in source tab in console
  
```
let x = 15 * 5;
debugger;
document.getElementById("demo").innerHTML = x;
```
## Fill the array with zeros
```
let arr = new Array(23).fill(0);
console.log(arr);
```
  ```
  
temporal dead zone- the temporal dead zone (TDZ) refers to the period of 
 time between the creation of a variable using the let or const keyword, and the 
 point at which the variable is initialized with a value. During the TDZ, if you try to access 
 the variable, you will get a ReferenceError because the variable is not yet defined.

 // reference error, syntax error, type error 
Reference Error:
A reference error occurs when you try to use a variable or function that 
has not been declared or is out of scope.

Syntax Error:
A syntax error occurs when there is a mistake in the syntax of your code. This can happen when you forget a closing bracket, misspell a keyword, 
or make some other syntax mistake

Type Error:
A type error occurs when you try to use a value 
that is not of the expected type

# Basic difference b/w var let, and const;
In summary, var has function scope, let and const have block scope. var can be redeclare 
and updated, let can be updated but not redeclare, and const cannot be updated or 
redeclare.

Eg. Function Scope
function a(){
    var x = 2;
    console.log(x);
}
a();

Eg. Block Scope
function b(){
    if (true){
        let x = 3;
        console.log(x);
    }
    console.log(x);
}
b();

# Block in JS
 a block is a set of statements enclosed in curly braces {}. Blocks are used to group statements together 
 into a single unit, and they can be used wherever a single statement is expected, 
 such as in loops, if statements, or function definitions.

 # we have two type of scope in javascript
 1. Global scope
 var x = 10; // Global variable

function myFunction() {
  console.log(x); // Output: 10 (accessing global variable)
}

myFunction();
console.log(x); // Output: 10 (accessing global variable)

 2. Local scope
 function myFunction() {
  var x = 10; // Local variable
  console.log(x); // Output: 10 (accessing local variable)
}

myFunction();
console.log(x); // Output: Error (x is not defined)


# Shadowing in JavaScript
Shadowing in JavaScript occurs when a variable declared in an inner scope has the same name as a variable 
declared in an outer scope. In this situation, the inner variable "shadows" the outer variable, meaning that 
the inner variable takes precedence and the outer variable becomes temporarily inaccessible.

var x = 10; // Global variable

function myFunction() {
  var x = 20; // Local variable with same name as global variable
  console.log(x); // Output: 20 (accessing local variable)
}

myFunction();
console.log(x); // Output: 10 (accessing global variable)

# Illegal shadowing
Illegal shadowing in JavaScript occurs when a variable in an inner scope has the same name as a variable in an outer scope, 
but the inner variable is declared with a different type of declaration keyword (let or const) than the outer variable 
(var or another let/const declaration). This can lead to unexpected results because the inner variable does not actually shadow the outer variable, but instead creates a new variable with the same name.

var x = 10; // Global variable

function myFunction() {
  let x = 20; // Illegal shadowing (let instead of var)
  console.log(x); // Output: 20 (accessing local variable)
}

myFunction();
console.log(x); // Output: 10 (accessing global variable)

# Block also follows the lexical chaining 

# CLOSURE:

A closure is the combination of a function bundled together (enclosed) with references to its surrounding 
state (the lexical environment).

In JavaScript, a closure is created when a function "remembers" the variables and parameters that were in its outer lexical environment (scope) when it was declared, even if 
those variables and parameters are no longer in scope when the function is called. 
This allows the function to access and manipulate those variables and parameters as if they were still in scope, even though they would normally be inaccessible or undefined.
Closures are created automatically when a function is defined inside another function, and can be used to create private variables and functions that are hidden from the global 
scope and can only be accessed by the outer function.

function outerFunction(x) {
  function innerFunction(y) {
    return x + y; // Accessing x from outer function's scope
  }
  return innerFunction;
}

var add5 = outerFunction(5); // Creates a closure with x = 5
console.log(add5(3)); // Output: 8 (accesses x = 5 from closure and y = 3 from function call)



# Function Statement
function myFunction() {
  var x = 10; // Local variable
  console.log(x); // Output: 10 (accessing local variable)
}

# Function Expression
const myFunctionExpression = function(){
  var x = 10; // Local variable
  console.log(x); // Output: 10 (accessing local variable)
}

# Anonymous Function
it is use when we need to assign a function to a variable
var greeting = function(name) {
  console.log("Hello, " + name + "!");
};
greeting("John"); // Outputs "Hello, John!"


# Named functions expression
const myNamedFunctionExpression = function xyz(name) {
  console.log("Hello, " + name + "!");
};
we can't call a function like xyz() it gives error.

# diff b/w params and arguments
function myFunction(params1, params2) {
  console.log(params1 + " " + params2);
}
myFunction(argue1, argue2)


# First class function
function are also first class citizen.
In JavaScript, functions are considered first-class citizens, which means they are treated like 
any other value, such as a number or a string. This allows functions to be passed as arguments to other functions, 
returned from functions, and stored in variables or data structures.

# CallBack functions
passing a function as an argument

# JavaScript is a synchronous and single-threaded language.

# Best example two handle the global variable using closures
function attachEventListener(){
  let count = 0 ;
  document.getElementById('btn').addEventListener("click", function(){
    count++;
    console.log(count);
  });
}
attachEventListener();

# closure function is heavy, it make our webpage slow
so, when we don't use eventListener then we should have remove this.

# CallStack 
it follows the "Stack" data structure
when every we run any code of JS first it create a execution context and push it onto the stack


# Callback Queue
A callback queue in JavaScript is a queue that holds callbacks that are waiting to be executed. 
Eg: 
function callbackFunction() {
  console.log("Callback function executed");
}

console.log("Before timeout");
setTimeout(callbackFunction, 2000);
console.log("After timeout");


# Event Loop

The event loop is a crucial part of JavaScript's concurrency model, which enables asynchronous and non-blocking programming. 
It is responsible for managing the execution of code in a single-threaded environment, allowing JavaScript to handle multiple 
tasks concurrently without blocking the main thread.

The event loop works by continuously monitoring the call stack and the callback queue. When the call stack is empty, 
the event loop checks the callback queue for any pending callbacks or events. If there are any pending callbacks, the event 
loop will add them to the call stack to be executed. Once the callback is executed, any new functions it calls will be added to the call stack, 
and the event loop continues to monitor the queue.
 
# Microtask Queue
Microtasks are scheduled using queueMicrotask() function or Promise.resolve() method. When a microtask is scheduled, it is added to the 
end of the microtask queue. When the current task in the event loop completes, the event loop will check the microtask queue for any pending 
microtasks and execute them before continuing with the next task in the event loop.

Eg.

console.log('1');
Promise.resolve().then(() => {
  console.log('2');
});
console.log('3');


All the callback which comes through the promises will come inside the microtask queue.

# Map, filter and reduce.
there are the higher order function.


# Local Storage and sessions storage

Yes, both local storage and session storage are browser web APIs that are used to store data in the browser. They provide a way for web developers 
to store data on the client-side, which can be used to improve the user experience of their web applications.

Local storage and session storage are both part of the Web Storage API, which is a standard defined by the World Wide Web Consortium (W3C). They allow
 developers to store key-value pairs in the browser, which can be accessed and manipulated using JavaScript.

Local storage is used to store data that persists even after the browser is closed or the user navigates away from the website. It is useful for storing 
user preferences, settings, and other data that needs to be retained between sessions.

Session storage, on the other hand, is used to store data that is only available for the current session. When the user closes the browser or navigates 
away from the website, the data is deleted. It is useful for storing temporary data that is only needed for the current session, such as a user's shopping 
cart in an e-commerce website.
  
  
  
  ```
  function debounce(fun, delay){
    let timer;
    return function(){
        clearTimeout(timer);
        timer = setTimeout(()=>{
            fun();
        }, delay);
    }
}

function throatle(fun, delay){
    let timerId;
    return function(){
        if (!timerId){
            timerId = setTimeout(()=>{
                fun();
                timerId = null;
            },delay);
        }
    }
}
  ```
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  

  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
