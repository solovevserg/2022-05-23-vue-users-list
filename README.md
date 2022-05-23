# 2022-05-23-vue-users-list

В этом репозитории вы найдёте полезные ссылки на материалы и примеры с кодом по теме лекции о JS-фреймворках для СГН3 от 23.05.2022.

## Live Demo

Созданное приложение домтупно по адресу <https://vue-users-list.web.app/>.

## Полезные ссылки

- [Документация Vue](https://vuejs.org/guide/introduction.html)
- [Документация Firebase](https://firebase.google.com/docs?hl=en)
- [Таблица со сравнением фреймворков в википедии](https://en.wikipedia.org/wiki/Comparison_of_JavaScript-based_web_frameworks)

## Как запустить

```bash
git clone https://github.com/solovevserg/2022-05-23-vue-users-list
cd 2022-05-23-vue-users-list
npm ci
npm run serve
```

## Обращение к API

Приложение обращается к API по адресу <http://sdal.pw/api/cdc/users>. Пример ответа API:

```json
[
    {
        "id": 2,
        "name": "Ford Schroeder",
        "followers": [1, 17, 221],
        "age": 30,
        "verified": true
    }
]
```

⚠ При включенных блокировзиков рекламы и трекеров приложение может работать некорректно из-за CORS.

## Снимок экрана

![Снимок экрана vue-users-list](/docs/screenshot.png)
