---
title: "Blog 1"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---


## Getting Started with Amazon CloudWatch Investigations

**Author:** Andres Silva  
**Date:** December 21, 2024  
**Topics:** Amazon CloudWatch, AWS CloudTrail, AWS Systems Manager

### Overview
How to set up and run your first investigation with the AI-assisted Amazon CloudWatch Investigations feature, including access control, encryption, and integrations.

### What CloudWatch Investigations Does
- Uses generative AI to correlate metrics, logs, traces, deploy events, and more.  
- Produces root-cause hypotheses and actionable insights to speed up incident response.

### Quick Start
1) Open CloudWatch console → AI Operations → Investigations → Configure for this account (IAM principal with `AIOpsConsoleAdminPolicy` or equivalent).  
2) Choose retention (default 90 days) and optional customer-managed KMS key.  
3) Review IAM access presets: Admin (`AIOpsConsoleAdminPolicy`), Operator (`AIOpsOperatorAccess`), Read-only (`AIOpsReadOnlyAccess`).  
4) (Optional) Connect to IAM Identity Center to assign suggestions to users.  
5) In Investigation configuration, let AWS auto-create the IAM role to read telemetry.  
6) Enhanced integration options:  
   - Tags for application boundary detection (narrow search space)  
   - CloudTrail for change event detection  
   - X-Ray and Application Signals for topology and health context  
7) (Optional) Third-party chat/SNS integrations.  
8) Complete setup and start the first investigation session.

### Next Steps & Hardening
- Run a trial investigation to validate access and data coverage.  
- Tune IAM roles/policies; prefer customer-managed KMS keys if required.  
- Add CloudTrail, X-Ray, App Signals to enrich hypotheses.  
- Keep incident-response posture strong while leveraging AI-driven triage.

### Tags
`Amazon CloudWatch` · `AWS CloudTrail` · `AWS Systems Manager` · `Cloud Operations` · `Monitoring`
- Analyzes the code.  
- Provides **a suggested diff update**.  
- Introduces **a new constructor using an `IOrderRepository` interface**, enabling easy mock injection in tests.  

I simply click **Accept Changes**, and everything updates cleanly and instantly.

---

## Example 2: Improving Performance

While working on the `Order` class, I noticed that the `containsItem` method was slow when handling large product lists.  

I selected the method and asked:  
> “This code runs slowly, please optimize it.”

Amazon Q Developer quickly:
- Analyzed the method (which used a traditional for-loop).  
- Suggested **using Java Streams** with `anyMatch()` instead.  
- Displayed a clear **diff view** highlighting the improvement.  

The result:
- **Significant performance boost**
- **Cleaner, more maintainable code**

---

## Conclusion

The integration of **Amazon Q Developer into Eclipse IDE (Preview)** has:

- **Enhanced Java development productivity**  
- **Accelerated learning and optimization**  
- **Unified interaction, learning, and code editing within the same environment**

In particular, the new **inline chat feature** enables developers to **interact directly with AI** without breaking their workflow.  

 If you’re an **Eclipse user**, I highly recommend **installing the Amazon Q Developer plugin today** to experience the difference yourself.

---
