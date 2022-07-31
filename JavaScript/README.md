# JavaScript Using Method And Example

### what is javaScript?
- JavaScript is high level, interpreted programming language used to make web pages more interactive. JavaScript is a dynamic programming language that's used for web development, web applications, game development, and lots more. JavaScript language is used both on the client-side and server-side allowing you to make web pages interactive.
### Why use JavaScript?
- Where HTML and CSS are languages that give structure and style to web pages, JavaScript gives web pages interactive elements that engage a user.


List of JavaScript:

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
- [LocalStorageAndSessionStorage](#LocalStorageAndSessionStorage)
- [useUpdatePassword](#useupdatepassword)
- [useUpdateProfile](#useupdateprofile)
- [useSendPasswordResetEmail](#usesendpasswordresetemail)
- [useSendEmailVerification](#usesendemailverification)


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
        <td>Brice Swyre</td>
        <td>Tax Accountant</td>
      </tr>
    </tbody>
  </table>
</div>



## 🌐 Socials: Connect with Emon Hossain!

[![Facebook Badge](https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white)](https://fb.com/emonhossain6) [![Linkedin Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/emon007iu/) [![Twitter Badge](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/@emon_hossain7) [![Mail Badge](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:emon.hossain.wd@gmail.com)

<h4>❤️🤔 You can follow my Github and other social accounts 🤔❤️</h4>
<h2>❤️ Thank you very much! ❤️</h2>
