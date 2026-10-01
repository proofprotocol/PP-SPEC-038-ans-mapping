# PP-SPEC-038: Proof of Efficacy Mapping to Agent Name Service (ANS)

**Status:** DRAFT v0.1  
**Author:** Craig Ellrod / Nebulonium, Inc. / HACKERverse®  
**License:** CC BY 4.0

**Normative specification:** [`PP-SPEC-038-Agent-Name-Service-ANS-Mapping.md`](./PP-SPEC-038-Agent-Name-Service-ANS-Mapping.md)

## Purpose

This repository defines a Proof Protocol mapping between Agent Name Service (ANS) and Proof Protocol evidence, efficacy, and proof semantics.

ANS is treated as a pluggable source of agent identity, naming, discovery, and resolution context. Proof Protocol remains framework-agnostic and independently establishes whether a selected control or identity-related claim performed as asserted.

## Repository contents

- `PP-SPEC-038-Agent-Name-Service-ANS-Mapping.md` — normative mapping specification
- `README.md` — repository overview
- `LICENSE` — license for original Proof Protocol material
- `CONTRIBUTING.md` — contribution guidance
- `CITATION.cff` — citation metadata

## Architectural principle

> **Threat frameworks are pluggable inputs to Proof Protocol. Proof Protocol is framework-agnostic.**

External frameworks and protocols can identify what should be tested. Proof Protocol independently establishes whether the control worked and what evidence proves the result.

## Ownership and external-framework notice

The Proof Protocol mapping is independently authored. ANS names, identifiers, specifications, implementations, and other upstream intellectual property remain with their respective owners. Mapping establishes interoperability, not dependency, endorsement, or transfer of ownership.
