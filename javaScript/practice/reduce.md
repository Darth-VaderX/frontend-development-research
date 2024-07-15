# Array.reduce
____

Задание: напишите полифилл для Array.reduce метода. Убедитесь, что ваша реализация поддерживает все функции собственного reduce метода, включая параметры аккумулятора и текущего значения, а также необязательное начальное значение.

```
Array.prototype.reduce = function (callback, initValue) {
  if (!Array.isArray(this)) return;
  if (typeof callback !== 'function') return;
  
  let acc = initValue ? initValue : this[0];
  let startIndex = initValue ? 0 : 1;

  for (let i = startIndex; i < this.length; i++) {
    if (i in this) {
      acc = callback(acc, this[i], i, this);
    }
  }

  return acc;
}
```