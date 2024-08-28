# Что делает оператор "assertion type"?

---

**Утверждение типа (type assertion)** в TypeScript — это способ явно указать компилятору TypeScript, что вы уверены в типе значения, даже если TypeScript по каким-то причинам не может сам это определить или предполагает другой тип.

```typescript
const someValue: any = "this is a string";
const strLength: number = (someValue as string).length;
```

## Когда использовать?

1. Работа с `any` или `unknown`
2. Изменение типа в специфических ситуациях
3. Избежание избыточных проверок типов

---

- [Что такое TypeScript? Какие его преимущества и недостатки?](./typeScriptIs.md)
- [Какие типы данных существуют в TypeScript?](./types.md)
- [Что такое interface и type? Какая между ними разница?](./typeInterface.md)
- [В чем разница между "tuple" (кортеж) и массивом в TypeScript?](./tupleArray.md)
- [Что такое generic?](./generic.md)
- [Какие вы знаете утилиты TypeScript?](./utils.md)
- [Что делает oператор типа "keyof"?](./keyofType.md)
- [Что делает оператор "!"?](./nonNullAssertionOperator.md)
- [Что делает оператор "as const"?](./const.md)
- [Главное меню](../README.md)
