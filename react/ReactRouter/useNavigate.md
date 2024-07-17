# useNavigate

---

`useNavigate` - возвращает функцию, которая может осуществлять навигацию.

```javascript
const navigate = useNavigate();
```

## Сигнатуры navigate

Передайте в значение `to` (такого же типа, как и to в [<Link>](./Link.md)) с необязательным вторым аргументом `options` (аналогично пропсам, которые можно передать в [<Link>](./Link.md)).
Передайте дельту, которую хотите переместить в стеке истории. Например, `navigate(-1)` эквивалентно нажатию кнопки **назад**.

## Свойства

- **replace (boolean)**: Если true, заменяет текущий вход в истории, а не добавляет новый.
- **state (any)**: Объект состояния, который будет доступен в новом маршруте.
- **preventScrollReset (boolean)**: При использовании компонента <ScrollRestoration> можно отключить сброс прокрутки в начало страницы.
- **relative (string)**: По умолчанию навигация относительна к иерархии маршрутов (relative: "route"), но можно использовать relative: "path" для относительной маршрутизации пути.
- **unstable_flushSync (boolean)**: Оборачивает начальное обновление состояния для этой навигации в вызов ReactDOM.flushSync.
- **unstable_viewTransition (boolean)**: Включает переход вида для этой навигации, оборачивая окончательное обновление состояния в document.startViewTransition().

```javascript
navigate("/profile", {
  state: { fromHome: true },
  replace: true,
  preventScrollReset: true,
  relative: "path",
  unstable_flushSync: true,
  unstable_viewTransition: true,
});
```
