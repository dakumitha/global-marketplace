# Architecture

## Architectural goal

Build a reusable commerce technology platform first, and use the same platform to assemble a mature Amazon-class marketplace.

## Four layers

### Applications

The twelve stakeholder applications provide user experiences:

- Customer Web
- Customer Mobile
- Seller Web
- Seller Mobile
- Delivery
- Warehouse
- Logistics Control
- Support
- Admin
- Finance
- Developer Portal
- Platform Operations

### Modules

Business capabilities such as:

- Identity
- Catalog
- Search
- Pricing
- Commerce
- Payments
- Inventory
- Logistics
- Returns
- Reviews
- Notifications
- Fraud
- Analytics
- AI

### Platform

Shared capabilities such as:

- Universal Integration Layer
- tenancy
- authorization
- events
- audit
- configuration
- feature flags
- observability

### Infrastructure

The deployment and runtime foundation:

- containers
- Kubernetes-compatible deployment
- infrastructure as code
- environments
- CI/CD
- monitoring
- backups and recovery

## Catalog architecture

Catalog structure must not depend on endlessly nested source-code folders.

We will use:

- taxonomy for category hierarchy
- product types for kinds of products
- attribute definitions for reusable fields
- attribute sets for groups of fields
- variants for purchasable variations
- collections for curated groupings

Example:

Movie -> Entertainment -> Movies -> Action

and:

T-Shirt -> Merchandise -> Clothing -> T-Shirts

are taxonomy paths, not separate application implementations.

A movie can have attributes such as director and runtime, while a T-shirt can have size and material. The same catalog engine handles both through configurable product types and attributes.

## Source of truth

Transactional systems remain authoritative. Search indexes, caches, analytics stores, and AI indexes are derived representations and must be repairable through synchronization/reconciliation.

