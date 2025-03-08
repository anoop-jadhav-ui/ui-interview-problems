[Home](../../README.md)

# Array or String Problems

## Remove Duplicate

create a function that takes an input string and returns a string with duplicates removed.

```js
    const str = "this is a test test string";

    function removeDuplicates(str) {
        // write code here
    }

    console.log(
        removeDuplicates(str);
    )

    // output -
    // this is a test string
```

## Student Scholarship

Sort students based on following criteria -

1. Student with higher marks should be given priority
2. When same marks should give priority to students with better attendace
3. When same attendace should give priority to female students

```js
const students = [
  { name: "Aarav Sharma", marks: 85, gender: "Male", attendance: 90 },
  { name: "Isha Mehta", marks: 92, gender: "Female", attendance: 95 },
  { name: "Rohan Patel", marks: 85, gender: "Male", attendance: 88 },
  { name: "Priya Verma", marks: 85, gender: "Female", attendance: 88 },
  { name: "Aditya Mehra", marks: 85, gender: "Male", attendance: 90 },
  { name: "Kavya Gupta", marks: 80, gender: "Female", attendance: 89 },
];
```

## Search Subject

Create a function that returns the depth of searched subject

```js
const data = [
  {
    title: "Mathematics",
    children: [
      { title: "Algebra", children: [] },
      { title: "Geometry", children: [] },
      {
        title: "Calculus",
        children: [
          { title: "Differentiation", children: [] },
          { title: "Integration", children: [] },
        ],
      },
    ],
  },
  {
    title: "Science",
    children: [
      {
        title: "Physics",
        children: [
          { title: "Mechanics", children: [] },
          { title: "Optics", children: [] },
        ],
      },
      {
        title: "Chemistry",
        children: [
          { title: "Organic Chemistry", children: [] },
          { title: "Inorganic Chemistry", children: [] },
        ],
      },
    ],
  },
];
```
