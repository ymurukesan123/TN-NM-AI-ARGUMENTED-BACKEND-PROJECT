# Phase 3 – Project Design Phase

## Architecture

```text
Client / Thunder Client / Postman
              |
              v
        Express REST API
              |
       +------+------+
       |             |
 Authentication    Routes
       |             |
       +-------> Controllers
                    |
          +---------+---------+
          |                   |
       MongoDB             Gemini AI
       /Mongoose            Service
          |                   |
          +---------+---------+
                    |
              JSON Response
```

## MVC Design

### Models
- `User.js`
- `Blog.js`

### Controllers
- `authController.js`
- `blogController.js`
- `aiController.js`

### Routes
- `authRoutes.js`
- `blogRoutes.js`
- `aiRoutes.js`

### Services
- `geminiService.js`

### Middleware
- `authMiddleware.js`
- `errorMiddleware.js`

## Database Design

### User Collection
```text
User
├── name
├── email
├── password
├── createdAt
└── updatedAt
```

### Blog Collection
```text
Blog
├── title
├── content
├── author
├── createdAt
└── updatedAt
```

## Request Flow

```text
Request
  ↓
Express
  ↓
Authentication Middleware
  ↓
Route
  ↓
Controller
  ↓
MongoDB / Gemini
  ↓
JSON Response
```

## Security Design
- Passwords are hashed before storage.
- JWT protects private routes.
- Authentication middleware validates tokens.
- Blog ownership/authorization checks are applied where required.
- Validation and centralized error handling improve API reliability.
