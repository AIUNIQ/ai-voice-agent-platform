# Error Handling Examples

## Missing Customer Email

Problem:

The customer requests an account action but no email is available.

System Response:

```json
{
  "success": false,
  "error": "missing_customer_email",
  "next_step": "request_email"
}
Agent Behavior:

I can help with that. What email is connected to your account?

Failed API Request
Problem:

CRM API returns an error.

System Response:
{
  "success": false,
  "error": "crm_api_failed",
  "status_code": 500,
  "next_step": "retry_or_escalate"
}
Agent Behavior:

I’m not able to complete that automatically right now. I’ll flag this for review so it can be handled properly.

Tool Execution Failure
Problem:

A business action fails.

Agent Rule:

The AI must not confirm completion unless the tool returns success.

Correct Response:

I wasn’t able to complete that action automatically. Let me route this for review.

