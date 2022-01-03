# OOPS: #

- There are mainly 4 Concepts:
  
  1. Abstarction

  2. Encapsulation

  3. Inheritence

  4. Polymorphism

## Benefits of oops: ##

- reuse of code through inheritance

- flexibility through polymorphism

- easier to troubleshoot

- code maintainability and readability


## Abstarction: ##

- hiding unecessary data and showing necessary data

- **eg:** ATM

**eg1:**  without abstarction 

```js

class ATM{
    constructor(withdraw){
        this.balance = 1000;
        this.min = 500;
        this.withdraw = withdraw;
    }
    getAmount(){
        if((this.balance-this.withdraw)>=this.min){
            console.log('withdraw successuful!!!')
        }
        else{
            console.log('withdraw failed!!!')
        }
    }
}

let obj = new ATM(1000);
obj.getAmount();
```

**eg2:**  with abstarction 

```js

class ATM{
    constructor(withdraw){
        this.balance = 1000;
        this.withdraw = withdraw;
    }
    getAmount(){
        this.min = 500;
        if((this.balance-this.withdraw)>=this.min){
            console.log('withdraw successuful!!!')
        }
        else{
            console.log('withdraw failed!!!')
        }
    }
}

let obj = new ATM(1000);
console.log(obj.min);
obj.getAmount();
```


## Encapsulation: ##

- binding both the data-variables and methods and hides then from other classes.

**eg:**

```js

class Person{
    constructor(name,age,salary){
        this.name = name;
        this.age = age;
        this.salary = salary;
    }

    getName(){
        console.log(this.name);
    }
    getAge(){
        console.log(this.age);
    }
    getSalary(){
        console.log(this.salary);
    }
}

let obj = new Person('john',34,65000);
obj.getName();
obj.getAge();
obj.getSalary();
```

## Inheritence: ##

- It is a mechanisham in which one class access the property of another class.

**eg:**

```js

class Parent{
    getMobile(){
        console.log('Iphone 11');
    }
}

class child extends Parent{
}

let obj = new child();
obj.getMobile();
```

## Polymorphism: ##

- one thing exist in more than one form 

- poly means *many* and morph means *form*

**eg:**

```js

class Parent{
    getMobile(){
        console.log('Iphone 11');
    }
}

class child extends Parent{
        getMobile(){
        console.log('Iphone 12');
    }
}

let obj = new child();
obj.getMobile();
```
