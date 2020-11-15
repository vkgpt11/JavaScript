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
![https://i.stack.imgur.com/GBn5a.jpg]
