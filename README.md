# login-auth-api

![Licence](https://img.shields.io/github/license/Ileriayo/markdown-badges?style=for-the-badge)
<br/>
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens)

This project is an API built using **Java, Spring Boot, H2DB as the in-memory database, and Spring Security with JWT for authentication control**. The API allows users to register, log in, and securely access user information using JWT tokens.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/PedroSmaxY/login-auth-api.git
```

2. Install dependencies with Maven
```bash
cd login-auth-api
mvn install
```
## Usage

1. Start the application with Maven:
```bash
mvn spring-boot:run
```

2. The API will be accessible at `https://localhost:8080`.

## API Endpoints
The API provides the following endpoints:

### 1. Auth

#### 1.1 Login
```markdown
POST - auth/login - Authenticate a user and return an access token
```

- Request Body
```json
{
  "email": "pedro@email.com",
  "password": "password"
}
```

- Response
```json
{
  "name": "pedro",
  "token": "*******"
}
```

#### 1.2 Register
```markdown
POST - auth/register - Register a new user and return an access token
```

- Request Body
```json
{
  "name": "pedro",
  "email": "pedro@email.com",
  "password": "password"
}
```

- Response
```json
{
  "name": "pedro",
  "token": "*******"
}
```

### 2. User

#### Get User Info
```markdown
GET - /user - Receive an accept message
```

- Headers
```http request
Authorization: Bearer <Token>
```

- Response
```json
{
  "message": "User information retrieved successfully."
}
```

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request to the repository.

When contributing to this project, please follow the existing code style, [commit conventions](https://www.conventionalcommits.org/en/v1.0.0/), and submit your changes in a separate branch.