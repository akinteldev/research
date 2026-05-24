# Governing Behavioral Personas and Value Encoding in Deployed LLM Systems

Large language model governance is moving beyond questions of model capability and misuse toward a harder institutional problem: who gets to define, constrain, audit, and revise the behavioral persona of AI systems once they are deployed at scale. Increasingly, LLM outputs are shaped not only by base-model training, but by constitutional rules, system prompts, retrieval layers, moderation services, enterprise policies, tool permissions, user customization, and runtime security controls. In practice, “AI behavior” is therefore a composite governance outcome rather than a property of a single model artifact, which complicates both regulatory compliance and accountability allocation across the supply chain ([Council of Europe, 2025](https://rm.coe.int/t-pd-2025-3-rev2-draft-guidelines-on-privacy-and-data-protection-in-th/48802ac31f); [MDPI, 2025](https://www.mdpi.com/2813-2203/5/1/8)).

This report examines an emerging governance landscape that is beginning to address that deployment-layer complexity. Public regulators and quasi-regulatory bodies are developing more concrete expectations for generative AI risk management, including the EU AI Act’s phased obligations, the implementation of rules for general-purpose AI, and the broader shift toward documentation, post-market monitoring, and enforceable compliance duties for providers and deployers ([IAPP, 2025](https://iapp.org/resources/article/global-ai-governance-eu); [STACK Cybersecurity, 2025](https://stackcyber.com/posts/ai-eu-act); [Stanford HAI, 2024](https://fsi9-prod.s3.us-west-1.amazonaws.com/s3fs-public/2024-12/GenAI_Report_REV_Master_%20as%20of%20Dec%2012.pdf)). In parallel, technical governance initiatives such as NIST’s Generative AI Public Working Group, Singapore’s Model AI Governance Framework for Generative AI, and OWASP’s GenAI security work are translating high-level principles into more operational controls for documentation, testing, assurance, and secure deployment ([Stanford HAI, 2024](https://fsi9-prod.s3.us-west-1.amazonaws.com/s3fs-public/2024-12/GenAI_Report_REV_Master_%20as%20of%20Dec%2012.pdf); [OWASP, 2026](https://genai.owasp.org/resource/state-of-agentic-ai-security-and-governance-1-0/)).

A central focus is the governance of value encoding itself. Constitutional AI and related alignment methods make behavioral constraints more explicit than earlier reinforcement-only approaches, but they also surface a political question often obscured in technical debates: whose norms are being embedded, through what process, and with what mechanisms for contestation or revision. Recent evidence suggests that even when such systems appear neutral or safety-oriented, their value profiles may align disproportionately with Northern European and Anglophone moral-cultural patterns, while in some cases extending beyond the range of positions observed in surveyed publics. This raises significant concerns for cross-cultural deployment, democratic legitimacy, and the concentration of normative power in a small number of firms authoring machine “character” for global users ([Lonepatient summary of 2026 arXiv paper, 2026](http://lonepatient.top/2026/03/31/arxiv_papers_2026-03-31)).

The report also situates persona governance within a broader assurance ecosystem that includes model cards, risk cards, layered audits, and emerging proposals for behavioral bills of materials capable of tracing which actor contributed which behavioral constraints or modifications. Such instruments matter because deployed LLM behavior often emerges compositionally: a foundation model vendor may define baseline refusals and tone; an enterprise deployer may add domain rules, retrieval sources, and escalation logic; downstream integrators may insert tool-use policies and guardrails; and end users may further steer outputs through prompts or custom settings. Where harms arise from this stack, existing governance frameworks still struggle to determine whether responsibility lies with the model provider, application deployer, system integrator, auditor, or user ([International AI Safety Report, 2026](https://internationalaisafetyreport.org/publication/international-ai-safety-report-2026); [Council of Europe, 2025](https://rm.coe.int/t-pd-2025-3-rev2-draft-guidelines-on-privacy-and-data-protection-in-th/48802ac31f); [MDPI, 2025](https://www.mdpi.com/2813-2203/5/1/8)).

Against this background, the report treats behavioral persona as a governance object in its own right: one that sits at the intersection of safety engineering, security practice, product design, compliance law, cultural pluralism, and institutional legitimacy. The core challenge is no longer simply how to make LLMs safe, but how to govern the authority to specify values, how to document and audit behavioral interventions across layered deployments, and how to create oversight structures that are sufficiently pluralistic, transparent, and accountable when AI systems mediate advice, knowledge, and interaction for entire populations ([Springer, 2025](https://link.springer.com/article/10.1007/s43681-025-00847-w); [OWASP, 2026](https://genai.owasp.org/resource/state-of-agentic-ai-security-and-governance-1-0/); [Stanford HAI, 2024](https://fsi9-prod.s3.us-west-1.amazonaws.com/s3fs-public/2024-12/GenAI_Report_REV_Master_%20as%20of%20Dec%2012.pdf)).

## Table of Contents

- Behavioral Control as a Governance Object in Deployed LLM Stacks
    - From model safety to runtime behavioral governance
    - Accountability failures in compositional deployments
- Comparative Architecture of the Main Frameworks and Mechanisms
    - Constitutional rule-setting, NIST controls, Singapore soft law, OWASP security guidance, and EU legal duties
        - A. Constitutional AI governance as proceduralized value encoding
        - B. NIST AI RMF and the Generative AI profile
        - C. Singapore’s 2024 Model AI Governance Framework for Generative AI
        - D. OWASP GenAI and agentic security guidance
        - E. EU AI Act obligations relevant to deployed behavior
- Regulatory Pressure Points for Behavioral Persona and Value Encoding
    - Where current frameworks actually constrain deployed conduct
    - 1) Documentation duties as indirect behavioral regulation
    - 2) Human oversight requirements as limits on machine character
    - 3) Security controls as preservation of behavioral boundaries
    - 4) Post-deployment monitoring and incident reporting
- Documentation and Assurance Instruments for Behavioral and Value Transparency
    - Comparative design logic of transparency artifacts
    - Model cards, risk cards, and system cards as partial windows into machine character
        - A. Model cards: baseline disclosure without deployment-legible persona mapping
        - B. Risk cards: contextualizing harms, but only if value conflicts are named explicitly
        - C. System cards: useful product-level framing, but vulnerable to curation bias
        - D. A comparative threshold for “behaviorally adequate” card-based disclosure
    - Behavioral bill-of-materials proposals and machine-readable compliance architectures
        - A. Why BBOM matters for value encoding, not just security
        - B. Standardization barriers and the risk of performative inventories
        - C. BBOM and the politics of behavioral provenance
    - Layered auditing as a complement to disclosure artifacts
        - A. Governance audit: who sets the values, by what process, with what legitimacy?
        - B. Model audit: does the model exhibit latent value skew or unstable safety persona?
        - C. Application audit: what persona does the assembled system actually enact?
        - D. Coordinated assurance: linking artifacts to audit evidence
- Lifecycle Allocation of Responsibility for Emergent Persona
    - A. Responsibility should be mapped by control function, not merely by vendor label
    - B. The missing institutional artifact: a persona change log across the deployment chain
- Failure Topologies Unique to Multi-Actor Persona Assembly
    - A. Persona can fail through interaction effects even when each layer appears compliant in isolation
    - B. Causal ambiguity creates predictable responsibility laundering
- Political and Cultural Contestation in Encoded Safety Personas
    - A. “Safe” persona design is not culturally neutral, and Western defaulting remains a structural risk
    - B. Cross-cultural deployment challenges are governance failures, not just localization problems
- Oversight Mechanisms Beyond Documentation: Institutional Checks on Machine Character
    - A. Why internal governance committees are insufficient for population-scale persona power
    - B. Appeals, override, and decommissioning rights should apply to persona-level harms
    - C. Procurement and public-sector deployment should require contestable behavioral governance
- Operationalizing
- Institutional Design Choices for External Scrutiny of Deployed LLM Behavior
    - From transparency artifacts to standing oversight institutions
    - Regulatory supervision and the limits of legal command-and-control
    - Third-party auditors, assurance markets, and the problem of auditing values in context
    - Civil society, affected communities, and contestation as governance infrastructure
- Standards Bodies, Public Accountability Ecosystems, and Cross-Jurisdiction Coordination
    - Standard-setting as a coordination layer for behavioral assurance
- Political Economy of Persona Rulemaking: Who Gets to Define “Good” Machine Conduct
    - Corporate constitutionalism as private governance over public discourse
    - Market incentives and the tendency toward overbroad, exportable safety defaults
    - The hidden layering of authority in enterprise deployments
    - Why “choice” by users does not solve legitimacy deficits
    - Governance implications for constitutional AI processes
- Evidence of Western-Centric Safety and Constitutional Bias in Persona Design
    - Safety language often universalizes historically local norms
    - Constitutional AI can encode bias through principle selection, not only data skew
    - The “Western” problem is not reducible to geography
    - Safety bias can also be internal to Western pluralism
- The Limits of Cultural Adaptation in Deployment-Layer Customization
    - Why downstream localization cannot reliably override upstream constitutional structure
    - Cultural prompting and adaptation can improve fit without solving legitimacy
    - Deployment adaptation can create norm collisions between layers
    - Less-resourced languages and markets face deeper adaptation constraints
    - Agentic systems make localization harder, not easier
- Cross-Jurisdiction Governance Problems: Legitimacy, Sovereignty, and Interoperability of Value Regimes
    - Conflicts between universal safety claims and plural legal-moral orders
    - Existing governance frameworks are better at risk management than value adjudication
    - The unresolved question of whose “public reason” governs transnational assistants
    - Jurisdictional fragmentation may intensify corporate power unless coordination improves
    - The risk of strategic adaptation: appearing local while preserving upstream hegemony
- Institutional Mechanisms for Contestability and Shared Authority over Machine Character
    - From disclosure to representation in persona governance
    - Persona councils, regional review boards, and sectoral norm panels
    - Behavioral change control should be governed like a public-risk process





## Behavioral Control as a Governance Object in Deployed LLM Stacks

### From model safety to runtime behavioral governance

A central shift in 2024–2026 governance discourse is that the relevant object of control is no longer only the base model, but the **deployed behavioral profile** produced by layered system design: provider alignment tuning, system prompts, retrieval and tool policies, enterprise policy wrappers, memory configurations, user instructions, and downstream application logic. This matters because “persona,” “tone,” “value expression,” “refusal style,” “deference level,” and “decision authority” increasingly emerge from composition rather than from weights alone. Regulatory and governance frameworks are therefore converging on a broader understanding of behavioral control that includes design-time alignment, deployment-time constraints, and post-deployment monitoring rather than narrowly focusing on training data or benchmark scores.

This shift is visible across multiple frameworks. The U.S. National Institute of Standards and Technology (“NIST”) positions generative AI governance inside a lifecycle risk-management architecture in which organizations must **govern, map, measure, and manage** risks, including those arising from LLM-specific failure modes and sociotechnical deployment contexts ([1](https://www.toxsec.com/p/ai-governance-requirements-2026), [2](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf), [3](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf)). Singapore’s 2024 **Model AI Governance Framework for Generative AI** similarly extends earlier AI governance work toward issues such as hallucination, copyright, misinformation, and value alignment, while emphasizing accountability, transparency, fairness, robustness, and security in a broader trusted ecosystem ([4](https://aiverifyfoundation.sg/wp-content/uploads/2024/05/Model-AI-Governance-Framework-for-Generative-AI-May-2024-1-1.pdf)). OWASP guidance has moved from static application security concerns toward **agentic** and **multi-agent** threat models that capture prompt injection, tool abuse, excessive agency, insecure memory, and orchestration-layer attacks—threats that directly shape or subvert runtime behavior ([5](https://www.imda.gov.sg/-/media/imda/files/about/emerging-tech-and-research/artificial-intelligence/mgf-for-agentic-ai.pdf)). The EU AI Act, although not drafted specifically around “persona,” imposes obligations on providers and deployers of many AI systems that directly affect behavior through risk management, technical documentation, logging, transparency, human oversight, accuracy/robustness/cybersecurity, and post-market monitoring ([6](https://eur-lex.europa.eu/eli/reg/2024/1689)).

The governance problem is therefore not simply “How do we make a model harmless?” but rather “Who is accountable for the final behavioral persona users experience, and by what institutional mechanisms can that persona be inspected, bounded, contested, and revised?” This is especially important in compositional settings where the system’s normative profile is neither singular nor transparent. A frontier model provider may publish a benign-sounding safety policy, yet an enterprise may wrap the model with aggressive sales optimization prompts, retrieval over biased internal guidance, and tool permissions that effectively convert a conversational assistant into a quasi-autonomous organizational actor. End-users then encounter a “machine character” that appears coherent but is actually the product of fragmented governance.

The accountability implications are substantial. Traditional product governance assumes a relatively stable artifact with an identifiable producer. Deployed LLM systems instead resemble **stacked governance environments** in which several actors each control a different layer of behavior:

| Layer | Typical controlling actor | Behavioral effect | Governance challenge |
|---|---|---|---|
| Base model pretraining/fine-tuning | Foundation model developer | Broad value priors, refusal tendencies, linguistic style, safety defaults | Opaque upstream decisions; proprietary secrecy |
| Constitutional/policy alignment | Foundation model developer or platform vendor | Normative rules, response constraints, harmlessness style | Limited public legitimacy of value selection |
| System prompt/application prompt | Enterprise deployer or integrator | Role, tone, task framing, escalation rules, refusal scope | Often undocumented and dynamically updated |
| Retrieval/context layer | Enterprise deployer | Which norms and facts are surfaced into outputs | Hidden institutional bias through corpus selection |
| Tool permissions and orchestration | Integrator/platform owner | Actionability, autonomy, external effects | Security and authority expansion beyond chatbot layer |
| Memory/personalization | Application owner | Persistent persona shaping and tailored persuasion | Privacy, manipulation, and uneven treatment risks |
| User prompting | End-user | Local behavior variation and attempted overrides | Hard to separate authorized customization from abuse |

In this environment, behavioral control becomes a problem of **institutional design**, not merely technical alignment. A provider can claim that harmful outputs result from downstream misuse; the deployer can claim they relied on a state-of-the-art model; the user can be blamed for adversarial prompting; and no actor may maintain an integrated record of the behavioral stack. This is the governance vacuum that newer frameworks only partially address.

Constitutional AI governance is relevant here because it offers a formalized process for encoding behavioral rules into model training and inference policy. Anthropic’s constitutional AI approach—while not itself a regulation—has shaped governance thinking by making explicit that model behavior can be steered through a set of textual principles used in self-critique and revision, rather than only through opaque human preference optimization ([7](https://www.anthropic.com/news/constitutional-ai-harmlessness-from-ai-feedback)). From a governance perspective, the innovation is not just a safety technique; it is the **externalization of behavioral rule-setting** into an inspectable policy artifact. Yet the political problem remains: who writes the constitution, whose values are represented, what dispute-resolution process exists when principles conflict, and what happens when deployment contexts differ across jurisdictions or cultural settings?

The concern is not hypothetical. Emerging scholarship on cultural value alignment suggests that LLMs encode **culturally situated value hierarchies** rather than neutral ethics. A 2025 study comparing Western and Eastern models argues that systems such as ChatGPT, Gemini, and DeepSeek express systematically different value emphases, consistent with broader individualist/collectivist distinctions, and warns against assuming a singular universal moral profile for AI systems ([8](https://arxiv.org/pdf/2505.17112)). This matters for governance because safety personas that appear universally “helpful” or “appropriate” may in fact normalize Western liberal assumptions about autonomy, speech norms, self-assertion, risk disclosure, or acceptable disagreement. When a handful of firms encode such assumptions into global platforms, behavioral governance becomes a problem of power asymmetry and normative centralization.

The challenge is amplified in enterprise settings. Many organizations now do not train their own models but instead deploy vendor APIs, third-party moderation layers, retrieval systems, copilots, and orchestration frameworks. Their effective behavioral governance is outsourced by default, yet they remain the socially visible actor from the user’s perspective. The result is a **responsibility inversion**: those with the least control over upstream alignment may bear the greatest reputational and legal exposure for downstream behavior. NIST’s emphasis on documented roles, ownership structures, and risk tolerance is important precisely because governance of deployed behavior otherwise disappears into contractual and technical seams ([1](https://www.toxsec.com/p/ai-governance-requirements-2026), [2](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf)).

A more precise governance vocabulary is therefore emerging around at least five distinguishable behavioral control functions:

1. **Norm selection**: choosing the principles or values to encode.
2. **Constraint implementation**: translating norms into prompts, filters, policies, reward models, tool permissions, and escalation rules.
3. **Behavioral assurance**: testing whether the system actually behaves in line with intended constraints under realistic conditions.
4. **Runtime supervision**: monitoring drift, jailbreaks, context-sensitive failures, and distributional changes.
5. **Contestability and revision**: enabling affected users, regulators, auditors, or impacted communities to challenge the encoded behavior.

Most current frameworks cover the first four unevenly, and the fifth only weakly. The gap is especially acute where “behavioral persona” affects politically or culturally sensitive domains—education, healthcare triage, employment screening support, public service interactions, safety advice, and mental health chat interfaces. In such cases, the system’s manner of speaking, deference style, confidence calibration, and normative assumptions can shape outcomes nearly as much as factual accuracy.

To clarify how emerging frameworks approach this object, the table below compares their main intervention points:

| Framework/mechanism | Primary governance target | How it affects deployed behavior | Main institutional weakness |
|---|---|---|---|
| Constitutional AI governance | Alignment principles and self-critique rules | Shapes refusal style, harmlessness, response norms, and tradeoffs | Principle selection lacks democratic legitimacy |
| NIST AI RMF + GenAI profile | Organizational AI risk management | Requires governance, mapping, measurement, and management of behavioral risks | Voluntary status outside procurement/sectoral incorporation |
| Singapore Model AI Governance Framework for Generative AI | Trusted ecosystem governance across lifecycle | Encourages accountability, transparency, safety, content provenance, and stakeholder processes | Soft-law character; implementation heterogeneity |
| OWASP GenAI/agentic guidance | Security and abuse pathways in LLM applications | Focuses on prompt injection, tool misuse, excessive agency, memory and orchestration vulnerabilities | Security-centric lens may underweight normative bias/persona politics |
| EU AI Act | Legal obligations for certain AI systems and GPAI models | Imposes documentation, risk management, transparency, oversight, logging, robustness requirements | Behavior-specific obligations are indirect and classification-dependent |

What is emerging, then, is a layered governance field in which “behavioral control” is assembled through technical standards, soft-law frameworks, security practice, and formal regulation. None individually resolves the deeper question of how values should be selected and revised at scale. But together they mark a transition away from viewing harmful behavior as an incidental bug and toward treating deployed model behavior as a **governable institutional output**.

### Accountability failures in compositional deployments

The most difficult governance cases arise when the behavioral persona seen by users is assembled across multiple firms and internal teams. A customer-service assistant, for example, may use a frontier vendor model aligned with one harmlessness profile, an enterprise system prompt optimized by another team, retrieval from region-specific policy documents, a tone-shaping middleware from a marketing vendor, and a tool layer capable of refunds or account actions. If the system becomes manipulative, discriminatory, or overconfident, causation is distributed. Existing governance frameworks increasingly recognize lifecycle and supply-chain risk, but few are yet adequate for **compositional accountability**.

This is where emerging documentation proposals become important. Traditional **model cards** document model-level intended use, performance, training data characteristics, and ethical considerations, but they are generally insufficient to describe the behavioral surface of a deployed agentic or enterprise-wrapped system. The proposed **Behavioral Bill of Materials (BBOM)** responds to this gap by cataloging an agent’s tool permissions, decision boundaries, memory architecture, orchestration patterns, failure modes, and runtime controls, explicitly arguing that organizations must document not just “what the model is” but “what the agent can do” ([9](https://techjacksolutions.com/ai/agentic-ai/govern/behavioral-bill-of-materials/)). Although BBOM is not a formal standard recognized by NIST, ISO, or the EU AI Act, it is a useful conceptual bridge because it reframes governance from model transparency to **behavioral transparency**.

The BBOM proposal is especially relevant to accountability gaps in layered deployments for three reasons.

First, it identifies that behavioral authority is expanded through **tool manifests and permissions**, not only through language generation. An LLM with no tools may produce risky advice; an LLM with CRM, email, code execution, and payment tools may operationalize that advice. Security and governance consequences therefore depend on runtime affordances, not just model quality. OWASP’s work on agentic and multi-agent threat modeling similarly centers the risks introduced when models acquire tool access, inter-agent communication, and autonomous planning capability ([5](https://www.imda.gov.sg/-/media/imda/files/about/emerging-tech-and-research/artificial-intelligence/mgf-for-agentic-ai.pdf)).

Second, the BBOM emphasizes that agent behavior changes over time and that documentation must be updated as systems evolve. This aligns with the EU AI Act’s expectation that technical documentation be kept current and with post-market monitoring duties for covered systems ([6](https://eur-lex.europa.eu/eli/reg/2024/1689), [9](https://techjacksolutions.com/ai/agentic-ai/govern/behavioral-bill-of-materials/)). In practice, however, most enterprises update prompts, safety middleware, retrieval corpora, and tool policies far more frequently than they revise formal governance records. This creates a divergence between documented and actual behavior.

Third, the BBOM frames the problem as one of **dynamic and compounding risk**, rather than static artifact inspection. That matters because behavior can emerge from interaction among components that are individually compliant. A provider’s refusal policy may be sound in isolation, but retrieval of aggressive internal sales scripts can transform the system into a highly persuasive and minimally contestable upselling agent. Likewise, a region-specific legal guidance overlay may make the assistant appear to adopt culturally narrow moral assumptions that were absent from the base model.

A useful way to map accountability in compositional deployments is to distinguish several failure modes:

| Failure mode | Description | Typical governance blind spot | Likely harmed parties |
|---|---|---|---|
| Upstream value opacity | Provider does not disclose alignment criteria or policy hierarchy | Deployer cannot assess normative fit for context | Users, deployers, affected communities |
| Prompt-layer normative drift | Enterprise modifies system instructions in ways that alter refusals or advice style | Changes fall outside formal change control | End-users, regulators, enterprise staff |
| Retrieval-induced bias | Context sources inject organizational or cultural bias into outputs | Governance focuses on model, not corpus governance | Vulnerable groups, customers, citizens |
| Tool-enabled escalation | Safe-seeming chatbot behavior becomes harmful when coupled to action tools | Security reviews separated from policy reviews | Third parties, customers, infrastructure |
| Memory-based personalization | Persistent memory changes persuasion profile or treatment | Privacy and fairness assessments conducted separately | Individuals subject to tailored influence |
| Shared-responsibility evasion | Each actor blames another layer | No integrated accountability record | Public, auditors, oversight bodies |

NIST’s AI RMF is strongest among the cited frameworks in articulating an organizational obligation to define **roles, responsibilities, risk tolerances, and accountability lines** across the lifecycle ([1](https://www.toxsec.com/p/ai-governance-requirements-2026), [2](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf)). Yet because the RMF is broad and voluntary, it often leaves unresolved how precisely responsibilities should be allocated in multivendor deployments. In practice, enterprises frequently adopt a “vendor assurance plus internal policy” model that is too thin for behavioral governance. Vendor documentation covers model safety in the abstract; internal policy covers acceptable use; neither captures the emergent behavior of the composed system.

Singapore’s framework is more explicit than many soft-law instruments in calling for a **trusted ecosystem** and collaboration among policymakers, industry, researchers, and like-minded jurisdictions ([4](https://aiverifyfoundation.sg/wp-content/uploads/2024/05/Model-AI-Governance-Framework-for-Generative-AI-May-2024-1-1.pdf)). That ecosystem framing is valuable because it recognizes that accountability cannot be reduced to a single firm. However, ecosystem language can also blur direct responsibility if not paired with operational obligations for specific actors. The challenge is to avoid replacing clear duties with diffuse stakeholder rhetoric.

One practical implication is that organizations need governance artifacts that correspond to the actual layers where persona and value encoding are decided. At minimum, a mature deployment should maintain:

- a **model provenance register** identifying all upstream providers and versions;
- a **behavioral policy register** documenting constitutional principles, system prompts, refusal rules, escalation thresholds, and localization adjustments;
- a **retrieval and memory register** describing what contextual sources can influence normative outputs;
- a **tool authority matrix** linking behavioral roles to permissible actions;
- a **change log** for prompt and policy modifications;
- a **contestability channel** for internal staff and external users to report problematic persona behavior;
- a **cross-layer incident taxonomy** distinguishing whether failures stemmed from model alignment, prompt design, retrieval, tool use, memory, or user manipulation.

These records are not uniformly mandated by any one framework, but they can be inferred as good practice from the combined logic of NIST risk governance, Singapore’s accountability and transparency principles, OWASP threat modeling, and EU documentation and monitoring obligations ([2](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf), [4](https://aiverifyfoundation.sg/wp-content/uploads/2024/05/Model-AI-Governance-Framework-for-Generative-AI-May-2024-1-1.pdf), [5](https://www.imda.gov.sg/-/media/imda/files/about/emerging-tech-and-research/artificial-intelligence/mgf-for-agentic-ai.pdf), [6](https://eur-lex.europa.eu/eli/reg/2024/1689)).

There is also an unresolved institutional issue concerning **who has authority to alter machine character**. In many enterprises, prompt engineers, safety teams, product managers, regional compliance teams, and customer-experience leaders all possess partial ability to change behavioral outputs. Yet these changes may not be reviewed by bodies with ethical, legal, or public-interest competence. The practical result is that machine “character” can be modified through routine product iteration rather than deliberate governance. This is a significant power asymmetry: small internal teams can redefine how millions of people experience authority, empathy, caution, or deference in machine interaction with limited external scrutiny.

The political salience becomes even sharper when LLMs mediate access to institutional services. A public-sector assistant configured to be highly deferential to official policy, minimally disclosive about uncertainty, and resistant to normative challenge could subtly narrow democratic contestation. Conversely, a healthcare triage assistant tuned for liability minimization may become so risk-averse and impersonal that it systematically disadvantages those with lower literacy or culturally different help-seeking norms. Neither problem is captured fully by conventional “accuracy” metrics.

Recent political-theory-oriented work on AI governance opacity suggests that as capability asymmetries grow, disclosure-based remedies lose traction because the governed system can game evaluation or become embedded inside governance processes themselves ([10](https://arxiv.org/list/cs/new)). While that paper is not a regulatory instrument, its argument is highly relevant: in advanced LLM deployments, accountability cannot rely solely on transparency artifacts if the practical determinants of behavior are dynamic, distributed, and manipulable. This strengthens the case for external assurance, runtime testing, and institutional contestability rather than disclosure alone.

For this reason, behavioral control governance should be understood as requiring at least three distinct accountability linkages:

1. **Vertical accountability**: between internal product teams and executive/board oversight.
2. **Horizontal accountability**: across vendors, integrators, deployers, and security teams.
3. **Public accountability**: to users, regulators, affected groups, and where relevant democratic institutions.

Current frameworks offer pieces of these linkages but do not yet fully integrate them. The practical governance frontier is therefore not another abstract principle set, but mechanisms that make compositional responsibility visible and enforceable.

## Comparative Architecture of the Main Frameworks and Mechanisms

### Constitutional rule-setting, NIST controls, Singapore soft law, OWASP security guidance, and EU legal duties

The frameworks named in the prompt operate at different levels of abstraction and authority. Their significance lies less in direct equivalence than in the way they collectively shape how organizations govern LLM behavioral persona. A comparative mapping helps clarify where each framework contributes and where key gaps remain.

| Instrument | Type | Formal authority | Primary scope | Behavioral relevance |
|---|---|---|---|---|
| Constitutional AI governance | Alignment methodology/governance pattern | Private-sector technical-governance approach | Training and response shaping via principle sets | Directly shapes refusal, harmlessness, conversational ethics |
| NIST AI RMF + GenAI profile | Risk management framework | Voluntary, influential via procurement and assurance | Enterprise AI governance lifecycle | Requires structured management of GenAI behavior risks |
| Singapore Model AI Governance Framework for Generative AI | Government-backed soft law/model framework | Non-binding but policy-signaling and ecosystem-shaping | Trusted adoption of GenAI across sectors | Links accountability, transparency, safety, provenance, and stakeholder trust |
| OWASP GenAI / agentic security guidance | Security best-practice guidance | Voluntary, practitioner-driven | LLM application, agent, and system security | Addresses behavioral subversion, tool misuse, memory and prompt threats |
| EU AI Act | Binding regulation in EU | Legal obligation where applicable | AI systems, GPAI models, high-risk uses, prohibited uses | Indirectly but materially shapes acceptable deployed behavior via compliance duties |

#### A. Constitutional AI governance as proceduralized value encoding

Constitutional AI governance deserves attention because it is one of the clearest examples of **behavioral rule externalization**. Rather than only relying on human preference labels, constitutional approaches define an explicit set of normative principles against which the model critiques and revises its own outputs. Anthropic’s published account framed the approach around harmlessness from AI feedback, using a constitution made up of principles drawn from sources such as public norms and human rights-oriented guidance ([7](https://www.anthropic.com/news/constitutional-ai-harmlessness-from-ai-feedback)). The governance significance is fourfold.

First, it creates a textual artifact—the “constitution”—that can in principle be reviewed, debated, versioned, and audited. This is a major improvement over entirely opaque reward modeling because it makes norm selection more legible.

Second, it changes the locus of accountability. The key governance question is no longer only whether annotators preferred one output over another, but who selected the governing principles and why.

Third, it introduces a structure for managing conflicts among values, such as harmlessness versus helpfulness, or user autonomy versus paternalistic refusal.

Fourth, it offers a bridge from internal alignment engineering to external governance by making it at least conceptually possible to compare constitutions across providers or contexts.

Yet constitutional AI governance also has serious limitations as a public governance mechanism. Provider-authored constitutions may be more legible than opaque RLHF pipelines, but they are still often drafted by private actors without broad democratic or cross-cultural legitimacy. Moreover, the public text of a constitution may not fully determine deployed behavior once it is filtered through hidden system prompts, moderation heuristics, or enterprise wrappers. Constitutional governance thus improves inspectability while still leaving substantial room for unilateral corporate norm-setting.

From an institutional-analysis perspective, constitutional AI can be understood as a **private administrative law for model behavior**: a set of internal principles, operationalized through repeatable procedures, producing quasi-public effects at scale. This is governance-relevant because millions of users may effectively interact not with a neutral interface but with a privately drafted moral-communicative regime.

#### B. NIST AI RMF and the Generative AI profile

NIST’s AI Risk Management Framework (“AI RMF 1.0”) structures AI governance around four functions—**Govern, Map, Measure, Manage**—and has become a baseline reference in U.S. public procurement and enterprise assurance discourse ([2](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf)). The subsequent **Generative AI Profile** extends this architecture to GenAI-specific issues, including synthetic content, confabulation, information hazards, CBRN-related misuse concerns, privacy leakage, and sociotechnical deployment risks ([3](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf)). Secondary compliance commentary correctly notes that the “Govern” function is the chokepoint because it requires organizations to establish documented ownership structures, risk tolerances, and accountability lines for AI decisions ([1](https://www.toxsec.com/p/ai-governance-requirements-2026)).

For behavioral control, NIST’s contribution is not a substantive value code but a governance operating system. Its relevance lies in several demands:

- organizations should define **governance structures** and accountability;
- they should **map context**, intended use, and affected stakeholders;
- they should **measure** risks and validity under real deployment conditions;
- they should **manage** and respond to identified risks over time.

This architecture is especially useful for deployed LLM persona because it forces organizations to treat behavior as context-dependent. An LLM’s “helpful” style in a consumer brainstorming app is not equivalent to “appropriate” behavior in legal information support, education, workplace assistance, or public services. The RMF thereby resists the idea that one provider-level alignment profile is sufficient across all domains.

The Generative AI Profile is also important because it recognizes that GenAI systems can cause harm through **persuasiveness, false authority, and synthetic interaction effects**, not merely through discrete classification errors. That orientation better fits concerns about persona and value encoding. However, NIST remains intentionally non-prescriptive regarding what moral values should be encoded. It focuses on process quality, risk identification, and management maturity rather than imposing a substantive behavioral norm.

This procedural orientation is both a strength and a weakness. It is a strength because it accommodates pluralism and sectoral variation. It is a weakness because organizations with mature-seeming governance processes can still encode highly contestable personas, provided they document and manage the associated risks. NIST can tell an institution to have an accountability mechanism; it cannot decide whether the chosen machine character is democratically legitimate or culturally fair.

#### C. Singapore’s 2024 Model AI Governance Framework for Generative AI

Singapore’s **Model AI Governance Framework for Generative AI**, released in May 2024, explicitly responds to the fact that generative AI reinforces legacy AI risks while introducing new risks such as hallucination, copyright infringement, and value alignment ([4](https://aiverifyfoundation.sg/wp-content/uploads/2024/05/Model-AI-Governance-Framework-for-Generative-AI-May-2024-1-1.pdf)). It positions its nine dimensions as a basis for global conversation and emphasizes accountability, transparency, fairness, robustness, security, and collaboration among policymakers, industry, researchers, and like-minded jurisdictions ([4](https://aiverifyfoundation.sg/wp-content/uploads/2024/05/Model-AI-Governance-Framework-for-Generative-AI-May-2024-1-1.pdf)).

This framework matters for behavioral control in three distinctive ways.

First, it explicitly situates generative AI governance within a **trusted ecosystem** rather than a narrow compliance model. That ecosystem framing is particularly apt for LLM persona because values are mediated by developers, deployers, users, and institutional context, not just by technical design.

Second, Singapore’s approach tends to combine governance principles with implementation-oriented tooling and assurance initiatives, including links to **AI Verify** and later ecosystem efforts such as the Global AI Assurance Pilot referenced in legal commentary ([11](https://www.twobirds.com/en/insights/2026/singapore/singapore-introduces-new-model-ai-governance-framework-for-agentic-ai)). This makes the framework more operational than many principle-only statements.

Third, by acknowledging value alignment among generative AI risks, the framework implicitly recognizes that trustworthiness is not exhausted by factual accuracy or cybersecurity. The style and normative structure of outputs are governance-relevant.

Even so, Singapore’s framework remains soft law. It exerts influence through signaling, convening, and assurance ecosystems rather than direct legal compulsion across the economy. Its effectiveness therefore depends on whether organizations internalize its expectations into procurement, governance committees, testing regimes, and documentation.

#### D. OWASP GenAI and agentic security guidance

OWASP’s contribution is often underestimated because it is framed as security guidance, but for deployed LLM behavior it is foundational. Behavioral persona can be **subverted** or **amplified** through security failures: prompt injection can override system rules; insecure output handling can produce unauthorized actions; tool misuse can turn persuasive language into operational harm; memory poisoning can alter a model’s future conduct; multi-agent orchestration can create emergent failure pathways. OWASP’s LLM and agentic guidance therefore addresses the conditions under which nominal behavioral policies fail in practice.

The IMDA document on a new **Model Governance Framework for Agentic AI** cites OWASP’s “State of Agentic AI Security and Governance 1.0,” “Agentic AI – Threats & Mitigations,” and “Multi-Agentic System Threat Modelling Guide,” indicating how central OWASP has become in practical governance discussions around agents ([5](https://www.imda.gov.sg/-/media/imda/files/about/emerging-tech-and-research/artificial-intelligence/mgf-for-agentic-ai.pdf)). The governance relevance is that OWASP focuses on **runtime integrity of policy enforcement**. A constitution or enterprise policy may say the model must not exfiltrate secrets, obey untrusted tool outputs, or take uncontrolled actions. OWASP asks whether the architecture actually prevents those outcomes.

This is vital because many harms attributed to “model misbehavior” are really failures of **guardrail integrity**. An enterprise assistant that adopts an abusive tone after a prompt injection incident is not simply badly aligned; it is insecurely governed. Security therefore becomes a constitutive part of behavioral governance, not an adjacent concern.

OWASP’s security-centric lens does, however, leave some gaps. It is strongest on adversarial manipulation and system compromise, but weaker on the legitimacy of the underlying behavioral norms. A perfectly secure model can still embody paternalistic, culturally narrow, politically biased, or manipulative design choices. Thus OWASP is necessary but insufficient for governance of value encoding.

#### E. EU AI Act obligations relevant to deployed behavior

The **EU AI Act** is the most legally consequential instrument in this field as of April 2026, although its relevance to LLM persona depends on the system category and role of the actor involved ([6](https://eur-lex.europa.eu/eli/reg/2024/1689)). It is not a “behavioral persona regulation” in explicit terms, but several obligations directly affect deployed behavior and risk management.

For **high-risk AI systems**, the Act requires a risk management system, data and data governance measures, technical documentation, automatic logging, transparency to deployers, human oversight, and appropriate levels of accuracy, robustness, and cybersecurity. These obligations matter because a deployed LLM used in a high-risk context cannot simply exhibit whatever persona product teams prefer; its behavior must be supportable within a documented risk management and oversight structure.

For **general-purpose AI (“GPAI”) models**, including models with systemic risk, the Act imposes obligations around technical documentation, information provision to downstream providers, copyright-policy compliance, and for systemic-risk GPAI, model evaluation, adversarial testing, risk mitigation, serious incident reporting, and cybersecurity. These obligations are relevant to behavioral control because downstream deployers need information about model limitations and safety characteristics to govern final behavior. Upstream documentation also affects whether enterprises can meaningfully assess normative fit and residual risks.

For certain AI-enabled interactions, the Act contains **transparency obligations**, including disclosure where users interact with AI in relevant circumstances and labeling of certain synthetic content. While these do not regulate persona content directly, they affect the social conditions under which persona is experienced by users.

The Act also prohibits certain harmful uses, including some manipulative or exploitative practices and some social scoring configurations, which can implicate deployed behavioral design where systems are built to unduly influence or exploit vulnerabilities. This is particularly relevant for persuasive personas and tailored affective interaction.

The key point is that the EU AI Act governs behavior **indirectly through obligations on risk systems, documentation, oversight, monitoring, and prohibited effects**. It does not tell providers whether a machine should sound warm, formal, deferential, or pluralistic. But it does require organizations in scope to show that the system’s real-world behavior is bounded by lawful governance processes and does not produce prohibited or unmanaged risks.

## Regulatory Pressure Points for Behavioral Persona and Value Encoding

### Where current frameworks actually constrain deployed conduct

A recurrent analytical mistake is to ask whether a framework “covers persona” in explicit language. Most do not. The more useful question is: **through which obligations or controls can they constrain the behavioral outputs and value expression of deployed LLM systems?** On that basis, several pressure points can be identified.

### 1) Documentation duties as indirect behavioral regulation

Documentation is often dismissed as procedural, but in the LLM context it can be one of the main levers for behavioral governance. If an organization must document intended purpose, limitations, risks, oversight arrangements, technical architecture, and post-deployment updates, it becomes harder to treat persona-shaping elements as informal or invisible.

The EU AI Act’s technical documentation requirements are a direct example ([6](https://eur-lex.europa.eu/eli/reg/2024/1689)). Although Annex-level obligations differ by system type, the overall logic is that providers of regulated systems must maintain enough documentation to demonstrate compliance and enable competent authorities to assess the system. In practice, this creates pressure to document the conditions under which outputs are generated, including risk controls and oversight design.

NIST AI RMF similarly encourages documentation of governance structures, risk tolerance, and context-specific controls ([2](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf)). Singapore’s framework, while not mandatory, points in the same direction by emphasizing transparency and accountability in a trusted ecosystem ([4](https://aiverifyfoundation.sg/wp-content/uploads/2024/05/Model-AI-Governance-Framework-for-Generative-AI-May-2024-1-1.pdf)).

Yet ordinary model cards are too thin for this purpose. They generally document model properties, not deployment-specific behavioral overlays. This is where proposals such as **risk cards** and **BBOM-style artifacts** become useful. Risk cards aim to present use-case-specific risk information in a more operational form than model cards; BBOM goes further by documenting behavioral capabilities, constraints, tool interfaces, memory design, and decision boundaries ([9](https://techjacksolutions.com/ai/agentic-ai/govern/behavioral-bill-of-materials/)). The governance significance is that they make it possible to ask concrete questions such as:

- What values govern refusal behavior?
- Under what conditions is the assistant allowed to be persuasive?
- Which tool calls can the model initiate autonomously?
- What memory persists and how does it affect future tone or recommendations?
- What context sources can alter the model’s normative stance?
- How are these settings localized across jurisdictions and cultures?

Without such records, accountability remains abstract.

### 2) Human oversight requirements as limits on machine character

Human oversight provisions, particularly under the EU AI Act for high-risk systems, are often read as requiring a human-in-the-loop checkpoint. But for behavioral governance they have a deeper implication: organizations must ensure that humans can **understand, monitor, and intervene** in system behavior before or after use where appropriate ([6](https://eur-lex.europa.eu/eli/reg/2024/1689)). This means the machine’s persona cannot be designed as an unquestionable authority beyond meaningful operator correction.

In practice, this has consequences for how systems present certainty, deference, and escalation. A high-risk or sensitive-domain LLM that projects excessive confidence, suppresses uncertainty, or discourages escalation to human channels may undermine the very possibility of effective oversight. Thus, behavioral design features become relevant to compliance, even if not named as such.

Singapore’s trust-oriented framing similarly suggests that users should be able to understand and appropriately rely on AI outputs within a transparent governance structure ([4](https://aiverifyfoundation.sg/wp-content/uploads/2024/05/Model-AI-Governance-Framework-for-Generative-AI-May-2024-1-1.pdf)). A persona that masks limitations or projects unwarranted empathy or authority is therefore at odds with the spirit of trusted deployment.

### 3) Security controls as preservation of behavioral boundaries

OWASP guidance shows that behavioral governance is impossible without security controls preserving the integrity of system instructions and trust boundaries. Prompt injection, retrieval poisoning, tool forgery, plugin abuse, insecure output execution, and memory manipulation all allow attackers or users to alter the model’s behavior outside authorized governance channels. This effectively privatizes machine character to whoever can manipulate context most successfully.

By centering threat modeling for multi-agent and tool-enabled systems, OWASP makes clear that “persona control” is inseparable from **policy integrity** ([5](https://www.imda.gov.sg/-/media/imda/files/about/emerging-tech-and-research/artificial-intelligence/mgf-for-agentic-ai.pdf)). An organization may think it has encoded a balanced and lawful assistant persona, but if untrusted documents can inject instructions that reverse safety or compliance boundaries, the true governor of behavior is the attacker.

This has regulatory implications. Under the EU AI Act, cybersecurity and robustness are compliance duties for covered systems ([6](https://eur-lex.europa.eu/eli/reg/2024/1689)). Under NIST AI RMF, adversarial resilience and operational risk management are part of responsible AI governance ([2](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf), [3](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf)). Security failures are therefore not separate from governance failures.

### 4) Post-deployment monitoring and incident reporting

Behavioral persona is not fixed at release. It drifts through model updates, prompt changes, shifting user populations, retrieval corpus evolution, adversarial adaptation, and localization experiments. Governance frameworks increasingly require or strongly encourage **ongoing monitoring** rather than one-time approval.

The EU AI Act


## Documentation and Assurance Instruments for Behavioral and Value Transparency

### Comparative design logic of transparency artifacts

While the prior report already noted that ordinary model cards are often too thin for deployment-specific behavior and that BBOM-style proposals can bridge from model transparency to behavioral transparency, this section goes further by comparing these instruments as distinct assurance technologies: what each artifact makes legible, who it is for, what stage of the lifecycle it addresses, and where it fails when persona is produced by layered vendor, enterprise, and user configurations.

A central governance difficulty for deployed LLM systems is that “behavior” is not a single property. It spans at least five partially separable objects: (1) model-internal tendencies shaped by pretraining and alignment, (2) policy-level refusal and safety rules, (3) interface and orchestration design, (4) tool-use permissions and action channels, and (5) contextual steering by prompts, retrieval, memory, and user interaction. Documentation instruments differ in which of these objects they render visible. For that reason, no single artifact currently functions as a complete transparency device for value encoding in deployed systems. The practical question is therefore not whether model cards, risk cards, behavioral bills of materials, audits, or post-market monitoring are individually sufficient, but how they can be layered into a disclosure-and-assurance stack that tracks the migration of normative control from model development to runtime deployment.

Table I compares the main documentation and assurance instruments now relevant to this problem.

| Instrument | Primary unit of analysis | Main audience | Typical contents | Strength for value/behavior transparency | Main limitation in compositional deployments |
|---|---|---|---|---|---|
| Model card | Model or model family | Developers, deployers, researchers, procurement actors | Intended use, limitations, evaluation metrics, training data descriptions, ethical/safety considerations | Useful for upstream baseline properties and declared limits | Poor at capturing downstream prompts, tools, memory, organization-specific personas |
| System card | Specific AI system or product release | Public, regulators, enterprise customers | System behavior, mitigations, testing, rollout constraints, known failures | Better than model cards for deployment framing | Often curated by provider; may omit enterprise modifications or runtime adaptation |
| Risk card | Use-case-specific deployment context | Risk, compliance, business owners, auditors | Hazard scenarios, affected stakeholders, controls, residual risk, escalation conditions | More operational for downstream deployment decisions | Depends heavily on local risk analysis quality; can fragment across teams |
| Behavioral Bill of Materials (BBOM) proposal | Executable agent/application stack | Integrators, security teams, auditors, incident responders | Prompts/policies, tool permissions, memory, orchestration, action boundaries, failure modes, dependencies | Strongest candidate for behavioral surface transparency in agentic systems | Not standardized; difficult to maintain under continuous updates |
| Audit report / assurance attestation | Governance process, model, or deployed application | Regulators, procurers, boards, independent assurance bodies | Scope, methods, findings, evidence, nonconformities, corrective actions | Converts disclosure into third-party-checked claims | Scope can be narrow; evidence access may be restricted by secrecy and vendor power |
| Post-market monitoring log / incident register | Deployed system in operation | Providers, deployers, regulators, safety teams | Performance drift, incidents, complaints, abuse patterns, corrective actions | Captures actual behavior after release rather than anticipated behavior only | Monitoring categories often underdeveloped for value/persona harms, especially cultural harms |

The comparative logic in Table I matters because deployed LLM governance is moving from static artifact disclosure toward chain-of-custody disclosure. A model card asks what the model is. A risk card asks what can go wrong in a particular use. A BBOM asks what the assembled system can perceive, remember, decide, and do. An audit asks whether any of those claims have been independently tested. Post-market monitoring asks whether the documentation matched reality after exposure to users, adversaries, and changing contexts. This progression tracks a broader shift in AI governance toward lifecycle accountability, reflected in the [OWASP GenAI Security Project](https://genai.owasp.org/), NIST-oriented assurance discussions, and EU compliance expectations for documentation, monitoring, and risk management even where the law does not expressly regulate “persona” as such ([1](https://genai.owasp.org/), [2](https://storage.ghost.io/c/44/95/449506ca-034e-480f-9725-fcde08ef1cc1/content/files/2026/03/AI-Risk-Management-Framework-Measure-Function.pdf?ref=aigl.blog), [3](https://digital.nemko.com/news/navigating-the-owasp-top-10-for-llm-applications-2025)).

The persistence of compositional deployment complicates all these instruments. In practice, many enterprise systems are assembled from a frontier model API, middleware, retrieval infrastructure, organization-authored prompts, safety filters, and user-facing workflow rules. The emergent persona is then not coextensive with any single component. This means a provider-issued model card can be accurate yet governance-incomplete, because it describes upstream tendencies but not the enterprise role-script that tells the assistant to prioritize retention, conceal uncertainty, or redirect complaints away from human review. Likewise, a risk card can accurately identify local harms while failing to disclose upstream constitutional choices that encode culturally specific assumptions about civility, political neutrality, or acceptable refusal behavior. A BBOM can expose runtime permissions while leaving unresolved who is normatively accountable for the values embedded in system prompts inherited from a vendor safety template.

This is not merely a documentation nuisance; it is a political allocation problem. Whoever controls the documentation format also shapes what is governable. Model cards historically arose from ML transparency debates focused on training data, benchmark performance, and intended use. They were not designed to expose institutionally significant questions such as: Which moral principles anchor refusal behavior? Which populations shaped preference data? Under what conditions does the assistant defer to local legal-cultural context rather than universalized provider policy? How does the system rank values such as politeness, safety, autonomy, anti-deception, ideological neutrality, or public-order concerns when these conflict? The more persona and behavioral style become policy instruments in their own right, the more documentation must evolve from technical description to normative traceability.

A useful analytic distinction is between **descriptive transparency**, **normative transparency**, and **operational transparency**. Descriptive transparency covers what the artifact is and how it was built. Normative transparency covers whose values, policy hierarchies, and assumptions shaped behavior. Operational transparency covers what the system can do in context. Model cards are comparatively strong on descriptive transparency; risk cards often improve operational contextualization; BBOM-style proposals most directly target operational transparency; and none of them, by default, robustly guarantee normative transparency. Yet normative transparency is indispensable for the report’s main topic, because the political controversy around deployed LLM persona is not only about security or error rates, but also about whose moral defaults are embedded at scale.

The current literature on cultural bias reinforces this point. Evidence from cross-national evaluations indicates that widely deployed LLMs can express values that resemble English-speaking and Protestant European countries, even when presented as general-purpose assistants; cultural prompting improves alignment for many jurisdictions but does not eliminate the underlying skew ([4](https://pmc.ncbi.nlm.nih.gov/articles/PMC11407280/)). Comparative work on China-origin and Western-origin systems similarly suggests that neither regional development pathway currently achieves robust cross-cultural generalization, and that stable, context-sensitive value alignment remains unresolved ([5](https://arxiv.org/html/2511.17256v1)). Documentation artifacts that omit cultural provenance, annotator composition, constitutional rule provenance, or region-specific adaptation logic therefore obscure one of the most governance-relevant determinants of deployed behavior.

This problem becomes sharper when one considers scale. A single corporate provider can distribute one “helpful, harmless, honest” persona, or one safety-optimized refusal style, across millions of organizations and hundreds of millions of end users. Enterprise deployers then inherit a behavioral substrate that they partly customize but rarely fully interrogate. The asymmetry is twofold: first, providers possess much more information about the alignment pipeline than downstream actors; second, users are often exposed to persona decisions without knowing whether they arise from law, policy, market incentives, or the vendor’s normative preferences. Existing documentation formats do little to resolve this asymmetry unless they are redesigned to expose provenance of behavioral constraints and their justifications.

For this reason, value and behavior transparency instruments should be evaluated along at least seven dimensions:

1. **Provenance**: who authored the behavioral rules or training preferences.
2. **Granularity**: whether they document the model, the system, the use case, or the live stack.
3. **Update discipline**: whether changes are versioned and attributable.
4. **Normative traceability**: whether competing values and tradeoffs are disclosed.
5. **Actionability**: whether the artifact supports operational intervention by deployers or auditors.
6. **Contestability**: whether affected parties can challenge behavioral choices.
7. **Interoperability**: whether the artifact can be integrated into assurance workflows, procurement, or regulation.

Table II applies these dimensions comparatively.

| Instrument | Provenance visibility | Granularity | Update discipline | Normative traceability | Actionability | Contestability | Interoperability |
|---|---|---|---|---|---|---|---|
| Model card | Medium for training/evaluation provenance; low for downstream prompts | Model-level | Usually release-based | Low to medium | Medium for procurement/screening | Low | Medium |
| System card | Medium | Product/system-level | Release-based, sometimes staged | Medium if candid about mitigations and policy choices | Medium | Low to medium | Medium |
| Risk card | Medium to high if tied to business owner and context | Use-case-level | Better suited to iterative updates | Medium to high if structured properly | High for deployment governance | Medium within organization | Medium |
| BBOM proposal | High potential if signed and versioned | Full runtime stack | Potentially continuous | Medium to high, depending on schema | High for security and control verification | Medium | Low today, potentially high if standardized |
| Independent audit attestation | Depends on audit access and scope | Variable | Periodic | Medium if methods/public reporting are strong | High for oversight escalation | Medium to high | High in regulated/procurement settings |
| Post-market monitoring file | High for operational changes if maintained rigorously | Deployed instance/fleet | Continuous | Often low unless incidents are classified in normative terms | High for corrective action | Medium if complaint channels exist | High if linked to compliance systems |

From an institutional-design perspective, the most important point is that these artifacts should not be treated as substitutes. A mature governance regime for LLM behavioral transparency would likely require at least one upstream descriptive artifact, one deployment-specific risk artifact, one runtime-architecture artifact, one independent assurance process, and one post-market feedback loop. This is already implicit in several sources. The [OWASP GenAI Security Project](https://genai.owasp.org/) combines risk taxonomy, governance guidance, and threat intelligence rather than relying on a single checklist ([1](https://genai.owasp.org/)). The “three-layered approach” to auditing LLMs expressly argues that governance audits, model audits, and application audits must complement one another because no single layer captures the whole risk surface ([6](https://arxiv.org/html/2302.08500), [7](https://arxiv.org/pdf/2302.08500)). Emerging compliance-as-code discussions similarly emphasize that policy, evidence, and enforcement need machine-readable linkages rather than isolated PDF disclosures ([8](https://arxiv.org/list/cs/new)).

The unresolved issue is standardization. Model cards and system cards have recognizable though variable conventions. Risk cards are less standardized but increasingly legible to governance and assurance practitioners. BBOM remains conceptually powerful but institutionally immature. Without common schemas, attestations, versioning norms, and update obligations, behavioral transparency remains too discretionary to support serious external accountability. In effect, many current artifacts are closer to governance communications than governance infrastructure.

### Model cards, risk cards, and system cards as partial windows into machine character

This section is distinct from the earlier discussion of “documentation duties as indirect behavioral regulation.” Instead of focusing on documentation as a generic regulatory lever, it examines the substantive representational limits of specific card-based instruments when the object of governance is machine character, value prioritization, and role performance in context.

#### A. Model cards: baseline disclosure without deployment-legible persona mapping

Model cards were originally proposed to provide structured information about ML models’ intended uses, performance characteristics, and limitations. In the LLM setting, they remain useful for upstream evaluation disclosure: benchmark results, training-data broad characteristics, known limitations, unsupported uses, and high-level safety notes. They are particularly valuable for procurement and internal model selection because they reduce informational asymmetry at the point where an enterprise chooses among vendors or decides whether a model is suitable for a domain.

Yet, as a transparency instrument for value encoding, model cards encounter three structural weaknesses.

First, they typically describe **capabilities and constraints**, not **normative policy hierarchies**. A model card may state that the model avoids harmful, illegal, or misleading outputs. It rarely specifies how the model balances dignity against autonomy, false-positive safety refusals against informational access, or universalized content rules against regional cultural norms. This matters because many disputes over LLM behavior concern overblocking, paternalism, ideological style, or culturally mismatched refusals rather than straightforward malfunction.

Second, model cards often present **aggregate or canonical behavior**, not **conditional behavior under layered control**. In an enterprise deployment, the user may interact not with the canonical provider model but with a role-constrained assistant instructed to comply with organization policy, use certain tools, adopt a specific tone, and avoid statements that increase legal liability. The persona that users actually encounter is therefore downstream of the object documented in the model card.

Third, model cards are weak on **update traceability**. Providers regularly alter safety behavior, refusal thresholds, and moderation interactions through silent or semi-silent updates. If the card is updated only episodically, it ceases to be a reliable behavioral artifact. Users and deployers may thus face changing machine character without a clear changelog of what shifted, why, for whose benefit, and with what tradeoffs.

These shortcomings are increasingly recognized in practice. Even security-centered sources now frame LLM governance as requiring more than perimeter security and more than static documentation. The Nemko discussion of the [OWASP Top 10 for LLM Applications 2025](https://digital.nemko.com/news/navigating-the-owasp-top-10-for-llm-applications-2025) emphasizes that securing AI requires comprehensive governance standards and security-by-design adapted to generative systems, implicitly acknowledging that ordinary software-style disclosure does not capture the real attack and failure surface ([3](https://digital.nemko.com/news/navigating-the-owasp-top-10-for-llm-applications-2025)).

A governance-relevant refinement would be to require model cards for advanced LLMs to contain a dedicated **behavioral provenance annex** with at least: (i) broad descriptions of alignment methods; (ii) categories of human annotators or preference data sources used in safety tuning; (iii) known cultural or linguistic asymmetries in safety performance; (iv) categories of hard policy rules that override contextual flexibility; and (v) a statement of what aspects of behavior are expected to change downstream through system prompting, tool use, or enterprise policy overlays. Such an annex would not solve deployment opacity, but it would improve handoff integrity between provider and deployer.

#### B. Risk cards: contextualizing harms, but only if value conflicts are named explicitly

Risk cards emerged partly because model-level transparency is too abstract for concrete deployment decisions. A risk card is typically use-case-specific and hazard-oriented: what can go wrong in this particular context, who may be harmed, how severe the impact is, what mitigations exist, what residual risk remains, and when escalation or withdrawal is required. This format is better suited than model cards to domains where persona and communication style materially affect outcomes—for example, mental-health support, educational advising, human resources screening support, customer complaint handling, or public-service assistance.

For behavioral governance, the principal strength of risk cards is that they force actors to specify **contextual stakes**. A system configured as a “supportive wellness coach” and one configured as a “collections assistant” may use the same underlying model, yet the first raises concerns around emotional dependency, false reassurance, and inappropriate pseudo-therapy, while the second raises concerns around coercive persuasion, opacity about rights, and exploitative behavioral targeting. A generic model card cannot capture this divergence; a risk card can.

However, risk cards only become genuinely informative for value transparency if they move beyond hazard enumeration to **value-conflict articulation**. In many organizations, risk templates are framed in terms of legal, operational, and reputational risk. That misses the core governance issue where deployed persona is concerned: the system may function as intended while still encoding contestable social values. An assistant that politely but systematically nudges users away from certain lawful political viewpoints, that consistently privileges a Western liberal framing of social issues, or that refuses culturally ordinary requests because they conflict with provider-trained moral assumptions may not trigger conventional “incident” categories. If the risk card does not ask about normative mismatch, representational exclusion, or cross-cultural intelligibility, those harms remain invisible.

Evidence on cultural bias indicates why this omission is serious. One study comparing OpenAI models against nationally representative survey data found that all evaluated models exhibited cultural values resembling English-speaking and Protestant European countries; cultural prompting improved alignment in 71–81% of countries and territories for later models, but improvement is not equivalent to neutrality or sufficiency ([4](https://pmc.ncbi.nlm.nih.gov/articles/PMC11407280/)). This suggests that any deployment intending to serve multiple populations should include risk-card fields such as: What cultural baseline does the assistant appear to assume? What localized prompting or policy adaptation has been validated? Which groups were consulted in evaluation? Under what conditions does the system defer to locally appropriate norms? What harms arise if users mistake provider values for neutral truth?

Without such fields, risk cards may overemphasize cybersecurity or legal compliance while underemphasizing symbolic or epistemic power. Yet the latter is central when corporate actors define machine character at population scale.

#### C. System cards: useful product-level framing, but vulnerable to curation bias

System cards occupy a middle ground between model cards and risk cards. They document a product or release rather than a base model in abstraction and may include safety mitigations, rollout constraints, domain limitations, and observed failure modes. For public-facing AI products, system cards can be more behaviorally informative than model cards because they recognize that orchestration, UI, and moderation layers alter outputs.

Still, as assurance instruments, system cards suffer from **curation bias**. They are usually authored by the provider of the system being described. Their narrative tends to foreground tested safeguards and known limitations, but not always the governance politics of the design choices. They may explain that the system refuses certain content or redirects users in sensitive domains, yet not disclose which values justified those thresholds, how many false positives were deemed acceptable, or whether external stakeholders contested those decisions. In other words, system cards can improve behavioral legibility without democratizing behavioral authority.

This is especially problematic where system cards are read as quasi-assurance documents by customers or the public. A system card is still a self-description unless independently verified. Its value is real, but its epistemic status should not be confused with audit evidence.

#### D. A comparative threshold for “behaviorally adequate” card-based disclosure

For deployed LLM governance, a card-based artifact should be considered behaviorally adequate only if it answers at least the following questions:

| Question | Why it matters |
|---|---|
| What role is the system instructed to perform? | Persona often follows role framing more than base capability |
| Which values or rules take priority when instructions conflict? | Reveals normative hierarchy |
| What classes of user vulnerability are anticipated? | Indicates whether power asymmetries are recognized |
| What tool actions can the system trigger or recommend? | Separates speech from consequential action |
| What memory or personalization features shape future responses? | Persona can become adaptive and relational |
| What cultural or regional assumptions were tested? | Prevents false claims of universality |
| What human override or complaint channels exist? | Essential for contestability |
| What changed from the previous version? | Machine character can drift silently |

Most current model cards do not meet this threshold. Some risk cards can. Some system cards partially can. The implication is that card-based disclosure remains necessary but not sufficient for serious behavioral governance.

### Behavioral bill-of-materials proposals and machine-readable compliance architectures

While prior sections referenced BBOM as a conceptual bridge from “what the model is” to “what the agent can do,” this section develops the idea in more institutional and technical detail, including its relationship to security governance, supply-chain visibility, and machine-readable assurance.

The analogy to a software bill of materials is deliberate. In cybersecurity, SBOMs became important because complex software products incorporate dependencies that create hidden risk transmission paths. Deployed LLM systems present an analogous, but behaviorally richer, dependency problem: the output persona and action profile may depend on the base model version, moderation API, system prompt, retrieval corpus, memory layer, tool schema, fallback rules, and external service permissions. A behavioral bill of materials seeks to make those dependencies visible in a structured way.

A mature BBOM schema would likely need to document at least six classes of components:

1. **Model dependencies**: base model(s), version identifiers, fine-tunes, adapters, safety model dependencies.
2. **Policy dependencies**: constitutions, rule lists, moderation policies, refusal templates, enterprise conduct rules.
3. **Context dependencies**: retrieval sources, ranking logic, memory stores, personalization signals, user segmentation logic.
4. **Action dependencies**: tool access, permissions, transactional authority, rate limits, approval gates.
5. **Orchestration dependencies**: agent frameworks, planner-executor chains, routing logic, multi-agent interactions.
6. **Assurance dependencies**: tests, red-team suites, guardrail validators, monitoring hooks, rollback conditions.

Such a schema would materially improve transparency for both security and governance purposes. The [OWASP GenAI Security Project](https://genai.owasp.org/) and related checklist efforts emphasize that risk in LLM applications often emerges from prompt injection, supply-chain vulnerabilities, excessive agency, data/model poisoning, and improper output handling rather than from the model in isolation ([1](https://genai.owasp.org/), [9](https://www.aigl.blog/llm-ai-cybersecurity-governance-checklist/), [3](https://digital.nemko.com/news/navigating-the-owasp-top-10-for-llm-applications-2025)). A BBOM directly supports those concerns because it inventories the pathways through which adversaries or misconfigurations can alter behavior.

The relevance of OWASP’s 2025 framing is especially clear here. As the 2025 Top 10 for LLM Applications highlights, the governing risk surface is broader than classic application security and includes emergent vulnerabilities specific to GenAI systems. Although the exact taxonomy is security-oriented, its governance implication is broader: organizations need asset inventories and control maps for the elements that actually shape model conduct in production ([10](https://genai.owasp.org/resource/owasp-top-10-for-llm-applications-2025/), [3](https://digital.nemko.com/news/navigating-the-owasp-top-10-for-llm-applications-2025)). A BBOM is one promising way to produce that map.

#### A. Why BBOM matters for value encoding, not just security

At first glance, BBOM may appear to be merely a technical security artifact. That reading is too narrow. In compositional LLM deployments, the same components that create security exposure also create normative exposure. For example:

- A retrieval corpus determines which institutional voice the assistant reproduces.
- A memory layer can make a “neutral assistant” become a personalized persuader.
- Tool permissions can convert advisory language into behaviorally consequential action.
- Escalation rules can determine whether the system acts deferentially toward human authority or presents itself as a quasi-autonomous decision-maker.
- Moderation policy hooks can impose a particular worldview about acceptable discourse, risk tolerance, or civility.

Thus, a BBOM can expose not only technical dependencies but also **governance loci**: where exactly values enter the stack. In a mature form, a BBOM should not merely enumerate artifacts; it should map each behaviorally significant component to an accountable owner, a rationale, an approval pathway, and a change history.

Table III sketches what such a governance-oriented BBOM might include.

| BBOM field | Example content | Governance value |
|---|---|---|
| Persona specification | “Customer support assistant prioritizing complaint de-escalation and policy-compliant retention” | Makes explicit the role and behavioral objective |
| Behavioral rule hierarchy | Legal compliance > user safety > enterprise policy > conversational helpfulness | Exposes normative ordering |
| Refusal and redirection policies | Categories of refusal, escalation to humans, emergency handling | Clarifies boundaries on autonomy |
| Tool/action manifest | CRM read/write, refund authority capped at \$50, email drafting only | Shows what the system can operationalize |
| Retrieval corpus sources | Internal policy manuals, public FAQs, region-specific legal database | Reveals epistemic dependence |
| Memory policy | Session only / persistent profile / vulnerability tagging prohibited | Addresses adaptive persona formation |
| Localization logic | Region-specific prompts for EU, India, MENA; fallback to default English policy | Exposes cultural adaptation design |
| Human control points | Mandatory supervisor approval for account closure or legal advice | Supports oversight |
| Monitoring triggers | Spike in refusal rates, regional complaint patterns, coercive language flags | Connects documentation to post-market vigilance |
| Change log | Prompt v4.2 adjusted to reduce overconfident claims in healthcare triage | Enables behavioral drift tracking |

A BBOM of this kind would do something current model cards rarely do: connect machine character to institutional decision rights. It would show whether the “voice” of the system comes from provider defaults, enterprise optimization, or sectoral compliance demands.

#### B. Standardization barriers and the risk of performative inventories

The case for BBOM is conceptually strong, but there are important barriers.

The first is **schema instability**. Unlike software dependencies, behavioral components are heterogeneous and partly interpretive. How should one represent a constitutional rule, a prompt policy, or a latent tendency induced by RLHF? Not all relevant influences are discrete modules. Some are probabilistic dispositions. This makes machine-readable standardization difficult.

The second is **commercial secrecy**. Providers may resist disclosing prompts, policy hierarchies, red-team findings, or moderation heuristics, claiming intellectual property or security concerns. Some of these concerns are legitimate. But excessive secrecy prevents deployers and regulators from assessing whether the persona they are inheriting is normatively appropriate for their context.

The third is **maintenance burden**. Deployed LLM stacks change constantly. If the BBOM is not automatically updated through CI/CD and configuration management, it quickly becomes stale. A stale behavioral inventory may be worse than none because it creates false confidence.

The fourth is **performative compliance**. Organizations may produce inventories that formally list components without making them decision-useful. A BBOM that says “safety policy module enabled” or “retrieval layer configured” but does not disclose scope, precedence, or failure conditions contributes little to accountability.

These barriers point toward the importance of machine-readable assurance systems. Emerging work on using OSCAL-like structures for AI assurance argues that policy, evidence, and enforcement can be linked so that compliance evidence is generated as a byproduct of system development and operation rather than compiled manually after the fact ([8](https://arxiv.org/list/cs/new)). Although this work is still early, its significance for behavioral governance is considerable. If prompts, policy files, tool manifests, test results, and monitoring hooks can be represented in machine-readable control structures, then documentation becomes auditable and version-controllable.

This also matters for the EU regulatory environment. The [EU AI Act](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32024R1689) is not a BBOM statute, but its documentation, logging, risk management, and post-market obligations create incentives for more structured evidence practices, especially for high-risk systems and GPAI-related compliance interfaces ([2](https://storage.ghost.io/c/44/95/449506ca-034e-480f-9725-fcde08ef1cc1/content/files/2026/03/AI-Risk-Management-Framework-Measure-Function.pdf?ref=aigl.blog)). Where GPAI models are embedded in [VLOPs/VLOSEs subject to the DSA](https://fsi9-prod.s3.us-west-1.amazonaws.com/s3fs-public/2024-12/GenAI_Report_REV_Master_%20as%20of%20Dec%2012.pdf), some AI Act obligations are presumed fulfilled through DSA risk-management structures unless significant uncovered systemic risks emerge; this is an example of how governance may increasingly depend on interoperable documentation across regimes rather than on single-purpose artifacts ([11](https://fsi9-prod.s3.us-west-1.amazonaws.com/s3fs-public/2024-12/GenAI_Report_REV_Master_%20as%20of%20Dec%2012.pdf)).

#### C. BBOM and the politics of behavioral provenance

One of the strongest normative arguments for BBOM is that it can make visible who has authority to define machine character. In many current deployments, that authority is distributed but not documented. A provider sets the default safety persona; an enterprise adds brand voice and compliance rules; a product team tunes conversion metrics; a security team restricts tools; and end users, through prompting, partially reshape outputs. The result is a layered constitution without a constitutional record.

A governance-oriented BBOM could provide that record. It would not automatically solve legitimacy questions, but it would make them concrete. Instead of debating in the abstract whether a chatbot is “biased,” stakeholders could inspect whether, for example, the enterprise selected a persuasion-optimized prompt template, imported a U.S.-centric safety policy into a non-U.S. market, or disabled uncertainty disclosures to reduce friction. This shifts oversight from generalized concern to attributable design choices.

### Layered auditing as a complement to disclosure artifacts

The prior report discussed the “three-layered approach” to LLM auditing primarily as a general governance mechanism. This section develops a narrower and more specific point: how layered auditing can function as the assurance backbone for behavioral and value transparency where cards and inventories are insufficient.

The basic insight of the three-layered approach is that different forms of audit answer different governance questions. Governance audits inspect organizational processes and accountability structures. Model audits examine performance, robustness, truthfulness, and security properties. Application audits assess downstream products and services in their real use context, including legal compliance and social impacts ([6](https://arxiv.org/html/2302.08500), [7](https://arxiv.org/pdf/2302.08500)). For value encoding and deployed persona, this architecture is especially useful because machine character can be altered at each layer.

#### A. Governance audit: who sets the values, by what process, with what legitimacy?

A governance audit is the natural place to examine constitutional or policy-setting processes. Questions here include:

- How are behavioral principles selected or revised?
- Which teams can alter refusal policies, moderation thresholds, or persona prompts?
- Are external stakeholders consulted for culturally sensitive applications?
- Is there board-level or senior governance oversight for population-scale persona changes?
- Are there documented rationales for balancing safety, autonomy, neutrality, and localization?
- Are incentives aligned, or do revenue teams effectively dominate behavior design?

These are not model-performance questions; they are institutional-accountability questions. They matter because value encoding is often upstream of technical execution. If a provider or enterprise has no documented process for selecting and revising machine conduct principles, downstream testing can identify symptoms but not correct the source of normative arbitrariness.

The governance audit is also where one should examine **pluralism capacity**. If the system is deployed across jurisdictions or communities with divergent norms, are there mechanisms for localized adaptation, stakeholder challenge, and escalation when default values are contested? Research on cross-cultural alignment underscores that no present paradigm can be presumed universally adequate, and that dynamic audit frameworks are necessary precisely because static single-step evaluations do not capture temporal instability and cultural divergence ([5](https://arxiv.org/html/2511.17256v1)).

#### B. Model audit: does the model exhibit latent value skew or unstable safety persona?

Model audits typically test technical properties, but for this report’s topic they should also probe behavioral tendencies and value expression. This means evaluating not only toxicity or jailbreak resistance, but also:

- consistency of refusal across languages and cultural framings;
- whether safety behaviors disproportionately reflect Western norms;
- susceptibility to prompt-induced shifts in moral stance;
- confidence calibration in ethically sensitive scenarios;
- differential treatment of culturally coded topics;
- persistence of harmful persuasion or deference patterns.

Empirical work suggests why such testing is needed. The comparative cultural-bias literature finds that major models often reflect Western cultural baselines and that prompting can modify but not eradicate these patterns ([4](https://pmc.ncbi.nlm.nih.gov/articles/PMC11407280/), [12](https://venturebeat.com/ai/large-language-models-exhibit-significant-western-cultural-bias-study-finds)). More recent comparative work indicates instability and incomplete cross-cultural generalization across both China-origin and Western-origin models ([5](https://arxiv.org/html/2511.17256v1)). A serious model audit should therefore include multilingual and cross-cultural suites, not merely English-centric red teaming.

This is also where some emerging threat-modeling work can be relevant, though it comes from a security perspective. The [AATMF mapping](https://www.researchgate.net/publication/400639053_Adversarial_AI_Threat_Modeling_Framework_AATMF_v3_Adversarial_AI_Threat_Modeling_Framework_Comprehensive_Security_Assessment_for_AI_Systems) of OWASP LLM Top 10 entries to adversarial tactics illustrates a broader point: structured technique catalogs make it easier to verify whether a model or system has actually been tested against known classes of failure, rather than merely described in prose ([13](https://www.researchgate.net/publication/400639053_Adversarial_AI_Threat_Modeling_Framework_AATMF_v3_Adversarial_AI_Threat_Modeling_Framework_Comprehensive_Security_Assessment_for_AI_Systems)). For behavioral governance, an analogous catalog of persona and value failure modes would improve audit rigor.

#### C. Application audit: what persona does the assembled system actually enact?

Application audits are the most important layer for compositional deployments because they assess the assembled product, not just the base model or provider process. This is where one can test the actual runtime persona under realistic prompts, retrieved content, memory effects, and tool access. It is also where one can observe interactions between commercial incentives and machine behavior.

For example, an application audit may reveal that:

- the enterprise prompt instructs the assistant to maximize user retention while appearing neutral;
- complaint-handling flows suppress disclosure of human appeal channels;
- retrieval grounding pulls from outdated or culturally narrow knowledge bases;
- personalization makes vulnerable users more susceptible to upselling;
- translated interfaces preserve provider refusals but lose culturally appropriate explanation styles;
- uncertainty warnings are disabled in order to create a smoother customer experience.

None of these issues is reliably inferable from a provider model card. Application audits are therefore the principal assurance mechanism for verifying whether the deployed system’s persona is acceptable in practice.

The “three-layered approach” explicitly argues that application audits should test legal compliance first and then evaluate downstream impacts on users, groups, and the environment ([7](https://arxiv.org/pdf/2302.08500)). For the present topic, one should add that application audits need to evaluate **behavioral legitimacy**: whether the system’s enacted persona is appropriate to the institutional role it occupies. A chatbot used in government services, education, finance, or healthcare carries quasi-public authority even if privately supplied. Its style of explanation, refusal, deference, and value-laden guidance is therefore not merely a UX choice.

#### D. Coordinated assurance: linking artifacts to audit evidence

The distinctive contribution of layered auditing is not just that it adds more tests; it creates a framework for reconciling inconsistent artifacts.

- A model card may claim broad multilingual safety competence.
- A risk card may classify cross-cultural misunderstanding as medium risk.
- A BBOM may show a default English safety prompt reused globally.
- Post-market complaints may reveal systematic mismatch in one region.

Only a coordinated audit process can determine which representation best matches the actual system and what corrective action is needed.

Table IV maps the relationship between artifacts and audit layers.

| Transparency artifact | Governance audit use | Model audit use | Application audit use |
|---|---|---|---|
| Model card | Checks whether upstream claims are governed and approved | Provides baseline claims to verify | Limited direct use; mainly reference point |
| Risk card | Tests whether risk ownership and mitigation plans are institutionalized | Can inform scenario selection | Core input for contextual harm testing |
| System card | Reviews release governance and public claims discipline | Supplies product-level behavior claims | Useful benchmark for observed system behavior |
| BBOM | Verifies ownership, change control, and dependency accountability | Identifies components affecting model-mediated behavior | Critical for tracing runtime failures and emergent behavior |
| Monitoring file | Assesses escalation and remediation governance | Can trigger re-testing priorities | Provides real-world evidence of deployed impacts |

This coordination function becomes more important as legal systems move toward mixed institutional models. The EU architecture under the AI Act involves multiple bodies—AI Office, AI Board, Scientific Panel, and national authorities—whose effectiveness depends on information flows and assurance capacity rather than on formal legal text alone ([14](https://fsi9-prod.s3.us-west-1.amazonaws.com/s3fs-public/2024-12/GenAI_Report_REV_Master_%20as%20of%20Dec%2012.pdf)). Where deployers


## Lifecycle Allocation of Responsibility for Emergent Persona

### A. Responsibility should be mapped by control function, not merely by vendor label

While the previous subtopic reports established that compositional deployments create fragmented accountability, this section addresses a different question: **how responsibility should be allocated across the lifecycle once one accepts that the final persona is co-produced by multiple actors**. The key governance error in many current programs is to assign responsibility according to contract position—provider, integrator, deployer, user—rather than according to the **specific control function** each actor exercised over the behavioral persona, value expression, and action scope of the deployed system.

In practice, the “character” that users encounter in an enterprise LLM system is assembled through a sequence of distinct governance acts, each of which can alter normative behavior without changing model weights. These acts include selecting the base model, accepting or rejecting the model provider’s safety profile, defining system prompts, setting escalation thresholds, curating retrieval corpora, connecting tools, defining permissions, writing fallback behaviors, setting human review rules, and determining what telemetry is captured for post hoc investigation. A legal or organizational accountability framework that treats only the base model provider as the author of behavior is therefore analytically incomplete; equally incomplete is a framework that assumes the enterprise alone owns the final persona merely because it controls the user interface.

The [EU AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) partially reflects this lifecycle logic by distinguishing obligations for providers, deployers, importers, distributors, and, for some systems, downstream modifiers. However, its strongest operational machinery is still better developed for category-based risk management, traceability, technical documentation, human oversight, and post-market monitoring than for the more subtle problem of **distributed authorship of behavioral persona** in compositional LLM stacks ([1](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)). The Act’s obligations on logging, documentation, robustness, oversight, and post-market surveillance matter because they create evidence trails, but they do not by themselves determine which actor is responsible when a persuasive, deferential, paternalistic, evasive, or ideologically slanted machine persona emerges from stacked prompts and middleware rather than from the base model alone.

A more useful institutional map distinguishes at least six control functions, each of which should be linked to a corresponding accountability duty.

| Control function | Typical actor(s) | Behavioral relevance | Accountability question |
|---|---|---|---|
| Alignment and refusal defaults | Model provider | Sets broad harmlessness style, refusal thresholds, normative priors | Were core behavioral assumptions disclosed and justified? |
| Application role construction | Enterprise product owner, integrator | Defines assistant identity, mission, tone, and goals | Who authorized the role-script and target behavior? |
| Context selection | Enterprise, domain team, retrieval vendor | Determines which documents, norms, and knowledge sources influence output | Who validated contextual sources for bias, legality, and regional fit? |
| Action enablement | Integrator, enterprise security, tool vendor | Converts language behavior into consequential acts | Who approved permissions and override logic? |
| Runtime moderation and intervention | Platform team, safety ops, trust and safety | Detects and halts harmful or out-of-scope behavior | Who monitors deviations and what triggers intervention? |
| User steering and local customization | End user, enterprise admin, reseller | Alters style, instructions, and occasionally policy boundaries | What forms of local modification are permitted and logged? |

This function-based framing matters because accountability gaps often arise not from complete absence of control, but from **misattributed control**. For example, a provider may design a relatively cautious default assistant. An enterprise then adds a system instruction to “resolve complaints without escalating unless legally required,” a marketing plugin that optimizes for conversion, and a retrieval source full of aggressive retention scripts. If the resulting assistant becomes unduly manipulative, the enterprise cannot plausibly shift all blame upstream. Yet the provider may still share responsibility if it exposed powerful persuasive affordances, weak policy-isolation mechanisms, or insufficient documentation about how its refusal hierarchy behaves under prompt conflict. Likewise, an integrator that packages unsafe defaults at scale may be neither a mere conduit nor a full provider in the colloquial sense, but it still performs a high-impact governance function.

This suggests a need for **behavioral responsibility matrices** analogous to cybersecurity shared responsibility models. Cloud security governance eventually learned that “the provider secures the cloud; the customer secures what is in the cloud” was too simple, but still superior to undifferentiated responsibility claims. Compositional LLM governance requires a similar move. The matrix should allocate duties not only for security and compliance artifacts, but for persona formation, norm selection, and value conflict management. ISO/IEC 42001’s management-system orientation is relevant here because it emphasizes organizational governance processes, roles, monitoring, and continual improvement, rather than single-point technical fixes ([2](https://www.iso.org/standard/81230.html); [3](https://www.iso.org/home/insights-news/resources/iso-42001-explained-what-it-is.html)). Yet ISO 42001 remains structurally generic; it does not specify a mature doctrine for tracing emergent machine character across multiple firms.

The U.S. governance environment shows a related limitation from the opposite direction. [NIST’s AI RMF](https://nvlpubs.nist.gov/nistpubs/ai/nist.ai.100-1.pdf) is strong on socio-technical risk management, mapping, measuring, and managing AI harms, and NIST’s work on monitoring deployed AI systems underscores that real-world operation creates new observability problems ([4](https://nvlpubs.nist.gov/nistpubs/ai/nist.ai.100-1.pdf); [5](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.800-4.pdf)). However, NIST’s framework is intentionally non-prescriptive and organization-centric. It helps a firm build a risk program, but it does not settle a cross-enterprise dispute about who “owns” an emergent persona when behavior is jointly produced through APIs, orchestration layers, and user-configurable policies.

The issue becomes more urgent as systems become more agentic. The source material indicates that enterprises are increasingly expected to produce logging, incident processes, impact assessments, and post-market plans, while runtime controls such as approval gates, scoped permissions, emergency shutdown paths, and anomaly alerts are becoming central governance tools rather than optional engineering extras ([6](https://www.getagentid.com/resources/ai-governance-in-2026); [7](https://genai.owasp.org/)). In agentic settings, the persona is not merely a matter of tone or politeness. It influences whether the system asks for confirmation, how aggressively it pursues a goal, how it interprets ambiguity, whether it escalates to humans, how it weighs user autonomy against paternalistic safety, and whether it adopts a sales, compliance, or care orientation. Those are institutional choices with distributional consequences.

A lifecycle allocation model should therefore separate four questions that are too often conflated:

1. **Who selected the value frame?**
2. **Who operationalized it into prompts, classifiers, and workflows?**
3. **Who exposed affected persons to the resulting behavior?**
4. **Who had the practical ability to detect and correct deviations?**

These questions can have different answers. A provider may select the initial safety frame; an integrator operationalizes it; the enterprise exposes users; a managed-service vendor runs monitoring; and end users may contribute adversarial or customization inputs. Governance quality depends on whether these answers are recorded ex ante rather than reconstructed after harm.

### B. The missing institutional artifact: a persona change log across the deployment chain

A persistent weakness in current governance practice is that organizations often keep records of model versions, security incidents, and compliance approvals, but not a **formal change history of persona-affecting interventions**. This creates a severe evidentiary problem. If an assistant’s behavior shifts from “informational and balanced” to “retention-optimized and escalation-averse,” an organization may struggle to identify whether the shift came from a provider model update, a changed system prompt, modified retrieval ranking, altered reward signals, an A/B-tested UX script, or a new tool policy.

This problem is recognized indirectly in post-deployment monitoring discussions. NIST notes that monitoring deployed AI systems is difficult because performance, context, and risk evolve after release, especially in socio-technical settings with feedback loops and changing environments ([5](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.800-4.pdf)). The enterprise source material similarly argues that paper compliance is inadequate where systems are adaptive, probabilistic, and continuously deployed, and that logging and observability are necessary to determine what actually happened in production ([6](https://www.getagentid.com/resources/ai-governance-in-2026)). But the particular gap for persona governance is not only “did the system malfunction?” It is “**who altered the behavioral stance, when, and with what authorization?**”

A persona change log would record, at minimum:

| Change category | Example | Required metadata |
|---|---|---|
| Provider-level behavior change | Updated refusal policy, new safety tuning, moderation endpoint change | Version, release notes, expected behavioral impact, downstream compatibility warnings |
| System prompt revision | Change from neutral assistant to retention-focused assistant | Author, approver, rationale, impacted jurisdictions/use cases |
| Retrieval corpus modification | Addition of region-specific policy library or sales playbook | Source owner, validation status, language/region tags, review date |
| Tool permission update | Granting refund authority or outbound messaging capability | Risk classification, approval rule, rollback path |
| Escalation policy change | Raising threshold for human review | Responsible manager, test results, affected populations |
| User/admin customization | Local prompt template or persona preset | Identity of modifier, policy boundary, expiration or audit cycle |

Such a log would not solve all normative disputes, but it would convert a large class of accountability disputes from speculative attribution to evidence-based analysis. It would also make visible a recurring pattern in enterprise deployments: **persona drift without executive awareness**. One team optimizes helpfulness, another optimizes conversion, another adds retrieval content, another loosens moderation to reduce false positives, and a customer-facing behavioral style emerges that no single committee explicitly approved. This is especially plausible in large organizations where product, legal, trust and safety, procurement, security, marketing, and localization functions each change a different layer.

Under the [EU AI Act’s](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) logic of traceability and post-market surveillance, these records are not alien to the regulatory spirit, even if the Act does not yet mandate a “persona log” by name ([1](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)). For high-risk systems, logging, technical documentation, human oversight, robustness, and post-market monitoring are central duties. For general-purpose AI models with systemic risk, the obligations include evaluations, risk mitigation, serious incident reporting, and cybersecurity safeguards, effective from **August 2, 2026** according to the cited legal analysis ([8](https://ai-law-center.orrick.com/eu-ai-act/general-purpose-ai/)). Yet these instruments still need translation into deployment-layer practices that are legible for behavioral authorship rather than only technical malfunction.

This is also where procurement and contract governance become important. The Medium source reflects a practical trend: teams increasingly have to produce risk files, impact assessments, incident processes, logging, and post-market plans, and U.S. federal buyers often expect NIST-aligned artifacts even absent a single federal AI statute ([9](https://medium.com/@Modexa/rules-risk-and-reality-eu-vs-us-ai-in-2026-aec6110b96de)). A sophisticated buyer should extend these requirements to include **behavioral provenance clauses**: obligations on vendors to disclose materially relevant behavior changes, safety-policy modifications, and controls for downstream prompt isolation. Without such clauses, downstream enterprises may be accountable to customers or regulators for persona shifts they were not promptly informed about.

An operationally mature persona change log would also permit **counterfactual review**. After an incident, investigators could ask whether the harmful behavior would likely have occurred absent a specific prompt revision, retrieval source, or tool permission. This would not always establish sole causation, but it would materially improve responsibility allocation. In governance terms, the goal is not metaphysical precision about where “the persona really resides.” It is sufficient to create a credible basis for assigning preventive duties, corrective obligations, and liability shares.

## Failure Topologies Unique to Multi-Actor Persona Assembly

### A. Persona can fail through interaction effects even when each layer appears compliant in isolation

Existing reports covered general accountability failures in compositional deployments. This section is narrower: it examines **failure topologies specific to behavioral persona assembly**, especially cases where no single layer is obviously defective but their interaction produces problematic machine character. This matters because most governance frameworks still assess controls component-by-component, while many persona harms are system-interaction harms.

A compositional LLM stack can exhibit at least five distinctive failure topologies.

| Topology | Mechanism | Why standard controls miss it | Typical manifestation |
|---|---|---|---|
| Normative amplification | Multiple benign nudges point in the same value direction | Each component seems low-risk individually | Excessive deference to corporate goals, over-refusal, over-persuasion |
| Policy collision | Different rule systems conflict under pressure | Testing often checks each policy separately | Inconsistent, arbitrary, or opaque responses |
| Contextual overfitting | Retrieval or local prompts dominate general safety priors | Upstream evals do not cover downstream context mix | Regionally biased or organizationally skewed persona |
| Incentive inversion | Business metrics subtly overpower safety or fairness intentions | Governance rarely audits KPI alignment | Manipulative tone, complaint deflection, dark-pattern dialogue |
| Action-persona mismatch | Harmless conversational style masks high-impact operational capacity | UX review and security review are siloed | User overtrust in systems with consequential tool access |

The first topology, **normative amplification**, occurs when several layers each make a modest adjustment toward a value—say, caution, brand friendliness, legal conservatism, or sales assertiveness—and the cumulative effect is much stronger than intended. A provider may tune for non-confrontation; an enterprise may add “be empathetic and solution-oriented”; a marketing team may instruct the system to “retain users where possible”; and a retrieval layer may supply scripts emphasizing loyalty offers over cancellation pathways. The final assistant can become systematically friction-adding or emotionally manipulative despite no single instruction explicitly saying “pressure the user.” Traditional red-teaming may miss this because the failure is not a jailbreak or overt policy violation; it is a **behavioral gradient** that accumulates over layers.

The second topology, **policy collision**, is common in multinational or regulated contexts. A provider may encode a general political-neutrality norm or a broad harassment policy; an enterprise may require a more context-sensitive explanation style; a local legal team may add region-specific restrictions; and user prompts may seek direct answers. The resulting system may oscillate between candor and evasiveness, or between deference and refusal, in ways that appear arbitrary to users. This is not merely a usability issue. Arbitrary persona instability can produce unequal treatment, especially when some users are more able than others to navigate refusals or extract actionable guidance.

The third topology, **contextual overfitting**, is especially salient for retrieval-augmented systems. The assistant’s perceived “values” may derive less from the base model’s constitutional alignment than from whichever documents are most salient in the retrieval corpus. An HR assistant drawing from legacy policy manuals, a health-support bot drawing from culturally narrow triage guidance, or a public-facing civic assistant drawing from outdated administrative language can all exhibit a persona that is formal, paternalistic, exclusionary, or legally overcautious in ways traceable to document curation rather than model alignment. Governance systems that focus on model cards or provider safety statements do not adequately capture this shift in authorship.

The fourth topology, **incentive inversion**, arises when performance metrics and optimization practices gradually re-encode values. If a system is evaluated mainly on conversion, resolution speed, ticket deflection, or complaint containment, teams may make seemingly small changes that steer the assistant toward behaviors inconsistent with the organization’s stated ethics. Because these changes are often implemented through prompt engineering, ranking, and workflow design rather than overt policy rewrites, they can evade formal ethics review. Here the accountability gap is not only technical but managerial: boards and executives often approve abstract principles while middle-layer product optimization silently defines the actual machine character.

The fifth topology, **action-persona mismatch**, is one of the most dangerous. A system may present as polite, transparent, and low-risk while being connected to consequential tools such as refunds, scheduling, eligibility determinations, outbound messaging, or account modifications. The gentle persona encourages user trust, but the underlying action capacity raises the stakes of every misjudgment. OWASP’s generative AI guidance emphasizes risks such as prompt injection, sensitive information disclosure, excessive agency, and insecure output handling precisely because tool use converts linguistic errors into material harms ([7](https://genai.owasp.org/)). Yet from a behavioral-governance standpoint, the salient problem is that persona can **mask power**. A “friendly assistant” is still an institutional actor if it can deny, recommend, escalate, or transact.

These topologies show why the behavioral persona of a deployed LLM system should not be governed solely as a content moderation issue. It is better understood as a **socio-technical control surface** where normative defaults, incentives, institutional priorities, and operational permissions interact.

### B. Causal ambiguity creates predictable responsibility laundering

Compositional deployments generate a form of what may be called **responsibility laundering through causal ambiguity**. Because behavior is co-produced, each actor can frame the harmful outcome as downstream or upstream. Providers can say the enterprise misconfigured prompts or retrieval. Enterprises can say the model’s latent behavior was unpredictable. Integrators can say they implemented client requirements. Users can be blamed for adversarial prompting. This diffusion is not incidental; it is structurally encouraged by current contractual and technical architectures.

The problem is aggravated by asymmetries in observability. Providers often possess better information about alignment pipelines, safety tuning, moderation thresholds, and version changes than downstream deployers. Enterprises possess better information about system prompts, business objectives, retrieval corpora, and user segmentation. Integrators possess better information about orchestration, middleware, and tool configuration. Users and affected communities often possess the least information, despite bearing substantial risk. This distribution means that no single actor may have full-stack visibility, but several actors may each have enough partial knowledge to deny sole accountability.

NIST’s emphasis on governance, mapping, measurement, and management is relevant because it rejects the idea that AI risk is purely technical; risk arises from context and use ([4](https://nvlpubs.nist.gov/nistpubs/ai/nist.ai.100-1.pdf)). Still, the AI RMF does not directly address how to prevent responsibility laundering in multi-firm deployments. ISO 42001 similarly requires organizational roles and responsibilities, but an enterprise can be fully certified in management-system terms while still lacking fine-grained attribution for persona-shaping interventions if its suppliers do not provide the necessary disclosures ([2](https://www.iso.org/standard/81230.html); [3](https://www.iso.org/home/insights-news/resources/iso-42001-explained-what-it-is.html)).

A more concrete governance response would require **joint incident reconstruction protocols**. When a serious behavioral incident occurs—discriminatory advice, manipulative retention dialogue, unsafe tool invocation, culturally offensive refusal behavior, or misleading representation of rights—the involved actors should be obligated to contribute relevant logs and version histories into a common investigatory record. This resembles aviation or industrial accident analysis more than ordinary software debugging. The purpose is not simply to find a broken component; it is to reconstruct the chain by which the system enacted a certain persona in context.

Such protocols are particularly important for systems that may fall under the [EU AI Act’s](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) higher scrutiny regimes or under U.S. state laws focused on discrimination and “reasonable care.” The supplied source indicates that **Colorado SB205**, effective **February 1, 2026**, requires developers and deployers of high-risk AI to exercise reasonable care to prevent algorithmic discrimination, with impact assessments, notices, documentation, and incident-related obligations ([10](https://medium.com/@Modexa/rules-risk-and-reality-eu-vs-us-ai-in-2026-aec6110b96de)). Where persona contributes to disparate treatment—for example, if some users are persistently nudged away from appeals, credit options, accommodations, or job opportunities—the behavioral layer cannot be dismissed as mere UX ornamentation. It becomes part of the discrimination pathway.

The governance implication is significant: **behavioral persona should be treated as potentially outcome-determinative evidence** in discrimination, consumer protection, and administrative fairness inquiries. A system that consistently sounds more certain to some groups, explains rights less fully to certain dialect communities, or adopts a more disciplinary tone in interactions with particular names or regions may produce differential outcomes even if its formal decision rule appears neutral. Current accountability structures are still weak at capturing this.

## Political and Cultural Contestation in Encoded Safety Personas

### A. “Safe” persona design is not culturally neutral, and Western defaulting remains a structural risk

The prior reports addressed value encoding as a governance issue in general terms. This section goes further by examining the **political and cultural dimensions of persona design**, including the evidence and structural reasons for Western-centric defaulting in deployed safety personas. The central analytical point is that many alignment and safety practices are presented as universal risk reduction, yet they often embody historically specific norms about civility, individual autonomy, offense, expertise, legality, and acceptable discourse.

One need not claim bad faith to identify this pattern. Frontier model providers and platform vendors are disproportionately headquartered in the United States and Western Europe, employ teams trained in particular legal and institutional traditions, and optimize for regulatory, reputational, and market pressures concentrated in those environments. The [OECD AI Principles](https://oecd.ai/en/ai-principles), [NIST AI RMF](https://nvlpubs.nist.gov/nistpubs/ai/nist.ai.100-1.pdf), ISO standards, and EU regulatory instruments all contribute important governance norms, but they also emerge from governance communities whose assumptions about fairness, dignity, transparency, harm, and oversight are not globally uncontested ([11](https://oecd.ai/en/ai-principles); [4](https://nvlpubs.nist.gov/nistpubs/ai/nist.ai.100-1.pdf); [2](https://www.iso.org/standard/81230.html); [1](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)). When these norms are operationalized through a small number of dominant providers, they can become de facto defaults at planetary scale.

Western-centric bias in safety personas can appear in several forms:

| Pattern | Example of encoded assumption | Deployment consequence |
|---|---|---|
| Liberal-individualist framing | Prioritizing individual consent/autonomy in contexts where collective or familial decision norms dominate | Responses may appear socially alien or impractical |
| High-formality institutional trust | Assuming officials, clinicians, or legal procedures are trusted and accessible | Advice may misfit low-trust or low-capacity settings |
| Narrow civility norms | Treating direct, emotional, or confrontational speech as unsafe or low-quality | Certain linguistic cultures are over-moderated or pathologized |
| Secularized moral vocabulary | Avoiding or flattening religiously grounded reasoning | Users may experience responses as normatively hollow or disrespectful |
| U.S./EU controversy maps | Over-indexing on speech sensitivities and taboo categories salient in Western discourse | Misprioritization of local harms elsewhere |
| Compliance-maximizing caution | Defaulting to liability-averse refusal styles | Under-service in contexts needing practical guidance |

These are not merely speculative risks. They follow from known properties of global AI production: concentrated provider power, proprietary alignment pipelines, and cross-border deployment into culturally plural settings. Even when models are multilingual, their behavioral safety layer may remain normatively anchored in the culture of the developer or primary market. The result is often a persona that appears “neutral” to its makers but carries specific assumptions about politeness, authority, conflict, sexuality, gender discourse, family structure, political legitimacy, and acceptable dissent.

The governance problem is compounded by the fact that safety personas often occupy a rhetorically privileged status. Because they are justified as risk mitigation, their normative content can be insulated from ordinary democratic contestation. A provider can frame a given refusal style, moral stance, or conversational boundary as simply “responsible AI,” even where reasonable cultures disagree. Corporate safety teams thus become quasi-constitutional actors: they define the speech boundaries, authority posture, and normative voice through which millions of people interact with machine systems.

This is especially important for enterprise deployments in public services, education, health, labor, and finance. An enterprise may assume that using a “safe” mainstream model reduces governance burden. Yet if the safety persona systematically misaligns with local communicative norms or social expectations, it can reduce accessibility, distort advice uptake, and produce hidden inequities. For instance, a highly formalized refusal style may look prudent in one jurisdiction but evasive or patronizing in another. An insistence on generic “consult a qualified professional” disclaimers may be appropriate where such professionals are accessible, but exclusionary where they are scarce. A model that persistently translates local ethical questions into U.S.-style rights discourse may impose an external normative vocabulary on users.

The [EU AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) does not directly adjudicate these deep cultural questions, but its concern with fundamental rights, human oversight, transparency, and risk management creates openings for them to be surfaced ([1](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)). However, the EU framework itself is also an expression of a regional constitutional order. Its values are legitimate within that order, but when systems built to satisfy EU and U.S. governance expectations are exported globally, they may function as vectors of **normative extraterritoriality**.

### B. Cross-cultural deployment challenges are governance failures, not just localization problems

Organizations often treat cross-cultural adaptation of LLM systems as a localization issue—translation, regional content, legal notices, local UX copy. That framing is too shallow. In compositional deployments, cross-cultural mismatch often concerns the **deep persona architecture**: what counts as respectful disagreement, how much directness is acceptable, when authority should be challenged, what role religious or customary norms can play, how gendered interaction is handled, how taboo topics are approached, and when uncertainty should be expressed.

These are governance questions because they concern whose values are encoded, by what process, and with what avenue for contestation. If a global provider ships a single safe persona across diverse markets, enterprises may inherit hidden cultural assumptions they cannot easily inspect. If they then add region-specific retrieval content without revisiting the upstream persona, they may create hybrid systems with contradictory normative signals: for example, locally grounded content delivered through an imported refusal style that feels alien to users. Conversely, heavy local customization without upstream safeguards can create region-specific harms or discriminatory behavior that providers later disclaim as downstream misuse.

A rigorous governance program should therefore require **cultural fit assessment** as part of deployment review, especially for high-impact uses. This is not the same as evaluating factual accuracy or bias in the narrow statistical sense. It means asking whether the enacted persona:
- communicates rights and obligations in locally intelligible ways;
- respects plural moral vocabularies without collapsing into relativism;
- avoids treating Western legal or therapeutic discourse as the only legitimate language of help;
- does not misclassify ordinary local speech as aggression, extremism, or unreliability;
- does not erase customary, religious, or community-based forms of reasoning where lawful and context-appropriate.

The challenge is institutional as much as technical. Most enterprises lack standing bodies with the legitimacy and expertise to adjudicate such questions. Product teams often rely on U.S.-based trust and safety heuristics or vendor defaults. Legal teams focus on jurisdictional compliance rather than cultural legitimacy. Localization teams can adapt wording but not deep alignment assumptions. End users may complain, but rarely have structured influence over the persona design process.

This is why multi-stakeholder oversight becomes relevant. Not because every prompt should be democratically voted on, but because high-scale deployed personas effectively constitute a form of **private normative infrastructure**. When a handful of corporations define the voice through which advice, explanation, refusal, triage, and assistance are delivered, they exercise population-scale cultural power. Oversight mechanisms should therefore include affected-community review, domain-specific ethics input, regional consultation, and contestation channels that are stronger than ordinary customer feedback queues.

The case is strongest in sectors where interpersonal style affects substantive outcomes. In employment support, a paternalistic or overly disciplinary tone may discourage applicants from contesting an adverse screening result. In health or mental health assistance, cultural mismatch can suppress disclosure or trust. In education, a homogenized “proper reasoning style” can privilege certain forms of argumentation and devalue others. In consumer finance, a deferential but opaque assistant can steer users away from understanding their options. These are not abstract symbolism issues; they can influence allocation of opportunities, services, and remedies.

## Oversight Mechanisms Beyond Documentation: Institutional Checks on Machine Character

### A. Why internal governance committees are insufficient for population-scale persona power

Previous sections in the broader report discussed documentation and auditing instruments. This section focuses instead on **institutional oversight mechanisms** suitable for controlling or contesting deployed machine character where corporate entities effectively define AI persona at scale. Internal review boards, responsible AI committees, and trust-and-safety teams are important, but they are rarely sufficient when the system’s behavioral persona reaches large populations or operates in high-stakes domains.

The underlying problem is one of legitimacy. If a company unilaterally decides how an LLM should speak about politics, religion, sexuality, self-harm, labor disputes, debt, immigration, or civic rights, it is not merely making a product design decision. It is allocating discursive power. Corporate boards and internal ethics committees may have expertise, but they usually do not represent the plurality of publics affected by the system. Moreover, they are structurally influenced by legal exposure, brand protection, and market incentives. This creates a tendency toward **risk-managed paternalism**: personas designed to minimize reputational harm and liability, even if that means under-serving contested user needs or suppressing legitimate but sensitive forms of expression.

The source material on enterprise governance in 2026 highlights the growing importance of runtime security, observability, logging, approval gates, and emergency intervention ([6](https://www.getagentid.com/resources/ai-governance-in-2026)). Those are necessary, but they answer mainly the question of operational control. They do not answer who should have standing to challenge the value assumptions embedded in the system’s persona, or how cultural and political disagreements should be adjudicated when they cannot be reduced to security threats.

Three oversight patterns are emerging conceptually, though none is yet fully institutionalized:

| Oversight model | Core idea | Strength | Limitation |
|---|---|---|---|
| External advisory councils | Diverse experts and community representatives review persona-relevant policies | Adds plural perspectives and public credibility | Often advisory only; risk of symbolic consultation |
| Sectoral assurance bodies | Domain-specific review of deployed systems in health, labor, education, finance, etc. | Better sensitivity to context and harm pathways | Resource-intensive; may lag technical change |
| Participatory redress mechanisms | Users and affected groups can contest behavioral patterns, not just individual outputs | Surfaces lived experience and cumulative harms | Requires infrastructure for aggregation and response |

A fourth, more ambitious model would be **behavioral impact panels** tied to major deployments or major model revisions. Such panels would examine not only safety and bias metrics, but the normative posture of the system: what forms of deference, contestability, disclosure, emotional tone, and persuasive strategy it adopts; how it varies across languages and regions; and whether those variations are justified. For frontier providers or major enterprise deployers, such panels could be linked to release approval for highly scaled or high-impact use cases.

This would align with broader currents in AI governance without simply duplicating existing compliance structures. The [OECD AI Principles](https://oecd.ai/en/ai-principles) emphasize human-centered values, transparency, robustness, accountability, and the capacity to intervene or decommission systems ([11](https://oecd.ai/en/ai-principles)). The [EU AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) emphasizes human oversight, logging, robustness, and post-market monitoring for relevant systems ([1](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)). [ISO 42001](https://www.iso.org/standard/81230.html) emphasizes organizational governance and continual improvement ([2](https://www.iso.org/standard/81230.html)). But none of these alone provides a robust public-facing institution for contesting machine character as such.

This gap is especially serious where providers of general-purpose AI models with systemic risk are required to perform evaluations, assess and mitigate systemic risks, report serious incidents, and ensure cybersecurity protection by **August 2, 2026** under the cited account of the EU framework ([8](https://ai-law-center.orrick.com/eu-ai-act/general-purpose-ai/)). If such models underpin thousands of downstream assistants, then upstream persona decisions can have societal effects far beyond any single application. Yet systemic-risk obligations today focus more clearly on technical, security, and broad public-safety concerns than on pluralistic governance of encoded character.

### B. Appeals, override, and decommissioning rights should apply to persona-level harms

One of the most underdeveloped areas in current governance is user recourse against persona-level harms. Existing complaint systems usually target discrete harmful outputs: inaccurate content, offensive language, unsafe advice. But many significant harms arise from **persistent behavioral patterns**—for example, chronic overconfidence, selective opacity, manipulation, excessive moralizing, differential warmth, systematic discouragement of appeals, or consistent routing away from human assistance. These are not always reducible to a single “bad answer.”

A mature governance architecture should give users and affected communities at least three forms of recourse:

1. **Pattern-level complaint rights**: the ability to report not only isolated outputs but recurring behavioral tendencies.
2. **Human review of consequential persona effects**: especially where tone, framing, or explanation affects access to rights, opportunities, or services.
3. **Escalatory override and decommissioning triggers**: where a system exhibits persistent persona-induced harm despite remediation attempts.

The OECD’s call for mechanisms to override, repair, or decommission AI systems when they exhibit undesired behavior is highly relevant here ([11](https://oecd.ai/en/ai-principles)). In many organizations, override rights are defined only in security or uptime terms. They should also apply to normative malfunction. If an assistant in a public-benefit, employment, education, or healthcare context persistently adopts a misleadingly authoritative, culturally alienating, or rights-obscuring persona, there should be a governance path to suspend or narrow its deployment pending review.

NIST’s work on monitoring deployed AI systems supports this direction by underscoring that real-world behavior must be observed continuously rather than assumed stable after launch ([5](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.800-4.pdf)). What remains underdeveloped is the **taxonomy of persona incidents**. Organizations should classify incidents not only by security breach, factual error, or policy violation, but by behavioral-governance categories such as:
- coercive or manipulative framing;
- opaque refusal without accessible explanation;
- culturally inappropriate or exclusionary interaction style;
- unjustified authority simulation;
- undue discouragement of escalation or appeal;
- systematically differential tone or responsiveness across user groups.

Without such categories, monitoring systems will undercount precisely the harms most characteristic of deployed machine character.

### C. Procurement and public-sector deployment should require contestable behavioral governance

A particularly important institutional lever is procurement. Public agencies and large enterprises can demand stronger persona governance from vendors than general market practice currently supplies. The sourced material indicates that U.S. federal procurement increasingly expects NIST-aligned risk artifacts and that teams are producing impact assessments, incident processes, and evaluation packages to clear reviews ([9](https://medium.com/@Modexa/rules-risk-and-reality-eu-vs-us-ai-in-2026-aec6110b96de)). Procurement should now move further by requiring:
- disclosure of persona-relevant upstream alignment assumptions;
- notice of material behavior changes in model updates;
- support for local policy isolation and regional customization with auditability;
- logs sufficient for behavioral incident reconstruction;
- user-facing disclosure when a consequential interaction is governed by machine persona rather than neutral information retrieval alone;
- evidence of cross-cultural testing where deployment spans diverse populations.

For public-sector use, additional constraints are justified. Administrative legitimacy requires not merely accurate answers but intelligible, contestable, and non-arbitrary institutional voice. If an agency deploys an LLM assistant to explain eligibility, route complaints, or assist applicants, it should not be permitted to hide behind vendor opacity when the system’s persona discourages contestation or subtly narrows perceived rights. The administrative state has long recognized due process, reason-giving, reviewability, and non-arbitrariness as core values. Deployed LLM personas can interfere with all four.

Thus, procurement and oversight frameworks should treat machine character as a matter of public accountability, not brand style. Where large populations rely on AI-mediated explanation and assistance, corporate decisions about “helpfulness,” “harmlessness,” “friendliness,” and “safety” become distributive political choices. The stronger the concentration of provider power, the stronger the case for external review, public-interest testing, and formal mechanisms by which affected groups can challenge persona norms they did not choose.

## Operationalizing


## Institutional Design Choices for External Scrutiny of Deployed LLM Behavior

### From transparency artifacts to standing oversight institutions

Previous sections addressed disclosure artifacts, layered audits, and the general case for external accountability. This section is narrower and more institutional: it evaluates which **standing oversight arrangements** are most plausible for governing the behavioral persona of deployed LLM systems once those systems are already in use. The key shift is from asking *what should be documented* to asking *who is authorized, resourced, and procedurally equipped to interrogate deployed behavior over time*.

The literature on external scrutiny of frontier systems has increasingly converged on the view that internal company processes are insufficient for high-impact models. Anderljung et al. argue that decisions concerning training, deployment, and use of frontier LLMs should not remain solely with developers, and organize the conditions for effective external scrutiny under the ASPIRE framework: **Access, Searching attitude, Proportionality to the risks, Independence, Resources, and Expertise** ([1](https://cdn.governance.ai/Towards_Publicly_Accountable_Frontier_LLMs.pdf)). Although framed at the frontier-model level, ASPIRE is especially salient for deployed behavioral governance because the most socially consequential harms often appear only in downstream operational settings, where prompt hierarchies, enterprise policy layers, retrieval corpora, and user segmentation shape what the system actually says and refuses to say.

For deployed behavior, each ASPIRE element takes on a more specific institutional meaning:

| ASPIRE element | Relevance to deployed persona/value governance | Typical institutional implication |
|---|---|---|
| Access | Oversight actors need access not just to a base model, but to deployed prompts, policy rules, logs, evaluation environments, and escalation pathways | Secure regulator portals, auditor sandboxes, researcher APIs, protected access to behavioral configuration evidence |
| Searching attitude | Oversight must be adversarial enough to test how persona fails under realistic user manipulation, not merely verify nominal policies | Mandated red-team protocols, challenge testing, complaint-triggered investigations |
| Proportionality | Stronger oversight should attach where deployed systems exercise gatekeeping, advice, triage, or public-facing authority at scale | Risk-tiered audit frequency, differentiated access rights, enhanced scrutiny for public services and sensitive sectors |
| Independence | Evaluators must be insulated from financial, contractual, and reputational dependence on the audited firm | Auditor rotation, conflict rules, public funding for civil-society review, regulator-appointed experts |
| Resources | Effective scrutiny requires budgets, compute, staff time, secure infrastructure, and legal protection | Supervisory fees, pooled testing infrastructure, grants to independent labs |
| Expertise | Behavioral review requires mixed competency in ML, safety, security, law, sociology, linguistics, and domain practice | Interdisciplinary assessment panels; certified specialist auditors |

This institutionalization problem is sharpened by the asymmetry between corporate control over model updates and public visibility into those updates. A deployer can change a system prompt, retrieval ranking rule, escalation threshold, moderation endpoint, or refusal rubric within hours, while affected users may only see a vague shift in “tone” or “character.” In such settings, public accountability ecosystems must be capable of handling **behavioral drift**, **silent policy changes**, and **contested normative choices** rather than only discrete model launches.

A central lesson from the emerging frontier-auditing literature is that mature oversight likely requires not just independent auditors, but also a meta-governance layer that supervises the auditors themselves. The proposal for a “**PCAOB-for-AI**,” by analogy to the U.S. Public Company Accounting Oversight Board, is relevant here because it identifies four institutional functions that ordinary one-off audits cannot supply: standard-setting, certification of auditors, inspection of audit quality, and revocation of credentials where warranted ([2](https://arxiv.org/pdf/2601.11699), [3](https://static1.squarespace.com/static/685262a5f3a19135202ed5b6/t/696915f8adf5d1209d1fad6e/1768494584085/Frontier_AI_Auditing%20%281%29.pdf)). Applied to deployed LLM persona governance, such a body would not merely ask whether a model is “safe”; it would determine whether a behavioral audit meaningfully tested the deployed system’s normative conduct in context.

This matters because behavioral governance can be superficially audited. A weak audit may verify that a company possesses a published policy, a model card, or a safety benchmark, while leaving untested whether the production system disproportionately refuses some political viewpoints, enacts paternalistic defaults in mental-health triage, or encodes a culturally narrow standard of “appropriate” speech. External scrutiny models that focus on paperwork without permitting live challenge testing risk becoming instruments of legitimation rather than accountability.

The oversight question therefore becomes one of **institutional division of labor**. Different actors have distinct comparative advantages:

| Actor class | Comparative advantage | Structural limitation |
|---|---|---|
| Sector regulators | Formal authority, sanctions, access powers, integration with legal obligations | Often limited technical capacity; may move slowly |
| Independent auditors | Repeatable assurance processes, evidence review, control testing | Risk of client capture; may underweight affected-community concerns |
| Civil-society organizations | Ground truth on lived harms, cultural legitimacy, issue spotting, participatory challenge | Resource scarcity; limited legal access rights |
| Standards bodies | Harmonization, common taxonomies, technical consensus-building | Weak enforcement; may be dominated by incumbents |
| Academic/research labs | Methodological innovation, independent evaluation paradigms | Often fragile access and funding; may face legal restrictions |
| Public complaint and ombud systems | Detection of real-world failure patterns | Reactive, fragmented, and often underpowered |

An effective public accountability ecosystem should therefore be **polycentric** rather than singular. No single institution can simultaneously supply democratic legitimacy, technical depth, enforcement power, cultural sensitivity, and global operational reach. Yet polycentricity alone is not enough. Without clear interfaces between institutions, fragmentation can intensify responsibility gaps. For example, a regulator may assume that third-party auditors will surface persona harms; auditors may assume that civil society will identify them; civil society may lack access to evidence; and standards bodies may produce vocabularies with no route to enforcement.

A useful way to evaluate oversight models for deployed behavior is to distinguish five governance functions:

1. **Detection** of problematic behavioral outputs or patterns;
2. **Attribution** of causal responsibility across the stack;
3. **Adjudication** of whether the behavior violates law, policy, or public norms;
4. **Remediation** through technical or organizational changes; and
5. **Public legibility** so outside actors can understand what changed and why.

Many current governance initiatives cover only one or two of these functions. The ASPIRE framework contributes mainly to the prerequisites for detection and partial attribution. Auditor proposals contribute to repeatable attribution and control testing. EU-style obligations on logging, documentation, and post-market monitoring strengthen remediation and legal traceability for some systems ([4](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai), [5](https://www.getagentid.com/resources/ai-governance-in-2026)). But deployed persona governance still lacks durable institutions for **adjudicating normative conflict** where the issue is not simply factual error or security compromise but disagreement over encoded values.

That gap is politically important. If a model consistently frames labor organizing as risky, treats some religious claims as suspicious, or refuses lawful discussion of contested reproductive-health issues under the banner of “safety,” the harm is not fully captured by robustness, discrimination, or cybersecurity metrics. It is a question of who gets to define acceptable machine conduct in public life. Oversight models must therefore be assessed not only for technical rigor but for their ability to govern **private normative infrastructure**.

### Regulatory supervision and the limits of legal command-and-control

Previous sections examined how existing frameworks indirectly constrain deployed conduct through documentation, logging, human oversight, and post-market duties. This section differs by focusing specifically on **regulators as institutional overseers of behavioral persona**, including where their authority is strong, where it is structurally weak, and how regulatory supervision interacts with other accountability actors.

The regulatory case for overseeing deployed LLM behavior is strongest where models function in legally sensitive, high-impact, or public-facing settings. The [EU AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) is the most developed binding framework in this space as of April 2026, particularly because it links risk classification to obligations such as technical documentation, logging, human oversight, robustness, and post-market monitoring for high-risk systems, while also imposing transparency duties in some lower-risk contexts and a regime for general-purpose AI models ([4](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai), [6](https://techjacksolutions.com/eu-ai-act/)). Even where the Act does not directly regulate “persona” as such, it creates leverage points over deployed behavior through conformity assessment, instructions for use, traceability, and operational monitoring.

For behavioral oversight, however, the regulator’s role is more complicated than ordinary product safety supervision. Deployed LLM persona often emerges from interaction between:

- a general-purpose model provider;
- the application developer or systems integrator;
- the enterprise or public-sector deployer;
- external data sources and retrieval systems;
- end-user prompts and contextual steering; and
- downstream human review or override processes.

This distributed architecture makes regulatory command-and-control less straightforward than in sectors where a single manufacturer controls a stable artifact. A regulator may know *that* harmful behavior occurred without readily knowing *which actor* had effective control over the relevant value choice. If a chatbot in a bank provides unduly paternalistic financial advice because the vendor’s safety tuning treats debt as a self-harm trigger, the bank’s system prompt reinforces caution, and the retrieval layer injects conservative policy guidance, then no single layer explains the resulting persona. Regulators therefore need mechanisms for **cross-entity evidence gathering** rather than firm-by-firm review in isolation.

A practical regulatory supervision model for deployed persona would likely require at least six powers or capabilities:

| Regulatory capability | Why it matters for persona/value governance | Current challenge |
|---|---|---|
| Configuration visibility | To inspect system prompts, policy rules, moderation settings, model versions, and major updates | Often treated as trade secrets or operationally fluid |
| Log access | To reconstruct what the system did in context and detect patterned harms | Privacy, security, and retention constraints |
| Cross-actor information requests | To attribute responsibility across provider, integrator, and deployer | Jurisdictional fragmentation; contracts limit visibility |
| Complaint intake and triage | To identify harms not captured by benchmark testing | Complaint systems rarely encode value/persona categories |
| Remedial authority | To require changes, suspend use, or impose conditions on deployment | Legal thresholds may be ill-suited to normative harms |
| Ongoing monitoring | To detect behavioral drift after deployment or model updates | Resource-intensive; regulators often underfunded |

The main legal challenge is that many behavioral harms are **contestable rather than obviously unlawful**. The regulator can act more decisively where outputs amount to discrimination, deception, unsafe advice, privacy breach, unlawful manipulation, or sectoral non-compliance. It is far harder where the issue is a persistent ideological slant, culturally narrow refusal style, or systematic privileging of one moral vocabulary over others. In such cases, regulators confront a legitimacy dilemma: if they intervene too little, corporate actors effectively set public norms; if they intervene too aggressively, they risk state overreach into speech, culture, and political contestation.

This is one reason why command-and-control regulation should not be the sole model. The state can define procedural duties, minimum safeguards, investigatory powers, and red lines, but it is poorly positioned to micro-manage the normative character of general conversational systems at scale. More promising is a **regulated ecosystem model** in which regulators set baseline duties and supervise the quality of private and semi-public scrutiny institutions.

The emerging analogy to financial auditing is instructive. Sarbanes–Oxley did not require securities regulators to personally perform every audit; it created a supervised audit ecosystem with public oversight of the auditors. The frontier-auditing literature explicitly suggests that AI governance may need an analogous layer that develops auditing standards, certifies auditors, inspects their work, and disciplines weak performers ([2](https://arxiv.org/pdf/2601.11699), [3](https://static1.squarespace.com/static/685262a5f3a19135202ed5b6/t/696915f8adf5d1209d1fad6e/1768494584085/Frontier_AI_Auditing%20%281%29.pdf)). For deployed persona, regulators could occupy at least three roles within such an ecosystem:

1. **Rule-setter of minimum duties**: specifying which deployed systems require behavioral logging, challenge testing, incident response, and documented escalation for value-sensitive use cases.
2. **Supervisor of assurance markets**: approving or recognizing audit schemes, accrediting conformity assessment bodies, and examining whether audits meaningfully probe deployed behavior.
3. **Backstop enforcer**: investigating severe failures, sanctioning deception or inadequate controls, and mandating remediation where risk thresholds are crossed.

The regulator’s comparative advantage lies in coercive authority and procedural due process. Yet regulatory supervision remains vulnerable to four failure modes.

First, **technical abstraction**: regulations are often written at a level that captures controls generically but not the concrete mechanisms through which persona emerges. For example, “human oversight” may exist on paper while the deployed system’s default refusal style still systematically narrows user agency.

Second, **resource asymmetry**: leading AI firms and large enterprise deployers may have more specialized staff, monitoring infrastructure, and operational data than national regulators. Without supervisory fees or dedicated technical units, regulators may struggle to inspect behavior in real time.

Third, **jurisdictional mismatch**: the provider, cloud host, integrator, and deployer may be in different countries; training may occur outside the regulator’s territory; inference may be routed globally. Behavioral governance can therefore exceed the comfortable jurisdictional boundaries of classic administrative law.

Fourth, **normative under-specification**: law can require transparency, risk management, and rights protection, but often does not specify how to resolve plural moral disagreement over what a “safe,” “respectful,” or “neutral” persona should be. This is where public accountability ecosystems need participatory and deliberative components beyond conventional compliance review.

A risk-based regulatory strategy is therefore more credible than universal persona policing. Regulators should prioritize settings where deployed LLM behavior carries strong allocative, epistemic, or psychological power: health triage, education, employment, financial advice, legal information, child-facing services, and public administration. In such contexts, the system’s conversational persona is not a cosmetic feature; it shapes access to options, credibility judgments, and de facto authority. Post-market monitoring plans and incident-reporting processes should expressly include **behavioral pattern harms**, not just technical failures. Existing practical governance discussions in industry already emphasize observability, logs, records, and intervention capabilities as necessary for operational control ([5](https://www.getagentid.com/resources/ai-governance-in-2026)). Regulators should require that these controls be interpretable for persona-governance purposes, such as identifying whether refusal rates, escalation patterns, or moralized warnings differ by topic, language, region, or user group.

An especially important regulatory issue is standing for affected parties. Many existing complaint systems are optimized for consumer dissatisfaction, privacy complaints, or discrimination claims, but not for contesting **machine character**. If a deployed educational tutor systematically frames indigenous knowledge as folklore but Western scientific paradigms as neutral truth, harmed communities may struggle to articulate this as a conventional legal claim. Regulators should therefore support complaint taxonomies and reporting channels that recognize epistemic and cultural harms where these are linked to access, dignity, or fair treatment.

This does not imply that regulators should determine substantive truth in every cultural dispute. Rather, they should require organizations to demonstrate **procedural legitimacy** in how value-laden behavioral choices are made, tested, reviewed, and revised. That includes evidencing stakeholder consultation, documenting trade-offs among competing values, monitoring for disparate cultural effects, and providing mechanisms for appeal or alternative modes where appropriate. In this sense, regulatory supervision should focus less on dictating a single machine morality and more on ensuring that the processes for encoding and revising machine behavior are contestable, reviewable, and not monopolized by narrow corporate or geopolitical constituencies.

### Third-party auditors, assurance markets, and the problem of auditing values in context

While previous sections discussed layered auditing as a conceptual architecture, this section examines a different question: **whether third-party audit institutions can realistically govern deployed LLM behavior and value encoding at scale**, and under what conditions they add genuine accountability rather than procedural reassurance.

Independent auditing is attractive because it promises repeatability, professionalization, and a structured evidentiary bridge between technical systems and legal or organizational obligations. The current frontier-auditing literature argues for more rigorous third-party assessment of safety and security practices at leading AI companies and explicitly contemplates ecosystem features analogous to mature assurance industries, including standards development, credentialing, audit-quality review, and independent oversight ([2](https://arxiv.org/pdf/2601.11699), [3](https://static1.squarespace.com/static/685262a5f3a19135202ed5b6/t/696915f8adf5d1209d1fad6e/1768494584085/Frontier_AI_Auditing%20%281%29.pdf)). For deployed persona governance, however, the question is not only whether audits exist, but **what exactly they audit**.

Behavioral persona cannot be fully inferred from upstream documentation or static benchmark scores. A credible audit of deployed LLM behavior therefore needs to test at least five object classes:

| Audit object | Example evidence | Why conventional audits may miss it |
|---|---|---|
| Normative rule-set | Policy rubrics, refusal taxonomies, constitutional prompts, escalation rules | Firms may document high-level principles but not operationalized value hierarchies |
| Runtime configuration | System prompts, routing logic, tool permissions, temperature controls, user segmentation rules | These are dynamic and may change more frequently than audit cycles |
| Contextual knowledge injection | Retrieval corpora, ranking logic, source whitelists, moderation overlays | Persona is often altered through content curation rather than model fine-tuning |
| Real-world behavioral outcomes | Topic-specific refusals, tone, deference patterns, advice style, differential handling across languages | Static testing underestimates context dependence and long-tail interactions |
| Governance response capacity | Incident handling, rollback procedures, appeals, human override, update approval | Existence of controls does not show whether they work under pressure |

This makes deployed-persona auditing substantially harder than auditing a stable financial control or cybersecurity baseline. The auditor must evaluate a live socio-technical system that may evolve continuously. Moreover, the most salient harms are not always binary failures. They may involve gradients of paternalism, selective credibility attribution, overly moralized safety messaging, or culturally asymmetrical notions of offensiveness.

Several design choices therefore determine whether third-party audits are meaningful.

**1) Scope definition.**  
If the audit scope is restricted to the foundation model developer, the most consequential downstream behavior may be missed. If it is restricted to the deployer, upstream alignment assumptions may be taken as fixed and unanalyzable. Audits must therefore specify the **system boundary** under review and, where possible, include shared-responsibility analysis across actors.

**2) Test design.**  
A compliance-oriented audit may check that risk assessments exist and logging is enabled. A behaviorally credible audit must also include scenario testing, challenge evaluation, multilingual and cross-cultural probes, and adverse-case sampling drawn from complaints and field incidents. Otherwise, audits risk validating paperwork rather than lived conduct.

**3) Independence and incentives.**  
The ASPIRE framework identifies independence as a core requirement for external scrutiny ([1](https://cdn.governance.ai/Towards_Publicly_Accountable_Frontier_LLMs.pdf)). In audit markets, dependence can arise not only from direct payment by the audited firm but from repeat business, consulting cross-sales, access dependence, and reputational incentives to avoid public confrontation. Persona governance heightens these risks because the audited issue often concerns sensitive political or cultural choices that firms may regard as brand-defining.

**4) Temporal adequacy.**  
An annual or pre-launch audit is insufficient where production prompts and policies are routinely revised. Audits need surveillance-like elements: periodic re-testing, material-change triggers, and complaint-linked follow-up. A static certificate can quickly become misleading.

**5) Public reporting.**  
If audit findings remain confidential, the public accountability function is weak. Yet full transparency may expose security vulnerabilities, proprietary methods, or sensitive misuse vectors. A layered reporting model is therefore needed: confidential technical annexes for regulators, detailed management findings for firms, and public summaries describing material behavioral risks, remediation status, and unresolved limitations.

The strongest case for third-party auditing lies where behavioral choices are **operationalizable into auditable claims**. For instance, an enterprise deployer might claim that its public-sector assistant:
- provides legally informational rather than advisory responses;
- escalates self-harm content to a human channel under specified conditions;
- applies equivalent refusal thresholds across major supported languages;
- records and reviews all prompt-policy changes affecting vulnerable-user interactions; and
- supports user contestation for adverse conversational outcomes.

Such claims can be tested. By contrast, a claim that the system is “neutral,” “balanced,” or “aligned with community values” is much harder to audit unless translated into more concrete criteria, such as procedures for stakeholder input, multilingual calibration evidence, topic-sensitive refusal parity analysis, or documented governance of contested values.

The literature on assurance audits of algorithmic systems is relevant here because it pushes beyond narrow technical validation toward evaluating whether claims about system behavior are supported by evidence and governance processes ([7](http://dx.doi.org/10.1145/3630106.3658957)). For deployed LLM persona, assurance should be claim-based but not claim-limited. Auditors should assess not only the claims a company chooses to make, but also whether omitted claims hide salient risks. For example, a firm may highlight toxicity mitigation while omitting the fact that its mental-health chatbot systematically discourages certain lawful identity or lifestyle discussions in some locales due to conservative policy tuning.

A sophisticated audit market would likely differentiate among at least four audit types:

| Audit type | Principal question | Likely commissioning party | Strength | Limitation |
|---|---|---|---|---|
| Compliance audit | Are required controls and records in place? | Deployer, regulator | Legally legible; standardized | Can become formalistic |
| Technical behavior audit | How does the system actually behave under challenge? | Deployer, provider, regulator | Empirically grounded | May miss governance legitimacy issues |
| Governance-process audit | How are value choices made, approved, and revised? | Boards, regulators, public bodies | Addresses normative process legitimacy | Harder to quantify |
| Field-impact audit | What harms or asymmetries arise in actual use? | Public agencies, civil society, regulators | Closest to lived impact | Data access and attribution are difficult |

The limitations are especially acute in compositional deployments. Suppose a hospital uses a vendor model through a health-tech integrator. The hospital customizes triage prompts, the integrator adds retrieval over medical protocols, and the vendor updates refusal heuristics following a general safety release. A third-party auditor may be hired by the hospital, but lack contractual access to the vendor’s policy layers; or hired by the vendor, but unable to inspect the hospital’s live deployment. The result is **assurance fragmentation**, where every actor can point to some audit, yet no audit covers the behavioral whole.

To address this, auditors need contractual and regulatory support for **federated evidence review**. This could include shared evidence rooms, common test suites run across layers, and standardized change-notification duties when one actor’s update may alter another actor’s deployed persona. Without such mechanisms, the audit profession may replicate the same fragmentation that afflicts substantive accountability.

There is also a deeper normative challenge: auditors are generally trained to evaluate conformance against standards, controls, or declared criteria. But value encoding in LLMs often implicates unresolved social disagreement. An auditor can test whether a company followed its own process for deciding how to respond to politically sensitive content; the auditor is less well-positioned to declare the resulting policy substantively legitimate. This limitation suggests that audit should be understood as necessary but not sufficient. It can improve **traceability, evidence quality, and procedural discipline**, but not fully settle disputes over the appropriate moral character of machine intermediaries.

For that reason, the strongest role for auditors in persona governance is likely twofold. First, they can verify that organizations maintain robust **behavioral control systems**: logging, testing, update review, incident handling, appeal routes, and risk assessment. Second, they can independently surface **empirical asymmetries**—for example, differential refusal patterns, linguistic unevenness, or topic-specific overblocking—that then become inputs into broader public or regulatory deliberation. Auditors should not be imagined as neutral philosophers of machine ethics; their value lies in disciplined evidence production under conditions of institutional independence.

The “PCAOB-for-AI” idea is thus especially relevant not because AI exactly resembles financial accounting, but because AI assurance will likely face familiar problems of market capture, inconsistent methodologies, and the temptation of symbolic audit. A supervisory body for AI auditors could:
- define minimum behavioral-audit procedures for high-impact deployments;
- accredit specialist auditors with sociotechnical and domain expertise;
- inspect whether audits included adequate adversarial, multilingual, and complaint-informed testing;
- require disclosure of conflicts of interest; and
- sanction audit firms that systematically deliver low-quality or misleading assurance ([2](https://arxiv.org/pdf/2601.11699), [3](https://static1.squarespace.com/static/685262a5f3a19135202ed5b6/t/696915f8adf5d1209d1fad6e/1768494584085/Frontier_AI_Auditing%20%281%29.pdf)).

Such a regime would still leave unresolved who defines the substantive benchmarks for good machine character. But it would materially improve the integrity of the institutions that evaluate behavioral claims.

### Civil society, affected communities, and contestation as governance infrastructure

Earlier discussion noted the need for affected-community review and stronger contestation channels than ordinary customer feedback. This section goes further by analyzing **civil society not merely as a consulted stakeholder, but as a constitutive part of the oversight architecture** for deployed LLM behavior.

Civil-society participation is often treated as normatively desirable but operationally secondary. In deployed persona governance, that is a mistake. Many of the most important harms are first legible not to regulators or auditors, but to journalists, watchdog groups, digital-rights advocates, linguistic minorities, disability organizations, labor organizers, teachers, mental-health groups, and community-serving intermediaries. These actors are often the earliest detectors of patterns such as:
- selective silencing of lawful but marginalized viewpoints;
- culturally specific misclassification of harmless speech as unsafe;
- paternalistic tone or over-refusal in welfare, health, or migration contexts;
- religious or linguistic asymmetries in content moderation and advice;
- systematic devaluation of non-Western knowledge frameworks; and
- behavioral changes after silent model or policy updates.

Anderljung et al.’s external scrutiny framework is helpful precisely because it implies that effective scrutiny depends not only on access for formally credentialed experts, but on an ecosystem of outside actors with incentive to search for failure ([1](https://cdn.governance.ai/Towards_Publicly_Accountable_Frontier_LLMs.pdf)). Civil society often has the strongest “searching attitude” because it is embedded in communities that experience harms directly. However, civil society typically lacks the **access, resources, and legal protections** that ASPIRE identifies as equally necessary. The result is a structural contradiction: the actors best placed to spot cultural and normative harms are often the least institutionally empowered to investigate them.

A serious public accountability ecosystem should therefore treat civil society as having at least four formal roles:

| Civil-society role | Function in deployed behavior governance | Institutional supports required |
|---|---|---|
| Independent evaluator | Conduct external testing, issue reports, benchmark harms, compare systems across groups | Research access, safe harbor, funding, APIs or controlled sandboxes |
| Complaint aggregator | Translate dispersed user grievances into structured evidence of systemic issues | Standardized reporting interfaces, data-sharing agreements, legal standing |
| Deliberative participant | Represent affected values in policy design, review boards, procurement, and standards work | Seats in advisory and standards processes, compensation, multilingual participation |
| Accountability amplifier | Use media, litigation, advocacy, and public campaigns to pressure remediation | Transparency obligations, whistleblower channels, anti-retaliation protections |

The challenge is to prevent civil society from being reduced to symbolic consultation. Many companies have convened advisory boards or red-team events that generate legitimacy benefits but little durable power. Without formalized rights of access, response obligations, and follow-through, “multi-stakeholder” can mask unilateral corporate control. Affected communities may be invited to comment on an already-determined policy architecture rather than shape the governance criteria themselves.

This problem is acute in cross-cultural deployments. Large commercial LLMs are frequently trained, aligned, and safety-tuned within institutions concentrated in North America and Western Europe, then deployed across jurisdictions with different legal baselines, religious sensibilities, historical memory, speech norms, and conceptions of dignity. Existing reports already noted the structural risk of Western defaulting. The oversight implication is that civil society must not be restricted to a generic diversity panel; it must include **regionally grounded and domain-specific interlocutors** able to identify where a system’s “safe” persona functions as cultural imposition.

Examples of where civil-society oversight is especially necessary include:
- language-specific refusal patterns that are stricter or sloppier in less-resourced languages;
- safety messaging that presumes U.S.-centric legal or therapeutic norms;
- automated educational or historical explanations that prioritize dominant geopolitical narratives;
- public-service assistants whose deference style discourages challenge by already marginalized users.

In such cases, the question is not merely whether the model is inaccurate. It is whether a private company has installed a population-scale conversational intermediary whose encoded values reshape what counts as legitimate inquiry or acceptable self-description. Civil society is uniquely positioned to contest those shifts because it can articulate harms that escape both technical metrics and formal legal categories.

Institutionally, several mechanisms can move civil-society participation from aspiration to governance reality.

**1) Structured researcher-access programs.**  
External researcher access is already identified as one pillar of scrutiny alongside red-teaming and auditing ([1](https://cdn.governance.ai/Towards_Publicly_Accountable_Frontier_LLMs.pdf)). For deployed behavior, such access should include controlled environments where approved external groups can test production-like systems, inspect policy updates at an appropriate level of abstraction, and submit reproducible findings. Access must be more than bug bounty logic; many behavioral harms are not security vulnerabilities.

**2) Public-interest funding pools.**  
If oversight depends on unpaid advocacy or sporadic philanthropy, scrutiny will be skewed toward well-connected regions and issues. Supervisory fees, procurement levies, or dedicated public grants could fund independent evaluation centers, community testing labs, and translation/linguistic review programs.

**3) Mandatory response duties.**  
Organizations should be required to respond within defined timelines to substantiated public-interest reports concerning deployed behavioral harms, including whether the issue is accepted, rejected, mitigated, or escalated for further review. Otherwise, civil-society findings remain discretionary inputs.

**4) Standing in regulatory and procurement processes.**  
Civil-society organizations, professional associations, and community groups should have pathways to submit evidence in conformity assessment disputes, post-market monitoring reviews, and public-sector procurement evaluations, particularly where deployed personas affect vulnerable populations.

**5) Safe-harbor and anti-retaliation protections.**  
Independent testing of LLM behavior can trigger contractual, anti-circumvention, defamation, or trade-secret pressures. Without safe harbor, only large institutions can participate in scrutiny, and many culturally specific harms remain unreported.

There is also a question of **representativeness**. Civil society is not monolithic, and some groups may themselves be ideologically aligned, donor-dependent, or unrepresentative of affected populations. Multi-stakeholder design must therefore avoid romanticizing “community input.” Useful correctives include transparent selection criteria, rotation, public disclosure of affiliations, plural representation across contested issues, and process rules that distinguish evidentiary claims from normative demands.

At the same time, the critique that civil society lacks technical sophistication is often overstated. Many of the relevant harms are hybrid: they concern both social meaning and technical behavior. A disability-rights organization may be better placed than an ML lab to detect when a system’s polite refusal style effectively denies autonomy; a migration-rights group may better identify when a chatbot’s framing systematically deters lawful options. Technical expertise remains necessary, but not sufficient.

One promising model is **paired scrutiny**, in which civil-society groups collaborate with independent technical labs or university centers. The community partner supplies grounded problem formulation and harm interpretation; the technical partner supplies test design, measurement, and reproducibility. This hybrid arrangement better fits persona governance than purely technical benchmarking because it joins empirical detection with socially legible interpretation.

A further reason civil-society oversight matters is that it can surface the **politics of omission**. Corporate transparency reports and audits tend to focus on known categories such as toxicity, bias, robustness, and security. But machine character is also encoded through what is not disclosed: the moral assumptions in a refusal taxonomy, the geography of policy testing, the languages omitted from red-teaming, the cultural worldview embedded in “helpfulness,” or the social groups excluded from advisory review. Civil-society actors are often the only institutions with incentive to ask why those omissions persist.

Thus, in a robust accountability ecosystem, civil society should be understood not as a peripheral stakeholder but as a **countervailing institutional force** against concentrated corporate authority over machine-mediated speech and advice.

## Standards Bodies, Public Accountability Ecosystems, and Cross-Jurisdiction Coordination

### Standard-setting as a coordination layer for behavioral assurance

The earlier report surveyed frameworks such as NIST AI RMF, ISO/IEC 42001, OWASP GenAI guidance, and EU legal obligations. This section is distinct in focus: it evaluates **standards bodies as coordinators of external scrutiny and behavioral assurance**, especially where hard law, audits, and public accountability need common vocabularies and interoperable expectations.

Standards bodies occupy an intermediate institutional position. They rarely have direct coercive power, but they shape what becomes measurable, procurable, auditable, and eventually regulable. In the LLM persona context, this agenda-setting function is highly consequential because the hardest governance problems involve ambiguity about what should count as evidence of acceptable deployed behavior.

General governance standards already emphasize lifecycle controls, roles, monitoring, and continuous improvement. Practical governance commentary in 2026 often treats [NIST AI RMF](https://nvlpubs.nist.gov/nistpubs/ai/nist.ai.100-1.pdf), [ISO/IEC 42001](https://www.iso.org/standard/81230.html), and related materials as organizational backbones for AI governance systems ([5](https://www.getagentid.com/resources/ai-governance-in-2026)). However, these instruments remain relatively high-level with respect to the normative and behavioral specifics of deployed LLM systems. They are better at saying that governance processes should exist than at defining what a sufficiently scrutinized conversational persona looks like in multilingual, multi-actor, high-stakes environments.

The value of standard-setting here lies in four coordination functions:

| Coordination function | Contribution to deployed persona governance |
|---|---|
| Terminology harmonization | Provides shared definitions for persona-relevant concepts such as refusal policies, escalation behavior, behavioral drift, and value-sensitive deployment |
| Evidence structuring | Clarifies what documentation, logs, tests, and change records should exist for auditors and regulators to review |
| Process comparability | Enables evaluation of whether different organizations follow sufficiently rigorous governance procedures |
| Market signaling | Allows procurement bodies, insurers, and counterparties to demand baseline behavioral assurance practices |

Without such coordination, each company defines its own safety language, each auditor its own test logic, and each regulator its own reporting expectations. This fragmentation is especially problematic in compositional deployments, where multiple firms and public agencies must exchange evidence about how a system’s behavior is assembled.

A mature standards agenda for deployed LLM behavior would likely need to cover at least six domains not yet fully stabilized across existing instruments:

1. **Behavioral change management**: when a prompt, policy, model version, or retrieval rule change is material enough to trigger re-testing or disclosure.
2. **Normative decision logging**: how organizations document value-laden policy choices, trade-offs, and approvals.
3. **Cross-lingual and cross-cultural evaluation protocols**: minimum expectations for multilingual testing and local contextualization.
4. **Complaint taxonomy for behavioral harms**: standard categories for reporting paternalism, ideological asymmetry, epistemic marginalization, overblocking, and refusal inconsistency.
5. **Shared-responsibility mapping**: how upstream and downstream actors allocate duties for persona-affecting controls.
6. **Public reporting tiers**: what should be disclosed publicly, to regulators, and to independent auditors.

The danger is that standards processes can be dominated by the most resourced firms, producing an industry-friendly vocabulary that narrows the range of legible harms. This is a familiar problem in transnational technical standardization, but it is particularly serious for LLM behavior because incumbents already control the dominant evaluation infrastructures, benchmark datasets, and production telemetry. If the same firms also dominate standard-setting, they may effectively define which kinds of machine character count as auditable or problematic.

This is why multi-stakeholder composition in standards bodies is not a procedural nicety but a governance necessity. Public-interest representation should include not only civil-society groups and academic experts, but also linguistically and regionally diverse participants, sector specialists


## Political Economy of Persona Rulemaking: Who Gets to Define “Good” Machine Conduct

### Corporate constitutionalism as private governance over public discourse

The existing reports already established that safety personas are not culturally neutral and that cross-cultural mismatch is a governance problem rather than a mere localization problem. This section therefore shifts from *whether* value encoding is political to *how power is organized* when firms operationalize values into deployed personas at scale. The relevant governance issue is not only bias in outputs, but the emergence of a private rulemaking function: a small number of model providers write behavioral constitutions, safety taxonomies, refusal styles, and moderation priorities that then propagate through APIs, enterprise wrappers, and downstream applications.

Constitutional AI and analogous policy-layer techniques are often described as methods for making model behavior more transparent, corrigible, and normatively constrained. Yet from an institutional perspective they also consolidate agenda-setting power. A provider decides which principles are elevated to constitutional status, how conflicts between principles are resolved, which exceptions are permitted, what kinds of speech trigger paternalistic intervention, and how much deference the system gives to user autonomy versus provider-defined risk avoidance. Those decisions can be partially documented, but the practical authority to determine machine character remains upstream and highly concentrated. In global deployments, this resembles a form of platform governance over communicative norms rather than a narrow engineering choice.

This concentration matters because deployed LLMs increasingly intermediate education, search, customer service, health triage, workplace assistance, and public-facing administrative communication. If one provider’s safety architecture becomes embedded across many sectors, the provider’s preferred style of caution, civility, moral framing, and deference to authority can become infrastructural. The Tech Policy Lab paper on U.S. law and generative AI warns that applying adaptations of the same LLM across multiple automated decision tasks can subject individuals to a homogeneous set of judgments shaped by training data and alignment choices, increasing arbitrary exclusion and disproportionately affecting marginalized groups; the paper gives examples including African American language being unfairly flagged by toxicity filters and culturally specific expression being misclassified as inappropriate ([1](https://techpolicylab.uw.edu/wp-content/uploads/2026/02/s43681-024-00451-4.pdf)). That observation should be extended beyond classification error: a homogeneous safety persona can also standardize a narrow theory of appropriate expression across many contexts.

A key asymmetry follows. Users experience the assistant as conversational and adaptive, but the institutional design is often one-directional. The provider can alter default refusals, emotional tone, ideological caution, sexual norms, or political sensitivity thresholds for millions of users at once. Individual users and many enterprise customers can tune prompts or retrieval layers, but they generally cannot inspect or negotiate the deeper policy hierarchy that determines the system’s fallback conduct. This creates what may be called **population-scale character setting**: firms define the default behavioral disposition of synthetic interlocutors that mediate everyday cognitive and social tasks.

The political significance of this should not be understated. Historically, contested questions about acceptable speech, advice, morality, and authority were distributed across schools, professions, courts, legislatures, religious institutions, media, and local communities. Deployed LLMs partially recombine these functions into commercial systems whose persona is shaped by internal safety teams, legal departments, trust-and-safety operations, red-team findings, and branding concerns. The result is not state censorship in the classic sense, but neither is it simple product design. It is a hybrid mode of private normative ordering.

### Market incentives and the tendency toward overbroad, exportable safety defaults

The quoted literature is especially useful here because it rejects the assumption that market incentives necessarily produce socially adequate safety. The U.S. law and generative AI analysis explicitly notes that “profit incentives do not automatically encourage robust safety efforts” and situates value disputes in a world characterized by cultural and value diversity rather than ethical consensus ([1](https://techpolicylab.uw.edu/wp-content/uploads/2026/02/s43681-024-00451-4.pdf)). From the standpoint of persona governance, the stronger point is that market incentives may produce **specific kinds** of safety: low-liability, brand-protective, scalable, and globally portable. Those are not the same as democratically legitimate or culturally responsive safety.

Providers face strong incentives to avoid scandal, legal exposure, and regulator attention. That often leads to generalized, easily administrable rules: broad sexual-content suppression; expansive self-harm intervention scripts; rigidly sanitized political tone; aggressive toxicity filtering; default deference to mainstream professional advice; and refusal templates designed for high recall rather than contextual legitimacy. Such defaults can be commercially rational because they reduce tail risks and simplify compliance operations across jurisdictions. But they also push systems toward a universalized “safe helper” archetype grounded in the provider’s preferred risk posture.

The issue becomes sharper when systems are exported into jurisdictions where conversational norms differ. In some settings, direct discussion of religion, family hierarchy, sexuality, death, or political authority may require forms of indirection, deference, or contextualization that a U.S.-trained safety persona does not provide. In others, a heavily paternalistic refusal style may be interpreted as moralizing or infantilizing. Conversely, a permissive style calibrated around Western assumptions about autonomy or open discussion may be seen as socially disruptive or unlawful. A single global persona therefore creates distributional effects: some users interact with a machine voice that feels native to their normative environment, while others must adapt themselves to the machine’s imported norms.

This is partly why recent alignment scholarship emphasizes pluralistic values rather than singular optimization. The *International AI Safety Report 2026* cites work such as *Value Kaleidoscope: Engaging AI with Pluralistic Human Values, Rights, and Duties*, Caputo’s legal-theory framework for pluralistic AI alignment, and sociotechnical work on aligning AI with pluralistic human values ([2](https://internationalaisafetyreport.org/sites/default/files/2026-02/international-ai-safety-report-2026.pdf), [3](https://internationalaisafetyreport.org/publication/international-ai-safety-report-2026), [4](https://www.preprints.org/frontend/manuscript/a5d014a0dbc5460091e8ce3a5d0fe092/download_pub)). In governance terms, this literature challenges the operational fiction that one constitutional layer can neutrally encode “human values” for global deployment. The more realistic picture is that providers choose among incommensurable goods—autonomy, dignity, non-offense, candor, public safety, equality, tradition, religious respect, therapeutic caution, child protection, anti-discrimination—and then conceal many of these tradeoffs behind general language like “helpful, harmless, and honest.”

### The hidden layering of authority in enterprise deployments

Corporate power is not limited to base-model providers, although they remain the dominant upstream actors. In enterprise deployments, value encoding is typically layered: the provider supplies moderation APIs, refusal boundaries, system instruction defaults, and latent alignment; the enterprise adds role definitions, domain-specific prohibitions, retrieval corpora, escalation policies, and brand voice; integrators may add security guardrails, policy engines, and conversation flows; end-users then shape behavior through prompts and iterative steering. The resulting persona is a negotiated artifact, but not an equal one.

Power asymmetry appears in three ways:

1. **Upstream irreversibility.** Enterprises can often add narrower restrictions, but they may be unable to remove broad provider-level moral or safety assumptions.
2. **Downstream attribution asymmetry.** Harms are experienced at the application level, while the causal source may lie in inaccessible upstream policy tuning.
3. **Normative dependency.** Smaller firms, public agencies, and civil-society deployers become dependent on the constitutional choices of a handful of foundation-model vendors.

This means market structure and persona governance are tightly linked. If a concentrated model market supplies the behavioral substrate for thousands of downstream products, then constitutional choices by a few firms can dominate the machine-mediated public sphere. The arXiv paper on governance opacity argues that as capability asymmetry grows, disclosure-based remedies become less effective and transparency loses traction when systems can game evaluation or become entangled with governance processes themselves; it identifies strain on legitimacy and non-domination as especially persistent across governance arrangements ([5](https://arxiv.org/abs/2604.14070)). Applied to persona governance, the point is that traditional transparency tools may not sufficiently discipline private actors who define machine character while also controlling the evidence by which that character is assessed.

### Why “choice” by users does not solve legitimacy deficits

A common response is that users can choose among providers, prompts, or applications, making persona a market preference rather than a legitimacy problem. That claim is weak for at least four reasons.

First, switching costs are real when assistants are embedded into enterprise workflows, operating systems, educational tools, or public services. Second, many users cannot evaluate the constitutional premises of a model before use. Third, app-level variety may mask common upstream alignment dependencies if many products use the same base model or moderation stack. Fourth, persona is often imposed in contexts where opting out is costly or impossible, such as workplace systems, school tools, public-benefit interfaces, or dominant consumer platforms.

Thus, user choice does not substitute for accountable rulemaking where machine personas shape access to information, advice, and institutional voice. In those settings, defining machine character becomes analogous to setting procedural norms for public-facing intermediaries. Even if the legal form remains private, the social function is quasi-public.

### Governance implications for constitutional AI processes

The main topic of the larger report includes constitutional AI governance processes. The political-economy lens here suggests that procedural safeguards for those processes should be judged less by whether they produce smoother refusals and more by whether they disperse authority, surface tradeoffs, and permit revision by affected communities. A constitution written solely by internal staff may improve consistency while worsening legitimacy. Likewise, documentation that lists principles without showing their provenance, prioritization logic, or regional variance remains insufficient.

A more institutionally serious constitutional process would distinguish at least five layers of authority:

| Governance layer | Typical actor | Main power over persona | Main legitimacy problem |
|---|---|---:|---|
| Base constitutional principles | Foundation model provider | Sets default moral hierarchy and refusal logic | Private unilateral rulemaking |
| Safety implementation | Provider trust/safety and policy teams | Encodes thresholds, classifiers, templated interventions | Hidden tradeoffs and overbreadth |
| Domain adaptation | Enterprise deployer | Adds role-specific norms and escalation rules | Limited ability to alter upstream assumptions |
| Interaction customization | Integrators / admins | Prompting, workflow, retrieval, UI framing | Can amplify or obscure upstream values |
| User steering | End user | Local conversational direction | Weak real control over hard boundaries |

This layered view reveals that “who defines machine character” is not a single decision but a stack of decision rights distributed unequally. Governance frameworks that emphasize documentation, red teaming, or incident reporting without reallocating or contestabilizing those decision rights leave the deepest power asymmetry intact.

## Evidence of Western-Centric Safety and Constitutional Bias in Persona Design

### Safety language often universalizes historically local norms

The previous reports noted structural Western defaulting. This section adds a more specific claim: Western-centricity is often visible not only in substantive outcomes but in the *grammar* of safety itself. Many deployed assistants encode a style of moral reasoning recognizable from Anglo-American institutional culture: rights talk, individual risk framing, therapeutic disclaimers, legalistic hedging, civility norms detached from local rhetorical practice, and a presumption that legitimacy comes from abstract universal principles rather than situated authority structures. This does not mean every Western model expresses identical values, nor that all non-Western contexts reject these forms. It means that systems frequently present one culturally situated style of safe conduct as if it were neutral procedural reason.

The literature cited in the user materials supports this broader diagnosis. The *International AI Safety Report 2026* references pluralistic-values research precisely because universal alignment remains unresolved ([2](https://internationalaisafetyreport.org/sites/default/files/2026-02/international-ai-safety-report-2026.pdf)). The cited *Value Kaleidoscope* work frames alignment in terms of pluralistic human values, rights, and duties rather than a single moral objective, underscoring the insufficiency of one-dimensional “human values” abstractions ([3](https://internationalaisafetyreport.org/publication/international-ai-safety-report-2026)). Likewise, the sociotechnical alignment paper foregrounds pluralistic human values as a core design challenge ([4](https://www.preprints.org/frontend/manuscript/a5d014a0dbc5460091e8ce3a5d0fe092/download_pub)). Taken together, these sources reinforce the point that safety constitutions cannot be presumed culturally innocent merely because they are framed in high-level ethical language.

One practical indicator of Western-centricity is when an assistant’s refusal or advice style defaults to idioms associated with U.S.-style institutional communication: disclaimers about liability, repeated referral to licensed professionals, assumptions about direct self-advocacy, and conflict-averse but strongly standardized civility enforcement. In many contexts, this appears as machine conduct that is formally polite but socially off-key. A second indicator is differential treatment of rhetorical forms common in minority or non-Western language communities. The Tech Policy Lab article’s example of African American language being unfairly flagged by toxicity filters is especially important because it shows that safety systems may interpret culturally situated speech through a majority-coded lens, turning linguistic difference into apparent risk ([1](https://techpolicylab.uw.edu/wp-content/uploads/2026/02/s43681-024-00451-4.pdf)).

### Constitutional AI can encode bias through principle selection, not only data skew

Discussion of Western-centricity often focuses on training data, but constitutional and policy layers deserve separate scrutiny. A model may be multilingual and broadly trained yet still exhibit Western-centric safety because post-training alignment has elevated a specific normative package. Principle selection matters: whether the constitution prioritizes non-offense over candor, individual consent over communal obligations, anti-paternalism over social conservatism, or vice versa. It also matters how conflicts are adjudicated. A rule such as “avoid reinforcing harmful stereotypes” can be applied narrowly to protect groups against abuse or broadly to suppress lawful discussion of culturally contested topics. A principle like “respect autonomy” may empower users in one setting while clashing with professional, familial, or religious norms in another.

The risk is not that constitutional AI is uniquely Western by definition. The risk is that, in practice, constitutional drafting and red-teaming ecosystems are concentrated in institutions with shared educational, political, and linguistic backgrounds. This concentration shapes what counts as harm, whose offense is legible, what forms of authority are trusted, and what social goals justify intervention. The values encoded in machine learning research itself have been criticized on similar grounds; Birhane et al.’s work, cited in the *International AI Safety Report*, examines the values embedded in ML research practice, highlighting that technical agendas are already value-laden before deployment ([2](https://internationalaisafetyreport.org/sites/default/files/2026-02/international-ai-safety-report-2026.pdf)).

A useful analytic distinction is between **substantive bias** and **procedural bias** in constitutions:

| Type of bias | How it appears in persona governance | Example consequence |
|---|---|---|
| Substantive bias | One moral framework is repeatedly preferred in conflict rules | Assistant consistently privileges individual self-expression over communal harmony, or the reverse |
| Procedural bias | Some communities have little voice in drafting, testing, and revising principles | Harm categories reflect the salience map of U.S./EU policy teams rather than global users |
| Linguistic bias | Safety classifiers and refusal templates are calibrated around majority-language norms | Minority vernaculars trigger false positives for toxicity or instability |
| Epistemic bias | Provider-approved institutions are treated as the default source of legitimate knowledge | Religious, customary, or community-led reasoning is sidelined even when lawful and relevant |
| Temporal bias | Safety constitutions freeze one historical moment’s norms into persistent defaults | Rapid social change in target jurisdictions is not reflected in model behavior |

This table is analytically important because governance remedies differ by bias type. More data will not solve procedural exclusion; better translation will not solve normative overreach; and transparency about refusal rates will not by itself reveal epistemic hierarchy.

### The “Western” problem is not reducible to geography

Care is needed here. Western-centricity should not be caricatured as simply “U.S.-made models reflect U.S. values.” The deeper issue is transnational elite convergence. Safety teams, legal advisors, benchmark designers, academic collaborators, and standards participants may be geographically diverse yet still share similar professional worldviews—rights-oriented, technocratic, managerial, secularized, platform-mediated, and Anglophone in working norms. This can produce machine personas that are globally polished but still narrow in moral imagination.

Such convergence has two governance consequences. First, it can create false confidence that a process is pluralistic because it includes geographically distributed experts. Second, it can crowd out forms of knowledge that do not present themselves in the idiom of policy workshops, benchmark taxonomies, or compliance checklists. The result is often not explicit hostility to non-Western values, but their translation into categories already legible to provider institutions. Duties become “preferences,” religious norms become “sensitive content,” communal obligations become “cultural context,” and sovereignty concerns become “market customization.”

The political concern is therefore not only bias but **assimilation pressure**: people must express their concerns in the constitutional language the provider recognizes. That is a subtle but consequential form of power.

### Safety bias can also be internal to Western pluralism

Another caution is that “Western-centric” may still be too broad. In practice, many deployed safety personas reflect not generic Western values but a narrower subset associated with large U.S. technology firms and adjacent professional cultures. Those cultures may overrepresent certain priorities—anti-harassment norms, liability avoidance, therapeutic framings of distress, procedural neutrality, anti-extremism heuristics, and reputational risk management—while underrepresenting others, including labor perspectives, religious conservatism, postcolonial concerns, disability justice specificities, linguistic minority experiences, or class-based differences in communicative style. Thus even within the West, machine constitutions may express elite-platform values rather than broad democratic consensus.

That matters for governance because global critiques of Western bias should not obscure internal representational deficits. A persona can be exclusionary abroad and domestically at the same time. The remedy is not to replace one civilizational center with another, but to build institutional processes that can represent contestation more faithfully.

## The Limits of Cultural Adaptation in Deployment-Layer Customization

### Why downstream localization cannot reliably override upstream constitutional structure

Existing reports already discussed why cross-cultural deployment is more than translation or local UX. This section narrows further to a deployment-layer question: even when enterprises want culturally appropriate adaptation, how much can they actually change? The answer is often: less than appears.

In compositional systems, downstream actors typically control prompts, retrieval, interface copy, tool access, and some policy logic. Upstream actors control model weights, fine-tuning history, moderation systems, system-level instructions, refusal templates, and often hidden reinforcement signals. Because base-model behavior shapes interpretation, style, and fallback responses, downstream localization may only decorate an upstream persona rather than reconstitute it. A company may tell the model to be respectful of local customs, but when the interaction nears a hard safety boundary the assistant commonly reverts to provider-default framing.

This is particularly important for constitutional AI because constitutional layers often sit close to the model’s core behavioral policy. If the constitution encodes a specific theory of harmful advice, offense, intimacy, or political risk, downstream developers may be unable to localize the system without either violating provider terms or inducing unstable behavior. The net effect is a narrow adaptation corridor: surface flexibility atop deep rigidity.

The practical consequences are visible in several recurring deployment patterns:

| Deployment pattern | What downstream actor changes | What remains upstream | Likely limitation |
|---|---|---|---|
| Prompt-localized assistant | Language, style, role description | Core refusal logic, latent moral hierarchy | Local tone without local normative fit |
| Retrieval-augmented localization | Local laws, cultural FAQs, policy docs | Interpretation of retrieved material; final response style | Contradictory outputs when local content conflicts with provider defaults |
| Domain fine-tuning | Sector-specific examples and tasks | Embedded safety priors and moderation boundaries | Better relevance but unchanged constitutional assumptions |
| UI/UX adaptation | Visual framing, disclaimers, escalation buttons | Underlying speech norms and intervention style | Perceived local product, imported persona |
| Region-specific filtering | Additional blocked topics or workflow controls | Base style and general risk categories | Can intensify overblocking without genuine cultural competence |

The significance for governance is that “local customization” should not be assumed to equal local control. In many cases it means that local deployers become responsible for harms caused by a personality architecture they cannot fully inspect or alter.

### Cultural prompting and adaptation can improve fit without solving legitimacy

The prior subtopic reports mentioned evidence that cultural prompting improves alignment in many jurisdictions. This section differs by examining the governance implications of that fact. Improvement under prompting is not the same as legitimate adaptation. If a model can be steered to mimic local values in 71–81% of countries and territories, as one prior report summarized, that shows some flexibility—but it also shows that local fit is contingent, prompt-mediated, and potentially shallow. Prompting may change rhetoric more readily than conflict resolution rules. It may alter examples and tone while leaving deep prioritization intact. It may also work unevenly across domains, overfitting benign conversations while failing under stress cases.

Moreover, culturally adaptive prompting can create a dangerous illusion of solved pluralism. Enterprises may believe they have localized a system because benchmark scores improve, while users still encounter imported assumptions in edge cases: family conflict, mental health, gender roles, religious authority, taboo topics, informal speech, or political grievance. This matters because legitimacy failures often appear at the margins rather than in routine interactions.

The sociotechnical alignment literature supports this caution by treating pluralistic alignment as an institutional and contextual challenge rather than a one-shot technical adjustment ([4](https://www.preprints.org/frontend/manuscript/a5d014a0dbc5460091e8ce3a5d0fe092/download_pub)). Likewise, the pluralistic orientation of *Value Kaleidoscope* implies that responsive engagement with values, rights, and duties requires more than a style transfer layer ([3](https://internationalaisafetyreport.org/publication/international-ai-safety-report-2026)).

### Deployment adaptation can create norm collisions between layers

A distinctive problem in compositional deployments is **norm collision**: downstream localization introduces local content or instructions that partially conflict with upstream alignment. The model then tries to reconcile incompatible directives, often producing unstable or incoherent behavior. For example, an enterprise assistant serving a conservative social context may retrieve local guidance that assumes stronger family authority or more restrictive norms around sexuality, while the base model’s constitutional layer still speaks in a strongly individual-autonomy idiom. The resulting response may alternate between deference to local norms and provider-style universal caution, confusing users and complicating accountability.

A similar collision occurs in public-sector or regulated uses. A government agency may require the assistant to explain local entitlements, procedural rights, and administrative obligations. Yet the provider’s default style may favor generic, decontextualized safety hedges or broad referrals to professionals, which can weaken procedural clarity. Even when all parties are acting in good faith, the assembled persona may become neither fully local nor reliably universal.

This is why deployment-layer review needs to focus on **interaction effects under normative conflict**, not just average task performance. Existing governance tools often emphasize security vulnerabilities, hallucinations, or prohibited content. They less often evaluate whether the assistant can maintain a coherent and legitimate moral voice when the retrieval layer, system prompt, enterprise policy, and provider constitution embody different value orders.

### Less-resourced languages and markets face deeper adaptation constraints

Adaptation limits are magnified in less-resourced languages and markets. Providers typically optimize highest-volume languages first; safety classifiers, red-team data, and constitutional exemplars are richer for English and a small number of major languages. Where linguistic resources are scarce, local deployers may lack both technical leverage and empirical evidence to validate adaptation. The system may therefore present itself as culturally general while relying on thinner safety calibration and weaker semantic understanding in the very settings where mismatch risk is highest.

The materials provided include discussion from the ELRA list emphasizing identity representation in LLMs, the encoding or erasure of diverse identities, and the need for methodological foundations from social science when measuring values, morals, and narratives across populations ([6](https://list.elra.info/mailman3/hyperkitty/list/corpora@list.elra.info/latest?count=200&page=3)). That line of work is relevant because low-resource cultural adaptation is not merely a translation challenge; it requires the ability to detect identity-linked meanings, rhetoric, and value-laden discourse without collapsing them into majority categories.

An implication for governance is that deployment approval should be stricter, not looser, in low-resource settings. Where providers have less evaluation coverage, stronger obligations should attach to uncertainty disclosure, local testing, and appeal channels. Otherwise, the populations with the least voice in constitutional drafting become those most exposed to miscalibrated persona enforcement.

### Agentic systems make localization harder, not easier

The broader governance landscape now includes emerging frameworks for agentic AI. The arXiv paper on autonomous agent economies notes that NIST launched an AI Agent Standards Initiative in February 2026 targeting interoperability, security, and testing, with additional work on agent identity and authorization, while Singapore released a January 2026 Model AI Governance Framework for Agentic AI as the first national framework specifically designed for agentic systems ([7](https://arxiv.org/html/2603.25100v1)). For persona governance, the relevance is that agentic systems expand the surface on which value encoding matters. The system no longer only speaks; it plans, delegates, transacts, and persists.

This increases adaptation difficulty. A conversational mismatch may be irritating; an agentic mismatch can produce concrete actions inconsistent with local norms or institutional expectations. If the agent decides when to escalate, whom to notify, how forcefully to challenge the user, what counts as suspicious behavior, or which authorities to defer to, constitutional bias migrates from dialogue style into workflow execution. Downstream customization may be even less effective here because action policies are intertwined with security and safety controls. Thus cultural adaptation in agentic deployments is likely to face a double bind: more consequential value conflicts and fewer permissible override points.

## Cross-Jurisdiction Governance Problems: Legitimacy, Sovereignty, and Interoperability of Value Regimes

### Conflicts between universal safety claims and plural legal-moral orders

This section differs from previous material by focusing less on cultural mismatch in user experience and more on governance conflict across jurisdictions. Once LLM personas are deployed globally, value encoding creates a problem of **interoperability between value regimes**. A provider may market one constitutional framework as universal safety, but states and communities may understand the same behavior as ideological filtering, moral intrusion, under-enforcement, or foreign normative influence.

Three layers of conflict are common:

1. **Legal conflict:** local law permits, requires, or forbids speech and assistance differently from provider policy.
2. **Institutional conflict:** local authorities expect different modes of deference, explanation, or escalation than the model provides.
3. **Cultural-political conflict:** the assistant’s style is perceived as importing foreign values into sensitive domains of family, religion, sexuality, political criticism, or social hierarchy.

The Bangladesh-focused commentary provided in the source set uses the language of “cultural sovereignty” to describe intimate social life being outsourced to foreign platforms with limited accountability to local cultural, religious, or ethical frameworks ([8](https://tuhinsarwar.com/exposing-adult-romantic-ai-companions)). That source is not a neutral institutional report, but it captures a governance concern that extends beyond one jurisdiction: when machine personas enter culturally sensitive domains, disputes are likely to be framed not just as consumer-protection problems but as sovereignty claims. This is especially salient for companionship systems, educational assistants, and public-information interfaces because they mediate norms, not only facts.

The challenge for governance is that pluralism cannot simply mean “each jurisdiction gets its own moral model” either. Some local demands will conflict with internationally recognized rights, anti-discrimination norms, or basic safety duties. Hence persona governance sits between two unsatisfactory extremes: universalized private constitutions that flatten pluralism, and unconstrained local tailoring that can legitimate repression or exclusion.

### Existing governance frameworks are better at risk management than value adjudication

Current frameworks under the larger report’s scope—constitutional processes, OWASP-style security guidance, model and risk cards, the EU AI Act ecosystem, and multi-stakeholder oversight proposals—are more mature in identifying risks than in adjudicating value conflict. OWASP guidance can help preserve system boundaries, prevent prompt injection, and limit harmful tool use, but security controls do not decide how a model should speak about religion, family authority, or political dissent. Documentation standards can disclose some assumptions, but they do not tell regulators when a provider’s exported persona has become an illegitimate exercise of private normative power. Even legal frameworks with fundamental-rights orientation generally regulate harms, transparency, and oversight structures more readily than the substantive content of machine character.

This gap matters because a large share of cross-jurisdiction conflict will not present as obvious illegality. Instead it will involve persistent low-grade legitimacy deficits: users feel misrecognized, institutions perceive foreign framing, local enterprises cannot fully adapt imported models, and governments suspect that behavioral defaults are shifting public discourse without local mandate. These are precisely the kinds of problems that technical assurance regimes tend to under-detect.

The governance-opacity paper is useful in this context because it emphasizes legitimacy, accountability, non-domination, subsidiarity, and resilience as evaluative dimensions ([5](https://arxiv.org/abs/2604.14070)). These dimensions offer a richer vocabulary than ordinary compliance language for assessing cross-jurisdiction value conflict. In particular:

- **Legitimacy** asks whether those subject to persona rules have reason to accept their authority.
- **Non-domination** asks whether firms can arbitrarily shape communicative conditions without effective checks.
- **Subsidiarity** asks whether value decisions are made at an appropriate level, close enough to affected contexts.
- **Resilience** asks whether institutions can adapt when value conflict generates backlash or harm.

### The unresolved question of whose “public reason” governs transnational assistants

Many alignment programs implicitly assume that a model should adopt something like public reason: a neutral, broadly shareable style of justification that avoids sectarian commitments. Yet in practice “public reason” is not culturally empty. It usually arrives in the form of secularized, rights-oriented, professionally sanitized discourse. That may be appropriate in some public-service contexts, but when exported globally and applied across intimate, educational, or community settings it can displace other legitimate forms of moral reasoning.

The problem is not that assistants should become sectarian. It is that no transnational provider can unilaterally decide what counts as universally acceptable public reason for all societies. If firms attempt this, they assume an authority that democracies themselves struggle to justify. If they decline entirely and localize everything, they risk fragmenting safety and enabling harmful or discriminatory deployments.

This suggests that governance should distinguish at least three categories of persona authority:

| Category | Appropriate source of authority | Governance implication |
|---|---|---|
| Baseline safety constraints against severe harm | Broad international and scientific consensus where available | Strong provider-level controls justified, but still reviewable |
| Context-sensitive norms of interaction and advice | Local institutions and affected communities | Requires regional adaptation and contestation mechanisms |
| Deeply contested moral-political questions | Democratic, legal, and plural deliberative processes | Providers should avoid pretending neutrality and expose tradeoffs explicitly |

Current governance regimes often collapse these categories. They treat all safety questions as if they were baseline severe-harm issues, thereby legitimating broad provider control over matters that are actually context-sensitive or deeply contested.

### Jurisdictional fragmentation may intensify corporate power unless coordination improves

An intuitive response to cross-jurisdiction conflict is more national regulation. But fragmentation has ambivalent effects. On one hand, it can force providers to account for local norms and legal requirements. On the other, it can increase dependence on large firms with the resources to manage compliance variants. Smaller actors may struggle to produce jurisdiction-specific personas, widening concentration. Large providers can then become brokers among legal systems, deciding how much adaptation is technically possible and where to standardize anyway.

The emerging attention to agentic governance may intensify this pattern. As noted, NIST’s 2026 initiative and Singapore’s 2026 agentic framework indicate that regulators are moving toward coordination on interoperability, security, and testing for agents ([7](https://arxiv.org/html/2603.25100v1)). However, interoperability at the technical level does not automatically produce interoperability at the value level. In fact, common technical standards may make it easier for a few global providers to export standardized action policies unless governance explicitly reserves space for local normative control.

### The risk of strategic adaptation: appearing local while preserving upstream hegemony

Cross-jurisdiction governance should also anticipate **strategic adaptation** by providers. Firms may localize visible elements—language, examples, region-specific legal notices, cultural holidays—while preserving the upstream constitutional architecture that matters most. This can satisfy superficial regulatory or market expectations without ceding real authority. It may also obscure user awareness that the assistant’s deep conflict-resolution rules remain imported.

A governance response would require not only outcome testing but **provenance disclosure**: which elements of persona are globally fixed, which are jurisdiction-specific, who authorized each variation, and what evidence supports its fit. Without that distinction, “localized” deployments can function as a veneer over centralized normative control.

## Institutional Mechanisms for Contestability and Shared Authority over Machine Character

### From disclosure to representation in persona governance

The earlier reports covered documentation artifacts and external scrutiny models. This section differs by specifying what institutional mechanisms are needed when the core problem is not lack of information alone, but lack of shared authority over machine character. In other words, the remedy for population-scale value encoding cannot be exhausted by model cards, risk cards, or even sophisticated auditing. Those tools are necessary, but they do not themselves create representation.

A more adequate governance design would treat persona rulemaking as a recurring institutional process with input, veto, revision, and appeal capacities distributed across multiple actors. The design challenge resembles governance of standards, medicine, or administrative procedure more than ordinary software release management. The key question becomes: how can different communities meaningfully influence the encoded conduct of systems they cannot individually inspect or retrain?

At minimum, four institutional functions are needed:

1. **Value provenance disclosure** – not merely what the model does, but where the governing principles came from.
2. **Plural input channels** – structured participation by regionally grounded, domain-specific, and affected-user groups.
3. **Conflict adjudication** – a mechanism for deciding when provider defaults should yield to local adaptation or rights-based constraints.
4. **Remediation and revision** – operational pathways to change machine conduct after legitimate challenge.

These functions can be distributed across providers, regulators, standards bodies, sectoral institutions, and civil-society intermediaries. The crucial point is that persona governance requires ongoing institutions, not one-time ethics statements.

### Persona councils, regional review boards, and sectoral norm panels

One practical mechanism is a **persona governance council** attached to major providers or required for high-impact deployers. Unlike generic ethics boards, such councils would focus specifically on behavioral constitutions, refusal taxonomies, intervention styles, and region-specific divergence. Their legitimacy would depend on composition, mandate, and powers. A purely advisory body handpicked by the provider would not suffice. More credible arrangements would include independent members, publishable dissents, conflict-of-interest rules, and authority to trigger external review.

A second mechanism is the **regional review board**. The purpose is not to demand full moral relativism, but to evaluate whether a globally deployed persona is imposing avoidable normative mismatch in a specific jurisdiction or language community. These boards would examine evidence from user complaints, red-team cases, civil-society submissions, and sector-specific deployments. They could recommend localized variants, stronger disclosures, or restrictions on use in sensitive domains.

A third mechanism is the **sectoral norm panel** for domains such as health, education, employment, public services, or intimate companionship. Machine character that is acceptable in entertainment may be unacceptable in welfare administration or mental-health support. Sectoral panels would therefore assess not only content risk but role legitimacy: what kind of voice should an assistant have in that institutional setting, and what kinds of persuasion, refusal, empathy, or deference are appropriate?

These mechanisms become especially important in agentic settings, where the system’s “character” affects not just words but decisions and actions. The movement toward AI agent standards and governance frameworks suggests an opening to embed such structures before action-capable personas become ubiquitous ([7](https://arxiv.org/html/2603.25100v1)).

### Behavioral change control should be governed like a public-risk process

Another institutional gap concerns updates. Providers routinely adjust safety policies, refusal thresholds, moderation systems, and constitutional prompts. Yet those changes can materially alter the machine’s social behavior for millions of users. If machine character is socially consequential, major behavioral updates should be subject to **change control** procedures analogous to those used in other public-risk domains.

A rigorous change-control regime would require:

| Change-control element | Why it matters for persona governance | Example trigger |
|---|---|---|
| Materiality threshold | Distinguishes cosmetic updates from conduct-changing revisions | New refusal class for political persuasion |
| Pre-deployment impact assessment | Identifies affected groups and likely cross-cultural effects | Expansion of self-harm intervention scripts |
| Regional variance analysis | Tests whether the update shifts behavior unevenly across languages or jurisdictions | Retuning toxicity filters |
| Notice and explanation | Lets enterprise customers and overseers understand new machine conduct | Revised constitutional principles |
| Post-change monitoring | Detects emergent harms and legitimacy complaints | Surge in false refusals in minority vernaculars |
| Rollback and remediation pathway | Prevents irreversible spread of harmful persona changes | Withdrawal of a miscalibrated moderation update |

This goes beyond ordinary software governance because the object of control

## Conclusion

The report finds that governance of LLM “behavioral persona” has shifted from a narrow focus on base-model safety to the full deployed stack, where values and conduct emerge from layered alignment methods, system prompts, retrieval, tools, memory, enterprise policy, and user steering. Existing frameworks each address part of this problem: constitutional AI makes rule-setting more legible but leaves legitimacy and representation unresolved; NIST and Singapore provide lifecycle and ecosystem governance structures; OWASP shows that security failures are also behavioral-governance failures; and the EU AI Act indirectly constrains persona through documentation, oversight, robustness, and monitoring duties. Yet none fully resolves the central accountability gap in compositional deployments, where providers, integrators, deployers, and users can all shape behavior while each can disclaim responsibility for the final machine character experienced by the public ([Anthropic, 2022](https://www.anthropic.com/news/constitutional-ai-harmlessness-from-ai-feedback); [NIST, 2023](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf); [NIST, 2024](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf); [Singapore IMDA, 2024](https://aiverifyfoundation.sg/wp-content/uploads/2024/05/Model-AI-Governance-Framework-for-Generative-AI-May-2024-1-1.pdf); [European Union, 2024](https://eur-lex.europa.eu/eli/reg/2024/1689); [OWASP/IMDA, 2026](https://www.imda.gov.sg/-/media/imda/files/about/emerging-tech-and-research/artificial-intelligence/mgf-for-agentic-ai.pdf)).

The most important finding is that value encoding is not just a technical safety issue but a political and institutional one. Evidence of cross-cultural divergence and Western-centric bias suggests that many “safe” personas universalize the assumptions of dominant corporate and regulatory cultures, while downstream enterprises often inherit those assumptions without meaningful ability to inspect or revise them. This creates significant power asymmetries when a small number of firms define machine character at population scale, especially in high-impact domains such as health, education, employment, finance, and public services. The clearest implication is that governance must move beyond model cards toward deployment-level artifacts and institutions: behavioral policy registers, risk cards, BBOM-style documentation, persona change logs, layered audits, cross-cultural testing, and stronger public, sectoral, and multi-stakeholder oversight. Next steps should therefore focus on making behavioral responsibility visible across the stack, standardizing machine-readable documentation and incident taxonomies, and building contestability mechanisms so affected users, communities, auditors, and regulators can challenge and revise encoded machine conduct rather than merely observe it after harm occurs ([Tech Policy Lab, 2026](https://techpolicylab.uw.edu/wp-content/uploads/2026/02/s43681-024-00451-4.pdf); [International AI Safety Report, 2026](https://internationalaisafetyreport.org/sites/default/files/2026-02/international-ai-safety-report-2026.pdf); [Anderljung et al., 2025](https://cdn.governance.ai/Towards_Publicly_Accountable_Frontier_LLMs.pdf)).


## References

- [https://ns2.journals.umcs.pl/sil/article/download/20001/pdf](https://ns2.journals.umcs.pl/sil/article/download/20001/pdf)
- [https://securityboulevard.com/2026/03/the-ultimate-guide-to-llm-security-in-2026/](https://securityboulevard.com/2026/03/the-ultimate-guide-to-llm-security-in-2026/)
- [https://fsi9-prod.s3.us-west-1.amazonaws.com/s3fs-public/2024-12/GenAI_Report_REV_Master_%20as%20of%20Dec%2012.pdf](https://fsi9-prod.s3.us-west-1.amazonaws.com/s3fs-public/2024-12/GenAI_Report_REV_Master_%20as%20of%20Dec%2012.pdf)
- [https://genai.owasp.org/llmrisk/llm09-overreliance/](https://genai.owasp.org/llmrisk/llm09-overreliance/)
- [https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)
- [https://www.preprints.org/frontend/manuscript/a5d014a0dbc5460091e8ce3a5d0fe092/download_pub](https://www.preprints.org/frontend/manuscript/a5d014a0dbc5460091e8ce3a5d0fe092/download_pub)
- [https://stackcyber.com/posts/ai-eu-act](https://stackcyber.com/posts/ai-eu-act)
- [https://www.youtube.com/watch?v=diqG08-bHJo](https://www.youtube.com/watch?v=diqG08-bHJo)
- [https://www.agiloft.com/blog/ai-in-the-eu-and-how-it-impacts-clm-and-legal-tech/](https://www.agiloft.com/blog/ai-in-the-eu-and-how-it-impacts-clm-and-legal-tech/)
- [https://sparkco.ai/blog/constitutional-ai-aligning-llm-safety-in-2025](https://sparkco.ai/blog/constitutional-ai-aligning-llm-safety-in-2025)
- [https://arxiv.org/html/2603.25100v1](https://arxiv.org/html/2603.25100v1)
- [https://www.facebook.com/worldeconomicforum/posts/ai-is-shifting-from-static-tools-to-autonomous-agents-that-require-new-framework/1351065073728394/](https://www.facebook.com/worldeconomicforum/posts/ai-is-shifting-from-static-tools-to-autonomous-agents-that-require-new-framework/1351065073728394/)
- [https://www.hunton.com/privacy-and-cybersecurity-law-blog/rules-for-general-purpose-ai-models-under-the-ai-act-become-applicable](https://www.hunton.com/privacy-and-cybersecurity-law-blog/rules-for-general-purpose-ai-models-under-the-ai-act-become-applicable)
- [https://huggingface.co/papers?q=cultural%20preference%20data](https://huggingface.co/papers?q=cultural%20preference%20data)
- [https://www.aigl.blog/](https://www.aigl.blog/)
- [https://aigi.ox.ac.uk/wp-content/uploads/2026/02/Open-Problems-in-Frontier-AI-Risk-Management-Final.pdf](https://aigi.ox.ac.uk/wp-content/uploads/2026/02/Open-Problems-in-Frontier-AI-Risk-Management-Final.pdf)
- [https://internationalaisafetyreport.org/publication/international-ai-safety-report-2026](https://internationalaisafetyreport.org/publication/international-ai-safety-report-2026)
- [https://analytics.usa.gov/data/live/all-pages-realtime.csv](https://analytics.usa.gov/data/live/all-pages-realtime.csv)
- [https://reference-global.com/download/chapter/9781836203742/10.0000/9781836203742-001.pdf](https://reference-global.com/download/chapter/9781836203742/10.0000/9781836203742-001.pdf)
- [https://cybernews360.com/research](https://cybernews360.com/research)
- [https://udk.ai/alignment_symposium_0.pdf](https://udk.ai/alignment_symposium_0.pdf)
- [https://tuhinsarwar.com/exposing-adult-romantic-ai-companions](https://tuhinsarwar.com/exposing-adult-romantic-ai-companions)
- [https://aigi.ox.ac.uk/wp-content/uploads/2026/01/Kolt-Caputo-et-al.-2026-Legal-Alignment-for-Safe-and-Ethical-AI.pdf](https://aigi.ox.ac.uk/wp-content/uploads/2026/01/Kolt-Caputo-et-al.-2026-Legal-Alignment-for-Safe-and-Ethical-AI.pdf)
- [https://securiti.ai/whitepapers/eu-ai-act-what-changes-now-what-waits-2026/](https://securiti.ai/whitepapers/eu-ai-act-what-changes-now-what-waits-2026/)
- [https://www.holisticai.com/blog/ai-regulation-in-2026-navigating-an-uncertain-landscape](https://www.holisticai.com/blog/ai-regulation-in-2026-navigating-an-uncertain-landscape)
- [https://www.preprints.org/manuscript/202603.1876](https://www.preprints.org/manuscript/202603.1876)
- [https://arxiv.org/list/cs/new](https://arxiv.org/list/cs/new)
- [https://arxiv.org/html/2511.17256v1](https://arxiv.org/html/2511.17256v1)
- [https://arxiv.org/abs/2511.17256](https://arxiv.org/abs/2511.17256)
- [https://internationalaisafetyreport.org/sites/default/files/2026-02/international-ai-safety-report-2026.pdf](https://internationalaisafetyreport.org/sites/default/files/2026-02/international-ai-safety-report-2026.pdf)
- [https://list.elra.info/mailman3/hyperkitty/list/corpora@list.elra.info/latest?count=200&page=3](https://list.elra.info/mailman3/hyperkitty/list/corpora@list.elra.info/latest?count=200&page=3)
- [https://www.unesco.org/sites/default/files/medias/fichiers/2025/09/CULTAI_Report%20of%20the%20Independent%20Expert%20Group%20on%20Artificial%20Intelligence%20and%20Culture%20%28final%20online%20version%29%201.pdf](https://www.unesco.org/sites/default/files/medias/fichiers/2025/09/CULTAI_Report%20of%20the%20Independent%20Expert%20Group%20on%20Artificial%20Intelligence%20and%20Culture%20%28final%20online%20version%29%201.pdf)
- [https://paulfloreswriter.wordpress.com/](https://paulfloreswriter.wordpress.com/)
- [https://www.linkedin.com/pulse/owasp-top-10-llms-meets-eu-ai-act-practical-bridges-mehler--5mq4f](https://www.linkedin.com/pulse/owasp-top-10-llms-meets-eu-ai-act-practical-bridges-mehler--5mq4f)
- [https://artificialintelligenceact.eu/high-level-summary/](https://artificialintelligenceact.eu/high-level-summary/)
- [https://www.ismsforum.es/ficheros/descargas/en---gobierno-de-la-ia1765878738.pdf](https://www.ismsforum.es/ficheros/descargas/en---gobierno-de-la-ia1765878738.pdf)
- [https://cleanaim.com/ai-governance/eu-ai-act/](https://cleanaim.com/ai-governance/eu-ai-act/)
- [https://genai.owasp.org/llm-top-10/](https://genai.owasp.org/llm-top-10/)
- [https://digitallibrary.usc.edu/API/Download/v1_0/GetOriginalLimited?Identifier=UC11399NC9H&SourceAction=API_VIEW_DETAILS_TRX&UsePreviewPdf=False](https://digitallibrary.usc.edu/API/Download/v1_0/GetOriginalLimited?Identifier=UC11399NC9H&SourceAction=API_VIEW_DETAILS_TRX&UsePreviewPdf=False)
- [https://openreview.net/pdf/766b35c7ee131a7bea87868302c4461fc950181a.pdf](https://openreview.net/pdf/766b35c7ee131a7bea87868302c4461fc950181a.pdf)
- [https://techpolicylab.uw.edu/wp-content/uploads/2026/02/s43681-024-00451-4.pdf](https://techpolicylab.uw.edu/wp-content/uploads/2026/02/s43681-024-00451-4.pdf)
- [https://artificialintelligenceact.eu/](https://artificialintelligenceact.eu/)
- [https://law-ai.org/treaty-following-ai/](https://law-ai.org/treaty-following-ai/)
- [https://www.adgully.com/exclusives/exclusive](https://www.adgully.com/exclusives/exclusive)
- [https://arxiv.org/list/cs.AI/new](https://arxiv.org/list/cs.AI/new)
- [https://www.researchgate.net/publication/373810991_Assessing_Cross-Cultural_Alignment_between_ChatGPT_and_Human_Societies_An_Empirical_Study](https://www.researchgate.net/publication/373810991_Assessing_Cross-Cultural_Alignment_between_ChatGPT_and_Human_Societies_An_Empirical_Study)
- [https://dailypioneer.com/uploads/2026/epaper/march/delhi-english-edition-2026-03-31.pdf](https://dailypioneer.com/uploads/2026/epaper/march/delhi-english-edition-2026-03-31.pdf)
- [https://venturebeat.com/ai/large-language-models-exhibit-significant-western-cultural-bias-study-finds](https://venturebeat.com/ai/large-language-models-exhibit-significant-western-cultural-bias-study-finds)
- [https://aclanthology.org/2026.findings-eacl.347.pdf](https://aclanthology.org/2026.findings-eacl.347.pdf)
