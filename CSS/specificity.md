# Что такое специфичность (вес селекторов) в CSS?

---

**Специфичность** — это алгоритм, благодаря которому браузер определяет, какие именно стили из всего набора применить к элементу. В вычислениях участвуют CSS-селекторы. Если одному и тому же элементу подходит сразу несколько CSS-правил с разными селекторами, то браузер применяет те стили, вес селектора которых больше. Правило каскада «кто ниже, тот и выигрывает» при этом может нарушаться.

1. Псевдоклассы `:is()`, `:has()` и `:not()` принимают вес наиболее специфичного селектора внутри скобок.
2. Комбинаторы `+`, `>`, `~`, универсальный селектор `*` и псевдокласс `:where()` веса не имеют.

## Система расчёта (0.0.0.0)

- Селектор по тегу увеличивают четвертую цифру - `0.0.0.1`
- Селекторы по классу, по атрибуту или псевдокласс увеличивают третью цифру - `0.0.1.0`
- Селекторы по идентификатору увеличивают вторую цифру - `0.1.0.0`
- Вшитые стили в атрибут **style** увиличивают первую цифру - `1.0.0.0`

Есть еще дополнительные 4 цифры (всего получается уже 8), если использовать `!important`. Например:

```
#id !important > .class !important;
div !important > #id
```

Стили в теге `style` имеют наименьший приоритет

---

- [Что такое CSS?](./CSSis.md)
- [Что такое блочная модель?](./boxModel.md)
- [Что такое псевдоклассы?](./pseudoclass.md)
- [Что такое псевдоэлементы?](./pseudoelement.md)
- [Какая разница между rem и em?](./emVSrem.md)
- [Какие бывают виды позиционирования?Что такое z-index?](./emVSrem.md)
- [Какие есть комбинаторы в CSS?](./combinators.md)
- [Вопросы по CSS](./CSS.md)
- [Главное меню](../README.md)