# Phase 8 – Project Demonstration

## 8.1 Demo Objective
Demonstrate the complete flow from user registration to AI-generated learning resources and administration.

## 8.2 Demo Sequence

### Step 1 – Start Backend
```bash
npm install
node index.js
```

### Step 2 – Health Check
Open:
```text
GET http://localhost:5000/
```

Expected:
```json
{
  "message": "AI StudyBuddy API is running"
}
```

### Step 3 – Student Registration
Use:
```text
POST /api/auth/register
```
Provide name, email, password and student role.

### Step 4 – Student Login
Use:
```text
POST /api/auth/login
```
Save the returned access token.

### Step 5 – Upload Study Material
Use:
```text
POST /api/materials/upload
```
Send a study file using multipart/form-data.

### Step 6 – Generate Summary
Use:
```text
POST /api/materials/:id/summarize
```

### Step 7 – Generate Flashcards
Use:
```text
POST /api/materials/:id/flashcards
```
Example:
```json
{ "count": 5 }
```

### Step 8 – Generate Quiz
Use:
```text
POST /api/materials/:id/quiz
```

### Step 9 – Generate Study Plan
Use:
```json
{
  "goal": "Prepare for semester examination",
  "hoursPerDay": 2,
  "days": 7
}
```

### Step 10 – Admin Demonstration
Login as admin and demonstrate:
- View users
- View statistics
- Delete a user

## 8.3 Presentation Points
- Problem
- Proposed AI solution
- Architecture
- Technology stack
- Database design
- Authentication/RBAC
- Gemini integration
- API demonstration
- Testing
- Future enhancements

## 8.4 Final Demo Outcome
The demonstration should show that a student can securely upload study material and obtain multiple AI-generated learning resources through REST APIs.
