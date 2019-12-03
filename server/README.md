[![Build Status](https://travis-ci.org/abidex4yemi/Basic-user-auth.svg?branch=develop)](https://travis-ci.org/abidex4yemi/Basic-user-auth)

# Introduction

Chat app backend

---

## API Spec

Endpoint JSON response

### Users (authentication)

```source-json
{
  "token": "jwt.token",
    "username": "fake",
}
```

## Endpoints

### Authentication

`POST /api/users/auth/login`

Example response body:

```source-json
{
    "success": true,
    "message": "Log in successful",
    "body": {
        "firstName": "fake",
        "role": "their role",
        "token": "jwt.token"
    }
}
```

### Registration:

`POST /api/users/auth/signup`

Endpoint request body

```source-json
{
	"firstName": "",
	"lastName": "",
	"password": "",
	"email": "",
	"username": ""
}
```

Endpoint JSON response

## Endpoints

### Authentication

`POST /api/users/auth/login`

Example response body:

```source-json
{
    "success": true,
    "message": "Log in successful",
    "body": {
        "firstName": "fake",
        "role": "their role",
        "token": "jwt.token"
    }
}
```

Example response body:

```source-json
{
    "success": true,
    "message": "Account created successfully, please check your email for account verification",
    "body": []
}
```

### Account verification:

`POST /api/users/auth/confirm/token`

Example response body:

```source-json
{
    "success": true,
    "message": "Account created successfully, please check your email for account verification",
    "body": []
}
```

### Get user permission

`GET /api/user/auth/permissions/:username`

Example response body:

```source-json
{
    "success": true,
    "message": "user permission",
    "body": {
        "role": ""
    }
}
```
