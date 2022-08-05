# JavaScript Using Method And Example

### what is javaScript?
- JavaScript is high level, interpreted programming language used to make web pages more interactive. JavaScript is a dynamic programming language that's used for web development, web applications, game development, and lots more. JavaScript language is used both on the client-side and server-side allowing you to make web pages interactive.
### Why use JavaScript?
- Where HTML and CSS are languages that give structure and style to web pages, JavaScript gives web pages interactive elements that engage a user.


List of JavaScript:

- [function](#function)
- [whileLoop](#whileLoop)
- [forLoop](#forLoop)
- [TemplateString](#TemplateString)
- [ArrowFunction](#ArrowFunction)
- [SpreadOperator](#SpreadOperator)
- [Map](#Map)
- [forEach](#forEach)
- [filter](#filter)
- [find](#find)
- [JSON](#JSON)
- [fetch_Keys_Values](#fetch_Keys_Values)
- [Array](#Array)
- [Object](#Object)
- [Table](#Table)
- [switch](#switch)
- [Output](#Output)

### function
<details>
<summary>
  <h3>What is function?</h3>
</summary>
<br >
function 
</details>

```js
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
        <td>Factorial </td>
        <td>  </td>
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
        <td>Factorial </td>
        <td>  </td>
      </tr>
       <!-- row 13 -->
      <tr>
        <th>10</th>
        <td>Factorial </td>
        <td>  </td>
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

```



## 🌐 Socials: Connect with Emon Hossain!

[![Facebook Badge](https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white)](https://fb.com/emonhossain6) [![Linkedin Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/emon007iu/) [![Twitter Badge](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/@emon_hossain7) [![Mail Badge](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:emon.hossain.wd@gmail.com)

<h4>❤️🤔 You can follow my Github and other social accounts 🤔❤️</h4>
<h2>❤️ Thank you very much! ❤️</h2>
