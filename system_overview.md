# System Overview

## System Description
A cloud-based financial services web application that allows customers to authenticate, view account balances, and initiate transactions. Internal staff have elevated access for support and operations.

## High-Level Components
- Web application (customer-facing)
- Authentication service (password + MFA)
- API layer (transaction and account services)
- Database (customer PII + financial data)
- Cloud infrastructure (network segmentation + IAM)
- Logging/monitoring (centralized logs, alerting)
- Third-party services (email delivery, analytics, identity providers)

## Users & Roles
- Customer: account access, transactions
- Support associate: account support, limited admin tools
- Admin: system configuration, privileged access

## Critical Assets
- Customer PII and financial account data
- Authentication systems and MFA
- Transaction engine and API integrity
- Cloud IAM roles and permissions
- Logs and monitoring visibility

