# Circle-Backend
This is the backend repo of a social networking site named CIRCLE, built using NodeJs, ExpressJs and MongoDB.

# API ROUTES

### Register user
```
POST http://localhost:3000/auth/register
```
```
Content-Type: application/json

{
    "firstName" : "Sarah",
    "lastName" : "Cavill",
    "email" : "Sarah@gmail.com",
    "password" : "789456"
}
```

### Login user
```
POST http://localhost:3000/auth/login
```
```
Content-Type: application/json

{
    "email" : "JohnDoe@gmail.com",
    "password" : "123456"
}
```
### Get user
```
GET http://localhost:3000/users/:id
Authorization: Bearer <token>
```

### add friend
```
PATCH http://localhost:3000/users/:id/:friendId
Authorization: Bearer <token>
```

### get user's friends
```
GET http://localhost:3000/users/:id/friends
Authorization: Bearer <token>
```

### Create a post
```
POST http://localhost:3000/posts/:userId/create
Authorization: Bearer <token>
```
```
Content-Type: application/json

{
    "description" : "This is some random description"
}
```

### Get all posts
```
GET  http://localhost:3000/posts/
```

### Get all posts of a user
```
GET http://localhost:3000/posts/:userId/posts
Authorization: Bearer <token>
```

### Update like of a post
```
PATCH http://localhost:3000/posts/:id/like
Authorization: Bearer <token>
```
