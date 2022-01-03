# Prototype #

- obj to obj chaining system which are hidden in vast

**eg:**

```js

function Movierules(){
    this.taxPayment = true;
    this.mukeshAd = function(){console.log('Ad is mandotary');}
}

let obj = new Movierules();

```

## Adding prototype to constructor function: ##

**eg:**

```js

Movierules.prototype.nationalAnthem = function(){console.log('Mandatory');}

```