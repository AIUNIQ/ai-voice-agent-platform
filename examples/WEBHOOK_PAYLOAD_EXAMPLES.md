# Webhook Payload Examples

## Customer Event Payload

```json
{
  "event_type": "customer_action",
  "customer": {
    "first_name": "Jane",
    "email": "jane@example.com",
    "phone": "+15551234567"
  },
  "source": "voice_agent",
  "timestamp": "2026-01-01T10:00:00Z"
}
