## 1. What is the difference between Promises and Observables?
|Promise|Observables|
|-------|-----------|
|A promise can only handle one event|Observables are for streams of events over time|
|Emits a single value | Emits multiple values over a period of time|
|Not Lazy | Lazy. An Observable is not called until we subscribe to it|
|Can not be cancelled | Can be cancelled by using the unsubscribe() method|
|It does not provide any operators | provides the map, forEach, filter, reduce, retry, retryWhen operators|

https://medium.com/@mpodlasin/promises-vs-observables-4c123c51fe13

## 2. Why and when to use forEach, map, filter, reduce, and find in JavaScript?
|Method|Use|
|-------|-----------|
|.forEach()| it has advantages over the `for` with regards to scoping & clean code |
|.map()| to **transform** elements in an array|
|.filter()| to **select** a subset of multiple elements from an array|
|.find()| to **select** a single elememt from an array|
|.reduce()| to **derive** a single value from multiple elements in an array.|

https://medium.com/@JeffLombardJr/understanding-foreach-map-filter-and-find-in-javascript-f91da93b9f2c

## 3. What is Immediately Invoked Function Expressions (IIFE)?
- Should be invoked immediately
- IIFEs have there own scope i.e. the variables you declare in the Function Expression will not be available outside the function.
- Similarly to other function IIFEs can also be named or anonymous, but even if an IIFE does have a name it is impossible to refer/invoke it.
- IIFEs can also have parameters. 
```
    // Declaring the parameter required. 
    (function(dt) { 
        console.log(dt.toLocaleTimeString()); 
        // Passing the Parameter. 
    })(new Date()); 
```

## 4. What are the ways to define an object in Javascript?
- **"object constructor" syntax**
``` let person = new Object();```

- **"object literal" syntax**
```let person = {};```

You can access the values of varriables inside an object using 
- Dot notation ```objectname.propertyname;```
- bracket notation ```objectname['propertyname'];```

```
    <script> 
    // an object 
    let person = {      
      name: "Mukul",  // by key "name" store value "Mukul" 
      age: 22        // by key "age" store value 22 
    };
    document.write(person.name+'</br>');  
    document.write(person['age']); 
    </script>
```
## 5. What is the difference between var, let and const?
![](https://i.stack.imgur.com/GBn5a.jpg)

## 6. What is Hoisting?
- Hoisting is the JavaScript interpreter's action of moving all variable and function declarations to the top of the current scope. 
- However, only the actual declarations are hoisted. Any assignments are left where they are.

**Below code will get transform :**
```
    console.log(counter); // undefined
    var counter = 1;
```
**to** 
```
    var counter;
    console.log(counter); // undefined
    counter = 1;
```

## 7. What is the use of `use strict`?
- Strict mode eliminates errors that would be ignored in non-strict mode, thus making javascript "more secured"
- It is the best practice to use strict in JS files.
- Keyword indicates that code should be interpreted in strict mode specifies to user agents like browsers, and throw an error if the code doesn't make sense
- Can prevent memory leaks 

### Scenario 1: [NO STRICT MODE]

```
var city = "Chicago"
console.log(city) // Prints the city name, i.e. Chicago
```

### Scenario 2: [NO STRICT MODE]

```
city = "Chicago"
console.log(city) // Prints the city name, i.e. Chicago
```
Without strict mode turned on, user agents often go through a series of modifications to problematic code in an attempt to get it to make sense.

### Scenario 3: [STRICT MODE]
```
'use strict';

city = "Chicago"
console.log(city) // Reference Error: asignment is undeclared variable city.
```

### Enable strict mode from eslint file
``` module.exports = {
    env: {
        es6: true
    },
    rules : {
        strict: ['error', 'global'],
        },
    };
```
https://stackoverflow.com/questions/1335851/what-does-use-strict-do-in-javascript-and-what-is-the-reasoning-behind-it

## 8. What is the difference between == vs === operators?
- The == operator will compare for equality after doing any necessary type conversions. 
- The === operator will not do the conversion, so if two values are not the same type === will simply return `false`

```
'1' === 1 // will return "false" because `string` is not a `number`
'1' == 1 // will return "true"
```
![](https://i.stack.imgur.com/yISob.png){height=50% width=50%}
