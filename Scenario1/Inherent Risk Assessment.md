## Inherent Risk Assessment.md

```markdown
| Category | Description | Likelihood | Impact | Risk Rating | Scenario |
|----------|-------------|------------|--------|-------------|----------|
| Prompt Injection | Malicious prompt manipulation to bypass restrictions | High | High | Critical | Role escalation through crafted prompts |
| Model Poisoning | Contamination of training data or fine-tuned models | Medium | High | High | Backdoor injection in custom model |
| Data Exfiltration | Extraction of sensitive data through AI responses | High | High | Critical | PII extraction via prompt engineering |
| Identity Spoofing | AI-generated personas to bypass authentication | Medium | High | High | Deepfake voice/text impersonation |
| Supply Chain Attack | Compromised foundation models or datasets | Low | High | Medium | Malicious code in third-party models |
| Model Inversion | Reverse engineering to extract training data | Medium | Medium | Medium | Membership inference attacks |
| Adversarial Inputs | Crafted inputs to manipulate AI behavior | High | Medium | High | Jailbreaking through adversarial prompts |
| Context Poisoning | Injection of malicious context into RAG pipeline | Medium | High | High | Contaminated vector embeddings |
| Privilege Escalation | Using AI to gain unauthorized system access | Low | High | Medium | AI-assisted lateral movement |
| Data Poisoning | Manipulation of knowledge base content | Medium | High | High | False information injection |