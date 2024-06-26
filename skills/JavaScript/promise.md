[Home](../../README.md)

# Promise

### Problem 1

Write the execution sequence of console logs - 

```js

function getData() {
  console.log("elephant");
  const p = new Promise((resolve) => {
    console.log("giraffe");
    resolve("lion");
    console.log("zebra");
  });
  console.log("koala");
  return p;
}
async function main() {
  console.log("cat");
  const result = await getData();
  console.log(result);
}
console.log("dog");
main().then(() => {
  console.log("moose");
});

```


### Problem 2

```js

// The promise, async/await style
const f1 = () => Promise.resolve("f1:done");
const f2 = (input) => Promise.resolve(input + " then f2:done");
const f3 = (input) => Promise.resolve(input + " then f3:done");






// Question 1.
// f1() ---res1--> f2(res1) ---res2--> f3(res2) ---res3-> solution

// Answer should be 
// f1:done then f2:done then f3:done








// Question 2.
// f1() ----res1---------------------> f3(res1) --------> solution
//      -x--err1--> f2(err1) --res2--> f3(res2) --------> solution


// Answer when f1 resolves
// f1:done then f3:done

// Answer when f1 rejects
// f1:done then f2:done then f3:done
```
