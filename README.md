# AI-Threat-Modelling
# AI Threat Modelling Workshop Summary

## Introduction
A worked AI threat-modelling exercise against "IntelliChat Pro", a fictional identity-aware enterprise chatbot built on Amazon Bedrock with retrieval-augmented generation (RAG). It is structured as a 4-hour workshop runbook that a team could follow, and models how attackers could target the chatbot's prompts, model, knowledge base and identity layer.

## Roles Modelled
The runbook is written for a cross-functional group: AI engineering, ML engineering, product, DevSecOps, AI security and compliance.

## Scope
Five attack scenarios were scoped: (1) prompt injection using role escalation, (2) poisoning of the fine-tuned model, (3) identity spoofing through AI-generated personas, (4) data exfiltration via crafted prompts, and (5) a supply-chain attack on training datasets. Scenario 1 is written up in full in this repository; Scenarios 2–5 are scoped for future write-up.

## Methodology
Scenarios are mapped to the cyber kill chain, using MITRE ATLAS (adversarial threat techniques for AI systems), MITRE ATT&CK, the OWASP Top 10 for LLM Applications, NIST AI RMF, and STRIDE adapted for AI systems to find control gaps.

## Conclusion
The inherent risk assessment identified 10 AI-specific risks: 2 critical, 5 high and 3 medium. Financial impact figures in the risk assessment are illustrative estimates, not measured values.

## Controls Required

- Regular AI model security audits specifically targeting the IntelliChat Pro system to detect prompt injection vulnerabilities and model drift.
- Patch management for Amazon Bedrock runtime, foundation models, and custom fine-tuned models to ensure protection against known AI vulnerabilities.
- Comprehensive employee training on AI prompt security awareness to educate users about prompt injection risks and social engineering through AI.
- Implementation of AI-specific Web Application Firewall (WAF) with prompt filtering capabilities tailored to the IntelliChat Pro application.
- Deployment of Multi-factor Authentication (MFA) enhanced with AI-based behavioral analysis for identity verification.
- Continuous AI model monitoring to detect adversarial inputs, model drift, and anomalous behavior patterns.
- Implementation of Role-based Access Control (RBAC) with AI context awareness within IntelliChat Pro to limit access to sensitive knowledge bases based on user identity and clearance levels.
- AI prompt sanitization and input validation to prevent injection attacks and malicious prompt manipulation.
- Model provenance tracking and supply chain security for all AI components including foundation models and training datasets.

# AI Threat Modelling Process Summary

```mermaid
mindmap
  root((AI Attack))
    STRIDE/MITRE/OWASP LLM/Kill Chain
      Inherent AI Risk Assessment
      ::icon(fa fa-robot)
      Critical AI Asset List
        Schedule and Scope AI Workshop
    AI Controls Required
      AI Risks<br/>Mitigations
      AI Risk Summary
        AI Remediation workflow
            Slack
            JIRA 
            MLOps Pipeline
    AI Scenarios
      Prompt Injection Attack
      Model Poisoning Attack
      Identity Spoofing Attack
      Data Exfiltration Attack
      Supply Chain Attack