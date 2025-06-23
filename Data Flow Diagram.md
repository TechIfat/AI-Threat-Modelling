
## Data Flow Diagram.md

```markdown
```mermaid
erDiagram
    USER }|--|| IDENTITY_PROVIDER : "authenticates_with"
    USER ||--o{ CHAT_SESSION : "initiates"
    USER ||--|| USER_PROFILE : "has"
    
    IDENTITY_PROVIDER ||--|| AWS_COGNITO : "integrates_with"
    AWS_COGNITO ||--|| RBAC_POLICY : "enforces"
    
    CHAT_SESSION ||--o{ MESSAGE : "contains"
    CHAT_SESSION ||--|| CONTEXT_MEMORY : "maintains"
    
    MESSAGE ||--|| PROMPT_SANITIZER : "processed_by"
    PROMPT_SANITIZER ||--|| BEDROCK_MODEL : "sends_to"
    
    BEDROCK_MODEL ||--|| FOUNDATION_MODEL : "uses"
    FOUNDATION_MODEL ||--o{ FINE_TUNED_MODEL : "enhanced_by"
    
    BEDROCK_MODEL ||--|| VECTOR_SEARCH : "queries"
    VECTOR_SEARCH ||--|| KNOWLEDGE_BASE : "searches"
    
    KNOWLEDGE_BASE ||--o{ DOCUMENT : "contains"
    KNOWLEDGE_BASE ||--|| ACCESS_CONTROL : "protected_by"
    
    USER_PROFILE ||--|| ROLE : "assigned"
    ROLE ||--|| PERMISSION : "grants"
    PERMISSION ||--|| KNOWLEDGE_BASE : "controls_access_to"
    
    CHAT_SESSION ||--|| AUDIT_LOG : "logged_in"
    AUDIT_LOG ||--|| CLOUDTRAIL : "stored_in"
    
    FINE_TUNED_MODEL ||--|| TRAINING_DATA : "trained_on"
    TRAINING_DATA ||--|| DATA_GOVERNANCE : "governed_by"