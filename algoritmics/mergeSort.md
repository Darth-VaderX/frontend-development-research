# Сортировка слиянием

---

```javascript
const mergeSort = (arr) => {
  if (arr.length <= 1) return arr;

  const mid = Math.floor(arr.length / 2);
  const left = arr.slice(0, mid);
  const right = arr.slice(mid);

  return merge(mergeSort(left), mergeSort(right));
};

function merge(left, right) {
  const sortArray = [];

  let i = 0;
  let j = 0;

  while (i < left.length && j < right.length) {
    sortArray.push(left[i] < right[j] ? left[i++] : right[j++]);
  }

  return sortArray.concat(left.slice(i), right.slice(j));
}
```
