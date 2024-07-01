```mermaid

erDiagram
    USER {
        int id PK
        string email
        string encrypted_password
        boolean admin
        datetime created_at
        datetime updated_at
    }
    PROFILE {
        int id PK
        int user_id FK
        string username
        string avatar
        datetime created_at
        datetime updated_at
    }
    TASK {
        int id PK
        int user_id FK
        string title
        string description
        boolean completed
        datetime created_at
        datetime updated_at
    }
    TIMER_RECORD {
        int id PK
        int user_id FK
        int task_id FK
        datetime start_time
        datetime end_time
        datetime created_at
        datetime updated_at
    }
    LEARNING_OUTCOME {
        int id PK
        int user_id FK
        string title
        string content
        datetime created_at
        datetime updated_at
    }
    FORUM {
        int id PK
        string title
        string description
        datetime created_at
        datetime updated_at
    }
    POST {
        int id PK
        int forum_id FK
        int user_id FK
        string content
        datetime created_at
        datetime updated_at
    }
    COMMENT {
        int id PK
        int post_id FK
        int user_id FK
        string content
        datetime created_at
        datetime updated_at
    }

    USER ||--o{ PROFILE : "has"
    USER ||--o{ TASK : "has"
    USER ||--o{ TIMER_RECORD : "has"
    USER ||--o{ LEARNING_OUTCOME : "has"
    USER ||--o{ POST : "writes"
    USER ||--o{ COMMENT : "writes"
    FORUM ||--o{ POST : "contains"
    POST ||--o{ COMMENT : "contains"
