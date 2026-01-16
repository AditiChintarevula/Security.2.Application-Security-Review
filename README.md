# 🔐 Application Security Review (CIMS)
# 📌 Overview

This project presents a detailed application security review of a Customer Information Management System (CIMS) designed to manage customer profiles, billing data, and internal CRM operations. The goal of the assessment was to identify security risks affecting sensitive customer and payment information and propose industry-aligned remediation strategies.

# 🎯 Objectives

Identify critical security vulnerabilities in application design and deployment

Evaluate compliance gaps against PCI DSS and SOX standards

Propose secure, scalable, and business-compatible remediation controls

# 🧩 Key Findings

Storage of cardholder data (including CVV) without encryption

SQL Injection vulnerability in customer update functionality

Public exposure of PostgreSQL database port (5432)

Hardcoded database credentials in application code

# ⚠️ Risk Summary
Risk-->	Severity
Unencrypted cardholder data -->	Critical
SQL Injection -->	Critical
Exposed database port	--> High
Hardcoded credentials	--> High
# 🛠️ Recommended Mitigations

Eliminate CVV storage and implement payment tokenization

Enable encryption at rest and in transit

Replace raw SQL queries with parameterized queries

Introduce a Web Application Firewall (WAF)

Store secrets using a secure secrets manager (e.g., AWS Secrets Manager)

Enforce network segmentation and least-privilege access

# 🏗️ Architecture Improvements

The proposed architecture introduces:

Secure API-based database access

Tokenized payment processing

Encrypted storage with external key management

Private subnet–isolated databases

# 📚 Standards & Frameworks

PCI DSS

SOX

OWASP Top 10

# 🧠 Key Takeaways

This project demonstrates practical application security assessment skills, secure architecture design, and compliance-driven risk mitigation.
