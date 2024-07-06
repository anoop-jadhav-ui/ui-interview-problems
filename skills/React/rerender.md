[Home](../../README.md)

# React rerender

```jsx
import { useState } from "react";

const Child = () => {
  console.log("child");
  return <div>Child</div>;
};

function Parent() {
  console.log("parent");
  const [count, setCount] = useState(0);

  const incrementCount = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <button onClick={incrementCount}>Count {count}</button>
      <Child />
    </div>
  );
}

export default Parent;
```