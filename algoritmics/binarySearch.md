# Бинарный поиск

---

```javascript
const binarySearch = (sortArray, searchNumber) => {
  let left = 0;
  let right = sortArray.length - 1;

  while (left <= right) {
    const mid = Math.floor((left + right) / 2);

    if (searchNumber === sortArray[mid]) {
      return mid;
    } else if (searchNumber < sortArray[mid]) {
      right = mid - 1;
    } else if (searchNumber > sortArray[mid]) {
      left = mid + 1;
    }
  }

  return -1;
};

const sortedArr = [5, 12, 23, 34, 45, 56, 67, 78, 89, 100];

console.log(binarySearch(sortedArr, 12));
```

- [Алгоритмы](./algoritmics.md)
