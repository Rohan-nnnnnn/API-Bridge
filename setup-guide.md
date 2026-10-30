APIBridge – Setup Guide

Overview

This guide explains the basic requirements and configuration needed to run APIBridge locally.

Prerequisites

- Docker
- n8n
- PostgreSQL
- Postman
- Access to the API used in the workflow

Environment Setup

1. Start the Services

Make sure your n8n and PostgreSQL services are running.

2. Configure PostgreSQL

- Create or select the database used by APIBridge.
- Configure the PostgreSQL connection in n8n.
- Verify that n8n can connect to the database.
- Ensure the required logging table is available.

3. Configure API Credentials

- Open the APIBridge workflow in n8n.
- Configure the required API credentials or authentication.
- Verify that the API endpoint and request settings match your integration.

Workflow Configuration

1. Open n8n.
2. Import or open the APIBridge workflow.
3. Review the webhook configuration.
4. Check the incoming request processing.
5. Verify the API integration settings.
6. Verify the success and error handling paths.
7. Check the PostgreSQL logging configuration.
8. Save and activate the workflow as required.

Testing with Postman

1. Open Postman.
2. Create a new HTTP request.
3. Select the HTTP method configured in the workflow.
4. Enter the n8n webhook URL.
5. Select JSON as the request body format.
6. Send a sample request.

Example JSON Input

```json
{
  "order_id": "ORD-1001",
  "amount": 2499,
  "currency": "INR"
}
```

The example uses top-level fields rather than a nested data object.

Verification

After sending a request:

- Check the webhook execution in n8n.
- Verify the API response.
- Check whether the correct success or error path executed.
- Verify that the execution information was recorded in PostgreSQL.

Troubleshooting

Webhook Not Responding

- Verify that n8n is running.
- Check the webhook URL and workflow activation state.
- Review the execution logs.

API Request Failing

- Verify the endpoint and HTTP method.
- Check authentication and request parameters.
- Review the API response and error details.

Database Logging Failing

- Verify PostgreSQL connectivity.
- Check the database credentials.
- Review the database operation in the n8n execution.

Notes

The exact API endpoint, credentials, database configuration, and webhook settings depend on the local project setup. Use the values configured in your actual workflow.
