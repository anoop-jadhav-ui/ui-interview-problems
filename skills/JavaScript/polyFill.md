[Home](../../README.md)

# Create Polyfills

## bind & apply

Write a polyfill for bind or apply method

```js
const pokemon = {
  name: "pikachu",
  type: "electric",
};

const mouse = {
  getType: function () {
    return this.type;
  },
};
```

## flatmap

Write a polyfill for flat map which accepts following array

`[1, 2, [3, 4], 5]`

and returns

`[1, 2, 3, 4, 5]`

## repeat

Implement the following -

```js
"pokemon".repeat(3, ";"); //output - pokemon;pokemon;pokemon
```

## Promise.allSettled

Implement the following -

```js
const promise1 = Promise.resolve("Result 1 - Success");

const promise2 = new Promise((resolve) => {
  setTimeout(() => {
    resolve("Result 2 - Success");
  }, 1000);
});
const promise3 = new Promise((_, reject) => {
  reject("Result 3 - Failed");
});

// Implement this function
function customAllSettled() {}

Promise.customAllSettled = customAllSettled;

const customResult = await Promise.customAllSettled([
  promise1,
  promise2,
  promise3,
]);

console.log(customResult);
```

<details>
<summary>Solution</summary>

```js
function customAllSettled(promiseList) {
  return new Promise((resolve) => {
    const results = new Array(promiseList.length);
    let settledCount = 0;

    promiseList.forEach((p, i) => {
      p.then((value) => {
        results[i] = { status: "fulfilled", value };
      })
        .catch((reason) => {
          results[i] = { status: "rejected", reason };
        })
        .finally(() => {
          settledCount++;
          if (settledCount === promiseList.length) {
            resolve(results);
          }
        });
    });
  });
}
```

</details>
