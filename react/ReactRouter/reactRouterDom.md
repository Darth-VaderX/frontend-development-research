# React Router Dom

---

- [Начало](#start)
- [Установка](#install)
- [Роутер](#router)
- [Link](#link)
- [NavLink](#navlink)
- [loader](#loader)
- [Меню](#menu)

---

<h2 id='start'>Начало</h2>

Он позволяет создавать сложные одностраничные web-приложения, использующие навигацию без обновления всей страницы (то есть без дополнительных обращений к серверу), а также работать с историей браузера, изменять URL в браузере и поддерживать синхронизацию состояния приложения с URL.
Маршрутизация на стороне клиента обеспечивается созданием `Router` и ссылками/редиректами на страницы с помощью `<Link>` и `<Form>`

---

<h2 id='install'>Установка</h2>

```
npm i react-router-dom
```

- [React](../react.md)
- [React Router](./reactRouter.md)
- [Router](./router.md)

---

<h2 id='router'>Роутер</h2>

**Router** - компонент верхнего уровня, благодаря которому, работают все остальные компоненты и хуки.

- **BrowserRouter** используется для обычных веб-приложений с History API.
- **HashRouter** используется для приложений без серверной поддержки для маршрутизации.
- **MemoryRouter** используется для тестирования и сред без настоящей истории браузера.
- **StaticRouter** используется для серверного рендеринга.
- **Native Router** используется специально для React Native приложений. Он обеспечивает маршрутизацию и навигацию внутри мобильного приложения.

### Добавление Router в приложение

1. **Импорт самого роутера и провайдера**

```
import { createBrowserRouter, RouterProvider } from 'react-router-dom'
```

2. **Создание маршрутизатора с заданными маршрутами**

```
const router = createBrowserRouter([
	{
		path: '/',
		element: <div>Hello Router!</div>,
	},
]);
```

3. **Добавление провайдера**

```
import React from "react";
import ReactDOM from "react-dom/client";
import { createBrowserRouter, RouterProvider } from "react-router-dom";
import App from "./App.jsx";
import "./index.css";

const router = createBrowserRouter([
  {
    path: "/",
    element: <App />,
  },
]);

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <RouterProvider router={router} />
  </React.StrictMode>
);

```

---

## <h2 id='link'>Link</h2>

`<Link>` - позволяет обновлять URL в браузере без дополнительных запросов документа с сервера.

#### Link атрибуты

1. **to: string** - описывает местоположение, которое является пунктом назначения для некоторой навигации.
2. **reloadDocument?: boolean** - указывает, нужно ли перезагружать всю страницу при клике на ссылку. Если установлено в `true`, то кликая на ссылку, браузер перезагрузит всю страницу, а не выполнит клиентскую навигацию.
3. **replace?: boolean** - eсли установлено в `true`, то переход по ссылке заменит текущий URL, а не добавит новую запись в историю
4. **state?: any** - дополнительное состояние, которое можно передать вместе с переходом по ссылке. Это состояние можно затем получить в компоненте, на который происходит переход, используя хук `useLocation`
5. **preventScrollReset?: boolean** - указывает, нужно ли предотвращать прокрутку страницы к началу при переходе по ссылке. Если установлено в `true`, то после перехода по ссылке позиция прокрутки останется неизменной.
6. **relative?: 'path' | 'route'** - определяет, как будет интерпретироваться относительный путь в атрибуте to, основываясь либо на текущем маршруте, либо на текущем URL.
7. **unstable_viewTransition?: boolean** - экспериментальное свойство, которое указывает, следует ли использовать переходы между представлениями _(view transitions)_ при переходе по ссылке. На данный момент это свойство нестабильно и может измениться в будущих версиях.

---

<h2 id='navlink'>NavLink</h2>

`<NavLink>` - в атрибут `className` передаём функцию, в аргументы которой попадает объект с состояниями `isActive` (будет `true`, если пользователь находится на URL `<NavLink>`) и `isPanding` (будет `true`, если данные еще загружаются и ссылка собирается стать активной).

---

<h2 id='loader'>Loader</h2>

Для загрузки данных маршрута необходимо в свойство `loader` маршрутизатора подключить функцию запроса.
Достать данные в компоненте с помощью хука `useLoaderData`.

```
import Root, { loader as rootLoader } from "./routes/root";

const router = createBrowserRouter([
  {
    path: "/",
    element: <Root />,
    errorElement: <ErrorPage />,
    loader: rootLoader,
    children: [
      {
        path: "contacts/:contactId",
        element: <Contact />,
      },
    ],
  },
]);

=>

import {useLoaderData} from "react-router-dom";
import { getContacts } from "../contacts";

export default function Root() {
  const { contacts } = useLoaderData();
  return <></>
}
```

- [Главное меню](../../README.md)
- [React](../react.md)
- [JavaScript](../../javaScript/javaScript.md)

  <span id='menu'></span>
