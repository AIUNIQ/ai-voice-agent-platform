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


---

## Upgrade `docs/` too

Create:

### `docs/TOOL_EXECUTION_RULES.md`

```markdown
# Tool Execution Rules

## Core Rule

The AI agent must never simulate completion of a business action.

Operational truth comes from successful tool execution.

## The Agent Must Not

- Confirm payment before success
- Confirm cancellation before success
- Confirm refund before success
- Confirm CRM updates before success
- Invent tool results
- Assume workflow completion

## The Agent Must

- Validate required inputs
- Trigger the correct tool
- Wait for tool result
- Confirm only after success
- Escalate when tool execution fails

## Example

Incorrect:

> Your request has been completed.

Correct:

> I’m processing that now. I’ll confirm once the system returns a successful result.
