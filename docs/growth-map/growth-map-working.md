
---
MLSecOps Field Manual – Growth Map (Working Document)

A living index that tracks what you learn, where it belongs, and how it evolves into a chapter.

---
1. Orientation

What to capture as you go:
Moments where ML security felt “different” in a tactile way.
Examples you’ll naturally write down:
• First time you saw ML behave non-deterministically and realized threat modeling had to adapt
• When agent behavior surprised you
• When inference deviated from training expectations

Destination: Chapter 1


---

2. Operating Environment

What to capture:
Every topology decision, pain point, and network/VM reality in your lab.
Examples:
• “Why ZFS snapshots saved me from poisoning my dataset.”
• “GPU contention under mixed loads—what I didn’t expect.”
• “VLAN segmentation that worked.”

Destination: Chapter 2


---

3. ML System Anatomy

What to capture:
The diagrams you draw to understand pipelines and RAG flows.
Examples:
• Your training → registry → inference pipeline
• Mapping trust boundaries between steps
• What broke the first time you wired your RAG system

Destination: Chapter 3


---

4. Threat Modeling

What to capture:
Every “attack-like” behavior you stumble onto.
Examples:
• RAG returning sensitive text unexpectedly
• Agent chains looping, merging, or failing
• Data drift masquerading as malicious activity

Destination: Chapter 4


---

5. Hardening ML Infrastructure

What to capture:
Every time you secure a component because the default felt unsafe.
Examples:
• Locking down Ollama endpoints
• Hardening vector DB access
• GPU isolation experiments in containers

Destination: Chapter 5


---

6. Monitoring & Observability

What to capture:
Dashboards you build because you absolutely needed them.
Examples:
• Drift graphs
• Latency spikes during agent tasks
• Retrieval failure rates
• GPU saturation alerts

Destination: Chapter 6


---

7. Securing RAG Systems

What to capture:
Anything involving embeddings, retrieval, and documents.
Examples:
• Poisoned document tests
• Prompt injection through retrieved text
• Access controls on the vector store

Destination: Chapter 7


---

8. Securing Agentic Systems

What to capture:
Any time an agent does something clever, wrong, or dangerous.
Examples:
• Tool-call misuse
• Unexpected file writes
• Escalation inside agent chains
• Guardrail patterns that worked

Destination: Chapter 8


---

9. ML Supply Chain Security

What to capture:
The entire dependency/model pipeline.
Examples:
• Verifying model integrity
• Freezing Python environments
• How you hardened base containers

Destination: Chapter 9


---

10. Secure Deployment & Lifecycle

What to capture:
Every lesson learned about rolling out and rolling back.
Examples:
• Canary testing a new model
• Measuring regressions
• Version control for checkpoints
• Fixing pipeline breakage during deployment

Destination: Chapter 10


---

11. Incident Response for ML

What to capture:
Any unexpected ML behavior that required triage.
Examples:
• Drift that looked like poisoning
• Misbehaving agent tasks
• A model “forgetting” behavior after retraining

Destination: Chapter 11


---

12. The Consulting Lens

What to capture:
Patterns you recognize after doing this repeatedly.
Examples:
• Common ML security gaps
• Simple fixes teams ignore
• How to assess ML maturity quickly
• Repeatable engagement structure

Destination: Chapter 12


---

13. Command Cheatsheets (RTFM Style)

What to capture:
Any shell command, API call, or snippet you used more than twice.
Examples:
• Proxmox GPU passthrough commands
• Vector DB queries
• Agent debugging commands
• Drift evaluation scripts

Destination: Chapter 13


---


