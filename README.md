# API Documentation
## Endpoints

## 1. Get Users
```
Method: GET
endpoint: /api/users
```


```json5
//response

{
   "users":[
      {
         "_id":"62bdce506dceebcff3c0a841",
         "name":"Samir Alam",
         "email":"samir1@gmail.com",
         "imageUrl":"uploads/images/289d5a30-f891-11ec-a7f0-7f1adca3f12f.png",
         "contacts":[
            
         ],
         "__v":0,
         "id":"62bdce506dceebcff3c0a841"
      },
      {
         "_id":"62bdce646dceebcff3c0a847",
         "name":"Samir Alam",
         "email":"samir11@gmail.com",
         "imageUrl":"uploads/images/347f5830-f891-11ec-a7f0-7f1adca3f12f.png",
         "contacts":[
            
         ],
         "__v":0,
         "id":"62bdce646dceebcff3c0a847"
      },
      {
         "_id":"62bdd299a83cb701b8b99c85",
         "name":"test test",
         "email":"test@test.com",
         "imageUrl":"uploads/images/b6e73750-f893-11ec-a59f-8b246d6b64a5.png",
         "contacts":[
            "62bdf3f8441254abff796636",
            "62bdf4f8b8f4b6f7080ff4ab"
         ],
         "__v":10,
         "id":"62bdd299a83cb701b8b99c85"
      },
      {
         "_id":"62bdd3635eba0ff8342d40a2",
         "name":"test test test",
         "email":"testtest@test.com",
         "imageUrl":"uploads/images/2f4c71b0-f894-11ec-9201-ad86d7298077.png",
         "contacts":[
            
         ],
         "__v":0,
         "id":"62bdd3635eba0ff8342d40a2"
      }
   ]
}
```

## 2. User signup.
```
Method: POST
endpoint: /api/users/signup
```
```json5
//request body
{
  "email": "testtestt@test.com"
  "name": "Samir Alam"
  "password": samirsamir"
  "imageUrl": (binary)
}

```
```json5
//response
{
   "userId":"62c2dd0a2f76f091fa049ffc",
   "email":"samir@gmail.com",
   "token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI2MmMyZGQwYTJmNzZmMDkxZmEwNDlmZmMiLCJlbWFpbCI6InNhbWlyQGdtYWlsLmNvbSIsImlhdCI6MTY1NjkzNzczOCwiZXhwIjoxNjU2OTQxMzM4fQ.QkNd5RE0f86SHt9gn8O7J7YufEz3GtFmeakPmrHwEHI"
}

```

## 3. User login.
```
Method: POST
endpoint: /api/users/login
```
```json5
//request body
{
  "email": "test@test.com"
  "password": samirsamir"
}

```
```json5
//response
{
   "userId":"62c2dd0a2f76f091fa049ffc",
   "email":"samir@gmail.com",
   "token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI2MmMyZGQwYTJmNzZmMDkxZmEwNDlmZmMiLCJlbWFpbCI6InNhbWlyQGdtYWlsLmNvbSIsImlhdCI6MTY1NjkzNzczOCwiZXhwIjoxNjU2OTQxMzM4fQ.QkNd5RE0f86SHt9gn8O7J7YufEz3GtFmeakPmrHwEHI"
}

```

## 4. Fetch contacts

```
Method: GET
endpoint: /api/contacts
```
```json5
//response

{
    "contact": [
        {
            "_id": "62bdf3f8441254abff796636",
            "title": "smair",
            "description": "samir",
            "imageUrl": "uploads/images/9acd3790-f8a7-11ec-9b2f-75886881d17b.jpeg",
            "address": "samir",
            "phone": "2536523526",
            "creator": "62bdd299a83cb701b8b99c85",
            "__v": 0
        },
        {
            "_id": "62bdf4f8b8f4b6f7080ff4ab",
            "title": "samir",
            "description": "smair",
            "imageUrl": "uploads/images/33d1e2b0-f8a8-11ec-abfa-b54f14063f2d.jpeg",
            "address": "samir",
            "phone": "2563258",
            "creator": "62bdd299a83cb701b8b99c85",
            "__v": 0
        }
    ]
}
```

## 5. Get contacts by userId:

```
Method: GET
endpoint: /api/contacts/user/:userId
```
```json5
//response
{
    "contacts": [
        {
            "_id": "62bdf3f8441254abff796636",
            "title": "smair",
            "description": "samir",
            "imageUrl": "uploads/images/9acd3790-f8a7-11ec-9b2f-75886881d17b.jpeg",
            "address": "samir",
            "phone": "2536523526",
            "creator": "62bdd299a83cb701b8b99c85",
            "__v": 0,
            "id": "62bdf3f8441254abff796636"
        },
        {
            "_id": "62bdf4f8b8f4b6f7080ff4ab",
            "title": "samir",
            "description": "smair",
            "imageUrl": "uploads/images/33d1e2b0-f8a8-11ec-abfa-b54f14063f2d.jpeg",
            "address": "samir",
            "phone": "2563258",
            "creator": "62bdd299a83cb701b8b99c85",
            "__v": 0,
            "id": "62bdf4f8b8f4b6f7080ff4ab"
        }
    ]
}

```

## 6. Update user contact
```
Method: PUT
endpoint: /api/contacts/:id
```

```json5
//request body

{
   "title":"samir contact",
   "description":"This is the contact description of samir.",
   "address":"itahari, sunsari",
   "phone":"9810456820"
}
```

```json5
//response
{
   "contact":{
      "_id":"62bdf4f8b8f4b6f7080ff4ab",
      "title":"samir contact",
      "description":"This is the contact description of samir.",
      "imageUrl":"uploads/images/33d1e2b0-f8a8-11ec-abfa-b54f14063f2d.jpeg",
      "address":"itahari, sunsari",
      "phone":"9810456820",
      "creator":"62bdd299a83cb701b8b99c85",
      "__v":0,
      "id":"62bdf4f8b8f4b6f7080ff4ab"
   }
}
```

## 7. Delete user contact

```
Method: DELETE
endpoint: /api/contacts/:id
```

```json5
//response
{
   "message":"Deleted contact"
}
```



