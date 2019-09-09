1. 🎖Write a function named calculateDogAge that:
  * [ ] Takes 1 argument: your puppy's age.
  * [ ] Calculates your dog's age based on the conversion rate of 1 human year to 7 dog years.
  * [ ] Outputs the result to the screen like so: "Your doggie is NN years old in dog years!"
  * [ ] Add an additional argument to the function that takes the conversion rate of human to dog years.

```js
// your code goes here
let puppy_age = +prompt("Enter Your Puppy's Age")
function calculateDogAge() {
  return puppy_age * 7;
}
calculateDogAge()


// OR
function calculateDogAge() {
  let puppy_age = +prompt("Enter Your Puppy's Age")
  return puppy_age * 7;
}
calculateDogAge()

```
2. 🎖Write a function named calculateSupply that:
  * [ ] takes 2 arguments: age, amount per day.
  * [ ] calculates the amount consumed for rest of the life (based on a constant max age).
  * [ ] outputs the result to the screen like so: "You will need NN to last you until the ripe old age of X"
  * [ ] Accept floating point values for amount per day, and round the result to a round number.

```js
// your code goes here
 function calculateSupply(age, amount_per_day){
   const max_age = 80 ;
   console.log (`You will need ${Math.round((max_age - age) * 365 * amount_per_day)} to last you until the ripe old age of 80`)
 }
```
3. 🎖Create a function called celsiusToFahrenheit:
  * [ ] Store a celsius temperature into a variable.
  * [ ] Convert it to fahrenheit and output "NN°C is NN°F".
  * [ ] Create a function called fahrenheitToCelsius:
  * [ ] Now store a fahrenheit temperature into a variable.
  * [ ] Convert it to celsius and output "NN°F is NN°C."

```js
// your code goes here
//  celsiusToFahrenheit
function celsiusToFahrenheit(){
  let value = +prompt("enter celcius") 
  return `${(value * 9 / 5) + 32} degree Fahrenheit is ${value} degree celcius`;
}
celsiusToFahrenheit()

// OR
const celsiusToFahrenheit = (val) => `${(val * 9 / 5) + 32} degree Fahrenheit is ${val} degree celcius`

// OR

function celsiusToFahrenheit(value){
   
  return `${(value * 9 / 5) + 32} degree Fahrenheit is ${value} degree celcius`;
}

celsiusToFahrenheit(32)

// fahrenheitToCelsius
function fahrenheitToCelsius(){
  let value = +prompt("enter celcius") 
  return `${(value - 32) * 5/9} degree celcius is ${value} degree  Fahrenheit`;
}
fahrenheitToCelsius()

// or

const fahrenheitToCelsius = (val) => `${(val - 32) * 5 / 9} degree celcius is ${val} degree Fahrenheit`


// OR
function fahrenheitToCelsius(value){
   
  return `${(value - 32) * 5 / 9} degree celcius is ${value} degree Fahrenheit`;
}

fahrenheitToCelsius(32)

```
4. 🎖The function below returns true if the parameter age is greater than 18. Otherwise it asks for a confirmation and returns its result:

```js
function checkAge(age) {
  if (age > 18) {
    return true;
  } else {
    // ...
    return confirm("Did parents allow you?");
  }
}
```
  4.1 🎖Convert the above function using ternary operator.
  ```js
  // your code goes here
  function checkAge(age){
   (age > 18) ? console.log(true) :
   console.log("Did parents allow you?");
  }
  checkAge(10)
  ```

  4.2 🎖Convert the above function using `||` operator.
  ```js
  // your code goes here
   function checkAge(age){
   (age > 18 || age == 18) ? console.log(true) :
   console.log("Did parents allow you?");
  }
  checkAge(10)
  ```
Will the function work differently if else is removed like below?

```js
function checkAge(age) {
  if (age > 18) {
    return true;
  }
  // ...
  return confirm("Did parents allow you?");
}
```
Is there any difference in the behavior of these two variants? If there is what is that?


5. 🎖 Write a function pow(x,n) that returns x in power n.

  * [ ] Use prompt to take values for x and n, and then shows the result of pow(x,n) using alert.
  * [ ] In this task the function should support only natural values of n: integers greater then 1.

```js
// Your code goes here
 function pow(x,n){
 	console.log( x**n);
 }

 //OR BY USING ARROW FUNCTION

   let pow = (x,n) => console.log( x**n);


// After writing code uncomment to check the answer.
// pow(3, 2); // 9
// pow(3, 3); // 27
// pow(1, 100); // 1
// pow(-31, 2); // "The number below 1 is not allowed"

6. 🎖Write a program that asks the user for a number n and gives them the possibility to choose between computing the sum and computing the product of 1,…,n. Return the result accordingly.

```js
// your code goes here
let number = +prompt("Enter number", "0 - 10");
let add_number = confirm(" u want me to sum the numbers");
let multiply_number = confirm(" u want me to mutiply the numbers");
if (add_number == true){
  function sum_add(){
  // let number = +prompt("enter number ", "0 - 10");
  let sum =  0;
  for( let i = 1 ; i <= number ; i++){
    // console.log(i)
    sum += i;
}
  console.log(sum);
 
}
sum_add() ;

}
else if (multiply_number == true){
	function multiply(){
  // let number = +prompt("enter number ", "0 - 20");
 	 let mutiply_value =  1;
  	for( let i = 1 ; i <= number ; i++){
      mutiply_value*=i

}
 		 console.log(mutiply_value);

 }
   multiply();

}


//  OR we can TO THIS
let number = +prompt("Enter number");
let operator = prompt("Enter s for sum OR p for product")
let output = +"";
let multiply_output = 1;
for(let j = 1; j <= number; j++){

  (operator == "s" ) ? output += j : (operator == "p") ? multiply_output *= j : alert("Invalid Input")
}
	console.log(output);
	console.log(multiply_output)
```
6. 🎖Write a program that asks the user for a number n using prompt and prints the sum of the numbers 1 to n

```js

function sum(){
  let number = +prompt("enter number ", "0 - 10");
  let sum =  0;
  for( let i = 1 ; i <= number ; i++){
    console.log(i)
    sum += i;
}
  console.log(sum);
}
sum() ;

// your code goes here
```
7. 🎖Modify the previous program such that only multiples of 5 or 7 are considered in the sum, e.g. n = 20 (5,7,10,14,15,20) 71

```js
// your code goes here
function sum(){
  let number = +prompt("enter number ", "0 - 20");
  let sum =  0;
for( let i = 1 ; i <= number ; i++){
  
    ( i % 5 == 0 || i % 7 == 0) ? sum += i :  console.log("sum cannot be performed" , i);
 
}
	 console.log(sum);

 }	
sum() ;
// if else way
// function sum(){
//   let number = +prompt("enter number ", "0 - 20");
//   let sum =  0;
// for( let i = 1 ; i <= number ; i++){
  
//    if ( i % 5 == 0 || i % 7 == 0) {
      
//      sum += i ;
//    }else {
//    	 console.log("sum cannot be performed" , i)
//    }
 
// }
// 	 console.log(sum);

//  }	
// sum() ;
```

8. 🎖Write a function `min` that takes two arguments and returns their minimum.

```js
// Your code here.
//  function min (a,b){
 	 
//  	 a < b ? console.log( a ): console.log(b ) 
//  }
//  min(3,2)

//  OR
function min (a,b){
 	 
 	if(a < b ) return a ;
 	return b
 }
var output = min(3,2);
console.log(output)


//OR

 function min (a,b){
 	 
 	 a < b ? return( a ) : b < a ? return(b):return("both inputs are equal") 
 }
 min(3,3)

console.log(min(0, 10));
// → 0
console.log(min(0, -10));
// → -10
```