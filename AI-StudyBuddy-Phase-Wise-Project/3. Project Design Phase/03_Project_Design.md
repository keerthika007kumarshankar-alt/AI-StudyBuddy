# Phase 3 – Project Design Phase

## 3.1 High-Level Architecture

```text
Client / Postman
       |
       v
   Express API
       |
  +----+-------------------+
  |                        |
Auth Middleware        Route Layer
  |                        |
  v                        v
JWT / RBAC             Controllers
                           |
             +-------------+-------------+
             |             |             |
          MongoDB       File Upload   Gemini AI
          /Mongoose       /Multer      Service
             |             |             |
             +-------------+-------------+
                           |
                    JSON API Response
```

## 3.2 Module Design

### Authentication Module
Handles registration, login, token refresh and logout.

### Authorization Module
Protects private routes and separates student/admin permissions.

### Material Module
Handles study-material upload, retrieval and deletion.

### AI Module
Communicates with Google Gemini to generate educational resources.

### Administration Module
Provides user management and application statistics.

## 3.3 Database Design

### User Collection
```text
User
├── name
├── email
├── password
├── role
├── createdAt
└── updatedAt
```

### Material Collection
```text
Material
├── user
├── title
├── content
├── filename
├── summary
├── flashcards[]
├── quiz[]
├── studyPlan
├── createdAt
└── updatedAt
```

## 3.4 Request Flow

```text
Request
  ↓
Express Middleware
  ↓
JWT Authentication
  ↓
Route
  ↓
Controller
  ↓
MongoDB / Gemini
  ↓
Controller Response
  ↓
JSON Response
```

## 3.5 Security Design
- Passwords are hashed using bcryptjs.
- JWT is used for authentication.
- Protected routes require authentication.
- Admin routes require admin role.
- Users are restricted from accessing other students' materials.

## 3.6 AI Prompt Design
AI prompts are generated dynamically using the uploaded study material. JSON-only prompts are used for structured flashcards and quizzes.
