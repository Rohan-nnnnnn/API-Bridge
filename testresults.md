APIBridge – Test Results

Overview

APIBridge was tested using Postman to verify successful API processing, duplicate request handling, and error handling.

Test Environment

- Automation Platform: n8n
- Database: PostgreSQL
- Testing Tool: Postman
- Request Format: JSON

Test Case 1 – Successful Request

Objective:

Verify that a valid API request is processed successfully.

Input:

```json
{
  "order_id": "ORD-1001",
  "amount": 2499,
  "currency": "INR"
}
```

Expected Result:

- Request is received through the webhook.
- API operation executes successfully.
- Success response is returned.

Status: Passed

Test Case 2 – Duplicate Request

Objective:

Verify that the workflow identifies and handles a duplicate request.

Expected Result:

- Duplicate request is detected.
- Duplicate processing is prevented or handled according to the workflow logic.
- Appropriate response is returned.

Status: Passed

Test Case 3 – Error Handling

Objective:

Verify that the workflow handles an unsuccessful API operation.

Expected Result:

- API failure is detected.
- Error-handling path executes.
- Appropriate error response is returned.

Status: Passed

Testing Summary

Three scenarios were tested using Postman:

- Successful request
- Duplicate request
- Error handling

The tests demonstrate API request processing and handling of different request outcomes.

Conclusion

APIBridge demonstrates API integration, duplicate request handling, and error management using n8n and PostgreSQL.
