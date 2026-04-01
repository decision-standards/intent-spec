# Changelog

All notable changes to this project will be documented in this file.

The format is based on Keep a Changelog principles.
This project follows semantic versioning in spirit, with draft-stage pragmatism until 1.0.0.

## [0.2.0] - 2026-04-01

### Added
- Explicit positioning of SIS as the decision contract layer for autonomous systems
- New contract-layer objects:
  - `evaluation`
  - `decision`
  - `execution_binding`
  - `evidence`
- New example payload aligned to the decision-contract model
- New evaluation-oriented OpenAPI surface centered on `/v1/evaluate-intent`
- Status language clarifying that execution is only admissible when:
  - `decision.result = "allow"`
  - `execution_binding.binding_status = "bound"`

### Changed
- Reframed the README from validation/governance language toward decision, execution binding, and system-level coherence
- Shifted the schema narrative from intent-only validation toward intent evaluation and execution admissibility
- Updated artifact naming to v0.2 draft artifacts:
  - `sis-v0.2.schema.json`
  - `sis-v0.2.example.json`
  - `sis-openapi-v0.2.yaml`
- Deprecated `evaluation_hints` in favor of explicit evaluation outputs
- Renamed public API emphasis away from resource lifecycle operations and toward contract evaluation

### Removed
- Implicit assumption that a validated decision is automatically executable
- Primary reliance on CRUD-style intent resource framing as the public standard surface

### Notes
- v0.2.0 is a draft-stage structural shift, not a stability signal
- 1.0.0 is reserved for a stable external contract with supporting reference implementations