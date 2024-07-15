# setTimeout
____

Задание: реализация setTimeout с использованием только цикла while и объекта Date.

```
function customSetTimeOut(callback, time) {
  const start = new Date();
  let end = new Date();

  while (end - start < time) {
    end = new Date();
  }

  callback();
}
```