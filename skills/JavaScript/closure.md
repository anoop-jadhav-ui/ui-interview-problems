[Home](../../README.md)

# Closure

### Problem 1


Is this a closure ?

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
