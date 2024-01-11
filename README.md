
# Exercise - Arrays and Loops

## Exercise 1
#### Create an empty array and fill it with different elements using the push-method. Log it to the console.
```js
const arr1 = [];
arr1.push(true)
arr1.push(30);
arr1.push({elephant: "heavy", color: "pink"})
console.log(arr1)
```
Output:
```
[ true, 30, { elephant: 'heavy', color: 'pink' } ]
```

## Exercise 2
#### Create an array containing arbitrary numbers. 
```js
const arr2 = [];
let iterations = Math.random() * 20;
for (let x = 0; x < iterations; x++){
    let nr = Math.ceil(Math.random()*20);  
    arr2.push(nr)
} 
console.log(arr2)
```
Output:
``` 
[ 18, 15,  4, 16, 15,  1, 12, 1,  5, 12,  6,  4,  8, 16, 5,  6, 18, 13, 19, 13 ]
```
#### Loop throught that array and multiply each element with 3 and log that to the console.
```js
for(let x= 0; x < arr2.length; x++){
    arr2[x] *= 3;
}
console.log(arr2)
```
Output:
``` 
[ 54, 45, 12, 48, 45,  3, 36, 3, 15, 36, 18, 12, 24, 48, 15, 18, 54, 39, 57, 39 ]
```

## Exercise 3
#### Create an array with numbers, and one empty array. Loop through the array with numbers and do an if check in each iteration. If that number is bigger then a specific number, 5 for example, add that number to the empty array. Log the new array to the console in the end. Remember to use the indexes to get the elements from the array with numbers.
```js
const arr3= [4,22,1,4,7,9,42];
const mtArr = [];
iterations = 0
while(iterations < arr3.length){
    if(arr3[iterations] < 7){
        mtArr.push(arr3[iterations])
    }
    iterations++;
}
console.log(mtArr)
```
Output:
```
[ 4, 1, 4 ]
```

## Exercise 4
#### Create an array with random numbers. 
```js
const randomNrs = [];
const randomAmount = Math.ceil(Math.random() * 30)
for(let x = 0; x< randomAmount; x++){
    randomNrs.push(Math.ceil(Math.random()*30))
}
console.log(randomNrs)
```
Output:
```
 [ 11, 10, 14, 17,  8, 24, 23,  2, 17, 18, 12 ]
 ```
#### Loop through the array and add them all together. Log the total sum of all the elements to the console. hint - You will need a variable here that store the sum as you iterate over the array.
```js
let sum  = 0;
randomNrs.forEach(num=>
    sum += num)
console.log(sum)
```
Output:
```
156
```

## Exerice 5
#### Create an array with some elements. Now search for a specific element while you are looping through the array. If you find the element you are searching for, log it to the console.
```js
const someElemnentsArr =[{someElement: "element"}, { someOtherElement: "element2"}, "element"]
for(let x = 0; x < someElemnentsArr.length; x++){
    if(someElemnentsArr[x].someElement === "element"){
        console.log(someElemnentsArr[x])
    }
}
```
Output:
```
{ someElement: 'element' }
```

## Exercise 6
#### Create an array with some elements 
```js
console.log(someElemnentsArr)
```
Output:
```
 [{ someElement: 'element' }, { someOtherElement: 'element2' }, 'element' ]
```
#### Remove the last element WITHOUT using `pop()`.
```js
someElemnentsArr.splice(someElemnentsArr.length-1, 1)
console.log(someElemnentsArr)
```
Output:
```
 [ { someElement: 'element' }, { someOtherElement: 'element2' } ]
```

## Exercise 7
#### Create an array with 10 different numbers. Find the biggest number in the array and log it to the console. hint - You will need a variable that holds the current biggest number.
```js
const intArr = [7, 2, 10, 5, 1, 8, 3, 9, 6, 4];
let highestValue = 0;
for(let x= 0; x< intArr.length; x++){
    if(intArr[x] > highestValue){
        highestValue = intArr[x]
    }
}
console.log(highestValue);
```
Output:
```
10
```

## Exercise 8
#### Create an array with some elements and an empty array. Using a loop, copy the content of the first array to the empty array.
```js
const arrayWithElements = [1, 'hello', true, { key: 'value' }, [3, 5]];
const arrayWithoutElements = [];
arrayWithElements.forEach(element=>
    arrayWithoutElements.push(element))
console.log(arrayWithoutElements)
```
Output:
```
[ 1, 'hello', true, { key: 'value' }, [ 3, 5 ] ]
```

## Exercise 9
####Create an array with some elements. Use a loop to empty the entire array so there are no elements left in the end.
```js
for(let x = arrayWithElements.length-1; x >= 0; x--){
    arrayWithElements.splice(x, 1)
}
console.log(arrayWithElements)
```
Output:
```
[]
```
