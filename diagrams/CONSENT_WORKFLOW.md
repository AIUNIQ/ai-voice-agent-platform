# Consent Workflow Diagram

```mermaid
flowchart TD
    A[Customer Expresses Interest] --> B[AI Explains Offer or Action]
    B --> C[AI Requests Explicit Consent]

    C --> D{Consent Received?}

    D -->|No| E[Continue Conversation or Clarify]
    D -->|Yes / Press 1| F[Log Consent Event]

    F --> G[Trigger Workflow]
    G --> H[Execute Business Action]
    H --> I{Action Successful?}

    I -->|Yes| J[Confirm Completion to Customer]
    I -->|No| K[Escalate or Provide Secure Fallback]

    J --> L[Update CRM]
    J --> M[Send Slack Alert]
    J --> N[Create Audit Record]
