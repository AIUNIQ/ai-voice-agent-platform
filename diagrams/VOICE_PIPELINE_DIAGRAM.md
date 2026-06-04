
---

### 2. `VOICE_PIPELINE_DIAGRAM.md`

Paste this:

```markdown
# Voice Pipeline Diagram

```mermaid
sequenceDiagram
    participant Customer
    participant Twilio
    participant ASR as Speech-to-Text
    participant LLM as LLM Layer
    participant Logic as Business Logic
    participant TTS as Text-to-Speech
    participant CRM
    participant Slack

    Customer->>Twilio: Speaks during call
    Twilio->>ASR: Sends audio stream
    ASR->>LLM: Converts speech to text
    LLM->>Logic: Determines intent and next action
    Logic->>CRM: Updates customer record if needed
    Logic->>Slack: Sends operational alert if needed
    Logic->>TTS: Sends response text
    TTS->>Twilio: Returns generated voice
    Twilio->>Customer: Plays AI response
