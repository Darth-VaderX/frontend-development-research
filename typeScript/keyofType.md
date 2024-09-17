# Оператор типа keyof

---

Оператор типа `keyof` в TypeScript используется для получения типа, представляющего ключи (имена свойств) указанного объекта или интерфейса. Он позволяет извлечь набор всех ключей объекта и использовать их для различных целей, таких как создание более безопасных и гибких типов.

```typescript
interface User {
  id: number;
  name: string;
  age: number;
}

type UserKeys = keyof User; // "id" | "name" | "age"

function getProperty<T, K extends keyof T>(obj: T, key: K): T[K] {
  return obj[key];
}

const user: User = { id: 1, name: "Alice", age: 30 };

const name = getProperty(user, "name"); // "Alice"
const age = getProperty(user, "age"); // 30
```

---

- [Что такое TypeScript? Какие его преимущества и недостатки?](./typeScriptIs.md)
- [Какие типы данных существуют в TypeScript?](./types.md)
- [Что такое interface и type? Какая между ними разница?](./typeInterface.md)
- [В чем разница между "tuple" (кортеж) и массивом в TypeScript?](./tupleArray.md)
- [Что такое generic?](./generic.md)
- [Какие вы знаете утилиты TypeScript?](./utils.md)
- [Что делает оператор "!"?](./nonNullAssertionOperator.md)
- [Что делает оператор "assertion type"?](./assertionType.md)
- [Что делает оператор "as const"?](./const.md)
- [Главное меню](../README.md)
