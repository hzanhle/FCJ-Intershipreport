---
title: "Blog 3"
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---

## Responsible AI in Practice: Data Reply Red Teaming on AWS

**Authors:** Cassandre Vandeputte, Davide Gallitelli, Amine Ait el Harraj  
**Date:** April 29, 2025  
**Topics:** Amazon Bedrock, SageMaker, Responsible AI, Red Teaming

### Why responsible AI
- GenAI introduces risks: hallucinations, unsafe outputs, IP leakage, controllability gaps.  
- Red teaming (adversarial simulation) uncovers vulnerabilities before bad actors exploit them.

### Threats & frameworks
- Model weaknesses + adversarial threats (prompt injection, data poisoning, sensitive info leakage, DoS).  
- Use OWASP Top 10 for LLMs as a reference to prioritize mitigations.

### AWS services for Responsible AI
- **Fairness:** SageMaker Clarify detects bias; SageMaker Data Wrangler rebalances data.  
- **Robustness:** Amazon Bedrock evaluations to test edge prompts and adversarial cases.  
- **Privacy/Security:** Bedrock Guardrails to filter content and protect sensitive data.  
- **Transparency:** LangFuse for audit trails and traceability.

### Data Reply Red Teaming Playground (Architecture)
- Identity: Amazon Cognito (and external IdPs) for secure access.  
- UI: AWS Amplify + React via ALB.  
- Knowledge: Amazon Bedrock Knowledge Bases + S3 + OpenSearch Serverless.  
- Model mgmt: Bedrock Guardrails, SageMaker for evaluation, multi-vendor model registry.  
- Evaluation:  
  - Online: AppSync (WebSocket) for real-time adversarial testing; focuses on OWASP LLM risks.  
  - Offline: SageMaker Clarify (bias), Amazon Comprehend (harmful content), Giskard + LLM-as-a-judge; LangFuse keeps the audit trail.

### Example policy: Answer – Deflect – Safe response
- In sensitive domains (e.g., mental health assistant):  
  - Answer when in scope.  
  - Deflect when out of scope.  
  - Safe response when expert confirmation is needed.

### Takeaways
- Red teaming is continuous; combine governance (policies) with technical controls.  
- Integrate evaluations (online/offline) before production; log everything for accountability.  
- Expand with SageMaker lifecycle tracking or IaC (CloudFormation) for controlled rollout.

### Tags
`Responsible AI` · `Red Teaming` · `Amazon Bedrock` · `Amazon SageMaker` · `Generative AI`

