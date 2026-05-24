# Contributing and Methodology

This document explains how the research in this archive was produced, what it represents, and how it should be used or cited.

---

## What These Reports Are

Each report in this archive is a **synthesis document** — a structured summary and analysis of publicly available primary sources on a defined research question. They are produced as part of the research pipeline that supports associated non-fiction publications.

Reports are:
- **Secondary research**, not primary empirical studies
- **Literature reviews**, cross-referencing multiple published sources
- **AI-assisted**, using large language models to accelerate synthesis, not to generate facts
- **Pre-editorial**, meaning they represent the raw research state before narrative shaping or authorial interpretation

Reports are **not**:
- Peer-reviewed academic papers
- Original empirical research or datasets
- Legal, compliance, or security advisory documents
- Operational guidance of any kind

---

## Research Pipeline

### Stage 1 — Source Collection
Primary sources are identified through academic databases, security vendor reports, law enforcement disclosures, threat intelligence platforms, and open-source intelligence. Sources are selected for relevance, credibility, and recency.

Accepted source types include:
- Peer-reviewed academic papers (arXiv, IEEE, ACM, USENIX)
- Security vendor threat intelligence reports (Mandiant, CrowdStrike, Broadcom/Symantec, Check Point, Unit 42, GuidePoint, AhnLab, etc.)
- Government and law enforcement disclosures (FBI IC3, CISA advisories, ENISA, FinCEN)
- Academic pre-prints and alignment research (Anthropic, OpenAI, DeepMind research blogs)
- Verified journalistic investigations from credible outlets

### Stage 2 — AI-Assisted Synthesis
Large language models are used as synthesis tools — to structure, cross-reference, and summarize source material at scale. The LLM does not generate facts; it organizes and summarizes facts present in the provided sources.

Risks introduced at this stage:
- **Hallucinated citations** — LLMs may generate plausible-sounding but non-existent citations. All citations in these reports should be verified against primary sources.
- **Misattribution** — statistics or findings may be attributed to the wrong source. Verify specifics before use.
- **Framing effects** — synthesis may introduce subtle framing biases not present in the original sources.

### Stage 3 — Human Review and Publication
The published books represent human editorial synthesis — selecting, interpreting, and contextualizing the synthesized research. The archive represents the research layer; the books represent the interpretive layer.

---

## How to Cite

### Citing the published books
Use standard citation formats for the published work (ISBN/ASIN available on the Amazon product pages). The books are the citable, editorially reviewed artifacts.

### Citing these reports
These reports are not independently citable as primary research. They function as an evidence trail. If a specific claim matters, cite the primary source embedded within the report, not the report itself.

Example: If a report states that Qilin posted 338 victims in Q1 2026, the correct citation is Check Point Research's Q1 2026 Ransomware Report — not this archive document.

### Citing primary sources from within these reports
Each report contains inline citations linking to primary sources. Follow the link and verify the claim before citing externally.

---

## Known Limitations

**Citation accuracy:** All inline citations should be verified before use. LLM-assisted synthesis can produce citation errors (wrong URL, wrong author, wrong year, or a plausible but non-existent paper). Approximately 5–10% of inline citations in AI-assisted research documents contain some form of error; treat them as pointers to check, not as verified facts.

**Data currency:** Threat intelligence data degrades quickly. Statistics about ransomware victim volumes, affiliate splits, or group activity are current as of the report's research period. Check the primary source for updated figures.

**Construct validity:** Terms used across different vendor reports (e.g., "ransomware incident," "data-leak site posting") are not standardized. Cross-vendor statistics are not directly comparable. The reports note these caveats where significant.

**LLM-introduced framing:** AI synthesis tools may introduce consistent framing biases — for example, overweighting sources that were more prominent in training data, or applying explanatory frameworks not present in the original sources. Apply critical reading accordingly.

---

## Scope Limitation and Responsible Use

This repository documents cybersecurity threats and vulnerabilities for the explicit purpose of understanding, awareness, and defense.

No content in this archive constitutes:
- Operational attack instructions
- Exploit code or proof-of-concept implementations
- Guidance on how to conduct malicious operations
- Playbooks for any illegal activity

The research standard applied throughout is **information, not ammunition** — detailed enough to inform defenders and policymakers, scoped to exclude operational details that would primarily serve attackers.

If you identify content in this archive that you believe crosses this line, open an issue or contact the repository owner directly.

---

## Contact

This repository is maintained by the author under the `akinteldev` GitHub account. For substantive corrections to factual claims, raise a GitHub issue with the specific claim, the report file, and the correcting primary source. Corrections that are verified against primary sources will be addressed.

---

*Last updated: 2026*
