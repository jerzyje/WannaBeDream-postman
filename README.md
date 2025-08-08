# Postman + newman + github pages + Simple store template

## The repository contains:

1. Local Store server and Postman collection for it.
2. petstore.collection.json - а collection of tests for the open API (the collection has not been modified and corresponds to the original)
3. StarWars3.collection.json - collection of tests for the open API
   (tests included into StarWars3.collection: Check max speed, Find film and setup in collectionVariables, Get Film Vehicle, Get Max Spacies, Check EyeColors)

### Updated in store.collection.json

Added to store.collection.json

- Request users with pagination and test that Response contains expected number of users
- Test sorting by price for product
- Test that Response matches JSON schema for users

## Report

The report is available at the link: https://nataliaperchishena.github.io/WannaBeDream-postman/.

The report is deployed to a separate branch gh-pages

## How to run automated testing and view the report in your fork

To be able to run tests and view the report in your GitHub Pages, do the following:

1. Fork the repository
   Click the "Fork" button in the upper right corner → select your GitHub profile or organization.

2. Enable Actions

- Go to Settings > Actions
- In the Actions permissions section, select "Allow all actions and reusable workflows"
- Click the Save button
- Go to the Actions tab (in the top menu)
  A message will appear: "Workflows aren’t being run on this forked repository..."
- Click the "I understand my workflows, go ahead and enable them" button

#### Possible issues.

Workflow is not visible in Actions.
GitHub does not automatically enable GitHub Actions in a fork until you make at least one push or make a change to the workflow file. This is standard security policy.
Solution: Make a minimal change to the wannaBe-first.yml file (Add an empty line or comment)

3. Enable GitHub Pages

- Go to your fork settings: https://github.com/YOUR-USERNAME/YOUR-FORK/settings/pages
- In the Build and deployment section:
  Source: select Deploy from a branch
  Branch: select gh-pages and / (root)
  Click Save

4. Run tests manually (optional)

- Go to the Actions tab in your fork
- Select the workflow "Run POSTMAN with Mock API and Publish Report"
- Click "Run workflow" (in the upper right corner)
- Select the desired collection (or leave the default value) → Run workflow

5. View the report
   Once the work is finished, the report will be available in your Pages at link: https://YOUR-USERNAME.github.io/YOUR-FORK/

### Note

The workflow starts automatically with every push to the main branch of your fork
You can also start it manually from the Actions tab

## How to deploy a Store template locally

1. Download this repo.
2. Run `npm i` (install node.js dependencies)
3. Run `npm run tern-on-api`(to run testing server locally )
4. Upload `store.collection.json` in Postman app.

### Details about local Store server

- Routes `/products`, `/orders` and `/users`. Below is a table of supported operations with `products` as example resource. The same operations are also supports for `orders/` and `users/`.

| VERB   | Route         | Input      | Output             |
| ------ | ------------- | ---------- | ------------------ |
| GET    | /products     | _None_     | **Array**          |
| GET    | /products/:id | **e.g 3**  | **Object**         |
| POST   | /products     | **object** | **Created object** |
| PUT    | /products     | **object** | **Updated object** |
| DELETE | /products/:id | **e.g 3**  | **Deleted object** |

- Tests: Test status code for REST API (200,400 and so on), Test response time

## Starter collection and challenge here

<a href="https://github.com/WannaBeDream/Postman-newman-ghActions"> /WannaBeDream/Postman-newman-ghActions</a>
