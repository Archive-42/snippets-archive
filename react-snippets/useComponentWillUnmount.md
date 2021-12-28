---
title: useComponentWillUnmount
tags: hooks,effect,beginner
firstSeen: 2020-01-03T16:00:56+02:00
lastUpdated: 2021-10-13T19:29:39+02:00
---

Executes a callback immediately before a component is unmounted and destroyed.

- Use the `useEffect()` hook with an empty array as the second argument. Return the provided callback to be executed only once before cleanup.
- Behaves like the `componentWillUnmount()` lifecycle method of class components.

```jsx
const useComponentWillUnmount = onUnmountHandler => {
  React.useEffect(
    () => () => {
      onUnmountHandler();
    },
    []
  );
};
```

```jsx
const Unmounter = () => {
  useComponentWillUnmount(() => console.log('Component will unmount'));

  return <div>Check the console!</div>;
};

ReactDOM.render(<Unmounter />, document.getElementById('root'));
```
