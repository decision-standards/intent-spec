# SIS v0.2.0 Release Notes

## Summary

SIS v0.2.0 is the first meaningful alignment release for the standard.

This release reframes SIS from an intent validation artifact into a clearer decision contract for autonomous systems. The core shift is simple:

**a valid decision is not the same thing as an executable decision**

SIS now models that distinction explicitly.

## What Changed

### 1. SIS is now positioned as the interface between decision and execution
The README and supporting artifacts now describe SIS as the decision contract layer for autonomous systems, rather than narrowly as a validation or governance mechanism.

### 2. The schema now reflects the actual contract
The spec now includes explicit structures for:

- `evaluation`
- `decision`
- `execution_binding`
- `evidence`

This makes the contract more complete and more defensible.

### 3. Execution binding is now first-class
This is the most important change in v0.2.0.

A decision alone does not imply execution permission. Execution is only admissible when:

- `decision.result = "allow"`
- `execution_binding.binding_status = "bound"`

That distinction is now part of the standard.

### 4. The API surface now reflects evaluation semantics
The reference API has been shifted toward evaluating SIS objects and returning decision-contract outputs, rather than focusing primarily on intent resource lifecycle operations.

## Why This Matters

Most AI and multi-agent failures do not happen because a model generated an obviously invalid decision.

They happen because the system moved from decision to action without a strong enough contract in between.

SIS exists to standardize that missing layer.

v0.2.0 is the first version that states that clearly across the README, schema, example payload, and API structure.

## Draft Status

v0.2.0 is still a draft release.

It should be treated as:

- structurally meaningful
- directionally stable
- still open to refinement before 1.0.0

This is not the final contract. It is the first aligned one.

## Artifact Set

This release uses:

- `sis-v0.2.schema.json`
- `sis-v0.2.example.json`
- `sis-openapi-v0.2.yaml`

## What Comes Next

Likely focus areas after v0.2.0:

- tighter field semantics
- extension guidance
- reference implementation behavior
- MCP packaging for adoption
- example use cases across multiple domains
- release discipline toward a stable 1.0.0 boundary

## Closing

SIS is not a model.
It is not a dashboard.
It is not just policy validation.

SIS defines the contract that makes autonomous execution explicit, constrained, and defensible.