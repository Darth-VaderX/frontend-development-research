# Последовательность скобок

---

```javascript
const bracketBalance = (bracketsString) => {
  if (bracketsString.length % 2 !== 0 || !bracketsString.length) {
    return false;
  }

  const brackets = {
    "{": "}",
    "[": "]",
    "(": ")",
  };

  const stack = [];

  for (let i = 0; i < bracketsString.length; i++) {
    if (brackets[bracketsString[i]]) {
      stack.push(bracketsString[i]);
    } else {
      if (brackets[stack.pop()] !== bracketsString[i]) {
        return false;
      }
    }
  }

  return stack.length === 0;
};
```

- [Алгоритмы](./algoritmics.md)
