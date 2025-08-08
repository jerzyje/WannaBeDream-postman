# Postman + newman + github pages + Simple store template

## The repository contains:

1. Local Store server and Postman collection for it
   --- Routes `/products`, `/orders` and `/users`. Below is a table of supported operations with `products` as example resource. The same operations are also supports for `orders/` and `users/`.

| VERB   | Route         | Input      | Output             |
| ------ | ------------- | ---------- | ------------------ |
| GET    | /products     | _None_     | **Array**          |
| GET    | /products/:id | **e.g 3**  | **Object**         |
| POST   | /products     | **object** | **Created object** |
| PUT    | /products     | **object** | **Updated object** |
| DELETE | /products/:id | **e.g 3**  | **Deleted object** |

--- Tests: Test status code for REST API (200,400 and so on), Test response time

### Updated in store.collection.json

Added:

- Request users with pagination and test that Response contains expected number of users
- Test sorting by price for product
- Test that Response matches JSON schema for users

2. A collection of tests for the open API - petstore.collection.json (the collection has not been modified and corresponds to the original)
3. A collection of tests for the open API - StarWars3.collection.json (new collection)
   (tests: Check max speed, Find film and setup in collectionVariables, Get Film Vehicle, Get Max Spacies, Check EyeColors)

## How to run collection tests with CI

Tests can be run via push to the repository and main branch, or manually via Actions in GitHub

Manual launch instructions via Actions in GitHub for those who have forked:

- Fork this repository (Click "Fork". It is usually in the upper right corner of the page, next to the "Star" and "Watch" buttons.)
- Go to the Actions → Run workflow tab, select a collection and click "Run workflow".
- After the test is complete, the report will be automatically deployed to GitHub Pages.
- Enable GitHub Pages in Settings → Pages by selecting Deploy from GitHub Actions.
- The report will open at: https://<your-nickname>.github.io/<your-repository>/

## Report

The report is available at the link:
The report is deployed to a separate branch gh-pages

## How to deploy a Store template locally

1. Download this repo.
2. Run `npm i` (install node.js dependencies)
3. Run `npm run tern-on-api`(to run testing server locally )
4. Upload `store.collection.json` in Postman app.

## Початкова колекція та завдання тут

<a href="https://svitla.com/blog/testing-rest-api-with-postman-and-curl"> Postman & Curl & REST article </a>
