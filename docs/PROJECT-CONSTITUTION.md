# Project Constitution

## 1. Purpose

Global Marketplace is a modular commerce platform designed to support an Amazon-class reference marketplace and reusable technology modules that can be deployed into a customer's own cloud environment.

## 2. Owner and learning principle

The owner will ultimately operate and maintain the system. Every important technical decision must therefore be explainable in plain language and teachable from first principles.

We will not use unexplained "AI magic" for important behavior.

## 3. Build principle

A feature is not complete merely because its screen works. A production feature requires:

- user experience
- API/business logic
- data model
- authorization
- validation and error handling
- tests
- documentation
- observability
- deployment path
- recovery/reconciliation where relevant

## 4. Backend authority

Transactional backend logic is authoritative for money, orders, inventory, permissions, security, and other business state.

AI may recommend, classify, summarize, or assist. AI must not silently become the source of truth for critical state.

## 5. Modular architecture

Modules must have clear contracts and should be usable independently where commercially and technically appropriate.

Catalog, search, payments, inventory, commerce, integration, and other capabilities must not become one inseparable application.

## 6. Customer-cloud principle

The target deployment model is:

> Your infrastructure. Your data. Your database. Our technology.

Customer data remains under the customer's control. Integrations must support secure adapters and least-privilege access.

## 7. Documentation

Documentation is part of the product. Important code must contain useful explanatory comments. Important flows must have Markdown documentation. Architectural decisions must be recorded.

## 8. CI/CD

GitHub Actions CI must remain green. We will diagnose failures before rerunning workflows and keep CI economical. Tests and quality gates must never be bypassed merely to obtain a green result.

## 9. Security

Security is designed in from the beginning: least privilege, secret management, dependency review, vulnerability scanning, auditability, safe defaults, and secure CI workflows.

## 10. Simplicity

We choose the simplest architecture that can satisfy the real requirement and grow safely. Complexity must have a reason.

## 11. Teaching rule

When a new technology is introduced, we will document:

1. what it is
2. why we need it
3. how it works
4. where it appears in the repository
5. how to test it
6. how to operate it
7. what can go wrong

