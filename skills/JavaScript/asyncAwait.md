[Home](../../README.md)

# Aync await

```js
function getTweet() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve("hi promise")
    }, 1000)
  })
}

async function getData() {
  console.log("hi async")
  const data = await getTweet();
  console.log(data);
}

console.log("hi global");
getData();

```