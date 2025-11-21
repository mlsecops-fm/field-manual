
# MLSecOps Field Manual™

The **MLSecOps Field Manual™** is a long-term, public, reproducible library of small MLSecOps modules, patterns, and a future book-length field manual.

The project grows slowly out of a private MLSecOps Lab and focuses on:

- **Reality over polish** – every module is based on something that actually ran in the lab.   
- **Reproducibility over complexity** – small, self-contained scenarios over giant monolithic labs.   
- **Operational clarity over abstraction** – logs, metrics, and failure modes instead of hand-wavy theory.   
- **Incremental contribution** – one module every few weeks compounds over years.   

This repo is the **public documentation + book project** that sits alongside a separate private **MLSecOps Lab** repo where all experiments run.

---

## Repository structure

```text
docs/
  book/                 # Concept and book scaffolding
    concept-v1.md       # Mission, philosophy, pillars, roadmap
    toc.md              # Working table of contents
    README.md

  growth-map/           # How raw notes become chapters
    field-manual-growth-map.md   # Empty sections for note capture
    growth-map-working.md        # What to capture in each section
    chapter-mapping-tracker.md   # Notes -> drafts -> manuscript
    README.md

  modules/              # Runnable MLSecOps modules (starting with Module 1)
    module-01-evasion-attack-logs-mitigation/
      README.md
      module-01-evasion-attack-logs-mitigation.md
      notebooks/
      assets/

  diagrams/             # Shared diagrams, threat models, architectures
  drafts/               # Chapter drafts as they emerge
  website/              # GitHub Pages entrypoint
    index.md

  meta/
    ai-context-guide.md # How this repo ties into the MLSecOps Lab and 5-year plan
```

---

## Relationship to the MLSecOps Lab

- **MLSecOps Lab** (private repo)
    
    - Proxmox cluster, VLANs, GPUs, RAG systems, agents, inference gateways, monitoring, etc.
        
    - This is the **R&D engine** where everything is actually run.
        
- **MLSecOps Field Manual™** (this repo)
    
    - Modules, patterns, anti-patterns, diagrams, and a future book.
        
    - This is the **public distillation** of what was learned in the lab.
        

---

## Module roadmap

Initial modules follow the roadmap in the Concept v1 document, starting with:

1. **Module 1 — Evasion Attack: Logs + Mitigation**
    
2. Safe model loading
    
3. LLM jailbreak + logging + mitigation
    
4. Retrieval poisoning (RAG)
    
5. Embedding drift detection
    
6. Agent tool misconfiguration demo  
    … and more over time.
    

Each module aims to be:

- runnable in 10–20 minutes
    
- self-contained
    
- grounded in real lab runs
    
- accompanied by logs, diagrams, and clear explanations
    

---

## Status

- ✅ Core concept and philosophy defined (`docs/book/concept-v1.md`)
    
- ✅ Growth Map and Chapter Mapping Tracker in place (`docs/growth-map/*`)
    
- ✅ Working Table of Contents defined (`docs/book/toc.md`)
    
- ✅ AI Context Guide written (`docs/meta/ai-context-guide.md`)
    
- ⏳ Module 1 scaffold created, implementation in progress
    
- ⏳ GitHub Pages site to be published once the first modules are ready
    

---

## License

This project is licensed under the **MIT License** – see `LICENSE` for details.

© 2025 Richard Spicer. MLSecOps Field Manual™. All rights reserved.
