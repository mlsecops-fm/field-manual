# MLSecOps Field Manual™ – Concept

## Mission

Build a public, reproducible library of practical MLSecOps modules demonstrating attacks, defenses, monitoring, and secure patterns—grounded in a realistic private lab.

## Three Pillars

**1. Private Lab** - Proxmox cluster where you run attacks, test defenses, observe logs, trigger failure modes

**2. Public Modules** - Small, runnable artifacts (notebooks/markdown) showing 1 attack/defense/pattern each

**3. Patterns Library** - Long-lived reference of secure patterns and anti-patterns

## Publishing Cadence

- Every 2-4 weeks: 1 module
- Every 2-3 months: 1 pattern/anti-pattern page
- Every 6-12 months: Compiled edition

## Scope

- Classic ML threats (evasion, poisoning, extraction)
- Defenses (adversarial training, input sanitization, hardening)
- Monitoring & drift detection
- Secure deployment & lifecycle
- Supply chain safety
- LLM/RAG/Agent security

## Initial Module Roadmap

1. Evasion Attack: Logs + Mitigation (FGSM)
2. Safe Model Loading (Pickle → ONNX → TorchScript)
3. LLM Jailbreak + Logging + Mitigation
4. Retrieval Poisoning (RAG)
5. Embedding Drift Detection
6. Agent Tool Misconfiguration
7. Inference Gateway Hardening
8. Drift + SIEM Integration
9. Anti-Pattern: Unsafe ML Security Practices
