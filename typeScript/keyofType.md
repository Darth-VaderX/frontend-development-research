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

- [Вопросы по Typescript](./typeScript.md)
