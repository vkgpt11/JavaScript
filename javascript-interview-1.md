# JavaScript interview Part - 1
## 1. What is the clouser in JS?
 - Closure means that an inner function always has access to the vars and parameters of its outer function, even after the outer function has returned.
Now, as per the definition above, InnerFunction() can access outerVariable even if it will be executed separately. Consider the following example.
 ```
 function OuterFunction() {

     var outerVariable = 100;

     function InnerFunction() {
         alert(outerVariable);
     }

     return InnerFunction;
 }
 var innerFunc = OuterFunction();

 innerFunc(); // 100
 ```
- One important characteristic of closure is that outer variables can keep their states between multiple calls. 
- Remember, inner function does not keep the separate copy of outer variables but it reference outer variables,
- That means value of the outer variables will be changed if you change it using inner function.

## 2. When to use Closure?
- Closure is useful in hiding implementation detail in JavaScript. In other words, it can be useful to create private variables or functions.

The following example shows how to create private functions & variable.
 ```
 var counter = (function() {
   var privateCounter = 0;
   function changeBy(val) {
     privateCounter += val;
   }
   return {
     increment: function() {
       changeBy(1);
     },
     decrement: function() {
       changeBy(-1);
     },
     value: function() {
       return privateCounter;
     }
   };   
 })();

 alert(counter.value()); // 0
 counter.increment();
 counter.increment();
 alert(counter.value()); // 2
 counter.decrement();
 alert(counter.value()); // 1
 ```
## 3. What is prototype?
- JavaScript is a dynamic language. You can attach new properties to an object at any time.
 ```
 function Student() {
     this.name = 'John';
     this.gender = 'Male';
 }

 var studObj1 = new Student();
 studObj1.age = 15;
 alert(studObj1.age); // 15

 var studObj2 = new Student();
 alert(studObj2.age); // undefined
 ```
 - The prototype is an object that is associated with every functions and objects by default in JavaScript, 
 - The prototype object is special type of enumerable object to which additional properties can be attached to it which will be shared across all the instances of it's constructor function.
  ```
  function Student() {
     this.name = 'John';
     this.gender = 'M';
 }

 Student.prototype.age = 15;

 var studObj1 = new Student();
 alert(studObj1.age); // 15

 var studObj2 = new Student();
 alert(studObj2.age); // 15
  ```
https://www.tutorialsteacher.com/javascript/prototype-in-javascript

## 4. What is prototype inheritance?
- an object can inherit properties from another object. The prototypal inheritance is achieved via the prototype linkage
 ```
 let animal = {
     legs: 4,
     walk: function() {
         console.log('walking on ' + this.legs + ' legs');
     }
 };

 let bird = {
     legs: 2,
     fly: function() {
         console.log('flying');
     }
 };

 bird.__proto__ = animal;
 ```
 ```
 bird.walk(); // walking on 2 legs
 ```
 When you call the walk() method on the bird object:
1. First, find the walk() method in the bird object. Since there’s no walk() method there, it follows the prototype chain to look up the walk() method in the animal object.
2. Second, execute the walk() method with the this value set to the bird object, not animal object,  so the this.legs property stores the value defined in the bird object.

## 5. What is the `new` keyword in javascript?
![](https://www.tutorialsteacher.com/Content/images/oo-js/new-keyword.png)

https://www.tutorialsteacher.com/javascript/new-keyword-in-javascript

## 9. What is the difference between function and method in javascript?
There is a slight difference - 

**Method** : Method is a function when object is associated with it.

    var obj = {
    name : "John snow",
    work : function someFun(paramA, paramB) {
        // some code..
    }
    workHard(){
        // hard work
    }

**Function** : When no object is associated with it , it comes to function.

    function fun(param1, param2){
    // some code...
    }
    
## 10. What is the use of `this` keyword in different contexts?
+ In **Functions** `this` refers to the global object (window, global)

        title = "Global";

        console.log(this.title);

        function func(){
            console.log("From Func: " + this.title);
        }

        func();

        function func2(){
            console.log("From Func2: " + this.title);
          title:"This is sub function"
            function subFunc(){
                console.log("From sub Func: " + this.title);
          }

            subFunc();
        }
        func2();

Code will output Global in all of the different contexts of `this`.

        function printMe(){
          console.log(this.toString());
        }
        printMe(); // Prints the window object
        let x = new printMe();
        x; // Prints a new object 

+ In **Methods** `this` refers to the current object.
        
        title = "Global";
        let obj = {
            x:10,
          display(){
            console.log(this.x + ":" + this.title)
          }
        }
        obj.display();

`this` Refers to the object context 

https://js.do/code/477053



