[Home](../../README.md)

# Scope

### Problem 1

```js
    const fruitName = "🥭"

    function getName() {
        console.log(fruitName);
    }

    function fruit() {
        const fruitName = "apple";
        getName();
    }

    fruit()
```

### Problem 2

```js
    let pokemon = {
        name: "blastoise",
        type: "💧",
        getType() {
            setTimeout(() => {
                console.log(this.type);
            }, 0)
        }
    }

    pokemon.getType()
```


### Problem 3

```js
    let pokemon = {
        name: "Charizard",
        type: "🔥",
        getType: () => {
            console.log(this.type);
        }
    }


    pokemon.getType()
```

### Problem 4

```js
    function getPokemonType() {
        console.log(this.type)
    }

    let pokemon = {
        name: "Venusaur",
        type: "🌱",
        getType: getPokemonType
    }

    pokemon.getType()
```
