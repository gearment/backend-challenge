# Backend Software Engineer Coding Challenge

## Overview
You are required to design and implement a simple RESTful API for a library management system. This system should allow users to perform the following actions:

1. Add new books.
2. View details of a specific book.
3. List all books.
4. Update book information.
5. Delete a book.

## Requirements

### 1. Add New Books

Endpoint: POST /books

Request Body: 

```json
{
    "title": "string",
    "author": "string",
    "published_date": "YYYY-MM-DD",
    "isbn": "string",
    "number_of_pages": "integer",
    "cover_image": "string (URL)",
    "language": "string"
}
```

Response:
- 201 Created: Book successfully added.
- 400 Bad Request: Invalid input data.

### 2. View Details of a Specific Book

Endpoint: GET /books/{id}

Response:

```json
{
    "id": "integer",
    "title": "string",
    "author": "string",
    "published_date": "YYYY-MM-DD",
    "isbn": "string",
    "number_of_pages": "integer",
    "cover_image": "string (URL)",
    "language": "string"
}
```

- 200 OK: Book details.
- 404 Not Found: Book not found.

### 3. List All Books

Endpoint: GET /books

Response:

```json
[
    {
        "id": "integer",
        "title": "string",
        "author": "string",
        "published_date": "YYYY-MM-DD",
        "isbn": "string",
        "number_of_pages": "integer",
        "cover_image": "string (URL)",
        "language": "string"
    },
    ...
]
```

- 200 OK: List of books.

### 4. Update Book Information

Endpoint: PUT /books/{id}

Request Body:

```json
{
    "title": "string",
    "author": "string",
    "published_date": "YYYY-MM-DD",
    "isbn": "string",
    "number_of_pages": "integer",
    "cover_image": "string (URL)",
    "language": "string"
}
```

Response:
- 200 OK: Book information updated.
- 400 Bad Request: Invalid input data.
- 404 Not Found: Book not found.

### 5. Delete a Book

Endpoint: DELETE /books/{id}

Response:
- 204 No Content: Book successfully deleted.
- 404 Not Found: Book not found.

## Additional Requirements
- Use any backend framework or language you are comfortable with.
- Use a relational database (e.g., MySQL, PostgreSQL) for storing book data.
- Ensure proper error handling and validation.
- Write unit tests for your API endpoints.
- Include a README file with instructions on how to set up and run your application, including how to run the tests.

## Evaluation Criteria
- **Correctness**: The API should work as specified and handle edge cases appropriately.
- **Code Quality**: Your code should be clean, well-organized, and follow best practices.
- **Documentation**: Clear documentation on setup, usage, and how to run tests.
- **Testing**: Adequate test coverage to ensure the reliability of the code.
- **Performance**: The API should be performant and handle a reasonable number of requests efficiently.

## Submission
Please submit your solution as a zip file or a link to a Git repository containing the code and necessary documentation. Ensure the repository is private if you prefer, and provide access to the evaluators.
