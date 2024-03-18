# Object.is
____
**Object.is():**
1. Является статическим методом глобального объекта __Object__ и определяет, являются ли два значения одним и тем же.
```
Object.is(value1, value2);
```
2. Не эквивалентен оператору ```==```, т.к. применяет различные приведения к обеим сторонам (если они не одного типа) перед проверкой.

3. Также не эквивалентен оператору ===. Разница между ```Object.is()``` и оператором ```===``` заключается в обработке ```0``` и ```NaN```.

```
console.log( Object.is(+0, -0));    // false
console.log( +0 === -0 );           // true

console.log( Object.is(NaN, NaN) ); // true
console.log( NaN === NaN );         // false
```

- [Вопросы к собеседованию](../../README.md)
- [Object.keys](./Object.keys.md)
- [Object.values](./Object.values.md)
- [Object.defineProperty](./Object.defineProperty.md)
- [Object.getOwnPropertyDescriptor](./Object.getOwnPropertyDescriptor.md)
- [Флаги и дескрипторы свойства](./flagsAndDescriptors.md)