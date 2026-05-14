# SAP CAP OData V4 Services for Cardano & Midnight

---

## Core Technical Principles

- **SAP Cloud Application Programming Model ([CAP](https://cap.cloud.sap/docs/))** as the application framework, providing service definitions, runtime and OData V4 protocol handling out of the box
- **Node.js/TypeScript** for type-safe service implementations, custom handlers and blockchain adapter logic
- **Strict CDS entity modeling** for blockchain objects (Transactions, UTxOs, Addresses, Assets, Metadata)
- **SAP-ready OData V4 endpoints** designed for S/4HANA, RAP and ABAP consumers as well as external interfaces covering both read and write operations
- **Full transaction lifecycle support**: on-chain data retrieval, transaction building, external and HSM-based signing, and submission via typed OData V4 actions
- **Blockchain data providers** integrated through a modular adapter layer (Blockfrost, Koios, Ogmios)
- **Plutus V3 smart contract interaction** through schema-driven, typed contract call definitions
- **Deterministic, schema-driven data contracts** as the single source of truth across ingestion, normalization, signing and OData exposure
- **Layered architecture** with clean separation between data ingestion, transaction building, signing workflows and OData service layer
- **Enterprise security patterns**: HSM integration, external signing delegation, request coalescing and audit-safe key handling


## Repository Structure

### 🔷 [ODATANO](https://github.com/ODATANO/ODATANO) Core OData Service for interacting with the Cardano Blockchain

The main repository. Connects SAP systems or any OData client to the Cardano blockchain via a SAP CAP-based OData V4 API, enabling secure on-chain data access and blockchain transaction execution. Built with SAP CAP and Cardano SDKs, it provides a unified integration layer that brings Cardano into business processes with full enterprise-grade security and auditability.

### 🔗 [TRACE](https://github.com/ODATANO/TRACE) Trusted Records Anchored on Chain for Enterprise

SAP Fiori + CAP application built on top of ODATANO. A dedicated module for anchoring business records on-chain in a tamper-proof, auditable manner. TRACE provides the foundation for traceability, compliance and ESG reporting use cases, where enterprises need verifiable, immutable proof of process steps stored on the Cardano blockchain.

### 📑 [FINCA](https://github.com/ODATANO/FINCA) Anchoring Financial Data on Chain (Cardano Foundation Reeve specification)

SAP Fiori + CAP application built on top of ODATANO. Anchors accounting data and financial reports — Balance Sheets and Income Statements — on Cardano as CIP-10 label-1447 metadata, following the Cardano Foundation Reeve specification. Verifiable accounting without a smart contract: one CIP-30 signature per anchor.

### 💲 [x402](https://github.com/ODATANO/x402) Implements the Cardano-x402-v2 spec, providing gated OData endpoints for agentic payments

Payment-gating library for SAP CAP built on top of ODATANO. Implements the Cardano-x402-v2 spec — gated OData endpoints return HTTP 402 until the caller proves on-chain settlement. Asset-agnostic, no database, no smart contract: replay defense is the Cardano UTxO model itself. Ships with a working example CAP app.

### 🕛 [NIGHTGATE](https://github.com/ODATANO/NIGHTGATE) Privacy Layer (Midnight)

Connects SAP systems to the **Midnight privacy chain** via a CAP-based OData V4 API, enabling confidential on-chain data access and privacy-preserving transaction execution. NIGHTGATE extends ODATANO's architecture into the privacy domain, acting as the gateway between SAP enterprise processes and Midnight's zero-knowledge infrastructure.

### 👁 [ODATANO-WATCH](https://github.com/ODATANO/ODATANO-WATCH) Monitoring & Verification

Provides deterministic monitoring and verification of blockchain-backed business transactions for enterprise systems. ODATANO-WATCH enables SAP environments to track, audit and validate the lifecycle of on-chain operations initiated through ODATANO — closing the loop between transaction submission and enterprise-grade confirmation.

### 🌐 [odatano.dev](https://github.com/ODATANO/odatano.dev) Official Website

The official landing page and documentation site for the ODATANO project, built with Astro. Serves as the public-facing entry point to the ecosystem, providing project context, architecture overviews, milestone updates and integration documentation at [odatano.dev](https://odatano.dev).

---

ODATANO is built with a strong focus on reliability, transparency and enterprise applicability demonstrating how Cardano and Midnight can be cleanly and simple integrated into real enterprise landscapes.
