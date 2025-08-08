# Postman + newman + github pages + Simple store template

## Репозиторій містить:

1. Локальний сервер Store та постман колекцію для нього
   --- Routes `/products`, `/orders` and `/users`. Below is a table of supported operations with `products` as example resource. The same operations are also supports for `orders/` and `users/`.

| VERB   | Route         | Input      | Output             |
| ------ | ------------- | ---------- | ------------------ |
| GET    | /products     | _None_     | **Array**          |
| GET    | /products/:id | **e.g 3**  | **Object**         |
| POST   | /products     | **object** | **Created object** |
| PUT    | /products     | **object** | **Updated object** |
| DELETE | /products/:id | **e.g 3**  | **Deleted object** |

--- Tests: Test status code for REST API (200,400 and so on) for , Test response time for

### Оновлено в store.collection.json

Додано:

- запит users with pagination і тест що Response contains expected number of users
- Test sorting by price for product
- Test that Response matches JSON schema for users

2. Колекцію тестів для відкритого АРІ - petstore.collection.json (колекція не модифікувалась)
3. Колекцію тестів для відкритого АРІ - StarWars3.collection.json (нова колекція)

-
-
-

## Як запустити тести колекцій на СI

Тести можна запустити через пуш на репозиторій і гілку main, або вручну через Actions

📌 Інструкція для тих, хто зробив форк:
Форкни цей репозиторій.

Перейди у вкладку Actions → Run workflow, вибери колекцію та натисни "Run workflow".

Після завершення тесту репорт буде автоматично задеплоєно на GitHub Pages.

Активуй GitHub Pages у Settings → Pages, обравши Deploy from GitHub Actions.

Репорт відкриється за адресою:
https://<твій-нік>.github.io/<твій-репозиторій>/

## Звіт

Звіт доступний за посиланням:

Звіт деплоїться на окрему гілку gh-pages

## Як розгорнути локально Store template

1. Download this repo.
2. Run `npm i` (install node.js dependencies)
3. Run `npm run tern-on-api`(to run testing server locally )
4. Upload `store.collection.json` in Postman app.

## Початкова колекція та завдання тут

<a href="https://svitla.com/blog/testing-rest-api-with-postman-and-curl"> Postman & Curl & REST article </a>
