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

- [Вопросы по Typescript](./typeScript.md)
