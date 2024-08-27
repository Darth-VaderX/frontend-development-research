# Привязка контекста

---

Методы `call`, `apply` и `bind` позволяют указать в каком контексте будет вызвана функция.

## Call

функция будет сразу вызвана c новым контекстом

```
func.call(context, arg1, arg2, ...)
```

## Apply

Тоже самое, что и **Call**, но принимает массив аргументов

```
func.apply(context, [arg1, arg2])
```

## Bind

Метод возвращает новую функцию, внутри которой `this` будет равным переданному контексту.

```
функция.bind(контекст, параметр1, параметр2...);
```

---

---

- [Что такое this, как определить его значение?](./this.md)
- [Что такое контекст выполнения (Execution Context)?](./executionContext.md)
- [Что такое лексическое окружение (LexicalEnvironment)?](./LexicalEnvironment.md)
- [Что такое окружение переменных (Variable Environment)?](./variableEnvironment.md)
- [Вопросы по JavaScript](../javaScript.md)
- [Главное меню](../../README.md)
