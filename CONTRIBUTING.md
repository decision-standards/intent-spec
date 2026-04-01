# Contributing to SIS

Thank you for contributing to SIS.

SIS is the decision contract layer for autonomous systems. The goal of this repository is to define a clear, implementation-neutral standard for expressing intent, evaluating admissibility, and binding execution conditions before action.

## What We Welcome

We welcome contributions that improve:

- schema clarity
- terminology consistency
- evaluation semantics
- execution binding semantics
- evidence and traceability patterns
- interoperability guidance
- real-world examples
- implementation-neutral documentation

## What Good Contributions Look Like

A strong contribution does one or more of the following:

- makes the core contract easier to understand
- reduces ambiguity in field meaning
- improves consistency across README, schema, examples, and API docs
- strengthens interoperability without overfitting to one product or vendor
- preserves the distinction between:
  - intent
  - evaluation
  - decision
  - execution binding
  - evidence

## What To Avoid

Please avoid contributions that:

- turn SIS into a vendor-specific product interface
- collapse decision and execution into the same concept
- over-engineer v0.2 with premature edge-case complexity
- introduce domain-specific assumptions into the core spec
- reframe SIS as only a governance, audit, or policy tool

SIS is broader than policy validation. It defines the contract between decision and execution.

## Contribution Principles

### 1. Execution-bound semantics
A decision is not executable unless execution binding is explicit.

### 2. Explicit structure over implied behavior
Fields should represent meaning directly. Hidden assumptions should be avoided.

### 3. Deterministic interpretation
The same payload should support the same interpretation across implementations.

### 4. Implementation neutrality
The standard should remain usable across industries, runtimes, and orchestration patterns.

### 5. Minimal viable standard
Add only what materially improves the contract. Keep the core small and defensible.

## How To Contribute

1. Fork the repository
2. Create a branch for your change
3. Make the change
4. Update related documentation if needed
5. Submit a pull request

## Pull Request Expectations

Please include:

- a clear summary of the change
- why the change improves SIS
- whether the change is breaking or non-breaking
- any README, schema, example, or OpenAPI updates required to keep the repo aligned

If your change affects semantics, include a short before/after explanation.

## Versioning Guidance

SIS is currently in draft status.

Use the following rule of thumb:

- patch version for wording, docs, and non-breaking cleanup
- minor version for structural or semantic additions
- major version only when the public contract is stable and intentionally broken

## Areas Needing Help

Contributors may find the most leverage in:

- clearer field descriptions
- more rigorous examples
- extension guidance
- response semantics
- schema/OpenAPI alignment
- reference implementation patterns
- MCP packaging guidance

## Code of Interpretation

When there is ambiguity, prefer the interpretation that preserves SIS as:

**the standard interface between decision and execution**

## Questions

If a proposed change materially alters the meaning of the contract, open an issue first before implementing a large PR.