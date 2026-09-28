# Phase 2 – Requirement Analysis

## 2.1 Functional Requirements

| ID | Requirement | Description |
|---|---|---|
| FR-01 | Registration | User can create an account |
| FR-02 | Login | User can authenticate with email and password |
| FR-03 | Token Management | Access/refresh tokens are generated and refreshed |
| FR-04 | Role Management | Student and admin roles are supported |
| FR-05 | Upload Material | Authenticated user can upload study material |
| FR-06 | View Materials | User can retrieve available materials |
| FR-07 | Delete Material | Authorized user can delete a material |
| FR-08 | Summarize | Gemini generates a concise summary |
| FR-09 | Flashcards | Gemini generates question-answer flashcards |
| FR-10 | Quiz | Gemini generates MCQ questions |
| FR-11 | Study Plan | Gemini generates a personalized plan |
| FR-12 | Admin Users | Admin can view/delete users |
| FR-13 | Admin Stats | Admin can view user/material statistics |

## 2.2 Non-Functional Requirements
- Security: password hashing and JWT authentication
- Performance: REST API with modular controllers
- Scalability: MongoDB and separated service modules
- Maintainability: controllers/routes/models/utils are separated
- Usability: clear JSON API responses
- Reliability: global error handling and validation
- Compatibility: Windows, macOS and Linux

## 2.3 User Roles

### Student
Can register/login, upload materials, view/delete owned materials, and generate AI learning resources.

### Admin
Can manage users and view platform statistics in addition to authenticated operations.

## 2.4 Software Requirements
- Node.js 16+
- npm 8+
- MongoDB
- Visual Studio Code or equivalent
- Postman
- Internet connection for Gemini API

## 2.5 Environment Variables
```env
PORT=5000
MONGO_URI=mongodb://localhost:27017/ai-studybuddy
JWT_ACCESS_SECRET=your_access_secret
JWT_REFRESH_SECRET=your_refresh_secret
GEMINI_API_KEY=your_gemini_api_key
NODE_ENV=development
```

## 2.6 API Requirement Summary
### Authentication
- POST `/api/auth/register`
- POST `/api/auth/login`
- POST `/api/auth/refresh`
- POST `/api/auth/logout`

### Materials
- POST `/api/materials/upload`
- GET `/api/materials`
- GET `/api/materials/:id`
- DELETE `/api/materials/:id`
- POST `/api/materials/:id/summarize`
- POST `/api/materials/:id/flashcards`
- POST `/api/materials/:id/quiz`
- POST `/api/materials/:id/study-plan`

### Administration
- GET `/api/admin/users`
- DELETE `/api/admin/users/:id`
- GET `/api/admin/stats`
