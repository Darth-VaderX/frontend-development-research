# метод Object.defineProperty

---

Object.defineProperty(obj, propertyName, descriptor)

**obj, propertyName** - oбъект и его свойство, для которого нужно применить дескриптор<br>
**descriptor** - применяемый дескриптор

Если свойство существует, `defineProperty` обновит его флаги. В противном случае метод создаёт новое свойство с указанным значением и флагами, если какой-либо флаг не указан явно, ему присваивается значение `false`.

```
let user = {};

Object.defineProperty(user, "name", {
  value: "John"
});

let descriptor = Object.getOwnPropertyDescriptor(user, 'name');

alert( JSON.stringify(descriptor, null, 2 ) );
/*
{
  "value": "John",
  "writable": false,
  "enumerable": false,
  "configurable": false
}
 */
```

## Метод Object.defineProperties

Метод Object.defineProperties позволяет определять множество свойств сразу.

```
Object.defineProperties(user, {
  name: { value: "John", writable: false },
  surname: { value: "Smith", writable: false },
});
```

---

- [Вопросы по JavaScript](../javaScript.md)
