# Node Ecosystem, TDD, CI/CD
## `Array.map()`
* `array.map()` function iterates over an array and runs a call back function for each item in the array .
* The callback receives the value and the index (optional)of the array element as a parameter.
* `.map()` will return a new array with the same length as the input array.

```

let array = [val1,val2,val3,val4 .. ];
  
let outputArray = array.map ((item,index=>{
    // callback function code block //
}))

```

## `Array.reduce()`
* `.reduce()` function iterates over an array and returns the last version of the **“accumulator”** .
* After the last iteration of the array, that **accumulator** value is returned to the caller. 
* initial value represents the value of the **accumulator** in the first iteration.
*  That return value gets fed into the next iteration so that you can continually operate on it and return the final value.
* `.reduce()` takes an array of objects and return back an object.

```

let array = [val1,val2,val3,val4 .. ];

let output = array.reduce( (accumulator,index) => {
    // callback function code block //
}, accumulatorValue);

```
## `superagent()` : with `.then()` code snippet 
```

const superagent = require ('superagent');
// then add the package 'npm install superagent'//

let url = `http://demo8340031.mockable.io/stuff`;

superagent.get(url)
  .then( data => {
    console.log(data.body);
  })
  .catch(err => console.error(err));

```
## `superagent()` : with `async / await` code snippet
```

async function fun1() {

    const superagent = require ('superagent');
    // then add the package 'npm install superagent'//

    let url = `http://demo8340031.mockable.io/stuff`;

    let data = await superagent.get(url);
    console.log(results.body);
}

fun1();

```
## promises 
when you use promises it's like saying : 
> the function should do it's work `.then()` bring me result data which i'll be handling .

* are a method of doing asynchronous programming with JS 
* a promise allows you to execute some code and “move on”, allowing for that code to take as long as it needs to run.
* Promises can be chained to run in sequence, or can run independently, and out of sequence.
* The `.then()` blocks. contain a callback function that will run if the previous operation is successful, and each callback receives as input the result of the previous successful operation, so you can go forward and do something else to it.
* Each `.then()` block returns another promise, meaning that you can chain multiple blocks onto each other, so multiple asynchronous operations can be made to run in order, one after another.
* The `.catch()` block at the end runs if any of the `.then()` blocks fail — in a similar way to synchronous `try...catch` blocks, an error object 

```
function fun1(params) {

  return new Promise( (resolve,reject) => {
    if( params === true ) {
      resolve('It worked!');
    }
    else {
      reject('It did Work ._. ');
    }
  })

}


fun1(params)

  .then( result => {
    console.log (result)
  })

  .catch( err => {
    console.error (err)
  });

```

## Are all callback functions considered to be Asynchronous? Why or Why Not?
No , not all of them , they're just functions and they're sometimes synchronous and sometimes not.
* its because that if a callback function is dependant on outside source of data like an api for example , it'll take time for the data to arrive and be available to be used by this callback function , in the other hand some callback functions have the data they need to get executed at hand for example : `.reduce ()` and `.map ()` mentioned earlier .
