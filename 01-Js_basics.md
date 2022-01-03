# Javascript Basics: #

## Variables: ##

- Var , Let , Const

## Arthmetic Operator: ##

**eg:**

```js
var a = 600;  // numbertype variables
var b = 10;   // numbertype variables
var c = a + b; // addition operator
var d = a - b; // subtraction operator
var e = a/b;  // divison operator
var f = a*b;  // multiplication operator
var g = a%b;  // modularity operator
document.write(c,d,e,f,g);  // 610
```

## JS - Output functions: ##

**eg:**

```js
var myName = 'Ravi';
var loc = 'Banglore';
var a = 540;
var b = 160;
var c = a + b;
console.log(c);
console.log(loc);
```

## Assignment Operators: ##

- one variable value is assign to  another variable value.

**eg:**

```js
var a;  // defining a variable
a = 200;  // value assigned to var
document.write(a); // prints value 
document.write("<br>");

var b;
b = a;
document.write(b); // prints b
document.write("<br>");

b += 50;
document.write(b); // prints b
```


## Increment and Decrement operators: ##

- increment (++)

- decrement (--)console.log(rollIn);

**eg:**

```js
var a = 500;
var b = 400;
document.write(a);
document.write("<br>");

a++;
document.write(a); 

a--;
document.write(a); 

++b;
document.write(b); 

--b;
document.write(b);
``` 

## Relational Operators: ##

**eg:**

```js
var a = 500;
var b = 400;

temp1 = (x==y);
document.write(temp1);

temp2 = (x!=y);
document.write(temp2);

temp3 = (x > y);
document.write(temp3);

temp4 = (x < y);
document.write(temp4);

temp5 = (x===y);
document.write(temp5);
```

## Logical operator: ##

**eg:**

```js
var a = 200;
var b = 30;
var c = 10;

var temp 1 = ( (a<b) && (a>c)); // both conditions will be true
document.write(temp1);

var temp 2 = ( (a<b) || (a>c)); // either one of the condition will be true
document.write(temp1);

var temp 3 = ( (!a<b) ); // either one of the condition will be true
document.write(temp1);
```

## concatenation operator: ##

**eg:**

```js
var fName = 'Ravi';
var lName = 'Kumar';
var fullName = fName + lName;
document.write(fullName);

var s1 = 'Banglore';
var n1 = 2020;
var mix = s1 + n1;
document.write(mix);
```


# control Statements: #

## If-else: ##

**eg:**

```js
var n = 23;
if (n%2 == 0){
    document.write("<h1>N is a Even Number</h1>");
}
else {
    document.write("<h1>N is a Odd Number</h1>");
}
```

## while loop: ##

**eg:**

```js

var i = 1;
while (i<=25){   // condition checks first and it increments
 document.write("<h1>"+i+"</h1");
 i++;
}
```

## Do-While loop: ##

**eg:**

```js

var i = 1;
do {           // increment and checks the condition
    document.write(i);
    document.write("<br>");
    i++;
}
while (i<=30);
```


## for loop: ##

**eg:**

```js

for (i=1; i<=50; i++)
{
 document.write(i);
 document.write(""<br>);
}
```


## Break and Continue : ##

**eg:**

```js

for(i=1; i<=50; i++)
{
    document.write(i);
    if(i==25) 
    break;          // breaks the loop
    document.write(",");
}
```

**eg1:**

```js

for(i=1; i<=50; i++)
{
    document.write(i);
    if(i==25) 
    continue;          // continues the loop by skipping the condition value
    document.write(",");
}
```


## POPUPS: **Alert,Confirm,prompt** ##

**eg:**

```js

alert("This is ALert Message");

var result = confirm("Are you Sure?");
document.write(result);

var myCity = prompt("Enter your City");
document.write("myCity");

var a = prompt("Enter your name");
var b = prompt("Enter your location");
if(a == "Ravi" && b == "Banglore"){
    alert("welcome to my website");
}
else {
    alert("unKnown user");
}
```


## Javascript Arrays: ##

**eg:**

```js

a = [10,20,30];
alert(a[2]);

var myArray =  new Array(10,20,30);   
alert(myArray[2]);
```

## Js_Array-Methods: ##

**eg:**

```js

var id = new Array("ravi", "kumar", "ged"));
id[1] = "romeo"   // changing the value in array using index
document.write(id);

var names = new Array("ravi","romeo","rambo","get");
var k = names.length;
document.write(k-1);  // prints the last value of the array by using array-length
document.write(k/2);  // prints the middle value of the array.

var names = new Array("ravi","romeo","rambo");
document.write(names.length);  // count the number of values in it and print it

var test = names.concat("reo","hyper","jio");   // adds the new values to the previous array at the end of the array
document.write(test)

var test1 = new Array(110,2,30,56,90);
test1.sort();   // sort the values in ascending order 
document.write(test1);

var arr = [12,45,67];
arr.pop();        // delete the last element in the array
console.log(arr)

var arr = [12,67,88];
arr.push(45);  // adds the new value in the last of the array
console.log(arr)

var arr = [12,34,566];
arr.shift(); // delete the first element in the array
console.log(arr);

var arr = [12,45,78];
arr.unshift(45); // add the value to the start of the array
console.log(arr);

var arr = [12,45,67];
arr.splice(2,4);  // removes from 2 element upto 4 elements in that array
console.log(arr);
```


# DOM (Document object model): #

## .innerHTML: ##

- shows the data which is in HTML.

**eg:**

```html

<html>
    <head></head>
    <body>
        <h2>Document and its methods</h2>
        <p>This is my paragraph</p>
        <li>List element</li> 

     <script type="text/javascript">
      alert(document.body.innerHTML);
     </script>   
    <body>
</html>
```

## document.getElementById: ##

**eg:**

```html
<html>
    <head></head>
    <body>
        <div id="myDiv">Welcome</div>
<script>
var a = document.getElementById("myDiv");
alert(a); // one method

var msg = "Welcome to myPub";
var a = document.getElementById("myDiv");
a.innerHTML = msg; // second method
</script>
</body>
</html>
```


## Event Handling: ##

- Event handling is of three phases:
  
   1. when user performs an action on keyboard/mouse.
   2. raises an event
   3. event function will be executed.

**eg:**

```html
<html>
    <head></head>
    <body>
        <button id="button">Clickhere</button>
        <div id="div1">This is previous msg</div>
        <script type="text/javascript">
   
        function fun1(){
            var msg = "This is recorded Message!!!";
            var d = document.getElementById("div1");
            d.innerHTML = msg;
        }
        vat btn = document.getElementById("button");
        btn.addEventListener("click",fun1);

        </script>
    </body>
</html>
```


## classic style : clickevent ##

**eg:**

```html

<html>
    <head></head>
    <body>
        <h2>Hello</h2>
        <input type="text" id="Textbox1"><br/><br/>
        <button onClick="fun1()">ClickMe</button><br/><br/>
        <span id="red">Display Result Here:</span>

        <script type="text/javascript">
     
        function fun1(){
            var txt = document.getElementById("Textbox1");
            var s = txt.value;
            var msg = "The value which you Entered is: " + s;
            var sp = document.getElementById("red");
            sp.innerHTML = msg;
        }
       </script>
    </body>
</html>
```


## classicStyle : KeyUp event ##

**eg:**

```html

<html>
    <head></head>
    <body>
        <h2>Hello</h2>
        <input type="text" id="Textbox1" onkeyup="fun1()"><br/><br/>
        <span id="red">Display Result Here:</span>

        <script type="text/javascript">
     
        function fun1(){
            var txt = document.getElementById("Textbox1");
            var s = txt.value;
            var msg = "The value which you Entered is: " + s;
            var sp = document.getElementById("red");
            sp.innerHTML = msg;
        }
       </script>
    </body>
</html>
```

## KeypressEvent: ##

**eg:**

```html

<html>
    <head></head>
    <body>
        <h1>Hello World!</h1>
        Name:
        <input type="text" id="Textbox">
        <script>

            function fun1(event){
                var ch = event.which;
                alert(ch);
            }

            var txt = document.getElementById("Textbox");
            txt.addEventListener("keypress", fun1);
        </script>
    </body>
</html>
```

## Adding CSS with javascript - style: ##

**eg:**

```html
<html>
    <head></head>
     <body>
         <h1>Adding CSS with JS</h1>
         <div id="div1">
టేబుల్ టెన్నిస్
Competitive table tennis.jpg
టేబుల్ టెన్నిస్ ఒక అంతర్జాతీయ ఆట. ఈ ఆటలో ఇద్దరు లేదా నలుగురు ఆటగాళ్ళు ఒక బల్లకు చెరో పక్క నిల్చుని చిన్న తేలికపాటి బంతిని చిన్న రాకెట్ల సాయంతో అటూ ఇటూ కొడుతుంటారు. ఈ బల్ల మధ్యలో ఒక వల (నెట్) ఉంటుంది. ప్రారంభ సర్వీసు మినహా, నియమాలు సాధారణంగా ఈ క్రింది విధంగా ఉంటాయి: ఆటగాళ్ళు తమ వైపు వచ్చిన బంతిని తమ వైపు టేబుల్ మీద ఒక సారి బౌన్సయ్యేవరకు ఆగాలి, తర్వాత బంతి కనీసం ఒక్కసారైనా ప్రత్యర్థి వైపు బౌన్సయ్యేలా తిరిగి కొట్టాలి. నిబంధనల ప్రకారం బంతిని తిరిగి కొట్టడంలో ఆటగాడు విఫలమైనప్పుడు ఒక పాయింట్ కోల్పోతాడు. దీన్ని పింగ్-పాంగ్ అని కూడా అంటారు.
         </div>
        
     <button id="btn">CLICKME!!!</button>   

     <script type="text/javascript">

     function fun1(){
        
        var d1 = document.getElementById("div1");
        d1.style.background = "#003366";
        d1.style.color = "#ffffff";
        d1.style.fontSize = "14px";
        d1.style.border = "1px solid #3399ff";
        d1.style.width = "200px";
        d1.style.boxShadow = "0px 8px 30px #000";
        d1.style.marginBottom = "30px";
     }

     var but = document.getElementById("btn");
     but.addEventListener("click",fun1);
     </script>    
     </body>
</html>
```


## changing img attributes on dynamic: ##

**eg:**

```html

<img src="img1.jpg" id="myImage" width="600px">
<br/>

<button id="button1">clickme</button>

<script>
    function fun1(){
        var temp = document.getElementById("myImage");
        temp.setAttribute("src", "img2.jpg");
        temp.setAttribute("title", "Green");
        temp.setAttribute("alt", "green-Wall");

    }

    var btn = document.getElementById("button1");
    btn.addEventListener("click",fun1);
</script>
```

## Focus and Blur methods: ##

**eg:**

```html
<input type="text" id="Textbox1">
<span id="span1" style="color:gray;display:none;">
use letters,numbers and hyphens.</span>

<script>
     
    function fun1()
    {
        document.getElementById("span1").style.display:inline;
    }

    function fun2(){
        document.getElementById("span1").style.display:none;
    }

    document.getElementById("Textbox1").addEventListener("focus",fun1);
    document.getElementById("Textbox1").addEventListener("blur",fun2);

</script>
```


## mouseover,mouseout,mousemove events: ##

**eg:**

```html
<div id="div1" onMouseOver="fun1()" onMouseOut="fun2()" onMouseMove="fun3()">mouseover me</div>

<script type="text/javascript">

var d = document.getElementById("div1");

function fun1(){
    d.style.backgroundColor = "#ffcc00";
    d.style.borderRadius = "10px";
}

function fun2(){
    d.style.backgroundColor = "#ff00dd";
    d.style.boxShadow = "1px 15px 15px #ccc";
}

function fun3(){
    var x = event.pageX;
    var y = event.pageY;
    d.innerHTML = x + "," + y;
    d.style.textAlign = "center";
    d.style.lineHeight = "200px";
}

</script>
```


## click and double click: ##

**eg:**

```html

<html>
    <head>
        <style>
            #div1{
                background-color: #ffff99;
                width: 250px;
                height: 250px;
                border: 1px solid red;
                border-radius: 8px;
            }
        </style>
    </head>
    <body>
          <div id="div1">Multiple events   
          </div>

          <script>

            function fun1(){
                this.innerHTML = "Double click Event Fired";
            }

            function fun2(){
                this.innerHTML = "click Event Fired!";
            }

            document.getElementById("div1").addEventListener("dblclick",fun1);
            document.getElementById("div1").addEventListener("click",fun2);
          </script>
    </body>
</html>
```