[Home](../../README.md)

# Generics

Add appropriate types

```ts
function wrapInArray(value) {
  return [value];
}

// Example Usage:
const numberArray = wrapInArray(5);        // Expected type: number[]
const stringArray = wrapInArray("hello");  // Expected type: string[]
const booleanArray = wrapInArray(true);    // Expected type: boolean[]
```