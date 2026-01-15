# Control Mapping (NIST CSF + CIS)

## Risk-to-Control Map
| Risk ID | Preventive Controls | Detective Controls | Framework Mapping |
|------|----------------------|-------------------|------------------|
| R-01 | Rate limiting, lockout, MFA | Auth anomaly alerts | NIST PR.AC, CIS 6/8 |
| R-02 | MFA required, device trust | New device/IP alerts | NIST PR.AC, CIS 6/8 |
| R-03 | Phishing training, conditional access | Suspicious sign-in alerts | NIST PR.AT, DE.CM |
| R-04 | Secure config policies, encryption | Cloud posture monitoring alerts | NIST PR.DS, DE.CM |
| R-05 | Least privilege, PAM | Privileged activity logging | NIST PR.AC, CIS 5/6/8 |
| R-06 | Centralized logging standards | SIEM detections + alert tuning | NIST DE.CM, RS.AN |
| R-07 | WAF, throttling, authz checks | API abuse detections | NIST PR.AC, DE.CM |
| R-08 | Vendor due diligence, least data sharing | Vendor monitoring + incident clauses | NIST ID.SC |

