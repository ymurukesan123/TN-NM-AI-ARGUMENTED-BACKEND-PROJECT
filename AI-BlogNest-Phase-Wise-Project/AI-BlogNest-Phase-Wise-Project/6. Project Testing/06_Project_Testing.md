# Phase 6 – Project Testing

## Testing Strategy
The REST API is tested using Thunder Client or Postman. Both successful and failure scenarios are covered.

## Test Cases

| ID | Test Case | Expected Result |
|---|---|---|
| TC-01 | Register valid user | User created |
| TC-02 | Register duplicate email | Validation/error response |
| TC-03 | Login valid credentials | JWT returned |
| TC-04 | Login invalid credentials | Authentication error |
| TC-05 | Profile without token | 401 response |
| TC-06 | Profile with valid token | User profile returned |
| TC-07 | Create blog with valid token | Blog created |
| TC-08 | Get all blogs | Blog list returned |
| TC-09 | Get blog by ID | Requested blog returned |
| TC-10 | Update owned blog | Blog updated |
| TC-11 | Delete owned blog | Blog deleted |
| TC-12 | Unauthorized blog update | Access denied |
| TC-13 | Unauthorized blog delete | Access denied |
| TC-14 | Generate AI blog | AI-generated content returned |
| TC-15 | Summarize content | AI summary returned |
| TC-16 | AI request without token | 401 response |
| TC-17 | Invalid blog ID | Appropriate error |
| TC-18 | Missing required fields | Validation error |
| TC-19 | Gemini API failure | Controlled error response |

## Security Tests
- Missing JWT
- Invalid JWT
- Expired/invalid authentication
- Cross-user blog modification
- Duplicate registration

## AI Tests
- Short topic
- Detailed topic
- Long content for summarization
- Empty content
- Gemini API unavailable

## Expected Result
Valid requests should return appropriate success status codes and JSON responses. Invalid or unauthorized requests should be rejected safely.
