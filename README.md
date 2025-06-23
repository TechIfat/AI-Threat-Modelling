# AI-Threat-Modelling
# AI Threat Modelling Workshop Summary

## Introduction
A 4 Hour AI threat modelling workshop took place to detail the runbook scenario of multiple AI attacks against the identity-aware chatbot system "IntelliChat Pro" built on Amazon Bedrock.

## Attendees
AI Engineering team, ML Engineers, Product Managers, DevSecOps Team, AI Security Specialists, and Compliance Officers.

## Scope
5 Scenarios were run covering: (1) Prompt Injection attack utilizing role escalation, (2) Model Poisoning attack against the fine-tuned model, (3) Identity Spoofing through AI-generated personas, (4) Data Exfiltration via crafted prompts, and (5) Supply Chain attack on training datasets.

## Methodology
All scenarios were run against the AI cyber attack killchain, utilizing the MITRE ATT&CK for AI methods, OWASP LLM Top 10, NIST AI RMF, and STRIDE adapted for AI systems for control gap assessments. Culminating in identified AI-specific risks.

## Conclusion
A total of 6 high risks and 4 medium risks were found during the AI threat modelling workshop.

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