# Метод Object.getOwnPropertyDescriptor

---

## Object.getOwnPropertyDescriptors()

Object.getOwnPropertyDescriptors(obj) - возвращает все собственные дескрипторы свойств данного объекта.

---

Object.getOwnPropertyDescriptor(obj, propertyName) - возвращает дескриптор свойства.

**obj** - oбъект, из которого мы получаем информацию<br>
**propertyName** - имя свойства

```
let descriptor = Object.getOwnPropertyDescriptor(Math, 'PI');

alert( JSON.stringify(descriptor, null, 2 ) );

{
  "value": 3.141592653589793,
  "writable": false,
  "enumerable": false,
  "configurable": false
}

```

---

- [Что делает Object.is?](/Object.is.md)
- [Как получить ключи объекта?](./Object.keys.md)
- [Как получить свойства объекта?](./Object.values.md)
- [Что такое дескрипторы свойств?](./flagsAndDescriptors.md)
- [Как установить дескрипторы свойств?](./Object.defineProperty.md)
- [Вопросы по JavaScript](../javaScript.md)
- [Главное меню](../../README.md)
