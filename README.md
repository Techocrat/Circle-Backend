# Circle-Backend

```
CIRCLE is an application that is built using Node.js, Express, and MongoDB. It is designed to provide users with an easy and intuitive platform to connect with others and share their thoughts and ideas.

Users of the Circle app will be able to register themselves by providing their basic information, such as their name, email address, and password. Once registered, they can log in to their account and start using the app's features. One of the main features of the Circle app is the ability to create posts. Users can write and share their thoughts, ideas, or any other content they want to share with their friends and followers. They can also like posts, either from their friends or from other users they follow.

Additionally, the Circle app allows users to add and remove friends, which enables them to connect with others and build their social circle. They can also view other users' profiles and posts, and interact with them. All these features are available only after the user has been authenticated, which ensures the security and privacy of the users' information.

In summary, the Circle app is a social platform that enables users to connect with others, share their thoughts and ideas, and build their social circle. It provides a user-friendly interface and various features to make the user experience more enjoyable, and at the same time, it takes security and privacy seriously by implementing authentication and authorization measures.
```





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
