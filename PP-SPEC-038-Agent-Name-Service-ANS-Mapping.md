# PP-SPEC-038: Proof of Efficacy Mapping to Agent Name Service (ANS)

| Field | Value |
|---|---|
| Status | DRAFT v0.1 |
| Author | Craig Ellrod, Nebulonium, Inc. (dba HACKERverse®) |
| Date | October 1, 2026 |
| License | CC BY 4.0 |
| Maps to | Agent Name Service (ANS) |
| Series | Proof Protocol Framework Mapping Specifications |

---

## 1. Purpose

This specification defines how Agent Name Service (ANS) identity, naming, discovery, and resolution claims can be bound to Proof Protocol test cases, evidence, and efficacy results.

The referenced external work remains authoritative for its own terminology, identifiers, requirements, and architecture. This document defines a **Proof Protocol mapping** and does not supersede or modify ANS.

## 2. Scope

ANS supplies agent identity and resolution context that can inform what identity-related conditions should be exercised. Proof Protocol supplies an independent evidence model for testing whether selected identity, resolution, authorization, or downstream control claims hold under defined conditions.

Independent witnessing and evidence-capture implementation are defined elsewhere in the Proof Protocol specification family.

## 3. Core Question

Proof of efficacy asks:

> **Was there a control, and did it work?**

For agent naming and identity systems, a successful lookup, identifier, or resolution event is evidence of a mechanism operating. It is not by itself proof that an identity-dependent security control protected a downstream action or target.

## 4. Metric Definitions

Against a defined adversarial corpus, each case is recorded as **blocked**, **detected**, **missed**, or **INVALID**.

Relevant measurements include:

- containment rate;
- detection rate;
- miss rate;
- false-positive rate against paired benign identity/resolution cases;
- robustness against spoofing, impersonation, stale or manipulated records, resolution substitution, replay, or bypass;
- version-level results; and
- INVALID status when required evidence is incomplete or broken.

Target levels are defined by the engagement and risk context rather than by this mapping.

## 5. Evidence Produced

Mapped tests can produce:

- **Proof records** binding identity/resolution context, control, test case, system/version, verdict, timestamp, and evidence references;
- **ProofStamp™** trusted timestamps bound to evidence/verdict objects;
- **ProofBundle™** packages containing proof records, metrics, corpus manifests, and environment/context;
- **ProofRegister™** records for issued proof artifacts; and
- corpus and environment manifests identifying the tested identity and resolution conditions.

## 6. Mapping to Agent Name Service (ANS)

| ANS context | Proof Protocol treatment | Evidence |
|---|---|---|
| Agent identifier/name | Bind the asserted identity to the test case and observed interaction. | Proof record; identity evidence |
| Registration claim | Test conditions involving valid, invalid, conflicting, or manipulated registration where applicable. | Execution evidence; verdict |
| Resolution result | Record what identity or endpoint was resolved and test security-relevant consequences. | Resolution evidence; proof record |
| Discovery mechanism | Exercise benign and adversarial discovery conditions. | Corpus manifest; robustness evidence |
| Identity binding | Test whether asserted bindings survive impersonation, substitution, replay, or stale-data conditions. | Efficacy result |
| Trust/verification assertion | Record the assertion separately from observed downstream behavior. | Control descriptor; proof record |
| Protected downstream action | Obtain target/application/tool evidence when required to establish whether the identity-dependent control actually constrained the action. | Outcome evidence |
| Version/environment context | Bind material ANS, agent, policy, and system versions to the result. | Environment descriptor |

## 7. Interoperability Rules

1. The ANS version/revision and relevant identifier SHOULD be recorded when available.
2. Upstream ANS identifiers and terminology MUST NOT be silently redefined.
3. Successful identity resolution does not by itself establish the efficacy of a downstream control.
4. Where efficacy depends on a protected downstream outcome, target, application, tool, SIEM, vendor, or equivalent evidence SHOULD complete the evidence round trip.
5. Missing required evidence MUST yield **INVALID**, not PASS.
6. Material changes to identity records, resolution behavior, agent implementation, policy, system version, environment, or corpus SHOULD trigger retesting where they can affect the result.

## 8. Framework-Agnostic Architecture

> **Threat frameworks are pluggable inputs to Proof Protocol. Proof Protocol is framework-agnostic.**

External frameworks and protocols can identify **what to test**: threats, vulnerabilities, controls, design assertions, identity claims, permissions, names, resolution behavior, or risk conditions. Proof Protocol independently establishes **whether the control worked and what evidence proves that result**.

No external framework or protocol is required for Proof Protocol to operate. A Proof Protocol implementation MAY use ANS, A2AS BASIC, MAESTRO, MITRE ATLAS, OWASP, AIVSS, a proprietary identity model, another recognized framework, or no external framework at all when the test condition is otherwise sufficiently defined.

Adding, replacing, muting, or removing a framework mapping does not alter the Proof Protocol architecture, evidence model, Proof of Efficacy determination, ProofBundle™, ProofStamp™, ProofRegister™, or independent corroboration requirements.

A mapping therefore establishes **interoperability**, not architectural dependency.

## 9. Relationship to Proof Protocol

This mapping is part of the Proof Protocol specification family maintained by Nebulonium, Inc.

The relationship is intentionally asymmetric:

> **ANS supplies agent identity, naming, discovery, and resolution context. Proof Protocol supplies the evidence model for determining whether a selected control or claim performed as asserted.**

No affiliation, endorsement, certification, or sponsorship by ANS's maintainers is implied.

## 10. Source Framework, Attribution, and License

Agent Name Service (ANS) is external work. Its names, specifications, implementations, and expressive materials retain their original ownership and licensing.

The ANS paper associated with this mapping has been reported as distributed under **CC BY 4.0**; code or other implementation artifacts may carry separate licenses and SHOULD be checked at their authoritative source before reuse.

This Proof Protocol mapping is independently authored and licensed under **CC BY 4.0**. Upstream material is referenced for interoperability and is not relicensed by this specification.

## 11. Versioning

This mapping is versioned independently of ANS. Material upstream changes SHOULD trigger a mapping review and, where necessary, a new version identifying the upstream revision mapped.

---

*Proof Protocol · proofprotocol.io · CC BY 4.0*
