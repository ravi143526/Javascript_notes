# Functional Programming #

- It is a form of programming which you can pass functions as parameters to other functions and also return them as values.

- we think and code in terms of functions.

- Javascript or any other functional programming language functions are objects.

- They are called function Objects.

**eg:**

```js

function greeting(){
    console.log('Hello World!!!');
}
greeting();

greeting.lang = 'Telugu';
console.log(greeting.lang);
```

**eg1:**

```js
const square = (x) => {
    return x * x;
}

console.log(square(10));

const twiceMultiply = square;

console.log(twiceMultiply(5));
```

```