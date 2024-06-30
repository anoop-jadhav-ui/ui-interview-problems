[Home](../../README.md)

# Closure

### Problem 1

```js
    let x = 100;

    function abc() {
        return x + 10;
    }

    function overload(sub) {
        let x = 30;
        return sub;
    }

    console.log(
        overload(abc)()
    )
```
