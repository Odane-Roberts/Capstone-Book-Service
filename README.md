
# Book-Service

The Book Service is a microservice designed to manage book transactions, . It provides a RESTful API for interacting with the book database.


## Run Application

###  Package Application with maven 

```bash
  mvn clean package
```

### Launch docker to build and run image 

```bash
  docker-compose up
```
## API Reference

Service will be runnnig on PORT 8090

GATEWAY PORT IS 8222
#### Get all books

```http
  GET /api/v1/books
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `bearer_token` | `string` | **Required**. Your API key from keycloak|

#### Get item

```http
  GET /api/v1/books/${id}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of item to fetch |
| `bearer_token`| `id`| **Required**. Your API key from keycloak|

#### TEST BOOK OBJECT
{

    "title": "The Great Wall",
    "author": "John Smith",
    "isbn": "978-1-765342-89-0",
    "publicationDate": "2022-06-15T00:00:00",
    "category": "NONFICTION",
    "quantity": 1,
    "status": "AVAILABLE"
}

#### ** Check Controller class for more endpoints


