# System Architecture

## High-Level Architecture

Customer
    │
    ▼
Twilio Voice
    │
    ▼
Speech Processing
(Whisper ASR)
    │
    ▼
LLM Layer
(OpenAI GPT-4o)
    │
    ▼
Business Logic Engine
    │
    ├── CRM Integration
    ├── Payment Processing
    ├── Knowledge Base
    ├── Compliance Logging
    └── Notification Services

Outputs:
- CRM Updates
- Slack Notifications
- Customer Actions
- Audit Records
