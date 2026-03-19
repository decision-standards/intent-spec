# SIS — Standard Intent Specification

A standard for representing and evaluating intent in AI systems before execution.

---

## Overview

SIS (Standard Intent Specification) defines a universal structure for how intent is expressed, evaluated, and executed across AI systems.

As agents begin to take actions — not just generate outputs — the missing piece is not execution infrastructure, but a consistent way to decide:

- what should happen  
- whether it is allowed  
- under what conditions it can proceed  

SIS provides that interface.

It sits between **intent formation** and **execution systems**, enabling consistent decision evaluation across agents, services, and environments.

---

## Why SIS Exists

Today, every system represents intent differently.

- Agents pass loosely structured payloads  
- Control logic is embedded in application code  
- Policies are fragmented across services  
- Decisions are opaque and non-portable  

This creates:

- inconsistent behavior  
- hidden decision logic  
- inability to audit or reproduce outcomes  
- fragile integrations between systems  

SIS standardizes the shape of intent so that decisions can be:

- **evaluated consistently**  
- **enforced deterministically**  
- **observed and explained**  
- **shared across systems**

---

## What SIS Defines

SIS defines a minimal, extensible structure for:

### 1. Intent
What action is being proposed.

### 2. Context
The data and environment surrounding the intent.

### 3. Constraints
Rules, policies, and boundaries applied to the intent.

### 4. Evaluation
The process of determining whether the intent is allowed.

### 5. Decision
The outcome of evaluation:
- approved  
- denied  
- modified  
- escalated  

### 6. Execution Binding
How an approved decision maps to execution systems.

---

## Core Model

```json
{
  "intent": {
    "action": "transfer_funds",
    "actor": "agent:finance",
    "target": "account:external",
    "amount": 5000
  },
  "context": {
    "environment": "production",
    "timestamp": "2026-01-01T12:00:00Z"
  },
  "constraints": [
    {
      "type": "limit",
      "rule": "max_transfer <= 1000"
    }
  ],
  "evaluation": {
    "status": "denied",
    "reason": "Amount exceeds allowed threshold"
  },
  "decision": {
    "result": "denied",
    "explanation": "Transfer amount violates policy"
  }
}
