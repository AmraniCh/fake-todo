### List todos

GET http://localhost:8000/api/todos
Accept: application/json

### Filter todo by userId

GET http://localhost:8000/api/todos?userId=2
Accept: application/json

### Try finding todo that does not exists

GET http://localhost:8000/api/todos/2222
Accept: application/json

### Create todo

POST http://localhost:8000/api/todos
Content-Type: application/json

{
    "title": "Hello",
    "userId": 1,
    "status": 1
}

### Update todo

PUT http://localhost:8000/api/todos/1
Content-Type: application/json

{
    "title": "World",
    "body": "Such a wondrous world we live in!!!",
    "userId": 1
}

### Update some attributes of todo

PATCH http://localhost:8000/api/todos/1
Content-Type: application/json

{
    "title": "Earth"
}

### Mark todo as done

PATCH http://localhost:8000/api/todos/1
Content-Type: application/json

{
    "status": 1
}

### Mark todo as pending

PATCH http://localhost:8000/api/todos/1
Content-Type: application/json

{
    "status": 0
}

### Delete todo

DELETE http://localhost:8000/api/todos/5
Content-Type: application/json
