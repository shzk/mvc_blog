# mvc_blog

## БД

| Таблицы | колонки | отношение |
| ------- | ------- | --------- |
| posts | id (ai), img, date, title, content, author_id, role | posts.author_id ( => users.id) |
| users | id (ai), name, email | users.id ( => posts.author_id => comments.author_id) |
| comments | id(ai), date, post_id, author_id, parent_id | comments.post_id ( => posts.id ), comments.author_id ( => users.id), comments.parent_id ( => comments.id) |


## Основной функционал
- Список постов/одиночная запись/ комментарии
- Регистрация/авторизация

## Админка
- Создание/редактирование/удаление поста - удаление только для автора
- Роли - Админ и автор, админ может управлять/редактировать/удалять авторов
- Написание/редактирование/удаление комментария/возможность ответа на конкретный комментарий

## Фронтенд
- Бутстрап 4, чтобы не использовать готовую верстку и для ускорения сборки
