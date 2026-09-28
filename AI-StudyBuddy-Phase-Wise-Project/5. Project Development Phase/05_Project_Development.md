# Phase 5 – Project Development Phase

## 5.1 Technology Stack
- Node.js
- Express.js
- MongoDB
- Mongoose
- Google Gemini 2.5 Flash
- JWT
- bcryptjs
- Multer
- CORS
- Nodemon

## 5.2 Project Structure

```text
AI-StudyBuddy/
├── Code Files/
│   ├── index.js
│   ├── package.json
│   ├── package-lock.json
│   ├── README.md
│   └── src/
│       ├── controllers/
│       │   ├── authController.js
│       │   ├── materialController.js
│       │   └── adminController.js
│       ├── middleware/
│       │   ├── auth.js
│       │   └── upload.js
│       ├── models/
│       │   ├── User.js
│       │   └── Material.js
│       ├── routes/
│       │   ├── auth.js
│       │   ├── materials.js
│       │   └── admin.js
│       └── utils/
│           ├── db.js
│           ├── gemini.js
│           └── tokens.js
└── uploads/
```

## 5.3 Core Development Components

### Authentication
`authController.js` implements registration, login, token refresh and logout.

### Middleware
`auth.js` protects private routes and provides admin-only authorization.

### Material Management
`materialController.js` handles upload, retrieval, deletion and AI operations.

### Gemini Integration
`gemini.js` provides a reusable `askGemini()` helper.

### Database
Mongoose models represent users and study materials.

## 5.4 AI Features

### Summarization
Input: uploaded material  
Output: concise bullet-point summary

### Flashcards
Input: material + desired count  
Output:
```json
[
  {
    "question": "What is ...?",
    "answer": "..."
  }
]
```

### Quiz
Input: material + desired count  
Output:
```json
[
  {
    "question": "Which ...?",
    "options": ["A", "B", "C", "D"],
    "answer": "A"
  }
]
```

### Study Plan
Input:
- Goal
- Hours per day
- Number of days

Output: day-by-day personalized schedule.

## 5.5 Running the Project

```bash
cd "Code Files"
npm install
```

Create `.env` using the variables in Phase 2, then:

```bash
node index.js
```

or configure the npm start script and use:

```bash
npm start
```

Server:
```text
http://localhost:5000
```

Health check:
```text
GET /
```
