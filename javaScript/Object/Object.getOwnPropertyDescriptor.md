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

- [Вопросы по JavaScript](../javaScript.md)
