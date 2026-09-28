# Phase 1 – Brainstorming & Ideation

## Project Title
**AI StudyBuddy – AI-Powered Learning Assistant Backend**

## 1.1 Idea
AI StudyBuddy is a backend platform that helps students convert study materials into useful learning resources using Generative AI.

## 1.2 Problem Identified
Students often spend significant time reading lengthy notes, preparing summaries, creating flashcards, making quiz questions, and planning revision schedules.

## 1.3 Proposed Idea
Build a secure REST API that allows authenticated students to upload study materials and use Google Gemini AI to generate:
- Concise summaries
- Flashcards
- Multiple-choice quizzes
- Personalized study plans

## 1.4 Target Users
- Students
- Administrators

## 1.5 Key Features
1. User registration and login
2. JWT-based authentication
3. Student/Admin role-based access
4. Study-material upload
5. AI summarization
6. AI flashcard generation
7. AI quiz generation
8. AI study-plan generation
9. Material management
10. Admin user and statistics management

## 1.6 Expected Benefits
- Reduces manual study preparation
- Makes revision faster
- Supports active recall through flashcards
- Provides self-assessment through quizzes
- Supports personalized study planning

## 1.7 Initial Technology Brainstorm
- Node.js
- Express.js
- MongoDB
- Mongoose
- Google Gemini API
- JWT
- bcryptjs
- Multer
- Postman

## 1.8 Final Concept
A modular AI-powered backend where authentication, database models, file handling, business logic, and AI services are separated for maintainability and future expansion.
