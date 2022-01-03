# promises: #

## synchronous and asynchronous JS: ##

**synchronous:** 

- Basically Javascript is synchronous.

- Synchronous means single-threaded (execute one after another)

**eg:**

```js
console.log("ravi");
console.log("kumar");
console.log("gedela");   // returns one by one
```

**asynchronous:**

- multiple things execute at a time.

**eg:**

```js
console.log("ravi");

setTimeout(() => {
 console.log("kumar");
}, 1000);

console.log("gedela");  // returns ravi,gedela after 1 second kumar will be returned because of the callback function setTimeout which set to one second 
```

## callbacks: ##

- A callback is a function passed as an argument to another function.

- example of callback is **setTimeout()**

**eg:**

```js

step1(10, function(result1, error) {
    if(!error){
        step2(result1 , function(result2, error){
            if(!error){
                step3(result2, function(result3, error){
                    if(!error){
                        console.log('Results' 
                        + result3);
                    }
                });
            }
        });
    }
});

// adding many callback functions gets a pyramid type structure in the left of the code that is called callback hell.

function step1(value,callback) {
    callback(value + 10, false);
}

function step2(value,callback) {
    callback(value + 10, false);
}

function step3(value,callback) {
    callback(value + 10, false);
}
```

# Promises: #

- it is one type of callback Hell solution. 

- A promise is a javascript object that links producing code and consuming code.

- **Producing code** is code that can take some time.

- **consuming code** is code that must wait for the result.


**eg:**

```js
const p1 = Promise.resolve('Like if you understood callbacks!!!');
const p2 = 100;
const p3 = new Promise((resolve, reject) => {
    setTimeout(resolve, 1000, 'Subscribe for more updates')
});
const p4 = Promise.reject('new Error');


Promise.all([p1,p2,p3]).then((values) => console.log(values));   // for call all promises

Promise.race([p3,p1,p2]).then((values) => console.log(values));  // returns the first one which is in first array of items either it resolved or rejected

Promise.allSettled([p1,p2,p3,p4]).then((values) => console.log(values));   // returns all values either they are resolved or rejected

Promise.any([p1,p2,p3,p4]).then((values) => console.log(values));   // returns the first resolved value of any object

```

- promises have three states and values:

```
1. Pending  (undefined)
2. Fulfilled  (resolved value)
3. Rejected  (reason for rejection)
```


## chaining of promises: ##

**eg:**

```js

step1(10, false)
     .then((result1) => step2(result1,false))
     .then((result2) => step3(result2,false))
     .then((result3) => console.log(result3))
     .catch((error) => console.log(error));
```

## Async/Await: ##

- Async and Await make promises easier to  write.

- **Async** makes a function return promise

- async functions always return promises

- **Await** makes a function wait for a promise.


**eg:**

```js

async function result(){    // the result from async is a promise only.
    let result1 = step1(10, false);
    console.log(result1);
}
result();     
```

**eg:**

```js

async function result(){
    let result1 = await step1(10, false);
    let result2 = await step2(result1, false);
    let result3 = await step3(result2, false);
    console.log(result3);
}

```