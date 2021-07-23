## Learn this 21 JavaScript Tricks To Code Like A Pro!

JavaScript is a programming language used primarily by Web browsers to create a dynamic and interactive experience for the user. Most of the functions and applications that make the Internet indispensable to modern life are coded in some form of JavaScript.
While JavaScript is not the only client-side scripting language on the Internet, it was one of the first and it is still the most widely used. Many developers believe that JavaScript is inefficient and finicky, so they have made many improvements to the language over the years.

Here are the 21 JavaScript tricks that makes you a JavaScript pro

21. #### Use logical AND / OR for conditions
```javascript
var xyz = 23;  
xyz == 10 && runFunction(); // is the same thing as if (xyz == 23) runFunction(); 
xyz == 5 || runFunction(); // is the same thing as if (xyz != 23) runFunction();
``` 
20. #### Avoid using for loop for arrays
Instead of using 
```javascript
var add = 10;  
for (var i in arrayAdd) {  
    add += arrayAdd[i];  
}
```
It is better to use
```javascript
var add = 10;  
for (var i = 0, len = arrayAdd.length; i < len; i++) {  
    add += arrayAdd[i];  
}
```
19. #### Filter unique values
We can use Set to create a new array with only the unique values.
```javascript
const array = [4,5,4,6,32,5,3,5,7,1,3,4]
const AnotherArray = [...new Set(array)];
console.log(AnotherArray); // Result: [4, 5, 6, 32, 3, 7, 1]
```
18. #### Comment your code often
Comments are a great way to summarise a code fragment’s purpose, saving your time it would take to determine it on their own.
```javascript
// declaring and initialising variable x
var x = 19
```
17. #### Use strict mode to catch silent errors
To opt into strict mode, add the line'use strict'; either at the top of your script section (if you want the whole section to be strict) or before the desired function (if only certain sections should be strict).
16. #### Write shorter loops with array methods
Instead of using 
```javascript
const prices = ['4.0', '3.2', '2.45'];
const formattedPrices = [];
for (let i = 0; i < prices.length; i++) {
    const price = parseFloat(prices[i]);
    if (price) { formattedPrices.push(price) }
}
console.log(formattedPrices);
```
It is better to use
```javascript
const prices = ['4.0', '3.2', '2.45'];;
const formattedPrices = prices.map(price => parseFloat(price));
console.log(formattedPrices)
```
15. #### Empty an array
```javascript
var someArray = ['apple' , 'banana' , 'watermelon' ];  
someArray.length = 0; // someArray will be equal to [].
```
14. #### Generate an array of numbers with numbers from 0 to max
```javascript
var someArray = [] , max = 50;
for( var i=1; someArray.push(i++) < max;);
console.log(someArray)   // someArray = [1,2,3 ... 50] 
```
13. #### use === instead of ==
The == (or !=) operator performs an automatic type conversion if needed. The === (or !==) operator will not perform any conversion. It compares the value and the type, which could be considered faster than ==.
```javascript
[10] === 10    // is false
[10]  == 10    // is true
```
> JavaScript is the only language that I'm aware of that people feel they don't need to learn before they start using it. ~Douglas Crockford
12. #### Append an array to another array
```javascript
var firstArray = [13,5,3,6,2,'string',true];
var secondArray = ["anotherstring" , 3,5,2,1 , false];
Array.prototype.push.apply(firstArray, secondArray);
// firstArray will be equal to [13, 5, 3, 6, 2, "string", true, "anotherstring", 3, 5, 2, 1, false]
```
11. #### Don’t use `delete` to remove an item from array
Use `splice` instead of using `delete` to delete an item from an array.Using `delete` replaces the item with `undefined` instead of the removing 
it from the array.
Instead of Using
```javascript
var items = [13,5,3,6,2,'string',true];
items.length; // return 7
delete items[3]; // return true 
items.length; // return 7
console.log(items) // [13, 5, 3, empty, 2, "string", true]
```
It is better to use
```javascript
var items = [13,5,3,6,2,'string',true];
items.length; // return 7
items.splice(3,1) ; 
items.length; // return 6 
console.log(items) // [13, 5, 3, 2, "string", true]
```
10. #### Rounding number to N decimal place using `toFixed`
```javascript
var number =3.2198379128;
number = num.toFixed(3); 
console.log(number)  // num will be equal to 3.219
```
9. #### Avoid using `with()` in your code
When you use `with()`, it inserts a variable at the global scope. Thus, if another variable has the same name it could cause confusion and overwrite the value.
8. #### Convert to String
To quickly convert a number to a string, we can use the concatenation operator + followed by an empty set of quotation marks "" .
```javascript
const number = 21 + "";
console.log(number); // Result: "21"
```
7. #### Float to Integer
If you want to convert a float to an integer, the faster way to truncate a float to an integer using |, the bitwise OR operator.
```javascript
console.log(33.9 | 0);  // 33
console.log(-33.9 | 0); // -33
```
6.  #### Get the Last Item(s) in an Array
The array method slice() can take negative integers, and if provided it will take values from the end of the array
```javascript
let someArray =  [13,5,3,6,2,'string',true];
console.log(someArray.slice(-1)); // [true]
console.log(someArray.slice(-4)); //  [6, 2, "string", true]
console.log(someArray.slice(-5)); //  [3, 6, 2, "string", true]
```
5. #### Avoid the use of `eval()`
Useing of eval is expensive operations as each time it is called script engine must convert source code to executable code.
```javascript
var func2 = eval(functionCodeHere);
```
4. #### Use switch/case statement instead of a series of if/else
Using switch/case is faster when there are more than 3 cases, and it is more elegant. Avoid using it when you have more than 3 cases.
3. #### Convert to Number
```javascript
let number = "21";
number = +number;
console.log(number); // 21
```
2. #### Comma Operator
In JavaScript, the `,` operator is used for evaluating each of its operands from left to right and returns the value of the last operand.
```javascript
let count = 10;
let num = (count++, count);
console.log(num); // 11
```
1. #### Use a Minifier
Before making your website live, It is better to use a JavaScript Minifier to minify your code, This will make your website load much faster

### Conclusion
There are many other tips, tricks and best practices, so if you have any ones to add please share it in the comment section.











