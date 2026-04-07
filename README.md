# galaxy-voyager-agent

## Architecture Diagram

```mermaid
flowchart TD
    A[User Input] --> B[Primary Agent]

    B --> C1[Knowledge Agent]
    B --> C2[Task Agent]
    B --> C3[State Agent]

    C1 --> D[Gemini Model]
    C2 --> D
    C3 --> D

    D --> E[Response]

    C2 --> F[Tools]
    F --> F1[Calendar]
    F --> F2[Notes]
    F --> F3[Task Manager]

    C3 --> G[State Memory]
