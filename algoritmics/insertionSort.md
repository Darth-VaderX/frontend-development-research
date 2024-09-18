# Сортировка вставками

---

```
const insertionSort = (array) => {
  const arr = array.slice();

  for (let i = 0; i < arr.length; i++) {
    let j = i + 1;

    while (j && arr[j] < arr[j - 1]) {
      const clone = arr[j - 1];
      arr[j - 1] = arr[j];
      arr[j] = clone;
      j--;
    }
  }

  return arr;
};

const arr = [64, 34, 25, 12, 22, 11, 90];

console.log(insertionSort(arr));

```

- [Алгоритмы](./algoritmics.md)
