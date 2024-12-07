[Home](../../README.md)

# Problem 1

Add appropriate types

```ts
function wrapInArray(value) {
  return [value];
}

// Example Usage:
const numberArray = wrapInArray(5);       // Expected type: number[]
const stringArray = wrapInArray("hello"); // Expected type: string[]
const booleanArray = wrapInArray(true);   // Expected type: boolean[]
const studentsArray = wrapInArray({name : 'Arvind'}); // Expected type: Student[]
```