# Прототипное наследование

---

## Proto

**proto** - есть у всех объектов. (функции это те же объекты) Обычно объекты наследуются от глобального объекта `Object` но исключение обекты созданные с помощью `Object.create(null)` (используется для хеш-таблиц).

```javascript
const obj = Object.create(null);

console.log(obj.__proto__); // undefined
console.log(Object.getPrototypeOf(obj)); // null

const obj1 = {};
const obj2 = {};

obj1.__proto__ === obj2.proto; // true, т.к. они наследуются от глобального объекта Object.
// Так же с числами(от Number), строками(String), массивами(Array)

// Функции expression/declaration/arrow/class - их _proto_ равны
```

**proto** ссылается на **prototype** класса/функции. Чтобы понять чему равен **proto** нужно знать с помощью какого конструктора класса был создан объект.

```javascript
const promise = new Promise(() => {}); // promise._proto_ === Promise.prototype

class Samurai {}
Samurai.__proto__ === Function.prototype; // т.к. под капотом создан с помощью new Function
```

## Prototype

**prototype** - есть у любого класса/функции. (у стрелочных функций нет)

- [Вопросы по JavaScript](../javaScript.md)
