# Loader

---

`Loader` — это функция, которая загружает данные до того, как компонент будет смонтирован. Он может использоваться для предварительной загрузки данных для страницы или компонента. Функцию необходимо инициализировать в свойство `loader` маршрутизатора и далее достать данные в компоненте с помощью хука `useLoaderData`.

По умолчанию функция `loader` принимает в себя объект с параметрами:

- **Params** - oбъект, содержащий параметры маршрута. Эти параметры извлекаются из динамических сегментов URL. Если маршрут определен как `/user/:userId`, и URL `/user/123` запрашивается, то params будет `{ userId: '123' }`.
- **Request** - oбъект запроса, содержащий информацию:
  - **URL:** Полный URL запроса.
  - **Headers:** Заголовки HTTP-запроса.
  - **Method:** HTTP-метод запроса (GET, POST, PUT, DELETE и т.д.).
  - **Body:** Тело запроса (обычно для POST и PUT запросов).
  - **Query Parameters:** Параметры запроса (например, ?search=value).
  - **Cookies:** Куки, отправленные вместе с запросом.
  - **Referrer:** URL-адрес страницы, с которой пришел запрос.
- **Signal** - oбъект, который можно использовать для отмены fetch-запроса, если пользователь покидает страницу или запрос больше не нужен. Можно передать `signal` в `fetch` для возможности отмены запроса.

```javascript
import { LoaderFunctionArgs } from "react-router-dom";

interface UserData {
  id: number;
  name: string;
  email: string;
}

export const fetchUserData = async ({
  params,
  request,
  signal,
}: LoaderFunctionArgs): Promise<UserData> => {
  const { userId } = params;

  try {
    const response = await fetch(`https://api.example.com/users/${userId}`, {
      signal,
    });

    if (!response.ok) {
      throw new Error("Failed to fetch user data");
    }

    const userData: UserData = await response.json();
    return userData;
  } catch (error) {
    throw new Error(`Error fetching user data: ${error.message}`);
  }
};
```

- [Главное меню](../../README.md)
- [React](../react.md)
- [Начало работы](./start.md)
- [Link](./Link.md)
- [NavLink](./NavLink.md)
