# Scope: #

-  local and global scopes.

**eg: Global scope**

```js
var num = 10;
function calc() {
    return num;
}
console.log(num); // return number =>   gets value
console.log(calc()); //return function => gets value
```

**eg: Local Scope:**

```js
function calc() {
    var num = 10;
    return num;
}
console.log(num); // return number =>   gets error
console.log(calc()); //return function => gets value
```


# Execution Context: #

- everything in javascript happens inside execution context.

- In this two components will be there: 

- one is memory also known as variable environment which contains variables and functions as key value pairs:

```js
key : value
a : 10
fn: {---}
```

- second is code component also known as thread of execution in which whole code is executed.

- Js is a synchronous single threaded language

- that means line by line execution.