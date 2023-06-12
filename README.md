# waytofuture
# BookStore WebAPI - README

This project is a BookStore WebAPI developed as Homework 1 for the Eczacibasi Bilisim & Patika Cooperation. It is built using .NET 6 and provides HTTP methods (GET, PUT, POST, DELETE) to interact with a book collection.

## Prerequisites
- [.NET 6 SDK](https://dotnet.microsoft.com/download/dotnet/6.0)

## Getting Started

1. Clone the repository:

```
git clone https://github.com/your-repo/bookstore-webapi.git
```

2. Navigate to the project directory:

```
cd bookstore-webapi
```

3. Build the project:

```
dotnet build
```

4. Run the project:

```
dotnet run
```

The API will be hosted locally on `http://localhost:5000` by default.

## Endpoints

### Get All Books

- **HTTP Method:** GET
- **Endpoint:** `/api/books`

This endpoint retrieves all the books in the bookstore.

### Get a Book

- **HTTP Method:** GET
- **Endpoint:** `/api/books/{id}`

This endpoint retrieves a specific book by its unique identifier (`id`).

### Add a Book

- **HTTP Method:** POST
- **Endpoint:** `/api/books`

This endpoint allows you to add a new book to the bookstore. You need to provide the book details in the request body in JSON format.

### Update a Book

- **HTTP Method:** PUT
- **Endpoint:** `/api/books/{id}`

This endpoint allows you to update an existing book by its unique identifier (`id`). You need to provide the updated book details in the request body in JSON format.

### Delete a Book

- **HTTP Method:** DELETE
- **Endpoint:** `/api/books/{id}`

This endpoint deletes a book from the bookstore based on its unique identifier (`id`).

## Request and Response Examples

### Get All Books - Request

```http
GET /api/books HTTP/1.1
Host: localhost:5000
```

### Get All Books - Response

```http
HTTP/1.1 200 OK
Content-Type: application/json

[
  {
    "id": 1,
    "title": "Lean Startup",
    "genreId": 1,
    "pageCount": 200,
    "publishDate": "2001-06-12T00:00:00"
  },
  {
    "id": 2,
    "title": "Herland",
    "genreId": 2,
    "pageCount": 250,
    "publishDate": "2010-05-23T00:00:00"
  },
  {
    "id": 3,
    "title": "Dune",
    "genreId": 2,
    "pageCount": 540,
    "publishDate": "2001-12-21T00:00:00"
  }
]
```

### Get a Book - Request

```http
GET /api/books/1 HTTP/1.1
Host: localhost:5000
```

### Get a Book - Response

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": 1,
  "title": "Lean Startup",
  "genreId": 1,
  "pageCount": 200,
  "publishDate": "2001-06-12T00:00:00"
}
```

### Add a Book - Request

```http
POST /api/books HTTP/1.1
Host: localhost:5000
Content-Type: application/json

{
  "id": 4,
  "title": "Lord Of The Rings",
  "genreId": 2,
  "pageCount": 1026,
  "publishDate": "1954-07-29T00:00:00"
}
```

### Add a Book - Response

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": 4,
  "title": "Lord Of The Rings",
  "genreId": 2,
  "pageCount": 1026,
  "publishDate": "1954-07-29T00:00:00"
}
```

### Update a Book - Request

```http
PUT /api
