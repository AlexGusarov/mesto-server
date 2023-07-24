# mesto-server
## Описание

Бекенд для сервиса Mesto - упрощенного аналога Instagram.  Позволяет создавать и хранить данные о пользователях и их фото.

Доступен по адресу:<br>


## Используемые технологии

Серверная часть написана на платформе **Node JS** с применением фреймворка **Express**. База данных — облачная **MongoDB**. Для валидации данных используется **Joi**. Для повышения безопасности и защиты от DDoS-атак подключены пакеты **helmet** и **express-rate-limit**. 

## API

Все данные передаются в формате JSON.<br>

Все роуты, кроме /signin и /signup, защищены авторизацией. 

| Метод  | Эндпойнт | Функция| Данные |
| :-     |   :-:    |   -   |  :-:  |
|**POST**   | /signin| вход пользователя | email, password  |
|**POST** | /signup   | регистрация |email, password|
|**GET** | /cards   | возвращает все фото пользователя  | |
|**POST** | /cards  | создает новое фото|  |
|**PUT** | /cards/:cardId/likes | ставит лайк на карточку | ID карточки |
|**DELETE** | /cards/:cardId | удаляет лайк | ID карточки |
|**GET** | /users/me | получить информацию о пользователе | - |
|**PATCH** | /users/me | обновить информацию о пользователе |  |
|**PATCH** | /users/me | обновить аватар  |  |
|**GET** | /users/:userId | получить пользователя по ID | ID |


