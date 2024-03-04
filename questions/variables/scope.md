# Scope (Область видимости)
____

Область видимости определяет доступность переменных в программе. Эта концепция лежит в основе замыканий и разделяет переменные на глобальные и локальные.

## Глобальная область видимости

Переменные, объявленные вне функций или блоков кода, имеют глобальную область видимости. Глобальные переменные доступны во всем скрипте после их объявления. Если переменная объявлена с помощью `var` или без ключевого слова вовсе, она становится свойством глобального объекта.

## Локальная область видимости

Переменные, объявленные внутри функций или блоков кода, имеют локальную область видимости.

### Блочная область видимости

Блочная область видимости создается при объявлении блока кода, таких как условные операторы `if`, циклы `for`, блоки `{}` и т.п. Переменные, объявленные с использованием ключевых слов `let` или `const` внутри блока кода, имеют блочную область видимости. Они доступны только внутри того блока, в котором они были объявлены.

### Функциональная область видимости

Функциональная область видимости создается при объявлении функции. Переменные, объявленные с использованием ключевого слова `var` внутри функции, имеют функциональную область видимости. Это означает, что такие переменные доступны во всей функции, включая блоки кода внутри нее.

[Вопросы к собеседованию](../../README.md)<br>
[Разница между var, let, const](./difference.md)<br>