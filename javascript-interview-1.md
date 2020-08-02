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
    
## What is the use of this keyword in different contexts?
