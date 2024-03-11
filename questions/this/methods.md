# Привязка контекста
____
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

- [Вопросы к собеседованию](../../README.md)
- [Ключевое слово this, как определить контекст](./methods.md)
- [Execution Context](./executionContext.md)
- [Lexical Environment](./LexicalEnvironment.md)
- [Variable Environment](./variableEnvironment.md)