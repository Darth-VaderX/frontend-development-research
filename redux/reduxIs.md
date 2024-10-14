# Что такое Redux?

---

**Redux** — библиотека управления состоянием для приложений, написанных на JavaScript. В Redux нельзя напрямую изменять состояние. Вместо этого ты должен отправить action — специальный объект, который описывает, что должно измениться.

- **Store** - объект, который содержит всё состояние приложения
- **Action** - объект с обязательным полем `type`, который определяет, какое именно действие нужно выполнить.
- **Reducers** - это чистые функции, которые принимают текущее состояние и экшен, а затем возвращают новое состояние.

- [Вопросы по Redux](redux.md)