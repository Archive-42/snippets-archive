---
title: find_index
tags: list,intermediate
firstSeen: 2020-03-10T22:38:48+02:00
lastUpdated: 2020-11-02T19:27:53+02:00
---

Finds the index of the first element in the given list that satisfies the provided testing function.

- Use a list comprehension, `enumerate()` and `next()` to return the index of the first element in `lst` for which `fn` returns `True`.

```py
def find_index(lst, fn):
  return next(i for i, x in enumerate(lst) if fn(x))
```

```py
find_index([1, 2, 3, 4], lambda n: n % 2 == 1) # 0
```
