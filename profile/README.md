# SAP–Cardano OData V4 API Architecture by Maximilian Weber

**Funded through Project Catalyst**
[projectcatalyst.io/funds/14/cardano-open-developers/sap-cardano-odata-v4-api-with-cap-and-sap-cardano-sdk](https://projectcatalyst.io/funds/14/cardano-open-developers/sap-cardano-odata-v4-api-with-cap-and-sap-cardano-sdk)

**ODATANO** is a technical engineering initiative by **Maximilian Weber**, funded through **Project Catalyst**, focused on creating a production-grade **OData V4 API layer** that connects SAP enterprise systems with the Cardano blockchain.

The project aims to provide a clean, typed, and extensible foundation for enterprise integrations by leveraging the **SAP Cloud Application Programming Model (CAP)** and modern Cardano tooling.

---

## Core Technical Principles

- **CAP Node.js/TypeScript architecture** as the backbone for all OData services
- **Strict CDS entity modelling** for blockchain objects (Transactions, UTxOs, Addresses, Assets, Metadata)
- **SAP-ready OData V4 endpoints** designed for S/4HANA, RAP, ABAP consumers and external interfaces
- **Blockchain data providers** integrated through a modular adapter layer (Blockfrost, Koios)
- **Deterministic, schema-driven data contracts** enabling automation, analytics, reporting and workflows
- **Layered architecture** supporting strong separation between data ingestion, normalization and OData exposure

---

## Project Scope

ODATANO establishes a unified integration layer that enables SAP systems to:

- Retrieve on-chain data in a consistent, typed, and SAP-native format
- Use blockchain information in ERP processes (logistics, finance, supply chain, ESG, automation)
- Build custom SAP applications on top of Cardano data using standard OData semantics
- Leverage standardized interfaces instead of custom REST or proprietary blockchain SDKs
- Align blockchain interactions with enterprise governance, compliance and auditability

---

## Long-Term Vision

ODATANO is designed as the foundation for a broader **SAP ↔ Cardano Gateway**, enabling:

- On-chain supply chain visibility
- Tokenized asset management
- Automated, rule-driven payments
- ESG and traceability data integrations
- Secure off-chain signing modules for SAP environments
- End-to-end orchestration of blockchain operations in SAP processes

---

## Repository Structure

The [ODATANO GitHub Organization](https://github.com/ODATANO) hosts all components required for the project:

### 🔷 [ODATANO](https://github.com/ODATANO/ODATANO) — Core OData Service (CAP)

The main repository. Connects SAP systems to the Cardano blockchain via a CAP-based OData V4 API, enabling secure on-chain data access and blockchain transaction execution. Built with SAP CAP and Cardano SDKs, it provides a unified integration layer that brings Cardano into SAP processes with full enterprise-grade security and auditability.

### 🌑 [NIGHTGATE](https://github.com/ODATANO/NIGHTGATE) — Privacy Layer (Midnight)

Connects SAP systems to the **Midnight privacy chain** via a CAP-based OData V4 API, enabling confidential on-chain data access and privacy-preserving transaction execution. NIGHTGATE extends ODATANO's architecture into the privacy domain, acting as the gateway between SAP enterprise processes and Midnight's zero-knowledge infrastructure.

### 👁 [ODATANO-WATCH](https://github.com/ODATANO/ODATANO-WATCH) — Monitoring & Verification

Provides deterministic monitoring and verification of blockchain-backed business transactions for enterprise systems. ODATANO-WATCH enables SAP environments to track, audit and validate the lifecycle of on-chain operations initiated through ODATANO — closing the loop between transaction submission and enterprise-grade confirmation.

### 🔗 [TRACE](https://github.com/ODATANO/TRACE) — Trusted Records Anchored on Chain for Enterprise

A dedicated module for anchoring business records on-chain in a tamper-proof, auditable manner. TRACE provides the foundation for traceability, compliance and ESG reporting use cases, where enterprises need verifiable, immutable proof of process steps stored on the Cardano blockchain.

### 🌐 [odatano.dev](https://github.com/ODATANO/odatano.dev) — Official Website

The official landing page and documentation site for the ODATANO project, built with Astro. Serves as the public-facing entry point to the ecosystem, providing project context, architecture overviews, milestone updates and integration documentation at [odatano.dev](https://odatano.dev).

---

ODATANO is built with a strong focus on reliability, transparency and enterprise applicability — demonstrating how Cardano can be cleanly integrated into real SAP landscapes.
