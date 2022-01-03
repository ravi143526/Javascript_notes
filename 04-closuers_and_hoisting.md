# closuers #

- scope chaining (scope level of variables in a function or class)

**eg1:**

```js
var a =10;
function HelloGreet(){
    var b = 20;
    console.log(b);
}
```

- In this example whenever we want to print a value simply type *a* in console it gives value but *b* value is not printed because of its scope and when we call it goes to grabage collection. in order to print *b* value we choose closure method.

**eg2:**

```js
var a =10;
function HelloGreet(){
    var b = 20;
    var ByeGreet = function(){console.log(b);}
}
var innerFunIs = HelloGreet();
```

- in this we can call new function *innerFunIs* instead of call *b* directly to gets in scope chaining and prints the value.



# Hositing: #

- It is javascript's default behaviour of moving declarations to the top.

**Hosting examples:**

```js
a = 5;
var a;
```

```js
c();
function c(){
    console.log('C');
}
```

**Hosting not Examples:**

```js
b =10;
let b;
```

```js
e = 10;
const e;
```

```js
d();
var d = function(){
    console.log('D');
}
```

## Declaration,Assign and Initialization: ##

```js
### Declaration: ###

- simply given a name and its data type.

- we cant see their value until we invoke/call.

**eg:**

var a;
function a(){};

### Assign: ###

- storing a value in a variable.

**eg:**

a = 5;


### Initialization: (Not Hoisted) ###

- both declaration and assigning a initial value.

**eg:**

var a =10;

```
**example:**

```js
var a = 10;
let b = 20;
const c = 30;
function d(){
    console.log('D')
};
var e = () => {
    console.log('E');
};
console.log(a,b,c);
d();
e();
```

**example:**

```js
console.log(a,b,c);
d();
e();
var a = 10;
let b = 20;
const c = 30;
function d(){
    console.log('D')
};
var e = () => {
    console.log('E');
};
```