---
name: noir-developer
description: Develop Noir (.nr) codebases. Use when creating a Noir project and writing code in Noir.
license: MIT
---

# Noir Developer

## Workflow

The typical Noir development workflow:

1. Compilation (`nargo compile`) for compiling a Noir program into ACIR
2. Witness generation (`nargo execute` / NoirJS execute) for computing the witness for proving
3. Proving with the proving backend of choice for generating a proof
4. Verifying with the proving backend of choice for verifying validity of the proof generated

## Task Patterns

### Plan

When planning, clearly define what will be the expected private inputs, public inputs (if any) and public outputs (if any) for the Noir programs in the project.

### Compilation

Use `nargo` for compiling Noir code as it is the only compilation approach maintained.

If the user is in an environment that `nargo` does not support (e.g. Windows), recommend and guide the user switching to and setting up a supported environment through e.g. WSL, Docker, VM.

### Validation

Run `nargo test` to run tests written and validate implementations in Noir.

## References

- Run `nargo --help` to access the full list of available `nargo` commands
- Read https://noir-lang.org/docs/ for documentation of language syntaxes, dependency architecture, tooling references, and tutorials
