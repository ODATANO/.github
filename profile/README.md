# SAP CAP OData V4 Services and Applications for Cardano & Midnight

---

## Core Technical Principles

- **SAP Cloud Application Programming Model ([CAP](https://cap.cloud.sap/docs/))** as the application framework, providing service definitions, runtime, and OData V4 protocol handling out of the box
- **Node.js/TypeScript** for type-safe service implementations, custom handlers, and blockchain adapter logic
- **Strict CDS entity modeling** for blockchain objects (Transactions, UTxOs, Addresses, Assets, Metadata)
- **SAP-ready OData V4 endpoints** designed for S/4HANA, RAP, and ABAP consumers as well as external interfaces covering both read and write operations
- **Full transaction lifecycle support**: on-chain data retrieval, transaction building, external and HSM-based signing, and submission via typed OData V4 actions
- **Blockchain data providers** integrated through a modular adapter layer (Blockfrost, Koios, Ogmios)
- **Plutus V3 smart contract interaction** through schema-driven, typed contract call definitions
- **Deterministic, schema-driven data contracts** as the single source of truth across ingestion, normalization, signing, and OData exposure
- **Layered architecture** with clean separation between data ingestion, transaction building, signing workflows, and OData service layer
- **Enterprise security patterns**: HSM integration, external signing delegation, request coalescing, and audit-safe key handling


# Repository Structure

## Core Services

### 🔷 [ODATANO](https://github.com/ODATANO/ODATANO) Core OData Service for interacting with the Cardano Blockchain

The main repository. Connects SAP systems or any OData client to the Cardano blockchain via a SAP CAP-based OData V4 API, enabling secure on-chain data access and blockchain transaction execution. Built with SAP CAP and Cardano SDKs, it provides a unified integration layer that brings Cardano into business processes with full enterprise-grade security and auditability.

### 🕛 [NIGHTGATE](https://github.com/ODATANO/NIGHTGATE) Privacy Layer (Midnight)

Connects SAP systems to the **Midnight privacy chain** via a CAP-based OData V4 API, enabling confidential on-chain data access and privacy-preserving transaction execution. NIGHTGATE extends ODATANO's architecture into the privacy domain, acting as the gateway between SAP enterprise processes and Midnight's zero-knowledge infrastructure.

## Specific Use Case Implementations

### 🔗 [TRACE](https://github.com/ODATANO/TRACE) Trusted Records Anchored on Chain for Enterprise

SAP Fiori + CAP application built on top of ODATANO. A dedicated module for anchoring business records on-chain in a tamper-proof, auditable manner. TRACE provides the foundation for traceability, compliance, and ESG reporting use cases, where enterprises need verifiable, immutable proof of process steps stored on the Cardano blockchain.

### 📑 [FINCA](https://github.com/ODATANO/FINCA) Anchoring Financial Data on Chain (Cardano Foundation Reeve specification)

SAP Fiori + CAP application built on top of ODATANO. Anchors accounting data and financial reports — Balance Sheets and Income Statements — on Cardano as CIP-10 label-1447 metadata, following the Cardano Foundation Reeve specification. Verifiable accounting without a smart contract: one CIP-30 signature per anchor.

### 💲[x402](https://github.com/ODATANO/x402) Implements the Cardano-x402-v2 spec, providing gated OData endpoints for agentic payments

Payment-gating library for SAP CAP built on top of ODATANO. Implements the Cardano-x402-v2 spec. Gated OData endpoints return HTTP 402 until the caller proves on-chain settlement. Asset-agnostic, no database, no smart contract: replay defense is the Cardano UTxO model itself. Ships with a working example CAP app.

### 🚚 [QUANTIX](https://github.com/ODATANO/QUANTIX) Delivery commitments that enforce themselves on-chain

SAP Fiori + CAP application with multi-feed Charli3 pull-oracle built on top of ODATANO. Enables atomic on-chain B2B procurement orders by bundling multiple price feeds into a single transaction. Dual coordinators with disjoint UTxO sets eliminate refresh congestion. Settlement and price proof are combined into a single atomic Cardano transaction. Grand Prize winner at Charli3 Hackathon 2026.

### 📝 [DAYPASS](https://github.com/ODATANO/DAYPASS) EU battery passport (Reg. 2023/1542) on Cardano

EU battery passport (Reg. 2023/1542) on Cardano: CIP-25 NFT anchors, AES-encrypted tiers, Merkle-field disclosure, and on-chain Groth16 ZK predicates. SAP CAP app on @odatano/core, with Catena-X PAC export like NIGHTPASS

### 🔋 [NIGHTPASS](https://github.com/ODATANO/NIGHTPASS) EU battery passport (Reg. 2023/1542) on Midnight

NIGHTPASS lets battery manufacturers prove EU Battery Passport compliance without disclosing the confidential supply-chain, material, and carbon-footprint data behind it. Built on Midnight's zero-knowledge infrastructure and exposed through a CAP-based OData V4 API, NIGHTPASS turns regulatory disclosure into verifiable proof

---

ODATANO is built with a strong focus on reliability, transparency, and enterprise applicability, demonstrating how Cardano and Midnight can be cleanly and simply integrated into real enterprise landscapes.
