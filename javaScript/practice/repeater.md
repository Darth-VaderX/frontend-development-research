# String Repeater
____

Задание : создайте метод, расширяющий прототип String для повторения заданной строки указанное количество раз. Например, вызов 'hello world'.repeating(3)должен вернуть 'hello world hello world hello world'

```
String.prototype.repeater = function (count) {
  let result = '';

  count = isNaN(count) ? 1 : count;
  count = Math.abs(count)

  for (let i = 0; i < count; i++) {
    result += ` ${this}`;
  }

  return result;
}

```