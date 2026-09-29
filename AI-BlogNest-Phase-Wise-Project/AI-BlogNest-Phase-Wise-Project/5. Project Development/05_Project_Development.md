# Phase 5 – Project Development Phase

## Technology Stack
- Node.js
- Express.js
- MongoDB
- Mongoose
- Google Gemini Generative AI
- JWT
- bcryptjs
- express-validator
- CORS
- Morgan
- dotenv
- Nodemon
- Axios

## Project Structure

```text
Code Files/
├── package.json
├── package-lock.json
├── README.md
├── thunder-client-ai-blognest-api.postman_collection.json
├── thunder-client-env.json
└── src/
    ├── server.js
    ├── app.js
    ├── config/
    │   └── db.js
    ├── models/
    │   ├── User.js
    │   └── Blog.js
    ├── middleware/
    │   ├── authMiddleware.js
    │   └── errorMiddleware.js
    ├── controllers/
    │   ├── authController.js
    │   ├── blogController.js
    │   └── aiController.js
    ├── routes/
    │   ├── authRoutes.js
    │   ├── blogRoutes.js
    │   └── aiRoutes.js
    └── services/
        └── geminiService.js
```

## Development Modules

### Authentication
Registration, login and authenticated profile retrieval.

### Blog Management
Full CRUD operations for blog posts.

### Gemini AI
AI-assisted blog generation and summarization.

### Middleware
JWT authentication, validation and centralized error handling.

## AI Features

### Generate Blog
Input can include a topic/title and related instructions. Gemini creates draft blog content.

### Summarize
Existing blog/content is supplied to Gemini and a concise summary is returned.

## Installation

```bash
npm install
```

Create `.env` using the variables from Phase 2.

## Run in Development

```bash
npm run dev
```

## Run in Production

```bash
npm start
```

## API Base URL

```text
http://localhost:5000
```

## Testing
The repository includes a Thunder Client/Postman collection and environment file for API testing.
