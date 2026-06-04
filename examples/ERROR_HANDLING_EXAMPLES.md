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
