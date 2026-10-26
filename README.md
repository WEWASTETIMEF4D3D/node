# FakeSteam — каталог игр (Node.js + Express + MySQL)

## Запуск
1. Установите Node.js и MySQL.
2. Создайте БД и таблицы с тестовыми данными:
   `mysql -u root -p < schema.sql`
3. Скопируйте `.env.example` в `.env` и впишите свой пароль MySQL и JWT_SECRET.
4. `npm install`
5. `npm run dev` (nodemon) или `npm start`
6. Откройте http://localhost:3000

## Страницы
`/` главная (слайдер), `/catalog.html` каталог (CRUD), `/about.html` о проекте (форма обратной связи), `/account.html` личный кабинет (вход, регистрация, избранное).

## API
| Метод | Маршрут | Описание |
|---|---|---|
| GET | /api/games?q=&genre=&sort= | список, поиск, фильтр, сортировка |
| GET | /api/games/:id | одна игра |
| POST | /api/games | добавить (нужен вход) |
| PUT | /api/games/:id | изменить (нужен вход) |
| DELETE | /api/games/:id | удалить (нужен вход) |
| GET | /api/genres | жанры |
| POST | /api/auth/register, /api/auth/login | регистрация и вход |
| GET/POST/DELETE | /api/favorites[/:gameId] | избранное |
| POST | /api/feedback | обратная связь |
