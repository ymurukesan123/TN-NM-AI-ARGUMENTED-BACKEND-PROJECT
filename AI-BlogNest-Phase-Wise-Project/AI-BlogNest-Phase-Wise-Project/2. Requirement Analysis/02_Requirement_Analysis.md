# Phase 2 – Requirement Analysis

## Functional Requirements

| ID | Requirement | Description |
|---|---|---|
| FR-01 | Registration | Create a user account |
| FR-02 | Login | Authenticate a user and issue JWT |
| FR-03 | Profile | Retrieve authenticated user profile |
| FR-04 | Create Blog | Create a new blog post |
| FR-05 | Read Blogs | List all available blogs |
| FR-06 | Read Blog | Retrieve a blog by ID |
| FR-07 | Update Blog | Modify an existing blog |
| FR-08 | Delete Blog | Remove an existing blog |
| FR-09 | Generate Blog | Generate draft content using Gemini |
| FR-10 | Summarize Blog | Generate an AI summary |
| FR-11 | Authorization | Restrict protected operations to authenticated users |

## Non-Functional Requirements
- Secure password storage using bcrypt
- JWT-based authentication
- RESTful API design
- MongoDB/Mongoose persistence
- Modular MVC structure
- Input validation and error handling
- CORS support
- AI service integration

## Software Requirements
- Node.js
- npm
- MongoDB
- VS Code or equivalent IDE
- Thunder Client/Postman
- Gemini API key

## Environment Variables

```env
PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/ai-blognest
JWT_SECRET=your_jwt_secret
GEMINI_API_KEY=your_gemini_api_key
GEMINI_MODEL=gemini-2.5-flash
```

## API Groups

### Authentication
- POST `/api/auth/register`
- POST `/api/auth/login`
- GET `/api/auth/profile`

### Blogs
- POST `/api/blogs`
- GET `/api/blogs`
- GET `/api/blogs/:id`
- PUT `/api/blogs/:id`
- DELETE `/api/blogs/:id`

### AI
- POST `/api/ai/generate-blog`
- POST `/api/ai/summarize`
