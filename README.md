# Postman-newman-ghActions tests

## Description

This project demonstrates a basic REST API for managing products, orders, and users. It includes integration tests using Postman and automated testing with GitHub Actions.

## Requirements

- Node.js
- npm
- Postman
- Newman

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/ArtemPerehonchuk/Postman-newman-ghActions.git
   cd Postman-newman-ghActions
   ```

2. Install dependencies:
    ```bash
    npm install
    ```
3. Start the local server:
    ```bash
    npm run tern-on-api
    ```

## API Routes
Routes `/products`, `/orders` and `/users`. Below is a table of supported operations with `products` as example resource. The same operations are also supports for `orders/` and `users/`.

| VERB     |Route          | Input      | Output             |
|----------|---------------|------------|--------------------|
| GET      | /products     | *None*     | **Array**          |
| GET      | /products/:id |  **e.g 3** | **Object**         |
| POST     | /products     | **object** | **Created object** |
| PUT      | /products     | **object** | **Updated object** |
| DELETE   | /products/:id | **e.g 3**  | **Deleted object** |


##  Testing with Postman:

1. Open Postman.
2. Import the store.collection.json collection.
3. Run integration tests.

## Running Tests Locally with Newman:

Newman is a command-line tool that allows you to run Postman collections. To run tests locally using Newman:

1. Install Newman locally:
    ```bash
    npm install newman --save-dev
    ````
2.  Run the Postman collection and viewing result:

- To run tests and generate report:
    ```bash
    npm run test:run
    ```
- Open report:

- Open on macOS via terminal:
    ```bash
    open output.html
    ````
- Open on Windows via Command Prompt:
    ```bash
    start output.html
    ```

## GitHub Actions Integration:

GitHub Actions will run the tests on every push and pull request to the main branch. You can view the results in the "Actions" tab of your GitHub repository.