---
title: camel
tags: string,regexp,intermediate
firstSeen: 2019-08-21T08:59:54+03:00
lastUpdated: 2020-11-02T19:27:07+02:00
---

Converts a string to camelcase.

- Use `re.sub()` to replace any `-` or `_` with a space, using the regexp `r"(_|-)+"`.
- Use `str.title()` to capitalize the first letter of each word and convert the rest to lowercase.
- Finally, use `str.replace()` to remove spaces between words.

```py
from re import sub

def camel(s):
  s = sub(r"(_|-)+", " ", s).title().replace(" ", "")
  return ''.join([s[0].lower(), s[1:]])
```

```py
camel('some_database_field_name') # 'someDatabaseFieldName'
camel('Some label that needs to be camelized')
# 'someLabelThatNeedsToBeCamelized'
camel('some-javascript-property') # 'someJavascriptProperty'
camel('some-mixed_string with spaces_underscores-and-hyphens')
# 'someMixedStringWithSpacesUnderscoresAndHyphens'
```
