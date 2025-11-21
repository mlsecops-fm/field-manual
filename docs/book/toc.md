
---
MLSecOps Field Manual — Working Table of Contents

A practical guide from a security engineer building, defending, and operationalizing machine-learning systems in the real world.

---
1. Orientation

What you naturally accumulate: clarity about what MLSecOps actually is when you’ve lived it rather than read about it.
• Why machine-learning systems behave differently than traditional apps
• How ML pipelines introduce new attack surfaces
• What “security engineer entering ML territory” feels like from the ground
• The boundaries between MLOps, AI engineering, and MLSecOps as you experience them
• A pragmatic definition: securing ML throughout its lifecycle using production-grade principles

Your lived experience becomes the compass here.


---

2. The Operating Environment

What you accumulate: all the quirks, topology realities, and architectural decisions from building your own lab.
• Your Proxmox cluster topology in practice
• VLAN segmentation patterns that worked or didn’t
• ZFS performance lessons
• GPU scheduling realities in a mixed workload environment
• Your inference gateway, observability stack, and RAG servers
• Common misconfigurations you’ll see again and again

This chapter becomes a compressed record of every “wait, why isn’t this working?” moment you’ll face.


---

3. ML System Anatomy for Security Engineers

What you accumulate: the mental model of each ML component by debugging and deploying it.
• Datasets as mutable infrastructure
• Feature stores and unintentional trust boundaries
• Model training pipelines (CI/CT/CD)
• Model registries and version drift
• Inference servers and the fragility of request patterns
• Agentic workflows and their cross-system trust assumptions
• RAG pipelines and the reality of vector store security

This is where your debugging logs become diagrams.


---

4. Threat Modeling Machine Learning

What you accumulate: threat patterns you’ll see repeatedly—some obvious, some sneaky.
• Data poisoning (real examples from your lab)
• Model extraction when you accidentally expose a footprint
• Prompt injection abuses inside your own agent stack
• Supply-chain risks from pip wheels, pre-trained models, and HuggingFace downloads
• Misuse: your first “I didn’t expect that output from this agent” moment
• Eval blind spots
• Inference-time evasion and the weirdness of adversarial inputs

This chapter is basically your “incident journal.”


---

5. Hardening ML Infrastructure

What you accumulate: every time you lock something down in your lab and realize the default was too trusting.
• Network segmentation strategies that survived load tests
• RBAC for training vs inference systems
• GPU isolation and privilege boundaries
• Safeguarding model artifacts
• Hardening vector databases
• Securing feature stores
• Container boundaries and PCIe considerations
• Logging schemas that actually caught problems

This is the chapter where future readers say: Ah, someone has already been burned by this.


---

6. Monitoring and Observability

What you accumulate: the dashboards you build because you needed them, not because a tutorial told you to.
• The signals that matter for ML systems (latency, drift, hallucination rates, poisoning anomalies)
• Traces through RAG pipelines
• Detecting agent runaway behavior
• GPU telemetry you end up depending on
• Model performance metrics that correlate to real security risk
• Alert patterns that were noise vs. actually helpful

You’re building your monitoring stack anyway—this simply captures the parts you ended up caring about.


---

7. Securing RAG Systems

What you accumulate: firsthand experience with semantic search, embeddings, and LLM integration.
• Attack surfaces of RAG architectures
• Protecting vector stores
• Preventing data exfiltration through embeddings
• Injection through retrieved context
• Document hygiene
• Access control inside retrieval layers
• Monitoring the “shape” of retrieval

This chapter grows from your own RAG implementation work.


---

8. Securing Agentic Systems

What you accumulate: the scars of debugging your own agent workflows.
• Tool safety boundaries
• Input/output validation loops
• Observability for agents
• Preventing tool-chain escalation
• Trust boundaries between agent steps
• Detecting malformed or adversarial outputs
• Evaluating emergent misbehavior

This is the frontier chapter—exactly the kind of thing nobody is documenting yet.


---

9. ML Supply Chain Security

What you accumulate: every dependency you vet, every model you pull, every packaging decision you make.
• Pretrained model risk profiles
• Dependency freeze and verification workflows
• Hashing and integrity checks
• Sources of model metadata truth
• Container image hygiene
• Policy-as-code patterns for ML packaging

This chapter forms itself as you lock down your training/runtime environments.


---

10. Secure Deployment & Lifecycle Management

What you accumulate: your pain points around rolling out updates, performing canary tests, and managing drift.
• Safe rollout patterns for models
• Secure rollback strategies
• Canary vs shadow deployment for ML
• Test patterns for inference safety
• Versioning discipline
• Mitigating stale feature drift in production environments

Every rollout teaches you something—you’ll write it down.


---

11. Incident Response for ML Systems

What you accumulate: the day something behaves strangely, and you chase it.
• Classification: poisoning vs misuse vs agent deviation vs drift
• Triage strategies
• Indicators of compromise that are ML-specific
• Forensic artifacts (training data, checkpoints, evaluation logs)
• Containment without breaking production
• Lessons-learned templates for ML incidents

This chapter becomes your “learned the hard way” chapter.


---

12. The Consulting Lens

What you accumulate: experience translating this into something a client would understand.
• What organizations get wrong
• The simplest recommendations that move the needle
• The Minimum Viable Security posture for ML
• How to scope an MLSecOps engagement
• Repeatable patterns across environments
• How to assess maturity without hand-waving

By month 18, you’ll naturally see patterns others don’t.


---

13. Tools & Commands (RTFM Style)

What you accumulate: every snippet you actually used.
• Proxmox commands
• Kubernetes commands (if you go that route)
• GPU inspection tools
• Vector DB commands
• Model registry CLI use
• Log filtering tricks
• Canary testing scripts
• Endpoint protection for inference nodes
• Your own utilities and scripts

This is your pocket guide section—the soul of an RTFM-style manual.


---

14. Appendices

What you accumulate: the details readers will appreciate but don’t belong in the main flow.
• Lab architecture diagrams
• Example threat models
• Example RAG/agentic architectures
• Example drift dashboards
• Example hardened deployment pipelines
• Reference architectures (based on your implementations)
---