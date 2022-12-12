<h1>
  <br>
  <br>
  SMS Bomber by <a href='https://t.me/svpgcorporation'>SvPg Corporation</a>
  <br>
</h1>

<h2 align="center">SMS бомбер в браузере + API</h2>

**Важное сообщение**
> Начиная с версии 1.0.0 мы прекращаем поддержку Node.JS API. Пользователи используют лишь сайт для организации атак а не API, как задумывалось при релизе, но Вы сможете организовывать атаки в своих приложениях, используя HTTP запросы. Скачать более раннюю версию можно [тут](https://github.com/shketov/bomber-api/releases/)

## Как использовать?

> Для использования SMSBomber требуется установить [NodeJS](https://nodejs.org/en/)
  * Распакуйте архив
  * Установите зависимости - `npm install`
  * Введите `npm start` или `node index`
   > Изначально запускается на `3000` порту, используйте флаг `--port` чтобы запустить на желаемом порту. Например: `node index.js --port=3001`
   
   

| Метод      | Описание                                                                                             |
| ---------- | ---------------------------------------------------------------------------------------------------- |
| **attack** | Иницилизация атаки. Принимает два параметра, `number` - номер телефона; `loop` - количество повторов |
| **stop**   | Остановка атаки. `number` - номер телефона                                                           |
| **list**   | Не принимает параметров, возвращает список активных атак в формате JSON 

```js
/* Отправка HTTP запроса с помощью request
(https://www.npmjs.com/package/request) */

const request = require("request");

request.get(
  {
    url: 'http://localhost:3000/attack',
    body: { "number": 79864765066, "loops": 1 }
  },
  function (err, res, json) {
    /* your code */
  }
);
```

  ## TODO
  
   * Лог отправки сообщений
   * Список активных атак в WEB версии
   * ~~Остановка атак в WEB версии~~


### Присоединяйся к нам
[![Telegram](https://img.shields.io/badge/Telegram-blue?style=for-the-badge&logo=Telegram)](https://t.me/svpgcorporation)
