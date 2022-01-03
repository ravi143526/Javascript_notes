# This #

- It will point an object.

- we can access the objects info like props/methods/events

- globally/locally

- base obj => window object(default obj in console)

**eg1:**

```js
this.window        // returns window object
```

**eg2:**

```js
function func1(){
    var x = 0;
    var y = 1;
    console.log(this);
}
func1();             // returns window object
```

**eg3:**

```js
var myObj = {
    heroName : 'AA',
    director : 'V V Vinayak',
    Movie : function(){
        console.log(this);
    }
}
myObj.Movie();        // returns obj values
```

## Use Strict: ##

- globally declared to get while script in strict mode

**eg1:**

```js
function L1(){
    "use strict"
    console.log(this);  // returns undefined
}
```