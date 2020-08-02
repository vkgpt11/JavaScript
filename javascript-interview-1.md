# JavaScript interview Part - 1
## What is the difference between function and method in javascript?
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
    
## What is the use of `this` keyword in different contexts?
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
