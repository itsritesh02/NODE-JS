# Important HTTP Status Codes

## 1. Success Codes (2xx)

200 - OK
Request successfully completed.

201 - Created
New resource successfully created.

204 - No Content
Request successful, but no response body.

## 2. Client Error Codes (4xx)

400 - Bad Request
Invalid input or request data.

401 - Unauthorized
Authentication is missing or invalid.

403 - Forbidden
User does not have permission.

404 - Not Found
Requested resource or route not found.

409 - Conflict
Resource already exists, such as duplicate email.

422 - Unprocessable Content
Request format is valid, but validation fails.

429 - Too Many Requests
Too many requests sent by the client.

## 3. Server Error Codes (5xx)

500 - Internal Server Error
Unexpected error on the server.

502 - Bad Gateway
Invalid response from an upstream server.

503 - Service Unavailable
Server is temporarily unavailable.

504 - Gateway Timeout
Upstream server did not respond in time.

## Interview Tip

Most important status codes for MERN interviews:

200, 201, 400, 401, 403, 404, 409, 422, 500.