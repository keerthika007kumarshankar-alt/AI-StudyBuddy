# Phase 6 – Project Testing

## 6.1 Testing Strategy
API testing is performed using Postman. Authentication, authorization, database operations, file upload and AI generation endpoints are tested separately.

## 6.2 Test Cases

| ID | Test Case | Expected Result |
|---|---|---|
| TC-01 | Register valid student | 201 and user created |
| TC-02 | Register existing email | 400 error |
| TC-03 | Login valid credentials | 200 and tokens |
| TC-04 | Login invalid credentials | 401 error |
| TC-05 | Access protected API without token | 401 error |
| TC-06 | Upload valid material | 201 and material created |
| TC-07 | Upload without file | 400 error |
| TC-08 | List own materials | 200 and materials returned |
| TC-09 | Access another user's material | 403 error |
| TC-10 | Delete own material | 200 |
| TC-11 | Generate summary | AI summary returned |
| TC-12 | Generate flashcards | JSON flashcards returned |
| TC-13 | Generate quiz | JSON MCQ returned |
| TC-14 | Generate study plan | Plan returned |
| TC-15 | Student accesses admin API | 403 error |
| TC-16 | Admin gets users | 200 |
| TC-17 | Admin gets stats | 200 |
| TC-18 | Invalid material ID | Appropriate error response |

## 6.3 Security Tests
- Invalid JWT
- Missing JWT
- Student-to-admin route access
- Cross-user material access
- Duplicate registration
- Password mismatch

## 6.4 AI Tests
- Short study material
- Long study material
- Empty/invalid content
- Flashcard count variation
- Quiz count variation
- Different study goals and durations

## 6.5 Expected Testing Result
The application should return appropriate HTTP status codes and JSON responses for valid and invalid requests. Protected resources must not be accessible without proper authentication/authorization.
