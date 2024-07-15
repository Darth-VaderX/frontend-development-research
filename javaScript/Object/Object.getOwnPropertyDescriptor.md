# Метод Object.getOwnPropertyDescriptor
____

Object.getOwnPropertyDescriptor(obj, propertyName) - возвращает дескриптор свойства.

**obj** - oбъект, из которого мы получаем информацию<br>
**propertyName** - имя свойства

```
let descriptor = Object.getOwnPropertyDescriptor(Math, 'PI');

alert( JSON.stringify(descriptor, null, 2 ) );
/*
{
  "value": 3.141592653589793,
  "writable": false,
  "enumerable": false,
  "configurable": false
}
*/
```

## Object.getOwnPropertyDescriptors()

Object.getOwnPropertyDescriptors(obj) - возвращает все собственные дескрипторы свойств данного объекта.
____
- [Вопросы к собеседованию](../../README.md)
- [Object.keys](./Object.keys.md)
- [Object.values](./Object.values.md)
- [Object.is](./Object.is.md)
- [Флаги и дескрипторы свойства](./flagsAndDescriptors.md)
- [Object.defineProperty](./Object.defineProperty.md)