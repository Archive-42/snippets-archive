---
title: useIsomporphicEffect
tags: hooks,effect,beginner
firstSeen: 2021-09-29T05:00:00-04:00
lastUpdated: 2021-10-13T19:29:39+02:00
---

Eesolves to `useEffect()` on the server and `useLayoutEffect()` on the client.

- Use `typeof` to check if the `window` object is defined. If it is, return the `useLayoutEffect()`. Otherwise return `useEffect()`.

```jsx
const useIsomorphicEffect =
  typeof window !== 'undefined' ? React.useLayoutEffect : React.useEffect;
```

```jsx
const MyApp = () => {
  useIsomorphicEffect(() => {
    window.console.log('Hello');
  }, []);

  return null;
};

ReactDOM.render(<MyApp />, document.getElementById('root'));
```
