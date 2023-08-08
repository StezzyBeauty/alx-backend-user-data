# 0x01. Basic authentication

<img src=https://camo.githubusercontent.com/dbee9377978d25748c641f11f50faedba44ee215b2e23d8abd7ac04619269f0d/68747470733a2f2f646f63732e6f7261636c652e636f6d2f63642f4531393837392d30312f3831392d333636392f696d616765732f73656375726974792d68747470426173696341757468656e7469636174696f6e2e676966>

## Simple API
Simple HTTP API for playing with User model.

## Files
### models/
- base.py: base of all models of the API - handle serialization to file
- user.py: user model

### api/v1
- app.py: entry point of the API
- views/index.py: basic endpoints of the API: /status and /stats
- views/users.py: all users endpoints

## Setup
```
$ pip3 install -r requirements.txt
```

## Run
```
$ API_HOST=0.0.0.0 API_PORT=5000 python3 -m api.v1.app
```

## Routes
- GET /api/v1/status: returns the status of the API
- GET /api/v1/stats: returns some stats of the API
- GET /api/v1/users: returns the list of users
- GET /api/v1/users/:id: returns an user based on the ID
- DELETE /api/v1/users/:id: deletes an user based on the ID
- POST /api/v1/users: creates a new user (JSON parameters: email, password, last_name (optional) and first_name (optional))
- PUT /api/v1/users/:id: updates an user based on the ID (JSON parameters: last_name and first_name)
