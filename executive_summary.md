# Executive Summary

## Scope
This assessment reviews cyber risk for a cloud-based financial services web application supporting customer login, account access, and transactions. The assessment focuses on key assets (PII, authentication, transaction integrity), likely threat scenarios (credential attacks, phishing, cloud misconfiguration), and control recommendations mapped to NIST CSF and CIS Controls.

## Top Risks Identified
1) Credential stuffing leading to account takeover (R-01, Score 20)  
2) Optional MFA enabling account takeover (R-02, Score 20)  
3) Logging and monitoring gaps reducing detection and response capability (R-06, Score 16)

## Recommended Priorities (Next 30–60 Days)
- Enforce MFA for customers and privileged users; introduce device/IP risk checks.
- Implement rate limiting, lockout policies, and tuned SIEM detections for auth abuse.
- Establish centralized logging standards across authentication and API layers, with alerting use cases aligned to high-risk scenarios.

## Expected Risk Reduction
These changes reduce the likelihood of account takeover, improve detection speed, and increase operational resilience while supporting compliance expectations for regulated financial environments.
