# Kantox Assessment

This project contains a collection of HTTP requests to interact with a REST API. The collection is designed to test and validate various API endpoints.

## Requirements

- [Postman](https://www.postman.com/downloads/) or any tool compatible with Postman collections.
- A running API server at `http://localhost:3000`.

## Global Variables

The collection uses the following global variables:

- `baseUrl`: Base URL of the API. By default, it is set to `http://localhost:3000`.

## Endpoints

### Posts

1. **GET /posts**
   - **Description**: Retrieves all posts.
   - **Tests**:
     - Verifies the `Content-Type` header is `application/json`.
     - Checks the status code is `200`.
     - Ensures the response time is less than 200ms.
     - Validates that each post object contains the fields `id`, `title`, and `author`.

2. **GET /posts/{id}**
   - **Description**: Retrieves a post by its ID.
   - **Tests**:
     - Verifies the `Content-Type` header is `application/json`.
     - Checks the status code is `200`.
     - Ensures the response time is less than 200ms.
     - Validates the schema of the response body.

3. **POST /posts**
   - **Description**: Creates a new post.
   - **Tests**:
     - Verifies the `Content-Type` header is `application/json`.
     - Checks the status code is `201`.
     - Ensures the response time is less than 100ms.
     - Validates that the response body contains the fields `id`, `title`, and `author`.

4. **PUT /posts/{id}**
   - **Description**: Updates an existing post.
   - **Tests**:
     - Verifies the `Content-Type` header is `application/json`.
     - Checks the status code is `200`.
     - Ensures the response time is less than 300ms.
     - Validates the schema of the response body.

5. **DELETE /posts/{id}**
   - **Description**: Deletes a post by its ID.
   - **Tests**:
     - Verifies the `Content-Type` header is `application/json`.
     - Checks the status code is `200`.
     - Ensures the response time is less than 200ms.

### Comments

1. **GET /comments**
   - **Description**: Retrieves all comments.
   - **Tests**:
     - Verifies the `Content-Type` header is `application/json`.
     - Checks the status code is `200`.
     - Ensures the response time is less than 200ms.
     - Validates that the response body is an array.

2. **GET /comments/{id}**
   - **Description**: Retrieves a comment by its ID.
   - **Tests**:
     - Verifies the `Content-Type` header is `application/json`.
     - Checks the status code is `200`.
     - Ensures the response time is less than 100ms.
     - Validates that the response contains the fields `id`, `body`, and `postId`.

3. **POST /comments**
   - **Description**: Creates a new comment.
   - **Tests**:
     - Verifies the `Content-Type` header is `application/json`.
     - Checks the status code is `201`.
     - Ensures the response time is less than 200ms.
     - Validates that the response contains the fields `id`, `body`, and `postId`.

4. **PUT /comments/{id}**
   - **Description**: Updates an existing comment.
   - **Tests**:
     - Verifies the `Content-Type` header is `application/json`.
     - Checks the status code is `200`.
     - Ensures the response time is less than 300ms.
     - Validates that the response contains the fields `id`, `body`, and `postId`.

5. **DELETE /comments/{id}**
   - **Description**: Deletes a comment by its ID.
   - **Tests**:
     - Verifies the `Content-Type` header is `application/json`.
     - Checks the status code is `200`.
     - Ensures the response time is less than 300ms.

### Profile

1. **GET /profile**
   - **Description**: Retrieves the user's profile.
   - **Tests**:
     - Verifies the `Content-Type` header is `application/json`.
     - Checks the status code is `200`.
     - Ensures the response time is less than 200ms.
     - Validates that the response contains the field `name`.

## Usage

1. Import the `collection.json` file into Postman.
2. Configure the global variable `baseUrl` if necessary.
3. Execute the requests and verify the results.

## License

This project does not have a specific license.