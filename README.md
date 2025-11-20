# ODATANO  
### SAP–Cardano OData V4 API Architecture by Maximilian Weber  
**Funded through Project Catalyst (https://projectcatalyst.io/funds/14/cardano-open-developers/sap-cardano-odata-v4-api-with-cap-and-sap-cardano-sdk)**

**ODATANO** is a technical engineering initiative by **Maximilian Weber**, funded through **Project Catalyst**, focused on creating a production-grade **OData V4 API layer** that connects SAP enterprise systems with the Cardano blockchain.

The project aims to provide a clean, typed, and extensible foundation for enterprise integrations by leveraging the **SAP Cloud Application Programming Model (CAP)** and modern Cardano tooling.

## Core Technical Principles

- **CAP Node.js/TypeScript architecture** as the backbone for all OData services  
- **Strict CDS entity modelling** for blockchain objects (Transactions, UTxOs, Addresses, Assets, Metadata)  
- **SAP-ready OData V4 endpoints** designed for S/4HANA, RAP, ABAP consumers and external interfaces  
- **Blockchain data providers** integrated through a modular adapter layer (Blockfrost, Koios)  
- **Deterministic, schema-driven data contracts** enabling automation, analytics, reporting and workflows  
- **Layered architecture** supporting strong separation between data ingestion, normalization and OData exposure  

## Project Scope

ODATANO establishes a unified integration layer that enables SAP systems to:

- Retrieve on-chain data in a consistent, typed, and SAP-native format  
- Use blockchain information in ERP processes (logistics, finance, supply chain, ESG, automation)  
- Build custom SAP applications on top of Cardano data using standard OData semantics  
- Leverage standardized interfaces instead of custom REST or proprietary blockchain SDKs  
- Align blockchain interactions with enterprise governance, compliance and auditability

## Long-Term Vision

ODATANO is designed as the foundation for a broader **SAP ↔ Cardano Gateway**, enabling:

- On-chain supply chain visibility  
- Tokenized asset management  
- Automated, rule-driven payments  
- ESG and traceability data integration  
- DeFi-inspired enterprise tooling  
- Secure off-chain signing modules for SAP environments  
- End-to-end orchestration of blockchain operations in SAP processes

## Repository Structure

This GitHub organization hosts all components required for the project, including:

- Core OData service implementation (CAP)  
- Blockchain integration modules  
- Data normalization & contract definitions  
- Documentation, specifications and architecture artifacts  
- Future modules for transaction creation, signing, and SAP process extensions  

ODATANO is built with a strong focus on reliability, transparency and enterprise applicability — demonstrating how Cardano can be cleanly integrated into real SAP landscapes.
