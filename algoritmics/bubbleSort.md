# Пузырьковая сортировка

---

```javascript
const bubbleSort = (arr) => {
  const sortArr = arr.slice(0);

  for (let i = 0; i < sortArr.length - 1; i++) {
    for (let j = 0; j < sortArr.length - 1 - i; j++) {
      if (sortArr[j] > sortArr[j + 1]) {
        const clone = sortArr[j + 1];

        sortArr[j + 1] = sortArr[j];
        sortArr[j] = clone;
      }
    }
  }
  return sortArr;
};

const arr = [64, 34, 25, 12, 22, 11, 90];
console.log(bubbleSort(arr));
```

- [Алгоритмы](./algoritmics.md)
