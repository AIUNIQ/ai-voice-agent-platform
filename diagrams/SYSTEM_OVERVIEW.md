# System Overview Diagram

```mermaid
flowchart TD
    A[Customer / Lead] --> B[Twilio Voice or SMS]
    B --> C[AI Voice Agent]
    C --> D[Speech Processing]
    D --> E[LLM Reasoning Layer]
    E --> F[Business Logic Engine]

    F --> G[CRM System]
    F --> H[Payment Platform]
    F --> I[Knowledge Base]
    F --> J[Slack Notifications]
    F --> K[Compliance Logs]

    G --> L[Customer Record Updated]
    H --> M[Transaction Status Returned]
    I --> N[Grounded Knowledge Response]
    J --> O[Operations Team Alerted]
    K --> P[Audit Trail Created]
