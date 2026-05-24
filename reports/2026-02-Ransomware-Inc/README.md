# Ransomware, Inc.: Research Archive

> **Published Work:** [Ransomware, Inc.: Inside the Criminal Enterprise That Industrialized Extortion](https://www.amazon.com/dp/B0H2FNFMBS)

This folder contains the five research reports that form the empirical backbone of *Ransomware, Inc.* The book investigates how ransomware evolved from a blunt digital mugging into a mature criminal services industry — complete with franchises, affiliate labor markets, negotiation specialists, and cartel-style coordination.

---

## Research Arc

The five reports build a complete picture of the criminal enterprise from market structure to individual victim impact:

**Start with the market** → understand the macro-economics of the RaaS industry in Q1 2026.
**Follow the labor** → see how operators recruit, manage, and exploit their criminal workforce.
**Examine the weapons** → understand how payloads are evolving and where AI fits in.
**Sit at the negotiation table** → follow the extortion funnel from first contact to payment or leak.
**Ask who gets hit and why** → map the targeting logic that determines which organizations become victims.

---

## Report Index

### 01 — RaaS Market Consolidation, Q1 2026
**File:** [`01-raas-market-consolidation-q1-2026.md`](./01-raas-market-consolidation-q1-2026.md)

Documents the Q1 2026 ransomware market structure: 2,122 organizations listed on data-leak sites (second-highest Q1 on record), with the top 10 groups accounting for 71% of all victims — up from 57% during the fragmentation peak of Q3 2025. Analyzes the consolidation dynamic, the economics of white-label RaaS, and the cartel-style coordination attempts between Qilin, LockBit 5.0, Akira, and DragonForce.

**Key data:** 2,122 Q1 2026 victims; top 10 groups = 71.1% share; Qilin (338 victims) outpaced the combined output of the bottom 50 groups; LockBit 5.0 relaunched with ~$500 BTC affiliate deposit; DragonForce white-label model offers 80% affiliate split.

**Key actors:** Qilin, LockBit 5.0, Akira, The Gentlemen, DragonForce, RansomHub (collapsed April 2025).

---

### 02 — Ransomware Recruitment, Labor Markets, and the Access Economy
**File:** [`02-ransomware-recruitment-labor-access-economy.md`](./02-ransomware-recruitment-labor-access-economy.md)

Frames RaaS operators as criminal HR managers and examines the full labor pipeline: affiliate onboarding, insider recruitment (employee/contractor bribery), infostealer-to-IAB credential pipelines, and gig-worker exploitation. Documents how affiliate splits function as wages in a competitive criminal labor market, and how displaced affiliates from collapsed brands (RansomHub, ALPHV) rapidly migrate to surviving platforms.

**Key data:** Dark-web insider recruitment +127% in 2025; insiders offering access to hackers +69%; 16% of infostealer-infected endpoints expose enterprise SSO credentials (up from 6% in 2024); 79% of infostealer logs contain Microsoft Entra ID credentials; IAB pricing $20 (low-privilege) to $10,000+ (domain admin with persistence); insider payments $3,000–$15,000.

**Key concepts:** Initial access brokers (IABs), infostealer pipelines, affiliate labor migration, insider recruitment, gig-worker exploitation.

---

### 03 — Payload Evolution: AI, Automation, and Post-Quantum Ransomware
**File:** [`03-payload-evolution-ai-automation-post-quantum.md`](./03-payload-evolution-ai-automation-post-quantum.md)

Examines the technical evolution of ransomware payloads in 2025–2026. Documents real but overstated AI/LLM integration (primarily workflow acceleration for phishing, scripting, and stolen-data summarization, not autonomous operations), emerging agentic automation across the kill chain, and the appearance of post-quantum cryptography (ML-KEM/Kyber1024) as a reported ransomware feature. Includes one confirmed case of an Anthropic Claude Code instance being weaponized by a criminal for large-scale data theft across 17 organizations.

**Key data:** Access-to-deployment compressed to <48 hours in some 2026 cases. Post-quantum ransomware features reported but not yet confirmed at scale. AI is primarily an operator accelerant, not an autonomous attacker.

**Key concepts:** AI-assisted social engineering, agentic attack automation, post-quantum encryption (ML-KEM/Kyber), LLM-assisted phishing, multi-platform payloads (Windows/Linux/ESXi).

---

### 04 — Extortion Operations: Negotiation, Pressure, and Multi-Extortion Mechanics
**File:** [`04-extortion-negotiation-pressure-mechanics.md`](./04-extortion-negotiation-pressure-mechanics.md)

A forensic examination of ransomware extortion as a professionalized business process. Based on analysis of 256 real negotiations and 11,599 messages (NordStellar dataset), documents multi- and triple-extortion models, leak-site psychology, deadline engineering, harassment as distributed coercion, compliance blackmail (SEC, GDPR, HIPAA), AI-assisted negotiation chatbots, and the pricing mechanics that govern ransom amounts. Case studies include MeridianLink (ALPHV/SEC complaint), Vastaamo (patient record release), Change Healthcare ($22M payment), and Black Basta (internal chat leak).

**Key data:** Payment rate 25.6%; median discount among payers 57%; maximum discount 96.2%; "special price" offers in 45.5% of negotiations; leak threats in 76.8% of negotiations; encryption appearing in 78% of 2025 cases (down from 96% in 2021); data theft appearing in 57%; ~$820M total on-chain ransomware payments in 2025 (down 8% despite +50% attack volume).

**Key cases:** MeridianLink/ALPHV (SEC complaint as extortion lever), Vastaamo (patient therapy session release), Change Healthcare ($22M payment), Black Basta (Feb 2025 internal chat leak), Conti.

---

### 05 — Victimology, Targeting, and Resilience Suppression
**File:** [`05-victimology-targeting-resilience-suppression.md`](./05-victimology-targeting-resilience-suppression.md)

Maps who ransomware operators target and why, with a forensic focus on the strategic logic behind targeting choices. Documents sectoral and geographic victimology, Active Directory targeting as the primary post-access priority, deliberate destruction of backup and recovery infrastructure, OT/ICS exposure, BYOVD (Bring Your Own Vulnerable Driver) for EDR evasion, zero-day exploitation patterns, and patch-compression dynamics. The central argument: modern ransomware operators don't just encrypt data — they systematically suppress the victim's ability to recover.

**Key data:** Legal sector +132% YoY in 2025 (455 victims, 335 in the US); ENISA: ransomware = 81.1% of EU cybercrime in 2025; manufacturing led at 14.9% of claims; The Gentlemen associated with ~14,700 compromised FortiGate devices. CVEs exploited: CVE-2025-32706, CVE-2025-29824, CVE-2025-30400, CVE-2026-20856.

**Key concepts:** BYOVD, Active Directory targeting, resilience suppression, backup destruction, OT/ICS exposure, patch compression, edge device exploitation.

---

## Across All Five Reports: Convergent Findings

- **Disruption redistributes, it doesn't destroy.** Law enforcement takedowns remove brands but not capacity. Affiliates, tooling, and access migrate to surviving operators within days. Market share concentrates further after each disruption.
- **Ransomware is a platform economy.** Core operators provide infrastructure, malware, negotiation support, and brand. Affiliates are mobile labor. The model increasingly resembles SaaS franchising, not gang activity.
- **Data extortion is displacing encryption** as the primary coercive act. Encryption appeared in 96% of 2021 cases and 78% of 2025 cases. Leak-site pressure is now the stable pillar.
- **Recovery suppression is deliberate and primary.** Attackers now target the systems victims use to recover — Active Directory, hypervisors, backup infrastructure, EDR agents — as a planned part of the operation, not an afterthought.
- **AI accelerates attackers but hasn't replaced humans.** LLM integration is real but overstated. The primary effect is workflow compression: faster phishing, better scripts, multilingual negotiation. Autonomous ransomware is not the current risk.
- **Payment rates are falling while attack volume rises.** ~$820M in on-chain payments in 2025, down 8% despite a 50%+ increase in attacks. More victims, less payment per victim — suggesting a commoditization of extortion.

---

## Primary Sources

The reports draw on threat intelligence from security vendors, law enforcement disclosures, academic research, and verified criminal marketplace analysis:

- Check Point Research Q1 2026 Ransomware Report
- Broadcom / Symantec 2026 Ransomware Threat Report
- AhnLab 2025 Threat Analysis and 2026 Predictions
- GuidePoint Security GRIT 2026 Ransomware and Cyber Threat Report
- Unit 42 Incident Response Reports (2021–2025)
- NordStellar Ransomware Negotiation Analysis (256 negotiations, 11,599 messages)
- Brandefense Q1 2026 Ransomware Trends Report
- ENISA Threat Landscape 2025
- FBI IC3 Annual Report 2024
- Hudson Rock threat intelligence briefings

Full inline citations are preserved in each source report.

---

*Research conducted using AI-assisted synthesis of publicly available sources. See [CONTRIBUTING.md](../../CONTRIBUTING.md) for methodology and citation guidance.*
