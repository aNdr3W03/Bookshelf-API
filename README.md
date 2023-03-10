# Bookshelf API

Build a RESTful API with web services using JavaScript, Node.js, Node Package Manager, Hapi Framework, and perform RESTful API testing automatically using Postman.

## Deployment

You can see the Bookshelf API deployment at the following link,  
[bookshelf-api-andrewbj.vercel.app/books](https://bookshelf-api-andrewbj.vercel.app/books "Bookshelf API").

## Installation

1. Clone this Repository
	```bash
	git clone https://github.com/aNdr3W03/Bookshelf-API.git
	```

2. Navigate to the project directory
	```bash
	cd Bookshelf-API-main
	```

3. Install all dependencies
	```bash
	npm install
	```

4. Run the server
	```bash
	npm run start
	```

5. Open on localhost port 5000, [localhost:5000/books](http://localhost:5000/books).

6. Stop the server by `ctrl + c`.

## Dependency

- [Hapi](https://hapi.dev "Hapi Framework")
- [nanoid](https://www.npmjs.com/package/nanoid "Nano ID")
- [ESLint (Airbnb Style)](https://www.npmjs.com/package/eslint-config-airbnb "ESLint Airbnb Style")
- [nodemon](https://www.npmjs.com/package/nodemon "nodemon")

## Run ESLint

```bash
npx eslint .
```

## Postman API Testing

API testing is done using Postman. There are a total of 104 tests consisting of 74 mandatory tests and 30 optional tests, with `POST`, `GET`, `PUT`, and `DELETE` methods.

This is the results of the API testing with Postman.

![Bookshelf API Test.postman_test_run.png](https://raw.githubusercontent.com/aNdr3W03/Bookshelf-API/main/Postman/Bookshelf%20API%20Test.postman_test_run.png "Bookshelf API Postman Test Result")

If you want to see the results of the API testing with Postman in the form of a `.json` file, you can see them at the following [link](https://raw.githubusercontent.com/aNdr3W03/Bookshelf-API/main/Postman/Bookshelf%20API%20Test.postman_test_run.json "Bookshelf API Test.postman_test_run.json").

You can see the files used to perform the API testing using Postman at the following link, [collection](https://raw.githubusercontent.com/aNdr3W03/Bookshelf-API/main/Postman/Bookshelf%20API%20Test.postman_collection.json "Postman Bookshelf API Test Collection") and [environment](https://raw.githubusercontent.com/aNdr3W03/Bookshelf-API/main/Postman/Bookshelf%20API%20Test.postman_environment.json "Postman Bookshelf API Test Environment").

## Bookshelf API Description

### 1. Add Book

**Request:**
- Method: `POST`
- Endpoint: `/books`
- Body:
	```json
	{
	  "name": string,
	  "year": number,
	  "author": string,
	  "summary": string,
	  "publisher": string,
	  "pageCount": number,
	  "readPage": number,
	  "reading": boolean
	}
	```

**Response:**
```json
{
  "status": string,
  "message": string,
  "data": {
    "bookId": string
  }
}
```

### 2. Get All Books

**Request:**
- Method: `GET`
- Endpoint: `/books`

**Response:**
```json
{
  "status": string,
  "data": {
    "books": [
      {
        "id": string,
        "name": string,
        "publisher": string
      }
    ]
  }
}
```

### 3. Get Book Detail

**Request:**
- Method: `GET`
- Endpoint: `/books/{id}`

**Response:**
```json
{
  "status": string,
  "data": {
    "book": {
      "id": string,
      "name": string,
      "year": year,
      "author": string,
      "summary": string,
      "publisher": string,
      "pageCount": number,
      "readPage": number,
      "finished": boolean,
      "reading": boolean,
      "insertedAt": date,
      "updatedAt": date"
    }
  }
}
```

### 4. Update Book

**Request:**
- Method: `PUT`
- Endpoint: `/books/{id}`
- Body:
	```json
	{
	  "name": string,
	  "year": number,
	  "author": string,
	  "summary": string,
	  "publisher": string,
	  "pageCount": number,
	  "readPage": number,
	  "reading": boolean
	}
	```

**Response:**
```json
{
  "status": string,
  "message": string
}
```

### 5. Delete Book

**Request:**
- Method: `DELETE`
- Endpoint: `/books/{id}`

**Response:**
```json
{
  "status": string,
  "message": string
}
```
