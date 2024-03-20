# Мемоизация
____
**Мемоизация** — сохранение результатов выполнения функций для предотвращения повторных вычислений. Это один из способов оптимизации, применяемый для увеличения скорости выполнения компьютерных программ. Функция мемоизации - это функция высшего порядка, в которой кеш хранится в замыкании.

```
// простая функция, прибавляющая 10 к переданному ей числу
const add = (n) => (n + 10);
add(9);
// аналогичная функция с мемоизацией
const memoizedAdd = () => {
  let cache = {};
  return (n) => {
    if (n in cache) {
      console.log('Fetching from cache');
      return cache[n];
    }
    else {
      console.log('Calculating result');
      let result = n + 10;
      cache[n] = result;
      return result;
    }
  }
}
// эту функцию возвратит memoizedAdd
const newAdd = memoizedAdd();
console.log(newAdd(9)); // вычислено
console.log(newAdd(9)); // взято из кэша
```

- [Вопросы к собеседованию](../../README.md)
- [Параметры функции](./arguments.md)
- [Динамическое количество параметров функции](./dynamicArguments.md)
- [Разница между Function Expression и Function Declaration](./difference.md)
- [Arrow Functions](./arrowFunction.md)
- [Каррирование](./currying.md)