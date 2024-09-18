# Variable Environment (окружение переменных)

---

**Окружение переменных** (Variable Environment) — это лексическое окружение, запись окружения которого хранит привязки, созданные посредством команд объявления переменных в текущем контексте выполнения.

В ES6 существует одно различие между компонентами [LexicalEnvironment](./LexicalEnvironment.md) и VariableEnvironment. Оно заключается в том, что первое используется для хранения объявлений функций и переменных, объявленных с помощью ключевых слов `let` и `const`, а второе — только для хранения привязок переменных, объявленных с использованием ключевого слова `var`.

```
let a = 20;
const b = 30;
var c;
function multiply(e, f) {
 var g = 20;
 return e * f * g;
}
c = multiply(20, 30);

GlobalExecutionContext = {
  ThisBinding: <Global Object>,
  LexicalEnvironment: {
    EnvironmentRecord: {
      Type: "Object",
      // Данные о привязках для идентификаторов
      a: < uninitialized >,
      b: < uninitialized >,
      multiply: < func >
    }
    outer: <null>
  },
  VariableEnvironment: {
    EnvironmentRecord: {
      Type: "Object",
      // Данные о привязках для идентификаторов
      c: undefined,
    }
    outer: <null>
  }
}
FunctionExectionContext = {

  ThisBinding: <Global Object>,
  LexicalEnvironment: {
    EnvironmentRecord: {
      Type: "Declarative", // В таких записях хранятся локальные переменные и параметры, объявленные с помощью
                           // let const, var или параметров функции.
      Arguments: {0: 20, 1: 30, length: 2},  // Данные о привязках для идентификаторов функции
    },
    outer: <GlobalLexicalEnvironment>
  },
VariableEnvironment: {
    EnvironmentRecord: {
      Type: "Declarative",
      // Данные о привязках для идентификаторов
      g: undefined
    },
    outer: <GlobalLexicalEnvironment>
  }
}
```

---

- [Вопросы по JavaScript](../javaScript.md)
