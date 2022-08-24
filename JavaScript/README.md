# JavaScript Using Method And Example

### what is javaScript?
- JavaScript is high level, interpreted programming language used to make web pages more interactive. JavaScript is a dynamic programming language that's used for web development, web applications, game development, and lots more. JavaScript language is used both on the client-side and server-side allowing you to make web pages interactive.
### Why use JavaScript?
- Where HTML and CSS are languages that give structure and style to web pages, JavaScript gives web pages interactive elements that engage a user.


List of JavaScript:

- [JSONStringify](#JSONStringify)
- [DOM](#DOM)
- [events](#events)
- [sliceSplice](#sliceSplice)
- [function](#function)
- [Recursion ](#Recursion )
- [String](#String)
- [whileLoop](#whileLoop)
- [forLoop](#forLoop)
- [TemplateString](#TemplateString)
- [ArrowFunction](#ArrowFunction)
- [SpreadOperator](#SpreadOperator)
- [concat](#concat)
- [Map](#Map)
- [forEach](#forEach)
- [filter](#filter)
- [find](#find)
- [JSON](#JSON)
- [fetch_Keys_Values](#fetch_Keys_Values)
- [Array](#Array)
- [Object](#Object)
- [switch](#switch)
- [jsProblemSolved](#jsProblemSolved)
- [Table](#Table)
- [Output](#Output)

### demo
<details>
<summary>
  <h3>What is ?</h3>
</summary>
<br >
 demo
</details>

```js

```
### JSONStringify
<details>
<summary>
  <h3>What is JSONStringify ?</h3>
</summary>
<br >
 JSONStringify
</details>

```js

let a = { x: 5, y: 6 }
console.log(a, typeof a)
//ans:  Object { x: 5, y: 6 } "object"

let b = JSON.stringify(a)
console.log(b, typeof b);
//'{"x":5,"y":6}' "string"

```

### DOM
<details>
<summary>
  <h3>What is events?</h3>
</summary>
<br >
events 
</details>

```js
1 option.
<button onclick="console.log(65)">Another button</button>

2 option.
//html file
<button id="make-blue">make blue</button>
//script file
const makeBlueButton = document.getElementById('make-blue');
makeBlueButton.onclick = makeBlue;
function makeBlue(){
    document.body.style.backgroundColor = 'blue'
}

3 option.
<button id="make-purple">make purple</button>
const purpleButton = document.getElementById('make-purple');
  purpleButton.onclick = function makePurple() {
      document.body.style.backgroundColor = 'purple'
  }
  4. 
  <button id="make-pink">Make Pink</button>
  const pinkButton = document.getElementById('make-pink');
  pinkButton.addEventListener('click', makePink)
  function makePink() {
    document.body.style.backgroundColor = 'pink'
  }
  6.
  <button id="make-green">Make green</button>
  const greenButton = document.getElementById('make-green');
  greenButton.addEventListener('click', function makeGreen() {
    document.body.style.backgroundColor = 'green'
  })
  
  7. final uses
  <button id="make-orange">Make orange</button>
   document.getElementById('make-orange').addEventListener('click', function () {
        document.body.style.backgroundColor = 'orange'
    })
    
    8.
    <a href="#" onclick="selectedItem(this)" class="btn btn-primary">SELECT
                                                4</a>
    
    // finale uses 
     <div id="comment-content">
     </div>
     //
     <div>
        <textarea name="" id="new-comment" cols="100%" rows="5"></textarea>
        <br>
        <button id="btn-post">Post</button>
    </div>
    //
    <script>
        // step- 1 add event listener to the post button
        document.getElementById('btn-post').addEventListener('click', function () {
            console.log('post click')
            //step 2 get the comment
            const commentBox = document.getElementById('new-comment');
            const newComment = commentBox.value;
            // step 3 set the comment inside the comment container
            // get the comment container
            const commentContent = document.getElementById('comment-content');
            // step 4 create p tag
            const p = document.createElement('p');
            // step 4.1 set the text of the commment as innerText
            p.innerText = newComment;
            //step 5 append child
            commentContent.appendChild(p)
            // clear the textArea
            commentBox.value = '';
        })
    </script>
```

### DOM
<details>
<summary>
  <h3>What is DOM?</h3>
</summary>
<br >
DOM 
</details>

```js
1. getElementsByTagName()
<h1 id="title">Fruits i like</h1>
//using
document.getElementById('title')

2. getElementById()
<h1 id="title">Fruits i like</h1>
//using
document.getElementById('title')

3. getElementByClass()
<ul>
  <li class="important-places">Sundarban</li>
  <li class="important-places">Bandorban</li>
  <li class="important-places">ShalBan</li>
  <li class="important-places">KataBan</li>
</ul>
//using:
document.getElementsByClassName('important-places')
//
const places = document.getElementsByClassName('important-places')
for(const place of places){
    console.log(place)
    console.log(place.innerText)
}

4. getElementByQuerySelector()
const sections = document.querySelectorAll('section');
for(const section of sections){
    console.log(section)
    section.style.border = '2px solid steelblue';
    section.style.margin = '20px';
    section.style.padding = '20px';
    section.style.borderRadius = '8px';
    section.style;
    section.style;

}

4. querySelectorAll()
const sections = document.querySelectorAll('section');
for(const section of sections){
    console.log(section)
    section.style.border = '2px solid steelblue';
    section.style.margin = '20px';
    section.style.padding = '20px';
    section.style.borderRadius = '8px';
    section.style;
    section.style;

}
5.
//whare to add
const placesList = document.getElementById('places-list');
// 2. what to be added
const li = document.createElement('li');
li.innerText = 'pahartoli bon'
// 3. add the child
placesList.appendChild(li)
console.log(placesList)
6.
  <button id="make-green">Make green</button>
  const greenButton = document.getElementById('make-green');
    greenButton.addEventListener('click', function makeGreen() {
        document.body.style.backgroundColor = 'green'
    })
7. final uses
 <button id="make-orange">Make orange</button>
document.getElementById('make-orange', function(){
      document.body.style.backgroundColor= 'orange'
  })

```
<div class="overflow-x-auto">
  <table class="table w-full">
    <!-- head -->
    <thead>
      <tr>
        <th></th>
        <th>Name</th>
        <th>Description</th>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <!-- row 1 -->
      <tr>
        <th>1</th>
        <td>getElementsByTagName()</td>
        <td>Array like object. HTMLCollection দিবে।</td>
        <td></td>
        <td></td>
      </tr>
      <!-- row 2 -->
      <tr>
        <th>2</th>
        <td>getElementById()</td>
        <td>Get the element with the specified id. কোন একটি নিদিষ্ট element কে পাবো</td>
        <td>getElementByClass() </td>
        <td>একই নামের className গুলা পাবো</td>
      </tr>
      <!-- row 4 -->
      <tr>
        <th>৪</th>
        <td>getElementByQuerySelector()</td>
        <td> যত গুলা থাকবে সব গুলার প্রথম টা পাবো </td>
        <td>querySelectorAll()</td>
        <td> যত গুলা থাকবে সব className গুলা পাবো</td>
      </tr>
      <!-- row 6 -->
      <tr>
        <th>6</th>
        <td>getAttribute()</td>
        <td> </td>
        <td>setAttribute()</td>
        <td> </td>
      </tr>
      </tr>
      <!-- row 8 -->
      <tr>
        <th>2</th>
        <td>innerText</td>
        <td> </td>
        <td>innerHTML</td>
        <td> </td>
      </tr>
      <!-- row 11 -->
      <tr>
        <th>11</th>
        <td>NodeList</td>
        <td> </td>
        <td>htmlcollection</td>
        <td> </td>
      </tr>
      <!-- row 13 -->
      <tr>
        <th>13</th>
        <td>parentNode</td>
        <td> </td>
        <td>childnodes</td>
        <td> </td>
      </tr>
       <!-- row 15 -->
      <tr>
        <th>2</th>
        <td>createElement</td>
        <td> </td>
        <td>appendChild</td>
        <td> </td>
      </tr>
   <!-- row 17 -->
      <tr>
        <th>17</th>
        <td>classList.add('places-area')</td>
        <td> html tag এর ভিতর class add করা</td>
         <td>.classList.remove('places-area')</td>
        <td> html tag এর ভিতর class remove করা </td>
      </tr>
       <!-- row 18 -->
      <tr>
        <th>18</th>
        <td>nextSibling</td>
        <td> </td>
         <td>previousSibling</td>
        <td> </td>
      </tr>
   <!-- row 19 -->
      <tr>
        <th>19</th>
        <td>addEventListener('click', functionName())</td>
        <td> </td>
         <td></td>
        <td> </td>
      </tr>
   <!-- row 20 -->
      <tr>
        <th>18</th>
        <td></td>
        <td> </td>
         <td></td>
        <td> </td>
      </tr>
    </tbody>
  </table>
</div>

### sliceSplice
<details>
<summary>
  <h3>What is sliceSplice?</h3>
</summary>
<br >
function 
</details>

```js
//slice
const friends = [12, 45, 32, 22, 44, 62, 29, 69, 87];
const friendsSlice = friends.slice(2, 6);
console.log(friendsSlice)
// Splice
// Removes elements from an array and,
//  if necessary, inserts new elements in their place,
//  returning the deleted elements.
const friends = [12, 45, 32, 22, 44, 62, 29, 69, 87];
const friendsSplice = friends.splice(2, 7);
//add new number (Example 99, 789, 888)
//const friendsSplice = friends.splice(2, 7, 99,789,888);
console.log(friendsSplice)
console.log(friends)

```

### function
<details>
<summary>
  <h3>What is function?</h3>
</summary>
<br >
function 
</details>

```js

// function declaration
// Example: 1
function add(first, second){
    const total = first + second;
    return total;
}


// Example: 2
document.getElementById('btn-add').onclick = function addBG(){

}


// Example: 3
const add1 = function add1(parameter1, parameter2){
    const total = first + second;
    return total;
};
// Example: 4
function add2(first, second){
    const total = first + second;
    return total;
}
// Example: 5
function add3(first, second){
    return first + second
}

// Example: 6
function add4(first, second){
    return first + second
}
// arrow function  Ex: 1
// Example: 7
const add4 = (first, second) => first + second;
// Example: 8
const add4 = (first, second) => first + ' ' + second;
// Example: 9 (no parameter arrow function)
const getPie = () => 3.14;
// Example: 10 (one parameter) 
const doubleIt = num => num * 2;
// Example: 11 (multi line arrow function)
const doMath = () => {
    const firstSum = x + y;
    const secondSum = y + z;
    const multiplyResult = firstSum + secondSum;
    const result = multiplyResult / 2;
    return result;
};


  //simple declaration
    //function declaration
    function startFan(){
        console.log('stand up')
        console.log('walk towards the switch')
        console.log('press the switch')

    }
    // call the function
    startFan()
    
  //  function with paramiter (Example 2)
    function functionName(parameters){
      /*   function body
        return */
    }
    // call the function
    let returedValue =  startFan(parameters);
    console.log(returedValue)
    
    // even & odd number
      function isEven(number){
          const remainder = number % 2;
          if(remainder == 0){
              // console.log('number is even')
              return true;
          }
          else{
              // console.log('number is odd')
              return false;
          }
      }
      let myNumberIsEven = isEven(588)
      console.log(myNumberIsEven)

      let herNumberIsEven = isEven(1231)
      console.log(herNumberIsEven)
      
      // year is a Leap Year or not (simplified way)?
      function isLeapYear(year){
          const remainder = year % 4;
          if(remainder === 0){
              console.log('year is leap year', year)
          }else{
              console.log('year is not a leap year', year)
          }
      }
      isLeapYear(2024)


```

### String
<details>
<summary>
  <h3>What is String?</h3>
</summary>
<br >

</details>

```js
//find the value in string (search string)
// using includes
const  lyrics  = 'Tumi bondhu kala pakhi ami jeno ki.';
const doesExist = lyrics.includes('pakhi');
console.log(doesExist)

const  lyrics  = 'Tumi bondhu kala pakhi ami jeno ki.';
//word গুলো split দিয়ে আলাদা করে।
const parts = lyrics.split('');
//slice  দিয়ে কোন index diya start hobe & কোন index end hobe
const partial = lyrics.slice(5, 15);
//
const joinInString = lyrics.join(', ');

console.log(parts)


```

### whileLoop
<details>
<summary>
  <h3>What is whileLoop?</h3>
</summary>
<br >

</details>

```js

 ### It takes 4 things to write a loop
  // 1. loop variable
  // 2. conditon inside while
  // 3. Loop body
  // 4. Change the loop variable
  ====================
  //simple typeing while loop
    let roastGiven = 0;
    while(roastGiven <= 17){
        console.log(roastGiven, 'rost den')
        roastGiven++;
    }
    //while loop in a reverse way
    let num = 10
    while(num >= 1){
        console.log(num)
        num--;
    }


```

### forLoop
<details>
<summary>
  <h3>What is forLoop?</h3>
</summary>
<br >

</details>

```js

 ### It takes 4 things to write a loop
  // 1. loop variable
  // 2. conditon inside while
  // 3. Loop body
  // 4. Change the loop variable
  ====================
// simple version of for loop (Example 1)
for(let i = 0; i < 7; i++){
    console.log(i)
}
 let numbers = [45, 87, 89, 56, 32, 51, 25]
// (Example 2)
for(let i = 0; i < numbers.length; i++){
    const number = numbers[i];
    console.log(number)
}
// (Example 3)
for(const number of numbers){
    console.log(number)  
}
// find the array element
console.log(numbers.indexOf(56))
// condition loop  break (Example 4)
for(let i = 1; i < 20; i++){
    console.log(i)  
    if(i > 5){
        break;
    }
}
// condition loop continue
let bookPrices = [234, 42, 124, 768, 91, 765, 231, 90, 89, 64, 200, 23, 201]
for(i = 0; i < bookPrices.length; i++){
    let bookPrice = bookPrices[i]
    if(bookPrice > 200){
        continue;
    }
    console.log(bookPrice, 'book price ')
}

//for loop in a reverse way
for (let i = 10; i >= 1; i--) {
    console.log(i)
}


//array value (array এর মান যোগ)
function getSumOfAnArray(numbers){
    let sum = 0;
    for(let i = 0; i < numbers.length; i++){
        const index = i;
        const element = numbers[index];
        sum = sum + element;
    }
    return sum;
}

// find array in odd numbers
function getOddNumbersOfAnArray(numbers){
    const oddNumbers = [];
    
    for(let i = 0; i < numbers.length; i++){
        const index = i;
        const element = numbers[index];
        if(element % 2 !== 0){
            console.log(index, element)
            oddNumbers.push(element)
            console.log(oddNumbers)
        }
    }
    return oddNumbers;
}

const myNumbers = [12, 43, 54, 65, 78, 91];
const oddNumbers = getOddNumbersOfAnArray(myNumbers)
console.log(oddNumbers)
const oddNumberSum = getSumOfAnArray(myNumbers)
console.log('odd number sum',oddNumberSum )

// multiplication 1 to 7
function factorial(number){
    let result = 1;
    for(let i = 1; i <=number; i++){
        result = result * i
    }
    return result;
}

const result = factorial(7);
console.log(result)

//সব থেকে বড় number ta বের করা।
function maxInArray(numbers) {
    //সব থেকে বড় number 0 ধরলাম।
    let largest = numbers[0];
    for (let i = 0; i < numbers.length; i++) {
        const index = i;
        const element = numbers[index];
        if (element > largest) {
            largest = element;
        }

    }
    return largest;
}

const heights = [167, 190, 120, 165, 139, 534];
const tallest = maxInArray(heights);
console.log('tallest person is', tallest)


```

### Recursion
<details>
<summary>
  <h3>What is Recursion?</h3>
</summary>
<br >
- Recursion is
</details>

```js
//factorial er man ber
let factorial = 1;
for(let i = 5; i >= 1; i--){
    factorial = factorial * i;
}
console.log(factorial)

// Recursion function  diya factorial er man ber
function factorial(i){
    if(i == 1){
        return 1;
    }
    return i * factorial(i-1)
}
const result = factorial(5);
console.log(result)
```

### TemplateString
<details>
<summary>
  <h3>What is Template String?</h3>
</summary>
<br >
- Template String is
</details>

```js
const numbers = [87, 342, 54, 23, 56, 234];
const student = {
    name: 'sakib Khan',
    age: 32,
    movies: ['king khan', 'dhakar masta,', 'aynabaji']
};
const about = `My name is ${student.name} age of ${student.age} has number ${numbers[2]} also liked mvies ${student.movies[2]}`;
console.log(about)
```

### ArrowFunction
<details>
<summary>
  <h3>What is Arrow Function?</h3>
</summary>
<br >
- Arrow Function is
</details>

```js
const getFiftyFive = () => 55
const addSixtyFive = num => num + 65;
const isEven = x => x % 2 == 0;
const addThree = (x, y, z) => x + y + z;
const doMath = (num1, num2) => {
    const sum = num1 + num2
    return sum
}
```
### SpreadOperator
<details>
<summary>
  <h3>What is SpreadOperator?</h3>
</summary>
<br >
- Spread Operatorn is
</details>

```js
//spread operator
const numbers = [87, 342, 54, 23, 56, 234];
const newNumbers = [...numbers];
numbers.push(99)
numbers.push(91)
numbers.push(93)

// create a new from an older array and add an element
const currentNumbers = [...numbers, 55];
console.log(numbers)
console.log(newNumbers)
console.log(currentNumbers)
}
// output
numbers [ 87, 342, 54, 23, 56, 234, 99, 91, 93 ]
newNumbers [ 87, 342, 54, 23, 56, 234 ]
currentNumbers [ 87, 342, 54, 23, 56, 234, 99, 91, 93, 55 ]
```

### concat
<details>
<summary>
  <h3>What is concat?</h3>
</summary>
<br >
- concat
</details>

```js
const friends = [13, 14, 11, 17, 21, 16, 15, 20];
console.log(friends)
const newFriendsAge = [12, 14, 13, 16];
const allFriends = newFriendsAge.concat(friends);
console.log(allFriends)
```

### Map
<details>
<summary>
  <h3>What is Map?</h3>
</summary>
<br >
- If you want to return an array by working for the element, you need to use a map. 
- Map return array
</details>

```js
const products = [
    { name: 'laptop', price: '3200', brand: 'Lenovo', color: 'Silver' },
    { name: 'phone', price: '3499', brand: 'iphone', color: 'golden' },
    { name: 'watch', price: '420', brand: 'casio', color: 'yellow' },
    { name: 'sunglass', price: '250', brand: 'reborn', color: 'black' },
    { name: 'camera', price: '39000', brand: 'canon', color: 'black' },
    { name: 'laptop', price: '3200', brand: 'Lenovo', color: 'Silver' }
];

const brands = products.map(product => product.brand);
console.log(brands)
const prices = products.map(product => product.price);
console.log(prices)
```
### forEach
<details>
<summary>
  <h3>What is forEach?</h3>
</summary>
<br >
- If you want to return an array by working for the element, you need to use a map. 
- Map return array
</details>

```js
const products = [
    { name: 'laptop', price: '3200', brand: 'Lenovo', color: 'Silver' },
    { name: 'phone', price: '3499', brand: 'iphone', color: 'golden' },
    { name: 'watch', price: '420', brand: 'casio', color: 'yellow' },
    { name: 'sunglass', price: '250', brand: 'reborn', color: 'black' },
    { name: 'camera', price: '39000', brand: 'canon', color: 'black' },
    { name: 'laptop', price: '3200', brand: 'Lenovo', color: 'Silver' }
];
products.forEach(product => console.log(product))
products.forEach(product => console.log(product.color))
products.forEach(product => {
})
```
### filter 
<details>
<summary>
  <h3>What is filter?</h3>
</summary>
<br >
- If a filter is used to conditionally select one or more elements of an array, the filter works condition wise.
</details>

```js
const products = [
    { name: 'laptop', price: '3200', brand: 'Lenovo', color: 'Silver' },
    { name: 'phone', price: '3499', brand: 'iphone', color: 'golden' },
    { name: 'watch', price: '420', brand: 'casio', color: 'yellow' },
    { name: 'sunglass', price: '250', brand: 'reborn', color: 'black' },
    { name: 'camera', price: '39000', brand: 'canon', color: 'black' },
    { name: 'laptop', price: '3200', brand: 'Lenovo', color: 'Silver' }
];
// filter
const cheap = products.filter(product => product.price <= 5000);
console.log(cheap)
const specificName = products.filter(product => product.name.includes('n'));
console.log(specificName)
```
### find  
<details>
<summary>
  <h3>What is find?</h3>
</summary>
<br >
- Find is used to conditionally find the first element in an array. If more than one element meets the condition, find returns the first element.
</details>

```js
const products = [
    { name: 'laptop', price: '3200', brand: 'Lenovo', color: 'Silver' },
    { name: 'phone', price: '3499', brand: 'iphone', color: 'golden' },
    { name: 'watch', price: '420', brand: 'casio', color: 'yellow' },
    { name: 'sunglass', price: '250', brand: 'reborn', color: 'black' },
    { name: 'camera', price: '39000', brand: 'canon', color: 'black' },
    { name: 'laptop', price: '3200', brand: 'Lenovo', color: 'Silver' }
];
//find
const special = products.find(product => product.name.includes('n'));
console.log(special)
```
### JSON  
<details>
<summary>
  <h3>What is JSON?</h3>
</summary>
<br >
- Find is used to conditionally find the first element in an array. If more than one element meets the condition, find returns the first element.
</details>

```js
const student = {
    name: 'sakib Khan',
    age: 32,
    movies: ['king khan', 'dhakar masta,', 'aynabaji']
};
// normal Object to JSON file
const studentJson = JSON.stringify(student);
console.log(student)
console.log(studentJson)

// JSON to Object file
const studentObject = JSON.parse(studentJson);
console.log(studentObject)
```
### fetch_Keys_Values  
<details>
<summary>
  <h3>What is fetch?</h3>
</summary>
<br >
- Find is used to conditionally find the first element in an array. If more than one element meets the condition, find returns the first element.
</details>

```js
// fetch
fetch('url')
.then(res => res.json())                                    
.then(data => console.log(data)
)

const student = {
    name: 'sakib Khan',
    age: 32,
    movies: ['king khan', 'dhakar masta,', 'aynabaji']
};
//keys
const keys = Object.keys(student);
console.log(keys )
// keys = ['name', 'age', 'movies']

// values
const values = Object.values(student);
console.log(values )
// values ['sakib Khan', 32, Array(3)]
```
### Array  
<details>
<summary>
  <h3>What is fetch?</h3>
</summary>
<br >
- Find is used to conditionally find the first element in an array. If more than one element meets the condition, find returns the first element.
</details>

```js
//simple array you know?
let numbers = [45, 68, 78, 56, 89, 98]
//1. get element value by index
let element = numbers[1]
console.log(element)
//2. set element value by index
numbers[1] = 77;
numbers[3] = 44;
console.log(numbers)
//3. find index of an element
let positionIndex = numbers.indexof(89)
console.log(positionIndex)

//=== Push and Pop===
//push (Add new elements to the first/last of an array)
numbers.push(55);
numbers.unshift(33);
//push (remove the the first/last element of an array)
numbers.pop();
numbers.shift();

//===Advance===
// add or remove from an array
const products = [
    { name: 'laptop', price: '3200', brand: 'Lenovo', color: 'Silver' },
    { name: 'phone', price: '3499', brand: 'iphone', color: 'golden' },
    { name: 'watch', price: '420', brand: 'casio', color: 'yellow' },
    { name: 'sunglass', price: '250', brand: 'reborn', color: 'black' },
    { name: 'camera', price: '39000', brand: 'canon', color: 'black' },
    { name: 'laptop', price: '3200', brand: 'Lenovo', color: 'Silver' }
];

const newProduct = {name: 'webcam', price: '670', brand: 'light blue'};

//copy products array and then add newProduct
const newProducts = [...products, newProduct];
//create a new array without one specific item
//remove item means create a new array without the 
const remaining = products.filter(product => product.name !== 'phone');

//array value (array এর মান যোগ)
function getSumOfAnArray(numbers){
    console.log(numbers)
    let sum = 0;
    for(let i = 0; i < numbers.length; i++){
        const index = i;
        const element = numbers[index];
        sum = sum + element;
        console.log(index, element, sum)
    }
    return sum;
}
const myNumbers = [12, 43, 54, 65, 78, 91];
getSumOfAnArray(myNumbers)

// find array in odd numbers
function getOddNumbersOfAnArray(numbers){
    for(let i = 0; i < numbers.length; i++){
        const index = i;
        const element = numbers[index];
        if(element % 2 !== 0){
            console.log(index, element)
        }
    }
}

//সব থেকে বড় number ta বের করা।
function maxInArray(numbers) {
    //সব থেকে বড় number 0 ধরলাম।
    let largest = numbers[0];
    for (let i = 0; i < numbers.length; i++) {
        const index = i;
        const element = numbers[index];
        if (element > largest) {
            largest = element;
        }

    }
    return largest;
}

const heights = [167, 190, 120, 165, 139, 534];
const tallest = maxInArray(heights);
console.log('tallest person is', tallest)


```

### Object
<details>
<summary>
  <h3>What is Object?</h3>
</summary>
<br >
- If you want to return an array by working for the element, you need to use a map. 
- Map return array
</details>

```js
let shoppingCart = {
    books: 3,
    sunglass: 2,
    kewboard: 4,
    mouse: 1,
    pen: 23
}
// when you kno the specific property name
let penCount = shoppingCart.pen;
let penCount2 = shoppingCart['pen']
// when you want all propeties keys name
let propertiesKeys = Object.keys(shoppingCart)
// when you want all propeties values name
let propertiesValues = Object.values(shoppingCart)


//set property values
shoppingCart.mouse = 15;
shoppingCart['mouse'] = 29;
shoppingCart[propertyName] = 89;


```

### numberStringConversion
<details>
<summary>
  <h3>What is forEach?</h3>
</summary>
<br >
- If you want to return an array by working for the element, you need to use a map. 
- Map return array
</details>

```js
//number To String Conversion
//Example 1
const input = '400';
const inputNum = +input;
console.log(typeof inputNum)

//String To Number Conversion
//Example 2
const input2 = 53;
const numStr = input2 + '';
console.log(typeof numStr)
```

### LocalStorageAndSessionStorage
<details>
<summary>
  <h3>What is LocalStorage And Session Storage?</h3>
</summary>
<br >
- Three working in Local storage and Session Storage 
-  setItem
- getItem
- removeItem
</details>

```js
   //Data add local storage
    const handleAddData = () => {
        localStorage.setItem('cart', '123')
    };
    //Data Read / Shows local storage
    const handleShowData = () => {
       const item = localStorage.getItem('cart')
       console.log(item)
    };
     //Data Remove local storage
    const handleRemoveData = () => {
        localStorage.removeItem('cart')
    };
    
    //Example
  <button onClick={handleAddData}>Add</button>
  <button onClick={handleShowData}>Read / Shows</button>
  <button onClick={handleRemoveData}>Remove</button>
  
  //Object Data add local storage
    const handleAddData = () => {
        localStorage.setItem('cart', JSON.stringify({abc: 1, bcd: 2}))
    };
    //Object Data Read / Shows local storage
    const handleShowData = () => {
       const item = JSON.parse(localStorage.getItem('cart'))
       console.log(item)
    };
     //Data Remove local storage (Remove same)
    const handleRemoveData = () => {
        localStorage.removeItem('cart')
    };
    
    
        // localStorage connect to ui
    useEffect(() => {
        if (products.length) {
            const storedProductIds = getFromLocalStorage();
            const previousCart = [];

            for (const id in storedProductIds) {
                const foundProduct = products.find(product => product.id === id);
                if(foundProduct){
                    const quantity = storedProductIds[id];
                    foundProduct.quantity = quantity
                    previousCart.push(foundProduct)
                }
            }
            setCart(previousCart)
        }

    }, [products])
    
    
    
    <details>
<summary>
  <h3>Local Storage Fake Db</h3>
</summary>
<br >
// use local storage to manage cart data
const addToDb = id =>{
// set localStorage
    let shoppingCart = {};

    //get the shopping cart
        // যেই নামে setItem করা হইছে সেই নামে পেতে হবে/
        const storedCart = localStorage.getItem('shopping-cart');
        if(storedCart){
            console.log(storedCart)
            // local store data save হই string হিসাবে  সেইটা getItem করার সময় normal javascript a conver korta hoi
            // সেই জন্য JSON.parse(storedCart) করা লাগে।
            shoppingCart = JSON.parse(storedCart)

        }

    // add quantity
   const quantity = shoppingCart[product.id];
        if (quantity) {
            // const newQuantity = quantity + 1;
            shoppingCart[product.id] = quantity + 1;

        } else {
            shoppingCart[product.id] = 1;
        }
        
    // local storage name set
        // step 1 key and value দুইটাই object হওয়া লাগবে;
        // step 2 object কে string convert korar jonno JSON.stringify(shoppingCart) করা লাগবে।
        localStorage.setItem('shopping-cart', JSON.stringify(shoppingCart))
}

const getStoredCart = () =>{
    let shoppingCart = {};

    //get the shopping cart from local storage
    const storedCart = localStorage.getItem('shopping-cart');
    if(storedCart){
        shoppingCart = JSON.parse(storedCart);
    }
    return shoppingCart;
}

const removeFromDb = id =>{
    const storedCart = localStorage.getItem('shopping-cart');
    if(storedCart){
        const shoppingCart = JSON.parse(storedCart);
        if(id in shoppingCart){
            delete shoppingCart[id];
            localStorage.setItem('shopping-cart', JSON.stringify(shoppingCart));
        }
    }
}

const deleteShoppingCart = () =>{
    localStorage.removeItem('shopping-cart');
}

export {
    addToDb,
    getStoredCart,
    removeFromDb,
    deleteShoppingCart
};- Find is used to conditionally find the first element in an array. If more than one element meets the condition, find returns the first element.
</details>
    
```

### switch

```js
//switch
let color = 'green';

switch (color) {
    case 'green':
        console.log('You are a green friend')
        break;
    case 'Blue':
        console.log('You are a Blue friend')
        break;
    case 'red':
        console.log('You are a red friend')
        break;
    case 'white':
        console.log('You are a white friend')
        break;
    case 'Black':
        console.log('You are a Black friend')
        break;
    default:
        console.log('You are a pink friend')
}

```

### jsProblemSolved

```js

### Number 1 
//Number 1 => Example 1
// charecter forword way of String (string  টা কে  সোজা দিক থেকে console.log করা)
// text = myString কারণ  parametar যেইটাই পাঠাই না কেন অন্য নামে recive kore 
// যেমন myString হিসাবে পাঠাইছে  text হিসাবে recived করছে
function reverseString(text){
    for(let i = 0; i < text.length; i++){
        const element = text[i];
        console.log(element)
        
        
    }
}
//Number 1 => Example 2
// charecter reverse way of String (string টা কে উল্টা দিক থেকে console.log করা)
function reverseString(text){
    for(let i = text.length; i >= 0; i--){
        const element = text[i];
        console.log(element)
    }
}

const myString = 'i am a good boy';
const reversed = reverseString(myString);
console.log(reversed)

//Number 1 => Example 3
// Word reverse way of String (string টা কে উল্টা দিক থেকে console.log করা)
function reverseWord(str){
    //split kore potita word ke alada alada kor hoisa
    const words = str.split(' ');
    const result = [];
    //-1 last element er index 1 kom (undifiend jate na dekhai) 
    for(let i =  words.length - 1; i >= 0; i--){
        const element = words[i];
        
        result.push(element)
    }
    // word gulo ek sentens anar jonno join kora hoisa
    const reversed = result.join(' ');
    return reversed;
}
const myString = 'i am a good boy';
const reversed = reverseWord(myString);
console.log(reversed)

//Number 1 => Example 4
// আগের দুটা মান যোগ করে পরের মান সেট করা
//const fibonacci = [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144]
/* 
    fibo[3] = fibo[2] + fibo[1]
    fibo[4] = fibo[3] + fibo[2]
    fibo[n] = fibo[n-1] + fibo[n-2]
    fibo[3] = fibo[i-1] + fibo[i-2]
*/
const fibo  = [0, 1];
// 0, 1 already define(0 ,1  value diyai dici tai 2 theke start korta hobe)
for(let i = 2; i <= 25; i++){
    fibo[i] = fibo[i - 1] + fibo[i - 2]
}
console.log(fibo)

//Number 1 => Example 5
//Remobe name duplicate From An Array
const  names = ['abul', 'babul', 'kable', 'dabul', 'ebul', 'babul', 'abul', 'kabul', 'gabul', 'cabul', 'babul', 'abul', 'abul', 'cabul'];
function removeDuplicate(names){
    const unique = [];
    for(let i = 0; i < names.length; i++){
        if(unique.includes(name) === false){
            unique.push(name)
        }
    }
    return unique;
}
const uniqueName = removeDuplicate(names);
console.log(uniqueName)
//Remobe Number duplicate From An Array
const friends = [12, 45, 32, 22, 44, 62, 29, 23, 22, 12, 45, 44, 69, 87];
function removeDuplicateNumber(friends) {
    const uniqueNumber = [];
    for (const friend of friends) {
        if (uniqueNumber.includes(friend) === false) {
            uniqueNumber.push(friend)
        }
    }
    return uniqueNumber
}
console.log(removeDuplicateNumber(friends))


<--Number 2-->
//Number 2 => Example 1
/* 
// Show output from 1-100
1. if the number is divisible by 3 then insted of the show 'foo', is number 5 then show 'bar'
2. if the number divisible by both 3and 5 then instead of the number show 'footbar'
*/
for (let i = 1; i <= 50; i++) {
    if (i % 3 === 0 && i % 5 === 0) {
        console.log('foobar')
    }else if (i % 3 === 0) {
        console.log('foo')

    } else if (i % 5 === 0) {
        console.log('bar')

    } else {
        console.log(i)
    }
}

//Number 2 => Example 2
/* 
Fixed: per item wood requirments
Vary: quantity
1. chair --> 3 cft
2. table --> 10 cft
3. bed --> 50 cft
*/
function woodCalculator(chairQuantity, tableQuantity, bedQuantity){
    const perChariWood =  3;
    const perTableWood = 10;
    const perBedWood = 50;

    const chairWood = chairQuantity * perChariWood;
    const tableWood = tableQuantity * perTableWood;
    const bedWood = bedQuantity * perBedWood;

    const total = chairWood + tableWood + bedWood;
    return total;
}
const totalWood = woodCalculator(2, 1, 1);
console.log('total wood required', totalWood)

//Number 2 => Example 3
// find cheapest price in array of object
const phones = [
    { name: 'Samsung', camera: 12, storage: '32gb', price: 36000, color: 'silver' },
    { name: 'Waltor', camera: 10, storage: '32gb', price: 22000, color: 'silver' },
    { name: 'Iphone', camera: 10, storage: '32gb', price: 82000, color: 'silver' },
    { name: 'Xiomi', camera: 10, storage: '32gb', price: 52000, color: 'silver' },
    { name: 'Oppo', camera: 10, storage: '32gb', price: 20000, color: 'silver' },
    { name: 'Nokia', camera: 10, storage: '32gb', price: 44000, color: 'silver' },
    { name: 'HTC', camera: 10, storage: '32gb', price: 62000, color: 'silver' },
    { name: 'Techno', camera: 10, storage: '32gb', price: 12000, color: 'silver' }
];
function cheapestPhone(phones) {
    let cheapest = phones[0]
    for (const phone of phones) {
        if (phone.price < cheapest.price) {
            cheapest = phone;
        }
    }
    return cheapest;
}

const mySelection = cheapestPhone(phones);
console.log(mySelection)

//Number 2 => Example 4

/* 
1.if ticket numbers is less then 100, per ticket price: 100
2.if tikcket numbers is more than 100, but less than 200. first 100  ticket price will be 100. rest tickets will be 900 taka per ticket.
    first 100 --> 100 tk
    rest ---> 90 tk
3. if you perchase more than tickets
first 100 ---> 100 tk
101-200 ---> 90 tk
200 + ---> 70 tk
*/
function ticketPrice(ticketQuantity){
    const first100Ticket = 100;
    const second100Ticket = 90;
    const restTicket = 70;
    if(ticketQuantity <= 100){
        const price = ticketQuantity * first100Ticket;
        return price;
    }
    else if(ticketQuantity <= 200){
        const first100Price = 100 * first100Ticket;
        const restTicketQuantity  = ticketQuantity - 100;
        const restTicketPrice  = restTicketQuantity * second100Ticket;
        const totalPrice = first100Price + restTicketPrice;
        return totalPrice;
    }
    else{
        const first100Price = 100 * first100Ticket;
        const second100Price = 100 * second100Ticket;
        const restTicketPrict = ticketQuantity - 200;
        const restTicketPrice = restTicketPrict * restTicket;
        const totalPrice = first100Price + second100Price + restTicketPrice;
        return totalPrice;
    }
}
const price = ticketPrice(101);
console.log(price)

//Number 2 => Example 5

// array এর ভিতর কোন কোন কিছু খুঁজে বের করা
const products = [
    {id: 1, name: 'walton Phone', price: 1900, color: 'silver'},
    {id: 2, name: 'mac book air', price: 1900, color: 'green'},
    {id: 3, name: 'Samsung Phone', price: 1900, color: 'yellow'},
    {id: 4, name: 'lenovo yoga lapTOP 2025', price: 1900, color: 'black'},
    {id: 5, name: 'I phone Phone', price: 1900, color: 'red'},
    {id: 6, name: 'dell inspiron laptop', price: 1900, color: 'blue'},
    {id: 7, name: 'nokia old age phone gone', price: 1900, color: 'pink'},
    {id: 8, name: 'htc phone', price: 1900, color: 'white'},
];
//search parameter diya products এর ভিতর যে কোন কিছু খুঁজবো
function matchedProducts(products, search){
    //খুজে যেইটা পাবো তার জন্য array declare (matched) করতে হবে।
    const matched = [];
    
    for(const product of products){
        if(product.name.toLowerCase().includes(search.toLowerCase())){
            matched.push(product)
        }
    }
    return matched;
}
//যেই object a phone  আছে সেই object খুজে দাউ
const result = matchedProducts(products, 'laptop');
console.log(result)



<--Number 3-->
//Number 1 => Example 1

//find largest number
let arr = [3,5, 6, 7, 8, 34, 6,5, 76, 126]
let largest = arr[0]
for(let i = 0; i < arr.length; i++){
    const element = arr[i];
    if(element > largest){
        largest = element;
    }
}
console.log(largest)

//Number 3 => Example 2

// calculate Electricity bill
//for first 100 unit - 5 tk
//for more than 100 unit 6 tk for every unit more than 100
//for more than 200 unit 7 tk for every unit more than 200
// 250 unit
//100 * 5 = 500
//(200 - 100) * 6
//(250 - 200) * 7

function electricity(unit) {
    let bill;
    if (unit <= 100) {
        bill = unit * 5
    } else if (unit <= 200) {
        const first100 = 100 * 5;
        const remaining = unit - 100;
        const remainingCost = remaining * 6;
        bill = first100 + remainingCost;
    } else if(unit > 200){
        const first100 = 100 * 5;
        const second100 = 100 * 6;
        const remaining = unit - 200;
        const remainingBill = remaining * 7;
        bill = first100 + second100 + remainingBill
    }
    return bill;
}

const result = electricity(150);
console.log(result)

//Number 3 => Example 3
// find if anybody got A+ from your friends
// marks = [78, 82, 69]
function checkGPA(arr){
    for(const mark of arr){
        if(mark >= 80){
            return true
        }
    }
    return false;
}
const result = checkGPA([78, 62, 69]);
console.log(result)

//Number 3 => Example 4
//check if a number is Prime
//1 number 11
//2 => number-1
function isPrime(number){
    for(let i = 2; i < number; i ++){
        if(number % i == 0){
            return false
        }
    }
    return true;
}
const result = isPrime(19);
console.log(result)

//Number 3 => Example 5



```
  
<details>
<summary>
  <h3> ### jsProblemSolved</h3>
</summary>
<br >

```js
  
  
 ### Practice problems
  
1) Harry’s mom gave him tk 1000 and asked him to buy some oranges and
apples. Write a program to help Harry calculate how much money the
shopkeeper will return. The total cost of 1 kg of oranges and 1 kg of
apples is tk 700.
2) Write a program to calculate the average marks of Mathematics,
Biology, Chemistry, Physics, and Bangla of a student.
3) John’s teacher gave him two variables. Each variable contains a string.
John’s teacher asked him to combine these two strings(‘I am going to
be’ and ‘an awesome web developer’) and print them in one line. Help
John write the program.
4) Sarah’s mother is teaching her mathematics. She gave Sarah the number
119 and asked her what the remainder would be if she divided the number
by 5. Help Sarah write the program.
  
5) নি চে র ভে রি য়ে বল ডি ক্লে য়ার এ ক োনটার মধ্যে কি কি সমস্যা আছে । দে খত ো বে র করতে
পার ো কি না?
Var price = 33
var name - Shabana
var boxName = ‘Cocola;
var 88_price = 34;
var enum = -1;
var _$box’78 = ‘Monika’;
var home-address = “kochu khet”;
  
6) You are given an array:
var fruits = ['Apple', 'Banana', 'Orange'];
  a) Find the index of ‘Banana’ and replace ‘Banana’ with ‘Mango’.
  b) Remove ‘Orange’ and add ‘Watermelon
  
 7) You and your friends Tom, Jane, Peter and John got their final exam
results. Your total score is 85, Tom’s total score is 66, Jane’s total score is
95, Peter’s total score is 56 and John’s total score is 40. The grading
chart is
80 or above A grade
60 or above B grade
50 or above C grade
40 or above D grade
39 or less => F grade
Write a program to find your and your friends’ grades using
if-else.

 8) You are given three numbers 13, 79, and 45. Write a program that will
print the largest number using if-else.
9) You are given a triangle with the sides 9, 8, 9. Write a program to check
whether a triangle is Isosceles or not using if-else.
Isosceles => two sides are equal
10) ক্লাস সে ভে র এর ফাইনাল এক্সাম এ তুমি ফার্স্ট হয়ে ছ। ত োমার বন্ধুআলি য়া, ডালি য়া,
সালি য়া, মালি য়া, লি লি য়া আর জ্বালাইয়া - তাদে র grade তুমি জান ো না। তবে তাদে র নম্বর
জান ো. আলি য়া 95 পে য়ে ছে , ডালি য়া 66 পে য়ে ছে , সালি য়া 80 পে য়ে ছে , মালি য়া পে য়ে ছে 59,
লি লি য়া পে য়ে ছে 47, জ্বালাইয়া পে য়ে ছে 77। তুমি JS code দি য়ে তাদে র grade বে র করে
দি তে পারবে ?
১) যারা ৫০ এর নি চে পে য়ে ছে , তাদে র grade F.
২) যারা ৫০ বা তার উপরে পে য়ে ছে , অথবা ৬০ এর নি চে পে য়ে ছে , তাদে র grade D.
৩) যারা ৬০ বা তার উপরে পে য়ে ছে , অথবা ৭০ এর নি চে পে য়ে ছে , তাদে র grade C.
৪) যারা ৭০ বা তার উপরে পে য়ে ছে , অথবা ৮০ এর নি চে পে য়ে ছে , তাদে র grade B.
৫) যারা ৮০ বা তার উপরে পে য়ে ছে , অথবা ৯০ এর নি চে পে য়ে ছে , তাদে র grade A.
৬) যারা ৯০ বা তার উপরে পে য়ে ছে , তাদে র grade A+.
  
11) তাড়াহুড়া করে স্কুলে র জন্য বে র হচ্ছ কি ন্তু রাস্তা পার হওয়ার সময় দে খলে , ট্রাফি ক
সি গন্যাল লাল রং। এই অবস্থায় যদি তুমি রাস্তা পার হওয়ার চে ষ্টা কর, তাহলে ডে ঞ্জার হতে
পারে । যদি হলদু রং হয় তাহলে ত োমার থে মে যাওয়া উচি ত। আর যদি ট্রাফি ক সি গন্যাল গ্রি ন
হয় তাহলে ত োমার রাস্তা পার হওয়া উচি ত। তাই একটা ক োড লি খে ফে ল ো। যে খানে আমরা
signal নামে একটা ভে রি য়ে বল থাকবে । সে টার মান green, yellow বা red হতে পারে ।
সে ই অনসুারে ডি ফারে ন্ট ডি ফারে ন্ট কাজ হবে । ত ো, সে ই ক োড ফটাফট লি খে ফে ল ো।
12) প্রতি দি ন ত োমার কাজ কি ?
১) রাত ৮ টা বাজে মডি উল আনলক কর ো
২) ফটাফট ভি ডি ও দে খে দে খে প্রাকটিস কর ো
৩) ভি ডি ও দে খতে দে খতে ন োটস নাও
৪) মডি উল শে ষ হলে পুরা মডি উল নি জে নি জে প্রাকটিস কর ো
৫) ক োন কি ছুবঝু তে না পারলে (চি ন্তা করে দে খ ো এইখানে কি ন্তু একটা শর্ত আছে ), সাপ োর্ট সে শনে
জয়ে ন কর ো
এখন ত োমার কাজ হচ্ছে একটা for লপু ১০ বার চালি য়ে উপরে র জি নি সগুলা আউটপুট হি সে বে
দে খান ো।
13) আবার একই জি নি স while লপু চালি য়ে ১০ বার দে খান ো।
14) উপরে র প্রব্লে মটাই while লপু রি ভার্স ওয়ে তে (decremental হি সে বে )করে দে খাও
15) উপরে র প্রব্লে মটাই for লপু রি ভার্স ওয়ে তে (decremental হি সে বে )করে দে খাও
16) ত োমার কাছে : ৮০০০০ টাকার বে শি হলে তুমি mac কি নবে , ৬০ টাকার বে শি হলে gaming ল্যাপটপ
কি নবে , ৪০ হাজার টাকার বে শি হলে lenovo yoga কম্পি উটার কি নবে , ২০ হাজার টাকার বে শি হলে পুরান
ল্যাপটপ কি নবে । না হয় তুমি ম োবাইল দি য়ে কাজ চালাবে ।
17) আসকে আমার মন ভাল ো নে ই এই কথা ৩৯ বার আউটপুট হি সে বে দে খাও।
18) while লপু কি ভাবে কাজ কর
  19) একটা ক োড লি খে ৫৮ থে কে ৯৮ পর্যন্ত যত সংখ্যা আছে সে গুলাকে দে খাও
20) একটা ক োড লি খে ৪১২ থে কে ৪৫৬ পর্যন্ত যত জ োর সংখ্যা আছে সে গুলাকে
দে খাও
21) একটা ক োড লি খে ৫৮১ থে কে ৬২৩ পর্যন্ত যত বি জ োড় সংখ্যা আছে সে গুলাকে দে খাও
22) তুমি এতদি ন যা যা জি নি স শি খছ ো সে গুলার নাম দি য়ে একটা array বানাও। তারপর একটা
for লপু দি য়ে সে ই array এর সব উপাদান কে আউটপুট হি সে বে দে খাও।
23) তুমি এতদি ন পর্যন্ত যে যে মডে লে র ম োবাইল ফ োন ইউজ করে ছ ো সে গুলার নাম দি য়ে একটা
array বানাও। তারপর একটা while লপু দি য়ে সে ই array এর উপাদান গুলা একটা একটা করে
আউটপুট হি সে বে দে খাও
24) একটা ফর লপু চালাও। ৩০ থে কে ৮৬ পর্যন্ত। আর এই লপু ৪৪ এ গে লে ব্রে ক করবে । সে ই
জি নি স ক োড করে দে খাও
25) ত োমার যত বই আছে সে গুলার দাম নি য়ে একটা array লি খে ফে ল ো। যে বই গুল োর দাম ২০০
টাকার উপরে সে গুলাকে স্কি প করবে । অর্থাৎ সে গুলাকে আউটপুট হি সে বে দে খাবে না। বাকি দে র কে
আউটপুট হি সে বে দে খাবে । দে খ ো করতে পার ো কি না।
26) Write a function called foo() which prints “foo” and a function called bar()
which prints “bar”. Call function bar() in the foo() function after printing. What
will be the output? Now call the foo() to see the output.
27) Write a function called make_avg() which will take an three integers and
return the average of those values.
28) Challenging: Write a function called make_avg() which will take an array of
integers and the size of that array and return the average of those values.
29) Write a function called odd_even() which takes an integer value and tells
whether this value is even or odd. You need to do it in 4 ways:
● Has return + Has parameter
● No return + Has parameter
 30) You are in a hurry to go to your school on time. But when you are crossing
the road, the traffic signal is red coloured. In this situation, if you try to cross the
road, you may be in danger.If you notice a yellow coloured traffic signal, you
should stop. If you notice a green coloured traffic signal, you should cross the
road. So write a JS code, where there is a variable called signal. Its value can
be green, yellow or red & we will get different activities as output depending on
the variable. So, hurry up.
31) একটা ফাংশন লি খবা যে টা ১৩ এর নামতা (multiplication table) আউটপুট হি সে বে
দে খাবে ।
32) একটা ফাংশন লি খবা যে টা যে ক োন নামকে uppercase বা রে গুলার কে ইস হি সে বে নি বে আর
আউটপুট হি সে বে সে ই নাম lowercase করে রি টার্ন করবে ।
33) fullName নামে একটা ফাংশন তৈ রী কর যে টা ত োমার নামে র প্রথম অংশ এবং ত োমার
নামে র শে ষে র অংশ প্যারামি টার হি সে বে নি বে । আর ত োমার নামে র দইু অংশ জ োড়া দি য়ে আউটপুট
হি সে বে ত োমার পূর্ন নাম রি টার্ন করে দি বে । যে মন ধর ো, hablu এবং kanto ইনপুট প্যারামি টার
হি সে বে দি লে আউটপুট হি সে বে hablu kanto রি টার্ন করবে ।
34) একটা ফাংশন লি খবা যে টাকে তুমি ক োন সংখ্যাকে ইনপুট হি সে বে দি লে সে সে ই সংখ্যার
square করে সে ই square কে রি টার্ন করবে ।
অর্থাৎ তুমি ইনপুট হি সে বে 5 দি লে সে টাতে স্কয়ারে হি সে বে 25 আউটপুট হি সে বে পাবে ।
35) Write a function that will take hour as the input parameter and will convert it
into minutes and will return the result in minutes.
36) Write a function findLeapYear() that will take the array [2023, 2024, 2025,
2028, 2030] as the input parameter and will check if each year is a leap year. If
a year is a leap year insert that year in a new array, return the new array and
print the result.
37) Write a function findOddSum() that will take the array [ 5, 7, 8, 10, 45, 30 ]
as the input parameter and will return the sum of the odd numbers.
38) leapYear() নামে ফাংশন লি খ ো এবং নে ক্সট ইয়ার অর্থাৎ ২০২৩ কি leap year নাকি সে টা
চে ক কর ো। Leap year হলে ফাংশন true রি টার্ন করবে আর leap year না হলে false রি টার
 করবে ।
39) ত োমার বয়স কি odd নাকি even সংখ্যা সে টা চে ক কর একটা ফাংশন দি য়ে । সে ই
ফাংশনকে ক োন সংখ্যা প্যারামি টার হি সে বে দি লে , সে ই সংখ্যা Even হলে ফাংশন true রি টার্ন
করবে আর Odd হলে false রি টার্ন করবে ।
40) এমন একটা ফ্যাংশনা লি খ ো যে টাকে তুমি ঘন্টাকে ইনপুট প্যারামি টার হি সে বে দি বে । আর সে
সে ই ঘন্টাকে মি নি টে কনভার্ট করে মি নি ট রি টার্ন করবে ।
41) একটা লপু লি খতে হবে যে টা ১ থে কে ১০০ পর্যন্ত যত সংখ্যা আছে সে টা দে খাবে
42) ৫০ থে কে ৮০ এর মধ্যে যত ো বি জ োড় সংখ্যা আছে সে গুলাকে দে খাবে ।
43) তি নটা সংখ্যা এর য োগ করতে পারবে এমন একটা ফাংশন লি খ ো
44) ত োমাকে ফাংশনে র ইনপুট হি সে বে সে লসি য়াস দি বে । তুমি ক্যালকুলে শন করে তাপমাত্রা
ফারে নহাইট এ কনভার্ট করে সে টার আউটপুট রি টার্ন করবে
45) একইভাবে উল্টা হি সাব করবে । যাতে ত োমাকে ফারে নহাইট হি সে বে তাপমাত্রা দি লে সে টাকে
সে লসি য়াস এ কনভার্ট করে আউটপুট দি বে ।
46) কে উ ১০০ এর মধ্যে কত মার্ক্স্ পে য়ে ছে সে টা ত োমাকে বলে দি বে । তুমি একটা ফাংশন দি য়ে বলে
দি বে সে এ+ পাবে নাকি অন্য ক োন গ্রে ড পাবে ।
47) সুদে র হি সাব করবে । জাস্ট হি সাব কে মনে করতে হয়। সে ই চি ন্তায় করবে । সুদ ভাল ো না খারাপ
সে টা এখন চি ন্তা করার দরকার নাই। জাস্ট একটা ফর্মুলর্মু া থাকলে সে টা কি ভাবে ক োড এ লি খতে হয়
সে ই এঙ্গে ল থে কে করার চে ষ্টা কর ো।
48) Suppose, you have an array with 8 elements. Find the smallest element of
that array.
Now for the previous array, try to find the second largest element.
49) Write a function and take an array as a parameter. Find the average of all
the elements of that array and return this average.
50) Write a function which takes the height and width of a rectangle as
parameters. Find out the area of that rectangle and print the result.
  51) একটা ক োড লি খ ো। যে টা দি য়ে ক োন একটা array এর মধ্যে সবচে য়ে ছ োট
সংখ্যা বে র করে দি তে পারবে ।
52) একটা ক োড লি খ ো যে টা দি য়ে তি নটা সংখ্যার মধ্যে সবচে য়ে ছ োট সংখ্যা বে র
করে দি বে ।
53) একটা ফাংশন লি খ ো। সে ই ফাংশনে র মধ্যে ইনপুট হি সে বে একটা array নি বে ।
সে ই array এর মধ্যে অনে কগুলা সংখ্যা থাকবে । ত োমার কাজ হবে ইনপুট নে য়া
array এর মধ্যে যতগুলা সংখ্যা আছে । সে ই সংখ্যা গুলার গড় বে র করবে ।
তারপর সে ই গড় ফাংশনে র রি টার্ন হি সে বে দি য়ে দি বে । একটুচি ন্তা কর ো। বঝু ার
চে ষ্টা কর ো। ট্রাই কর ো। দে খ ো পার ো কি না।
54) একটা ফাংশন লি খ ো। যে টা ইনপুট প্যারামি টার হি সে বে একটা আয়তক্ষে ত্রে র
দৈ র্ঘ্য আর উচ্চতাকে নি বে । তারপর সে ই আয়তক্ষে ত্র এর area (আয়তন) কে
রে জাল্ট হি সে বে রি টার্ন করবে ।
55) (ট্রি কি ) ক োন একটা array এর মধ্যে অনে কগুলা সংখ্যা আছে । সে ই সংখ্যাগুল ো
থে কে second largest সংখ্যা বে র করার একটা প্র োগ্রাম লি খ ো। দরকার হলে
গুগলে সার্চ দাও। তারপর সার্চ রে জাল্ট দে খে বঝেুঝে বঝেুঝে করার চে ষ্টা কর ো।
56) একটা ফাংশন লি খ ো। সে টার মধ্যে তি নটা প্যারামি টার নি বে । এই তি নটা
প্যারামি টার হবে ক োন একটা ত্রি ভুজে র তি নটা বাহু এর দৈ র্য্য। এখন ত োমার কাজ
হচ্ছে ফাংশনে র ভি তরে কি ছুহি সাব নি কাশ করে ত্রি ভুজে র area (আয়তন) বে র
করা। ক োন একটা ত্রি ভুজে র তি নটা বাহুর দৈ র্য্য দে য়া থাকলে সে টা থে কে কি ভাবে
আয়তন বে র করতে হয় সে ই ফর্মুলর্মু া গুগল থে কে খুজেঁজে বে র কর ো।
57) ক োন একটা সংখ্যা প্রাইম সংখ্যা (prime number) কি না। সে টা চে ক করার একটা
ফাংশন লি খ ো।
58) দইুটা ভে রি য়ে বল এর মধ্যে য োগ, বি য় োগ, গুণ, ভাগ কি ভাবে করতে হয় সে টা কি জান ো।
অর্থাৎ তুমি কি +, -, *, /, %এইগুলার ব্যবহার জান ো। তাহলে নাম্বার টাইপে র দইুটা ভে রি য়ে বল
লি খ ো তারপর তাদে র য োগ করে সে টার মান আরে কটা ভে রি য়ে বল এ রাখ ো। একইভাবে ওই দইুটা
ভে রি য়ে বল এর মধ্যে বি য় োগ, গুন, ভাগ এবং ভাগশে ষ বে র কর ো।
59) তুমি কি দইুটা ভে রি য়ে বল এরমধ্যে তুলনা করতে পার ো। কম্পারি জন করতে পার ো। যে দইুটা
ভে রি য়ে বল এর মধ্যে প্রথমটা সে কে ন্ডটা এর চাইতে ছ োট, বড়, অসমান, সমান , ছ োট বা সমান,
  বড় বা সমান। এইগুলা চে ক করতে পার ো। অর্থাৎ <, >, ==, !=, <=, >= চি হ্নগুলা ব্যবহার করতে
পার ো। তাহলে দইুটা সংখ্যা টাইপে র ভে রি য়ে বল ডি ক্লে য়ার করে তাদে রকে এই ছয়ভাবে তুলনা করে
ক োড লি খে ফে ল ো।
.
60) ত োমার যদি দইুটা শর্ত পূরণ করতে বলে । এবং দইুটা শর্তে র মধ্যে দইুটাই পূরণ করতে হবে ।
তাহলে তুমি কি সে টা চে ক করতে পারবে ? একইভাবে যদি বলে তুমি দইুটা শর্তে র যে ক োন একটা
পূরণ করতে পারবে । অর্থাৎ তুমি && এবং || এর ব্যবহার করতে পার ো কি না। যদি পার ো তাহলে
নি জে নি জে এই রকমে র ক োড লি খে ফে ল ো।
61) তুমি কি একটা শর্ত পালন করলে একটা কি ছুকরবে । শর্ত পূরণ না করলে অন্য কি ছুএকটা
করবে এমন ক োড লি খতে পারবে । অর্থাৎ তুমি কি if-else এর ক োড লি খতে পারবে । পারলে একটা
ক োড লি খে ফে ল ো
.
62) ত োমাকে যদি বলে একটা while লপু দি য়ে ৭ থে কে ১৯ পর্যন্ত যতগুলা বি জ োড় সংখ্যা আছে
সে গুলা দে খাতে । তুমি কি সে টা দে খাতে পারবে ? পারলে সে ই ক োড লি খে ফে ল ো।
63) ত োমাকে যদি বলা হয় তুমি একটা array ডি ক্লে য়ার করবে । এবং সে টার মধ্যে কয়টা উপাদান
আছে সে টা বে র করবে হবে । সে ই array এর এর মধ্যে চতুর্থ পজি শন এর উপাদান চে ইঞ্জ করতে
হবে । array এর মধ্যে দইুটা উপাদান য োগ করতে হবে । এবং একটা উপাদান কে বে র করে দি তে
হবে । তুমি কি সে টা করতে পারবে ।
.
64) তুমি কি একটা ফর লপু দি য়ে ক োন একটা array এর সবগুলা উপাদানকে দে খাতে পারবে । সে টা
রে গুলার for লপু হ োক বা for of হ োক। হলে সে ই স্টাইলে একটা ক োড লি খে ফে ল ো।
65) ত োমাকে যদি বলা হয়। একটা array এর মধ্যে ৮০ এর চাইতে বড় সংখ্যা থাকলে সে গুলাকে
console log করে দে খাতে সে টা কি তুমি পারবে ? তাহলে তুমি সে ই ক োড করে ফে ল ো
.
66) তি নটা সংখ্যার গুনফল বে র করে ফাইনাল রে জাল্ট আউটপুট হি সে বে রি টার্ন করতে হবে । তুমি
কি সে ই ক োড লি খতে পারবে । যদি পার ো তাহলে সে ই ক োড লি খে ফে ল ো।
67) একটা অবজে ক্ট ডি ক্লে য়ার করবে । সে টাতে তি নটা প্রপার্টি থাকবে । এবং ক োন একটা প্র োপার্টি
এর মান চে ইঞ্জ করবা।
68) সি ম্পল একটা ফাংশন লি খতে হবে । যে টার নাম হবে feetToInch এবং এই ফাংশন
ইনপুট হি সে বে নি বে feet আর রি টার্ন করবে inch । অর্থাৎ এই ফাংশনকে ক োন
একটা ফি ট বলে দি লে সে রি টার্ন হি সে বে বলে দি বে কত ইঞ্চি হয়।
  69) একদম ফাংশন এর নাম হুবহু centimeterToMeter নাম দি য়ে একটা ফাংশন
লি খবে । এই ফাংশনে ইনপুট হি সাবে কে উ সে ন্টি মি টার দি বে আর সে ই সে ন্টি মি টার
কে মি টার এ কনভার্ট করে রে জাল্ট রি টার্ন করবে ।
.
70) আরে কটা ফাংশন লি খবে যে টার নাম লি খবে । যে ই ফাংশনে র নাম হবে paperRequirements
এই ফাংশনে র প্যারামি টার হি সে বে তি নটা প্যারামি টার হবে । প্রথম প্যারামি টার হবে তুমি প্রথম বই
কত কপি ছাপাতে চাও। সে কে ন্ড প্যারামি টার হবে তুমি সে কে ন্ড বই কত কপি ছাপাতে চাও। আর
থার্ড প্যারামি টার হবে তুমি থার্ড বই কত কপি ছাপাতে চাও। অর্থাৎ ক োন বই এর কত কপি ছাপান ো
হবে সে টাই প্যারামি টার হি সে বে নি বে ।
এইবার ভাল ো করে খে য়াল কর ো।
প্রথম বই ছাপান োর জন্য পৃষ্ঠা লাগবে ১০০ টা
সে কে ন্ড বই ছাপান োর জন্য পৃষ্ঠা লাগবে ২০০ টা
তৃতীয় বই ছাপান োর জন্য পৃষ্ঠা লাগবে ৩০০ টা
এখন ত োমার কাজ হচ্ছে paperRequirements নামক ফাংশন লি খে ফে লা যাতে । সে ই ফাংশনকে
কল করে ক োন বই এর কত কপি লাগবে বলে দি বে প্যারামি টার হি সে বে । আর ফাংশন হি সাব করে
বলে দি বে ত োমার সর্বম োট কতপৃষ্ঠা কাগজ লাগবে ।
উত্তর হি সে বে সংখ্যা রি টার্ন করবে ।
.
71) একটা ফাংশন লি খবে । এই ফাংশনে র নাম হবে bestFriend তারপর সে ই ফাংশনে
ইনপুট প্যারামি টার হি সে বে একটা array নি বে । সে ই array এর মধ্যে ত োমার সব
ফ্রে ন্ডে র নাম থাকবে । এখন ত োমার কাজ হচ্ছে যে ফ্রে ন্ড এর নাম সবচে য়ে বড় সে ই ফ্রে ন্ড এর
নাম রি টার্ন করে দে য়া। এই ক্ষে ত্রে তুমি নামটা অর্থাৎ ফ্রে ন্ডে র নাম (স্ট্রি ং) রি টার্ন করতে হবে ।
.
72) এইটা একটুট্রি কি হতে পারে । একটা array এর মধ্যে অনে কগুলা সংখ্যা থাকবে ।
ত োমার কাজ হচ্ছে সংখ্যা গুলা একটার পর একটা করে চে ক করা। এবং সংখ্যা
গুলা যদি পজি টিভ সংখ্যা হয়। অর্থাৎ শনূ্য বা শন্যেূন্যে র চাইতে বড় হয় তাহলে
সে গুলাকে ক োন একটা array এর মধ্যে রাখবে । আর যদি নে গে টিভ সংখ্যা হয়।
তাহলে লপুটা স্টপ করে দি বে । এবং লপু বন্ধ করার আগ পর্যন্ত যতগুলা পজি টিভ
সংখ্যা পাওয়া গে ছে । সে গুলা রি টার্ন করে দি বে ।
  
``` 
</details>


### Table
<div class="overflow-x-auto">
  <table class="table w-full">
    <!-- head -->
    <thead>
      <tr>
        <th></th>
        <th>Name</th>
        <th>Answer</th>
      </tr>
    </thead>
    <tbody>
      <!-- row 1 -->
      <tr>
        <th>1</th>
        <td>integer</td>
        <td>পূর্ণ সংখ্যা 1, 2, 40, 43 [parseint()]</td>
      </tr>
      <!-- row 2 -->
      <tr>
        <th>2</th>
        <td>float</td>
        <td> ভগ্নাংশ সংখ্যা decimal: 2.3, 43.23, 54.4 [parsefloat()]</td>
      </tr>
       <!-- row 3 -->
      <tr>
        <th>3</th>
        <td>==, ===</td>
        <td>== check the value, and === check the value and typeof</td>
      </tr>
      <!-- row 3.1 -->
      <tr>
        <th>3</th>
        <td>let price1 = price1 + 10</td>
        <td>let price1 +=10</td>
      </tr>
       <!-- row 4 -->
      <tr>
        <th>3</th>
        <td>let price1 = price1 - 10</td>
        <td>let price1 -=10</td>
      </tr>
       <!-- row 5 -->
      <tr>
        <th>3</th>
        <td>let price1 = price1 * 10</td>
        <td>let price1 *=10</td>
      </tr>
       <!-- row 6 -->
      <tr>
        <th>3</th>
        <td>let price1 = price1 / 10</td>
        <td>let price1 /=10</td>
      </tr>
       <!-- row 7 -->
      <tr>
        <th>3</th>
        <td>Data Type</td>
        <td>Premitive Data Type, Non Premitive Data Type</td>
      </tr>
      <!-- row 8 -->
      <tr>
        <th>8</th>
        <td>Premitive Data Type</td>
        <td>Number, String, Undefined, Null, Boolean</td>
      </tr>
       <!-- row 9 -->
      <tr>
        <th>9</th>
        <td>Non Premitive Data Type</td>
        <td>Object, Array, Function </td>
      </tr>
      <!-- row 10 -->
      <tr>
        <th>10</th>
        <td>Variable </td>
        <td> declare, naming convention, variable types, primitive, math operations. </td>
      </tr>
       <!-- row 11 -->
      <tr>
        <th>10</th>
        <td>Factorial </td>
        <td>A factorial is a function that multiplies a number by ev ery number below it till 1. </td>
      </tr>
       <!-- row 12 -->
      <tr>
        <th>10</th>
        <td>Conditionals </td>
        <td> comparison: >, <, >=, <=, ===, !==, if-else  </td>
      </tr>
       <!-- row 13 -->
      <tr>
        <th>14</th>
        <td> Array</td>
        <td> Declare, index, get values, set values, indexOf, push, pop </td>
      </tr>
       <!-- row 14 -->
      <tr>
        <th>14</th>
        <td> Loop</td>
        <td> for loop, while loop, break, continue </td>
      </tr>
       <!-- row 15 -->
      <tr>
        <th>15</th>
        <td> Function</td>
        <td> declare, parameters, return, call, use the returned value from a function </td>
      </tr>
       <!-- row 16 -->
      <tr>
        <th>16</th>
        <td> Objeect</td>
        <td> declare, properties, keys , values, get prop value, set value, loop object. </td>
      </tr>
       <!-- row 17 -->
      <tr>
        <th>17</th>
        <td> String</td>
        <td>String হচ্ছে imutable. এর মান বা value change করা যাই না.  </td>
      </tr>
       <!-- row 17 -->
      <tr>
        <th>17</th>
        <td> String</td>
        <td>  Apply Search includes, indexOf, startswith, endswith </td>
      </tr>
      
       <!-- row 17 -->
      <tr>
        <th>17</th>
        <td> destructing two way (valriable value swap)</td>
        <td> Array to Array /* [first, second] = [second, first] */, Object to Object </td>
      </tr>
       <!-- row 17 -->
      <tr>
        <th>17</th>
        <td> Array Check</td>
        <td> //check array using Array.isArray | console.log(Array.isArray(friends)) </td>
      </tr>
       <!-- row 17 -->
      <tr>
        <th>17</th>
        <td> Array Name Check (ase ki na) </td>
        <td> const friends = [13, 14, 11, 17, 21, 16, 15, 20]; | console.log(friends.includes(19))</td>
      </tr>
        <!-- row 18 -->
      <tr>
        <th>18</th>
        <td> preventDefault</td>
        <td> e.preventDefault();</td>
      </tr>
       <!-- row 17 -->
      <tr>
        <th>17</th>
        <td> Math </td>
        <td> Math, abs, pow, round, ceil, floor, and random number </td>
      </tr>
         <!-- row 19 -->
      <tr>
        <th>19</th>
        <td>Math.random() </td>
        <td>Math.random((Math.random()*1000)) // output 0.7895253939768327</td>
      </tr>
        <!-- row 20 -->
      <tr>
        <th>20</th>
        <td>Math.round() </td>
        <td> Math.round((Math.random()*10000)) // output 4492</td>
      </tr>
        <!-- row 21 -->
      <tr>
        <th>19</th>
        <td><a href="#" onclick="selectedItem(this)" class="btn btn-primary">SELECT</a> </td>
        <td> function er vitor this diya mane oi tai select kora </td>
      </tr>
        <!-- row 22 -->
      <tr>
        <th>22</th>
        <td>Date</td>
        <td>const today = new Date()  </td>
      </tr>
       <!-- row 23 -->
      <tr>
        <th>23</th>
        <td> </td>
        <td> </td>
      </tr>
       <!-- row 24 -->
      <tr>
        <th>24</th>
        <td> </td>
        <td> </td>
      </tr> <!-- row 25 -->
      <tr>
        <th>22</th>
        <td> </td>
        <td> </td>
      </tr> <!-- row 25 -->
      <tr>
        <th>22</th>
        <td> </td>
        <td> </td>
      </tr> <!-- row 22 -->
      <tr>
        <th>22</th>
        <td> </td>
        <td> </td>
      </tr> <!-- row 22 -->
      <tr>
        <th>22</th>
        <td> </td>
        <td> </td>
      </tr>

    </tbody>
  </table>
</div>


### Output

```js

বেসিক জাভাস্ক্রিপ্ট (ভেরিয়েবল, এরে, কন্ডিশন, লুপ) এর চেকলিস্ট। 
ভালো করে মনোযোগ দিয়ে একটার পর একটা চেকলিস্ট ধরে ধরে চেক করবে। একটাও বাদ দিবে। বাদ দিলেই তোমার আব্বার কাছে বিচার দিবো। 
১. জাভাস্ক্রিপ্ট কি জিনিস এইটা কি জানো?
২. জাভাস্ক্রিপ্ট কিভাবে কাজ করে সেটা কি জানো?
৩. ভেরিয়েবল কি জিনিস?
৪. ভেরিয়েবল কিভাবে ডিক্লেয়ার করে 
৫. ভেরিয়েবল এর মান কিভাবে চেইঞ্জ করে বা আপডেট করে। 
৬. কি কি ধরণের ভেরিয়েবল হয়। সেগুলা কি কি (হিন্টস: Numeric, String, Boolean)
৭. জাভাস্ক্রিপ এ primitive and non primitive data types কি কি ? উদাহরণ হিসেবে বলো। 
৮. ভেরিয়েবল এর নাম কিভাবে কিভাবে ডিক্লেয়ার করতে হয়। কোন কোন জিনিস নাম এ লেখা যাবে না। অর্থাৎ Variable এর naming convention সম্পর্কে বলো। 
৯. দুইটা ভেরিয়েবল এর মধ্যে =, -, *, /, % কিভাবে করে? 
১০. শর্টহ্যান্ড গুলো জানতে হবে। বিশেষ করে +=, -=, *=, /= জানতে হবে। 
১১.. ++ এবং -- এর কাজ কি ? এইটা কি জানো। 
১২ parseInt, parseFloat, toFixed এইগুলা কি করে? 
--------------
১৩. Array কি জিনিস। এইটা কিভাবে কাজ করে? কিভাবে Array ডিক্লেয়ার করতে হয় 
১৪. array এর মধ্যে কয়টা উপাদান (element) আছে সেটা কিভাবে বের করে 
১৫. array এর উপাদান গুলা এর পজিশন ( index) কিভাবে কাজ করে। কত দিয়ে শুরু হয়। এবং মান কিভাবে চেইঞ্জ হয়। 
১৬. কোন একটা উপাদানের index এর মান  -১ বলতে কি বুঝায় 
১৭. কিভাবে index দিয়ে কোন একটা array এর মধ্যে উপাদান এর মান খুঁজে বের করতে পারো 
১৮. কিভাবে কোন একটা index পজিশন এ array এর উপাদান এর মান চেইঞ্জ করতে পারবে 
১৯. একটা Array এর মধ্যে কোন একটা উপাদান এর মান তোমাকে দেয়া আছে এখন সেটার index তুমি কিভাবে খুঁজে বের করতে পারো?
২০. ধরো, কোন একটা ইনডেক্স দিয়ে উপাদান খুঁজতে গেছো। কিন্তু সেটার মান না দিয়ে তোমাকে undefined দেখাচ্ছে। সেটা দেখে তুমি কি বুঝবে? (একটু গুগলে সার্চ দাও। আমরা কোর্স এ এইটা আলোচনা করিনি। তারপরেও চেষ্টা করে দেখো)
২১. কোন একটা Array এর মধ্যে লাস্ট উপাদান হিসেবে কোন উপাদান হিসেবে যোগ করতে চাইলে কিভাৱে যোগ করবে। আবার Array থেকে শেষের উপাদান টা বের করে দিতে চাইলে কিভাবে বের করে দিবে
২২. কোন একটা Array এর মধ্যে প্রথম উপাদান হিসেবে কোন উপাদান হিসেবে যোগ করতে চাইলে কিভাৱে যোগ করবে। আবার Array থেকে প্রথম উপাদান টা বের করে দিতে চাইলে কিভাবে বের করে দিবে
২৩. তুলনা কিভাবে করতে হয়। এইগুলার মানে কি:  >, <, ==, !=, <=, >=, ===, !==, &&, ।। 
২৪. তোমার কাছে:  ৮০০০০ টাকার বেশি হলে তুমি mac কিনবে, ৬০ টাকার বেশি হলে gaming ল্যাপটপ কিনবে, ৪০ হাজার টাকার বেশি হলে lenovo yoga কম্পিউটার কিনবে , ২০ হাজার টাকার বেশি হলে পুরান ল্যাপটপ কিনবে। না হয় তুমি মোবাইল দিয়ে কাজ চালাবে। 
---------------------
২৫. আসকে আমার মন ভালো নেই এই কথা ৩৯ বার আউটপুট  হিসেবে দেখাও। 
২৬. while লুপ কিভাবে কাজ করে 
২৭. for লুপ কিভাবে কাজ করে 
২৮. while লুপ এর মধ্যে লুপ ভেরিয়েবল চেইঞ্জ না করলে কি সমস্যা হয়। 
২৯. একটা কোড লিখে ৫৮ থেকে ৯৮ পর্যন্ত যত সংখ্যা আছে সেগুলাকে দেখাও 
৩০.একটা কোড লিখে ৪১২ থেকে ৪৫৬ পর্যন্ত যত জোর সংখ্যা আছে সেগুলাকে দেখাও  
৩১. একটা কোড লিখে ৫৮১ থেকে ৬২৩ পর্যন্ত যত বিজোড় সংখ্যা আছে সেগুলাকে দেখাও 
৩২.while আর for loop এর মধ্যে পার্থক্য কি 
৩৩ তুমি এতদিন যা যা জিনিস শিখছো সেগুলার নাম দিয়ে একটা array বানাও। তারপর একটা for লুপ দিয়ে সেই array এর সব উপাদান কে আউটপুট হিসেবে দেখাও। 
৩৪. তুমি এতদিন পর্যন্ত যে যে মডেলের মোবাইল ফোন ইউজ করেছো সেগুলার নাম দিয়ে একটা array বানাও। তারপর একটা while লুপ দিয়ে সেই array এর উপাদান গুলা একটা একটা করে আউটপুট হিসেবে দেখাও 
৩৫. একটা ফর লুপ চালাও। ৩০ থেকে ৮৬ পর্যন্ত। আর এই লুপ ৪৪ এ গেলে ব্রেক করবে। সেই জিনিস কোড করে দেখাও 
৩৬. তোমার যত বই আছে সেগুলার দাম নিয়ে একটা array লিখে ফেলো। যে বই গুলোর দাম ২০০ টাকার উপরে সেগুলাকে স্কিপ করবে। অর্থাৎ সেগুলাকে আউটপুট হিসেবে দেখাবে না। বাকিদের কে আউটপুট হিসেবে দেখাবে। দেখো করতে পারো কিনা। 
------
উপরের ৩৬ এর মধ্যে যদি তুমি ৩০-৩৬ টা করে ফেলতে পারো তাহলে তুমি ভালোই অবস্থানে আছো। এইটা চালাতে থাকো। এখনো কিছু হয়ে যায়নি। তাই ওভার কনফিডেন্ট হওয়ার কিছু নাই এখনো তো বলতে গেলে তেমন কিছুই শুরু হয়নি। । জাস্ট চালাতে থাকো। 
.
যদি তুমি ২০-২৯ টা করে ফেলতে পারো তাহলে তুমি মোটামুটি চলে টাইপের অবস্থানে আছো। হালকা আরেকটু সিরিয়াস হলে বা সামনে করতে করতে লাইনে চলে আসবে। তোমার দ্বারা পসিবল। তবে এইটা ধরে রাখতে হবে। এবং সম্ভব হলে আরেকটু ভালো চেষ্টা করতে হবে। 
.
যদি তুমি ১০-১৯ টা করে ফেলতে পারো তাহলে তুমি টাইট সিচুয়েশন এ আছো। এফোর্ট ভালো দিতে হবে। চেষ্টার পরিমান বাড়াতে হবে। বুঝে নেয়ার চেষ্টা করতে হবে। মডিউল দেখার সাথে সাথে মনোযোগ বাড়াতে হবে। মডিউল বুঝতে না পারলে আমাদের হেল্প নিতে হবে। তাহলে লাইনে নিয়ে আসতে পারবে। একটু বেশি হার্ডওয়ার্ক করলে। 
.
আর যদি ০-৯ টা পারো। তাহলে সত্যি কথা হচ্ছে-- তোমার অবস্থা ভালো না। এইটাই বাস্তবতা। এবং এই কন্ডিশন চলতে থাকলে তোমাকে দিয়ে বেশি কিছু আশা করা যাবে না। এই অবস্থা থেকে উতরাতে হলে অনেক অনেক বেশি সময় দিতে হবে। অনেক অনেক অনেক বেশি এফোর্ট দিতে হবে।  এইটার পিছনে অনেক বেশি লেগে থাকতে হবে।

অনেকগুলো যদি বাটন থাকে এবং সেই বাটনের উপর বেইজ করে যদি কিছু ডিসপ্লে করতে হয় তাহলে নিচের কোন এপ্রোচ এ আগানো ওয়াইজ হবে?
১। প্রতিটা বাটনের জন্য আলাদা ইভেন্ট হ্যান্ডেলার অ্যাড করা এবং প্রতিটি ফাংশন থেকে ডিসপ্লে করা।
২। ইভেন্ট বাবল/ডেলিগেট করে একটি ইভেন্ট হ্যান্ডেলার অ্যাড করা এবং প্রাপ্ত ভ্যালুর উপর ইফ এলস কন্ডিশন (সুইচ কেইস বা স্ট্যাটিক অবজেক্ট ও ইউজ করা যেতে) ইউজ করে ডিসপ্লে করা।
৩। ইভেন্ট বাবল/ডেলিগেট করে একটি ইভেন্ট হ্যান্ডেলার অ্যাড করা এবং previousElementSibling /nextElementSibling.innerText এইভাবে খুজে খুজে তথ্য বের করে ডিসপ্লে করা।

```



## 🌐 Socials: Connect with Emon Hossain!

[![Facebook Badge](https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white)](https://fb.com/emonhossain6) [![Linkedin Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/emon007iu/) [![Twitter Badge](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/@emon_hossain7) [![Mail Badge](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:emon.hossain.wd@gmail.com)

<h4>❤️🤔 You can follow my Github and other social accounts 🤔❤️</h4>
<h2>❤️ Thank you very much! ❤️</h2>
