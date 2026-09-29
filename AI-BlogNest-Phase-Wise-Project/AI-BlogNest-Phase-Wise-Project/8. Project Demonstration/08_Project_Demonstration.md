# Phase 8 – Project Demonstration

## Step 1 – Install Dependencies

```bash
npm install
```

## Step 2 – Configure Environment

Create `.env`:

```env
PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/ai-blognest
JWT_SECRET=your_jwt_secret
GEMINI_API_KEY=your_gemini_api_key
GEMINI_MODEL=gemini-2.5-flash
```

## Step 3 – Start Server

```bash
npm run dev
```

## Step 4 – Register User

```text
POST /api/auth/register
```

Example:
```json
{
  "name": "Student",
  "email": "student@example.com",
  "password": "123456"
}
```

## Step 5 – Login

```text
POST /api/auth/login
```

Save the returned JWT and use it as a Bearer token.

## Step 6 – View Profile

```text
GET /api/auth/profile
```

## Step 7 – Create Blog

```text
POST /api/blogs
```

Example:
```json
{
  "title": "Introduction to Artificial Intelligence",
  "content": "Artificial intelligence is..."
}
```

## Step 8 – View Blogs

```text
GET /api/blogs
```

## Step 9 – Update Blog

```text
PUT /api/blogs/:id
```

## Step 10 – Delete Blog

```text
DELETE /api/blogs/:id
```

## Step 11 – Generate AI Blog

```text
POST /api/ai/generate-blog
```

Provide a topic/title and relevant instructions according to the API implementation.

## Step 12 – Summarize Content

```text
POST /api/ai/summarize
```

Provide the content to be summarized.

## Step 13 – Demonstrate Testing
Run the supplied Thunder Client/Postman collection and show:
- Authentication
- Blog CRUD
- AI generation
- AI summarization
- Unauthorized request handling

## Presentation Order
1. Problem statement
2. Proposed solution
3. Objectives
4. Architecture
5. Technology stack
6. Database models
7. Authentication
8. Blog CRUD
9. Gemini AI integration
10. Testing
11. Future enhancements
