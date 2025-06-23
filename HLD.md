## HLD.md

```markdown
```mermaid
flowchart TD
    subgraph "User Interface Layer"
        UI[Web Interface]
        Mobile[Mobile App]
        API[REST API Gateway]
    end
    
    subgraph "Identity & Authentication"
        Cognito[Amazon Cognito]
        IAM[AWS IAM]
        RBAC[Role-Based Access Control]
    end
    
    subgraph "AI Processing Layer"
        subgraph "Amazon Bedrock"
            FM[Foundation Models]
            Claude[Claude 3.5 Sonnet]
            Titan[Amazon Titan]
        end
        
        subgraph "Custom AI Components"
            FT[Fine-tuned Model]
            PS[Prompt Sanitizer]
            ContextEngine[Context Engine]
        end
    end
    
    subgraph "Data & Knowledge Layer"
        subgraph "Vector Databases"
            Pinecone[Pinecone Vector DB]
            OpenSearch[Amazon OpenSearch]
        end
        
        subgraph "Knowledge Sources"
            S3[S3 Document Store]
            RDS[Amazon RDS]
            DynamoDB[User Context DB]
        end
    end
    
    subgraph "Security & Monitoring"
        CloudTrail[AWS CloudTrail]
        GuardDuty[Amazon GuardDuty]
        WAF[AWS WAF with AI Rules]
        KMS[AWS KMS]
    end
    
    subgraph "External Integrations"
        LDAP[Enterprise LDAP]
        Slack[Slack Integration]
        Email[Email Services]
    end

    UI --> API
    Mobile --> API
    API --> Cognito
    Cognito --> IAM
    IAM --> RBAC
    
    API --> PS
    PS --> FM
    FM --> Claude
    FM --> Titan
    Claude --> FT
    
    FT --> ContextEngine
    ContextEngine --> Pinecone
    ContextEngine --> OpenSearch
    
    Pinecone --> S3
    OpenSearch --> RDS
    RBAC --> DynamoDB
    
    API --> WAF
    WAF --> CloudTrail
    CloudTrail --> GuardDuty
    
    Cognito --> LDAP
    ContextEngine --> Slack
    ContextEngine --> Email
    
    S3 --> KMS
    RDS --> KMS
    DynamoDB --> KMS