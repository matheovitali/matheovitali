# AIOS — Local-first agent execution system

[Back to profile](../README.md)

**Personal engineering project · In development · Source code private**

## Goal

AIOS explores a local-first system for **supervised AI-assisted tasks**. Its objective is to make agent execution understandable and controllable: the human should be able to define permissions, observe a task's state and distinguish an intended action from an action that was actually executed.

The project is experimental and **is not presented as a production-ready autonomous agent**.

## Technology and architecture

- **Python** for orchestration and runtime-side functionality
- **Rust / Tauri** for desktop integration and a native boundary
- **Vue / TypeScript** for the desktop interface
- **Ollama** for local-model integration
- Automated tests for state transitions, policy behavior and execution boundaries

The design separates four concerns:

1. **Desktop presentation** — shows task information and requests deliberate confirmation.
2. **Core state** — tracks tasks, runs and outcomes.
3. **Policy checks** — govern whether a requested capability is permitted.
4. **Supervised runtime** — performs authorized work and records the result.

These are architectural responsibilities rather than a promise that every subsystem is fully shipped.

## Engineering challenges

**Permission before execution.** A model proposal should not grant itself authority. Execution requires explicit scope and enforceable checks outside the presentation layer.

**Uncertain outcomes.** A timeout or interrupted process does not automatically mean the underlying action failed. Task and run states need to communicate uncertainty rather than report invented success.

**Process supervision.** On Windows, reliably identifying and stopping child processes requires attention to process ownership and lifecycle behavior.

**Local inference.** Ollama integration has been exercised with a real local-model response in development; this is a narrowly scoped proof, **not** a performance or production-readiness claim.

**Testability.** Using controlled test providers and bounded execution allows policy and runtime behavior to be exercised without assuming the model is always available or predictable.

## What this case study demonstrates

- Designing **permission-bounded agent workflows**
- Working across Python, Rust and a TypeScript desktop UI
- Modeling task/run state and evidence of execution
- Applying a test-first approach to safety-sensitive runtime behavior

## Current limits

The system is in active development, with unresolved integration and lifecycle work. Internal tests and reviews are not equivalent to external certification. There is **no public source release or independently reproducible build linked here**.

This page intentionally omits operational security details, unpublished code and machine-specific configuration. An isolated demonstration may be published after a dedicated release and security review.
