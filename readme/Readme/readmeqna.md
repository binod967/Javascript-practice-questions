# Arrays and Objects
## Question no.1
Reverse an array without using .reverse()
```
function reverseArray (arr) {
  var myArray = [1, 2, 3, 4, 5];
  var output = [];
  for (var i = myArray.length - 1; i >= 0; i--){
    output.push(myArray[i]);
  }
console.log(output);
}
var myArray = [1, 2, 3, 4, 5];
    function reverseArray (arr){
        for (var start = 0, end = myArray.length - 1; start < end; start++, end--) {
    var temp = myArray[start];
    myArray[start] = myArray[end];
    myArray[end] = temp;
}
console.log(myArray);
}
```
## Question no.2
Find the second largest number in an array
```
var arr = [10, 20, 50, 5, 45];
var n = arr.length;
var largest = -Infinity;
var secondLargest = -Infinity;
for (var i = 0; i<n; i++){
    largest = Math.max(largest, arr[i]);
}
for (var i = 0; i<n; i++){
    if (arr[i] < largest){
        secondLargest = Math.max( secondLargest, arr[i]);
    }
}
console.log(largest,  secondLargest);
```
## Question no.3
Remove duplicates from an array
```
var array = [9, 9, 9, 1, 1, 2]
array = [... new Set(array)]
console.log(array);
```
## Question no.4
Group array items by a property (e.g., group people by age)
```
var people =[
    {name: "Binod", age: 20},
    {name: "Ram", age: 25},
    {name: "Hari", age: 30},
    {name: "Shyan", age: 30},
    {name: "sita", age: 25}
];
var data = Object.groupBy(people, ({age}) => age);
console.log(data);
```
# Functions & Scope
## Question no.1
Explain and create a closure
```
function outerFunction (){
    const outerVariable = "It is outerFunction ";
    function innerFunction (){
        console.log(outerVariable);
    }
    return innerFunction;
}
    const output = outerFunction();
    output();
```
## Question no.2
Create a function that returns a counte
```
function createCounter(n) {
	
	return function(){
		return n++;
	}
}
const counter = createCounter(10)
console.log(counter())
console.log(counter())
console.log(counter())
```
# Recursion
Factorial using recursion
```
function factorial (n) {
    if (n===0 || n === 1){
        return 1 ;
}
return n * (factorial(n - 1));
}
console.log(factorial(6));
```    
