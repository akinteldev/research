![AKAY RESEARCH](assets/akay_research.jpg)

# Research Repository: Archive

> A transparent, public archive of independent research reports underpinning published non-fiction works on cybersecurity, artificial intelligence, and digital threats.

---

## What This Repository Is

Each book in the associated publication catalogue is built on a foundation of original research synthesis. This repository archives the raw research reports in their pre-publication state — before editorial shaping, narrative structuring, or authorial interpretation.

The purpose is transparency: if a claim appears in a published book, its evidential roots should be traceable. This archive makes that tracing possible.

---

## Published Works and Research Archives

### The Agreeable Machine
*How Artificial Intelligence Learned to Lie, Flatter, and Pass the Test*

> How frontier AI models develop sycophancy, deception, and hidden misalignment — and why these are structural properties of how AI is built and evaluated, not bugs to be patched.

**Publication:** [Amazon](https://www.amazon.com/dp/B0GY2H44FF)
**Research Archive:** [View Reports](./reports/2026-01-The-Agreeable-Machine/)
**Threat Intelligence Brief:** [THREAT-INTEL.md](./reports/2026-01-The-Agreeable-Machine/THREAT-INTEL.md)

Five reports covering: artificial psychology as a security framework · jailbreak ecosystem empirical analysis (2023–2026) · deceptive alignment detection methods · LLM-as-Judge vulnerabilities · governance of AI behavioral personas.

---

### Ransomware, Inc.
*Inside the Criminal Enterprise That Industrialized Extortion*

> How ransomware evolved from a blunt digital crime into a mature criminal services industry — with franchises, affiliate labor markets, negotiation specialists, and cartel-style coordination.

**Publication:** [Amazon](https://www.amazon.com/dp/B0H2FNFMBS)
**Research Archive:** [View Reports](./reports/2026-02-Ransomware-Inc/)
**Threat Intelligence Brief:** [THREAT-INTEL.md](./reports/2026-02-Ransomware-Inc/THREAT-INTEL.md)

Five reports covering: RaaS market consolidation Q1 2026 · affiliate recruitment and labor markets · payload evolution and AI integration · extortion negotiation mechanics · victimology and resilience suppression.

---

## Research Methodology

Research follows a three-stage pipeline designed to maintain data traceability from source to publication.

### Stage 1 — Data Acquisition
Collection of primary telemetry, academic pre-prints, security vendor reports, law enforcement disclosures, and open-source intelligence (OSINT). Sources are cited inline within each report.

### Stage 2 — Synthesis
Raw source material is processed using AI-assisted synthesis tools for recursive filtering, cross-referencing, and pattern identification. Reports are archived in their original generated state to preserve source fidelity without editorial bias.

### Stage 3 — Curation
Published books represent the final layer of human synthesis — applying strategic context, narrative structure, and editorial judgment to the synthesized data. The books are interpretations; this archive is the evidence base.

---

## Repository Structure

```
research/
├── README.md                          ← This file
├── CONTRIBUTING.md                    ← Methodology, citations, and usage guidance
├── assets/                            ← Visual assets
└── reports/
    ├── 2026-01-The-Agreeable-Machine/ ← AI safety and LLM behavioral security
    │   ├── README.md                  ← Book summary and report index
    │   ├── THREAT-INTEL.md            ← Extracted threat intelligence brief
    │   └── 01–05 *.md                 ← Source research reports
    └── 2026-02-Ransomware-Inc/        ← Ransomware economics and operations
        ├── README.md                  ← Book summary and report index
        ├── THREAT-INTEL.md            ← Extracted threat intelligence brief
        └── 01–05 *.md                 ← Source research reports
```

---

## Disclosures

### Nature of Research
These reports are the result of AI-assisted synthesis of publicly available information. They constitute secondary research and literature reviews rather than original empirical studies or peer-reviewed findings.

### Technical Limitations
The use of Large Language Models in research introduces the possibility of technical inaccuracies or misattributions. These documents are provided as raw synthesis. Users are advised to verify citations against primary sources before applying this information to production security environments, legal proceedings, or policy decisions.

### Scope Limitation
This archive documents threats and vulnerabilities for the purpose of understanding and defense. No content in this repository constitutes operational instructions, attack playbooks, or actionable guidance for malicious use.

---

## Using This Research

If you are a **security practitioner:** Start with the THREAT-INTEL.md files for each book — they extract the key findings, CVEs, actor profiles, and defensive priorities in structured, skimmable format.

If you are a **researcher or journalist:** The full source reports contain detailed inline citations to primary sources. Each report's table of contents maps the analytical scope.

If you are a **reader of the books:** This archive shows the evidentiary foundation for claims made in the published text. Where something in a book strikes you as surprising or specific, the originating source is traceable here.

---

*For methodology details, citation guidance, and usage terms, see [CONTRIBUTING.md](./CONTRIBUTING.md).*
