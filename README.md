# Standard Bank - Transaction Core API

High-performance microservice for processing inter-bank transfers with real-time Anti-Fraud and compliance validation. Built following Standard Bank Group architecture patterns.

**Tech Stack:** Java 17, Spring Boot 3, Spring Security, Microservices, API Gateway, MySQL / Oracle, Rate Limiting

**Architecture:**
Client App -> API Gateway (Rate Limiting & Auth) -> Transaction Service -> Core Banking DB (Oracle)
                                           -> Anti-Fraud Service (Pre-Core Validation)
                                           -> KYC Compliance Check

**Key Features:**
- Pre-Core validation to reduce Oracle DB load (cost saving)
- Anti-Fraud rules: suspicious amount > 1M AOA, same account transfer block
- RESTful API: POST /api/transfers, GET /api/accounts/{id}/balance
- Scalable for high-volume transactions

**Why this architecture?**
Standard Bank processes millions of transactions daily. Validating before hitting Core saves resources and prevents fraud early.

**Author:** Almerindo Jamba
BSc Computer Engineering - UCAN (Universidade Católica de Angola) - 4th Year
Luanda, Angola | +244 940 147 778 | github.com/almerindojamba2022-rgb

#standardbank #javadeveloper #angola