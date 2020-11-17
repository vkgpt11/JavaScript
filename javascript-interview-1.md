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



