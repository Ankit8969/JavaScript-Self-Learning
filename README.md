## About JavaScript
> JavaScript was initially created to  ###make web pages alive.
> Today, JavaScript can execute not only in the browser, but also on the server, or actually on any device that has a special program called the JavaScript engine.

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

  # NExt Update from 19
  
  
  
  
  
  
