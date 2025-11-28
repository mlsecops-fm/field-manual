# MLSecOps Field Manual™ – Table of Contents

## 1. Orientation

- Why ML systems differ from traditional apps
- ML pipeline attack surfaces
- MLOps vs MLSecOps boundaries
- Pragmatic definition of MLSecOps

## 2. Operating Environment

- Proxmox cluster topology
- VLAN segmentation patterns
- ZFS performance lessons
- GPU scheduling realities
- Inference gateway architecture
- Common misconfigurations

## 3. ML System Anatomy

- Datasets as mutable infrastructure
- Feature stores and trust boundaries
- Training pipelines (CI/CT/CD)
- Model registries and version drift
- Inference servers
- Agentic workflows
- RAG pipelines and vector stores

## 4. Threat Modeling

- Data poisoning
- Model extraction
- Prompt injection
- Supply chain risks
- Misuse scenarios
- Eval blind spots
- Adversarial inputs

## 5. Hardening ML Infrastructure

- Network segmentation
- RBAC for training vs inference
- GPU isolation
- Model artifact protection
- Vector database hardening
- Feature store security
- Container boundaries
- Logging schemas

## 6. Monitoring & Observability

- Drift detection signals
- RAG pipeline traces
- Agent runaway detection
- GPU telemetry
- Performance metrics as security signals
- Alert patterns

## 7. Securing RAG Systems

- RAG attack surfaces
- Vector store protection
- Embedding exfiltration prevention
- Injection through retrieval
- Document hygiene
- Access control patterns
- Retrieval monitoring

## 8. Securing Agentic Systems

- Tool safety boundaries
- Input/output validation
- Agent observability
- Tool-chain escalation prevention
- Trust boundaries
- Adversarial output detection
- Emergent misbehavior evaluation

## 9. ML Supply Chain Security

- Pretrained model risks
- Dependency verification
- Integrity checks
- Model metadata sources
- Container hygiene
- Policy-as-code patterns

## 10. Secure Deployment & Lifecycle

- Safe rollout patterns
- Rollback strategies
- Canary vs shadow deployment
- Inference safety tests
- Versioning discipline
- Feature drift mitigation

## 11. Incident Response

- Classification (poisoning/misuse/drift)
- Triage strategies
- ML-specific IoCs
- Forensic artifacts
- Containment patterns
- Lessons-learned templates

## 12. Consulting Lens

- Common organizational gaps
- High-impact recommendations
- Minimum viable security
- Engagement scoping
- Repeatable patterns
- Maturity assessment

## 13. Tools & Commands

- Proxmox commands
- Kubernetes commands
- GPU inspection
- Vector DB queries
- Model registry CLI
- Log filtering
- Canary testing scripts
- Utilities

## 14. Appendices

- Lab architecture diagrams
- Threat model examples
- RAG/agent architectures
- Drift dashboards
- Hardened deployment pipelines
- Reference architectures
