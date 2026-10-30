# APIBridge – Smart API Integration Hub

APIBridge is an API integration and automation hub built using n8n and PostgreSQL. It automates API request processing, validates incoming data, handles successful and failed responses, and maintains execution logs for better reliability and traceability.

## Features

- Webhook-based API request handling
- Incoming data processing and validation
- API integration and response handling
- Success and error handling paths
- PostgreSQL-based execution logging
- API testing using Postman
- Automated workflow execution using n8n

## Tech Stack

- **Automation:** n8n
- **Database:** PostgreSQL
- **API Testing:** Postman
- **Data Format:** JSON
- **Integration:** REST APIs and Webhooks

## How It Works

1. An API request is received through the n8n webhook.
2. Incoming data is processed and validated.
3. The workflow performs the configured API integration.
4. The response is checked and routed through the appropriate success or error path.
5. Execution details are logged in PostgreSQL.
6. The workflow returns the appropriate response.

## Example Input

```json
{
  "order_id": "ORD-1001",
  "amount": 2499,
  "currency": "INR"
}
```

## Error Handling

APIBridge includes separate handling for successful and failed API operations. This helps identify unsuccessful requests and maintain execution records for debugging and monitoring.

## Database Logging

PostgreSQL is used to store execution details, including successful and failed delivery records. This provides a record of workflow activity.

## Testing

The workflow was tested using Postman with sample API requests. Both successful and error-handling paths were tested.

## Project Purpose

The goal of APIBridge is to demonstrate how APIs can be connected, automated, monitored, and managed through workflow automation.

## Author

**Rohan Narlawar**

- GitHub: https://github.com/Rohan-nnnnnn
- LinkedIn: https://www.linkedin.com/in/rohan-narlawar-149291354
- Email: rohannarlawar31@gmail.com
