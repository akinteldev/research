# Threat Intelligence Brief: Ransomware, Inc.

> Research companion to [Ransomware, Inc.: Inside the Criminal Enterprise That Industrialized Extortion](https://www.amazon.com/dp/B0H2FNFMBS)

This document extracts the key threat intelligence findings from the five research reports. It is structured for security practitioners, incident responders, and threat analysts who need actionable signal without reading the full source documents.

**Scope:** Ransomware-as-a-Service economics, dominant operators, affiliate labor markets, payload evolution, extortion mechanics, victimology, and resilience suppression. All data points are drawn from cited primary research; see individual reports for full source attribution.

**Data currency:** Primary data reflects Q1 2026 threat landscape. Statistics from 2025 full-year reporting are labeled accordingly.

---

## 1. Market Overview: Q1 2026

The ransomware threat landscape in early 2026 is defined by **consolidation after disruption** — fewer groups, higher concentration, more industrialized operations.

**Volume**
- **2,122** organizations listed on ransomware data-leak sites in Q1 2026 (Check Point Research) — second-highest Q1 on record
- **7,874** tracked victims in full-year 2025 (NCC Group) — **+50% year-over-year**
- **7,960** DLS-listed victims in 2025 (Check Point) — **+53% YoY**
- **6,182** total extortion attacks in 2025 including data-theft-only (Broadcom/Symantec) — **+23% vs 2024**
- Monthly average Q1 2026: **707 victims/month**

**Concentration**
- Top 10 groups: **71.1%** of Q1 2026 victims — up from **57%** at the Q3 2025 fragmentation peak
- Qilin + Akira + The Gentlemen + LockBit: **41%** of all Q1 2026 victims combined
- **21 new groups** emerged in Q1 2026; most posted fewer than 10 victims each

**Financial**
- **~$820M** in on-chain ransomware payments in 2025 — **down 8%** from 2024, despite **+50%** attack volume
- Payment rate at historic low of **23%** in Q3 2025 (Coveware via GuidePoint); ~25% in Q4 2025
- Median ransom payment Q4 2025: **$325,000** (**+132% quarter-over-quarter**)
- **~$2.1B** in ransomware payments across 2022–2024 (US Treasury/FinCEN)

---

## 2. Dominant Operators

### Qilin
- **338 victims** in Q1 2026 — most active operator for the third consecutive quarter
- **1,022–1,044 victims** across full-year 2025; **1,800+** since inception
- Growth: **701 victims by October 2025**, up **+280%** from April 2025
- Affiliate split: **80%** for payments ≤$3M; **85%** for payments >$3M
- Added spam/automated negotiation features and a "Call Lawyer" function for affiliates
- Exceeded the combined output of the bottom 50 groups in Q1 2026

### LockBit 5.0
- **163 victims** in Q1 2026 — **+106%** from Q4 2025
- Relaunched September 2025 on RAMP forum after Operation Cronos disruption
- LockBit 5.0 features: cross-platform targeting (Windows/Linux/ESXi), new evasion, faster encryption, randomized file extensions
- Affiliate onboarding: approximately **$500 Bitcoin deposit** (filter mechanism)
- Top-performer affiliate splits: up to **90%**
- Payments dropped **79%** immediately following Operation Cronos; Q1 2026 marks confirmed re-entry into top tier
- US target share reduced to **21.2%** (down from historical ~50%+) — apparent law-enforcement risk response

### Akira
- Approximately **203 victims** in Q1 2026 (derived estimate)
- **$244M total proceeds** since emergence
- **16%** of all claimed 2025 ransomware attacks (Broadcom/Symantec)
- **622 incidents** in 2025 (AhnLab — #1 most active group in their dataset)
- Primary sectors: consumer goods, industrial manufacturing
- Standard affiliate split: ~80%

### The Gentlemen
- **166 victims** in Q1 2026 — up from **40** in Q4 2025 (**+315% quarter-over-quarter**)
- Associated with a pre-staged pool of approximately **14,700 compromised FortiGate devices**
- Rapid affiliate attraction or access-pool deployment in Q1 2026

### DragonForce
- Primary architect of white-label RaaS model in 2025–2026
- Offers affiliates **80% profit share** under separate brands using DragonForce infrastructure
- Attempted cartel formation with LockBit and Qilin (September 2025) — "equal competition conditions" / "dictate market conditions" rhetoric
- Represents the clearest documented case of ransomware-as-a-franchise

### RansomHub (Collapsed)
- **760+** victims since 2024; collapsed April 2025
- Offered affiliates up to **90% profit share** before shutdown
- Collapse triggered major affiliate migration wave, primarily to Qilin and Akira
- Demonstrates how disruption redistributes capacity rather than eliminating it

---

## 3. Affiliate Economics and Labor Markets

### Affiliate Split Benchmarks (Q1 2026)

| Operator | Affiliate Share | Notes |
|---|---|---|
| LockBit 5.0 | Up to 90% (top performers) | ~$500 BTC deposit required |
| RansomHub | Up to 90% | Before April 2025 collapse |
| Qilin | 80% / 85% | Threshold at $3M payment |
| Akira | ~80% | Competitive with market |
| DragonForce | 80% | White-label model |
| Legacy operators | 60–70% | No longer competitive |

### Initial Access Broker (IAB) Market

- IAB listings: **105** unique organizations' remote access offered for sale in a single month (Hudson Rock)
- **$14M+** in on-chain payments to IABs in 2025
- Pricing: **$20** (low-privilege credentials) → **$10,000+** (domain admin with persistence)
- Infostealer logs: **16%** of infected enterprise endpoints expose SSO credentials (up from 6% in 2024)
- **79%** of infostealer logs contain Microsoft Entra ID credentials
- **1.17M** logs contain credentials plus active session cookies

### Insider Recruitment

- Dark-web insider recruitment listings: **+127%** increase in 2025
- Employees/contractors offering access: **+69%** increase in 2025
- Payment range: **$3,000–$15,000** depending on access sensitivity
- Primary recruitment channels: dark-web forums, encrypted messaging, direct contact through corporate email systems

### Access-to-Deployment Compression

- In some 2026 cases, time from initial access to ransomware deployment: **<48 hours**
- Reflects maturation of pre-staged access pools and streamlined affiliate playbooks

---

## 4. Tactics, Techniques, and Procedures

### Initial Access
- Mass exploitation of edge devices: Fortinet (FortiGate), Ivanti, Cisco, VMware ESXi
- Infostealer credential harvesting via cracked software, fake CAPTCHA pages, phishing
- Insider recruitment (bribed employees or contractors)
- Purchased initial access from IAB marketplaces
- Fake update pages and social engineering lures

### Post-Access Priorities (in order)
1. **Active Directory compromise** — domain admin access is the primary first-priority post-access action
2. **EDR/security tool disablement** — BYOVD (Bring Your Own Vulnerable Driver) used to kill endpoint detection
3. **Backup and shadow-copy destruction** — recovery infrastructure elimination
4. **Hypervisor targeting** — ESXi/virtual machine mass encryption
5. **Lateral movement** — credential harvesting, pass-the-hash, Kerberoasting
6. **Data exfiltration** — staged before encryption for double-extortion
7. **Payload deployment** — encryption last, after resilience suppression is complete

### Resilience Suppression (Central Tactic)
Modern ransomware operations explicitly target the systems victims use to recover, not just the data:
- Active Directory destruction (removes authentication and authorization infrastructure)
- VSS (Volume Shadow Copy) deletion
- Backup system access and deletion (on-premises and cloud)
- EDR agent killing via BYOVD
- Update infrastructure compromise (WSUS exploitation: CVE-2026-20856)

### Bring Your Own Vulnerable Driver (BYOVD)
- Used to load a vulnerable, signed driver that grants kernel-level access to kill EDR agents
- Difficult to detect because the driver itself is legitimately signed
- Increasingly commoditized — BYOVD kits available in criminal marketplaces

### Multi-Platform Payloads
- LockBit 5.0, Akira, and other leading operators deploy payloads targeting Windows, Linux, and VMware ESXi simultaneously
- Maximizes damage per intrusion and prevents "escape" to alternate infrastructure

---

## 5. CVEs Actively Exploited

| CVE | Component | Type | Notes |
|---|---|---|---|
| CVE-2025-32706 | Windows Common Log File System | Elevation of Privilege | Actively exploited in 2025 campaigns |
| CVE-2025-32701 | Windows Common Log File System | Elevation of Privilege | Companion to CVE-2025-32706 |
| CVE-2025-30400 | Microsoft DWM Core Library | Elevation of Privilege | Exploited in ransomware deployment chains |
| CVE-2025-32709 | Windows Ancillary Function Driver (WinSock) | Elevation of Privilege | Post-exploitation privilege escalation |
| CVE-2025-29824 | Windows | Escalation | Associated with PipeMagic / RansomExx |
| CVE-2026-20856 | WSUS (Windows Server Update Services) | Remote Code Execution | Update infrastructure compromise vector |
| CVE-2026-21265 | Windows Secure Boot | Security Feature Bypass | Boot-level persistence |

**Edge device exploitation (no specific CVE — ongoing):** Fortinet FortiGate, Ivanti Connect Secure, Cisco ASA/FTD, VMware ESXi remain high-value, frequently exploited targets.

---

## 6. Extortion Mechanics

Based on analysis of 256 real ransomware negotiations and 11,599 messages (NordStellar dataset):

### Negotiation Statistics
- Payment rate: **25.6%** of negotiations ended in payment
- Median discount for paying victims: **57%** off initial demand
- Maximum observed discount: **96.2%**
- "Special price" offers: appeared in **45.5%** of conversations
- Leak threats: issued in **76.8%** of conversations
- Attacker commitments fulfilled (decryptors provided): **68%** of cases where payment was made (Unit 42)

### Extortion Tactic Evolution (Unit 42, 2021–2025)
- Encryption only: 96% (2021) → 78% (2025) — declining as primary coercive act
- Data theft/exfiltration: 53% (2021) → 57% (2025) — stable and growing
- Harassment: 5% (2021) → 10–13% (2025) — growing as pressure multiplier

### Multi-Extortion Model
Modern operations routinely combine:
1. **Encryption** — immediate operational disruption
2. **Data leak threat** — long-term reputational and regulatory pressure
3. **Harassment** — direct contact with customers, partners, regulators, or media
4. **DDoS** (less common) — additional operational disruption
5. **Regulatory blackmail** — threatening to notify or file complaints with SEC, GDPR authorities, HIPAA enforcement

### AI-Assisted Negotiation
- AI-assisted negotiation chatbots reported in use by multiple operators (Picus Security, Axios)
- Used for: initial contact automation, multilingual communication, discount calculation, deadline management
- Not yet autonomous — human operators remain involved in high-value negotiations

### Notable Extortion Cases
- **MeridianLink / ALPHV:** First documented case of a ransomware operator filing an SEC complaint against their own victim for failing to disclose the breach within the required window — using regulatory compliance as a coercive lever
- **Vastaamo (Finland):** Therapy session notes released publicly when the organization refused to pay — direct patient harm at scale
- **Change Healthcare:** $22M ransom payment by UnitedHealth Group, one of the largest confirmed payments on record
- **Black Basta:** Internal chat logs leaked February 2025, exposing key members, victim list, and poor decryptor key management
- **Conti:** Threatened to publish negotiation details if victim spoke to media

---

## 7. Victimology and Targeting

### Sectors Most Impacted (2025 Data)

- **Manufacturing:** 14.9% of ransomware claims (ENISA EU data) — #1 target globally
- **Healthcare:** FBI IC3 2024 top complaints; high ransom compliance due to operational criticality
- **Legal Services:** **455 victims in 2025** (GRIT) — **+132% YoY** from 196 in 2024; 335 of 455 were US firms
- **Government/Critical Infrastructure:** FBI IC3 2024 top categories
- **Financial Services:** High-value targets; elevated compliance risk

**EU Specific:** Ransomware accounted for **81.1%** of all EU cybercrime activity in 2025 (ENISA).

### Geographic Distribution
- United States: historically 40–60% of ransomware victim listings; LockBit specifically reduced US share to 21.2% post-Cronos as law-enforcement risk response
- Activity documented across **98 countries** (Brandefense Q1 2026)

### Target Selection Logic
Operators optimize for:
1. **Payment likelihood** — organizations with cyber insurance, regulatory exposure, or operational criticality
2. **Ability to pay** — revenue thresholds; SMBs targeted by lower-tier affiliates, large enterprises by top operators
3. **Resilience weakness** — organizations with poor backup hygiene, flat Active Directory structure, or legacy EDR
4. **Regulatory leverage** — healthcare, financial services, and legal sectors offer compliance-blackmail multipliers
5. **Geopolitical safety** — operators avoid targets in CIS countries to reduce Russian law enforcement risk

### The Gentlemen: Pre-Staged Access
- Associated with ~**14,700 compromised FortiGate devices** held before operational deployment
- Represents a pattern of large-scale pre-staging — acquiring access before selecting victims based on payment-likelihood scoring

---

## 8. Threat Actors Quick Reference

| Actor | Status Q1 2026 | Key Characteristic |
|---|---|---|
| Qilin | Active — dominant | Most active operator; aggressive affiliate economics; automated negotiation features |
| LockBit 5.0 | Active — recovering | Relaunched Sep 2025; cross-platform; reduced US exposure |
| Akira | Active — stable | $244M total proceeds; manufacturing focus; consistent top-3 operator |
| The Gentlemen | Active — breakout growth | +315% QoQ in Q1 2026; FortiGate access pool |
| DragonForce | Active — ecosystem builder | White-label model; cartel architect |
| RansomHub | Collapsed April 2025 | 760+ victims; collapse drove affiliate migration |
| ALPHV/BlackCat | Disrupted 2024 | SEC complaint innovation; affiliate exit scam collapse |
| Clop | Active — periodic | MOVEit legacy; Oracle EBS exploitation; mass-posting model |
| Black Basta | Disrupted | Internal chat leak Feb 2025; key member exposure |
| Anubis | Emerging | "Data ransom" investigative model; regulator notification threats |

---

## 9. Defensive Priorities (Derived from Attacker Targeting Logic)

These priorities are derived directly from documented attacker TTPs — what attackers consistently target first determines what defenders must protect most:

1. **Active Directory hardening** — tiered AD model, privileged access workstations, Kerberoasting protections
2. **Backup architecture** — immutable, air-gapped or offline backups; separate credential management; tested recovery procedures
3. **EDR protection** — prevent BYOVD via driver block lists; protect EDR agents from privileged termination
4. **Edge device patching** — Fortinet, Ivanti, Cisco, VMware ESXi are the primary initial access vectors; patch velocity matters
5. **Credential hygiene** — MFA everywhere, especially VPN and remote access; infostealer monitoring for leaked credentials
6. **Insider threat program** — monitor for dark-web recruitment signals; privileged access anomaly detection
7. **Incident response planning** — tabletop exercises specifically for ransomware; pre-negotiated external IR and legal retainers
8. **Regulatory compliance readiness** — understand SEC, HIPAA, GDPR disclosure timelines before an incident; attackers weaponize compliance gaps

---

*This document is a secondary synthesis. Verify all statistics and claims against the primary sources linked in the individual research reports before applying to production security or legal decisions.*

*Research conducted using AI-assisted synthesis of publicly available sources. See [CONTRIBUTING.md](../../CONTRIBUTING.md) for methodology and citation guidance.*
