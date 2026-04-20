---
layout: post
title: "Tracking Governance Documents at OpenAI and Anthropic: 2023-2026"
description: A chronological record of RSP, Model Spec, and Preparedness Framework revisions, tracing the trajectory of governance degradation from primary sources until the removal of halt provisions.
permalink: /en/archives/2026/04/10/governance-documents-tracking/
lang: en
alt_lang_url: /ja/archives/2026/04/10/governance-documents-tracking/
date: 2026-04-10T09:00:00Z
last_modified_at: 2026-04-10T09:00:00Z
author: founder
categories: [strategic-forecasting]
tags: [AI, governance, OpenAI, Anthropic, RSP, Model Spec, Preparedness Framework, AI safety]
---

This article is a companion to "[The AI Revolution Is Already Uncontrollable]({{ site.baseurl }}/en/archives/2026/04/09/ai-revolution-uncontrollable/)," tracking the primary sources of governance documents in chronological order.

## Period 1: "The Dawn of LLMs" September 19, 2023 -- May 7, 2024

The era when LLMs were still chat interfaces with no autonomous execution capabilities. *

- Anthropic RSP v1.0 (September 19, 2023)
- OpenAI Preparedness Framework Beta (December 18, 2023)

Anthropic established AI Safety Levels (ASL) in its Responsible Scaling Policy v1.0, calibrated to model capability. Models demonstrating capabilities above a given threshold were subject to a scaling pause or deployment delay until adequate safety measures were in place.

OpenAI's Preparedness Framework Beta defined a four-tier risk scale (Low / Medium / High / Critical) across five tracked categories: CBRN (Chemical, Biological, Radiological, Nuclear), Cybersecurity, Persuasion, Model Autonomy, and Unknown Unknowns. Models reaching High could not be deployed; models reaching Critical could not be developed further.

Both companies shared a common stance: models with dangerous capabilities would not be released. The documents from this period defined halt decisions at the model level and treated threshold attainment as an automatic trigger for halting.

## Period 2: "Establishing the Assistant's Operational Policy" May 8, 2024 -- March 31, 2025

The assistant's role and risk assessment criteria are formalized for operational use.

- OpenAI Model Spec, first edition (May 8, 2024)
- Anthropic RSP v2.0 (October 15, 2024)
- Anthropic RSP v2.1 (March 31, 2025)

The first edition of the Model Spec described the assistant's role as analogous to "a talented, high-integrity employee," operating within an explicit Chain of Command (Platform > Developer > User > Tool) as a rule for ensuring safety and legality. Additionally, the assistant's baseline behavior was described as "following explicit instructions and reasonably addressing implied intent without overstepping."

RSP v2.0 redefined ASLs from a per-model risk classification mechanism to safety standards to be met at the time of development and deployment.

The policy made explicit the commitment "not to train or deploy models capable of causing catastrophic harm unless we have implemented safety and security measures that will keep risks below acceptable levels," and defined specific capability thresholds for CBRN and AI R&D.

RSP v2.1 further subdivided the v2.0 CBRN threshold and AI R&D threshold (CBRN-3 / CBRN-4, AI R&D-4 / AI R&D-5), previewing the thresholds that would require ASL-4.

## Period 3: "The Emergence of Agents and the Degradation of Risk Assessment" April 15, 2025 -- May 13, 2025

AI systems are recognized as becoming "increasingly agentic," yet risk tracking of autonomous behavior is relaxed and the risk assessment system degrades.

- OpenAI Preparedness Framework v2 (April 15, 2025)

Preparedness Framework v2 acknowledged that AI systems are "increasingly agentic" and will "soon have the capability to create meaningful risk of severe harm."

Simultaneously, the Model Autonomy category from the original Preparedness Framework Beta was split into three. AI Self-improvement was promoted to a Tracked Category, while Long-range Autonomy and Autonomous Replication and Adaptation were demoted to Research Categories. Risks associated with AI autonomy were acknowledged, yet risk tracking of autonomous behavior itself was relaxed.

Furthermore, the principle that "reducing risk generally does not require reducing capability" was codified. This effectively asserts that risks inherent in AI can be resolved through operational measures -- a declaration notably different in character from the pre-emptive exclusion and halting of risks that cannot be mitigated operationally, a principle that had persisted since Period 1.

Read mechanically, this creates a logical structure in which the capability of the LLM itself can be excluded from the risk evaluation function, securing room to frame any disaster, damage, or social change caused by LLMs as an operational problem rather than a problem with the LLM.

In addition, it was explicitly stated that "the SAG does not have the ability to 'filibuster.'" The CEO can appoint SAG (Safety Advisory Group) members and its chair, and can also bypass the group altogether. While the Board's Safety and Security Committee (SSC) is stipulated to be able to overrule the CEO's decisions, if the CEO were to defy the Board, that would constitute a rebellion against its largest sponsors -- the investors -- before it would be a question of ethics or safety, making this a near-minimal provision. This suggests the possibility that internal pathways for intervening in AI development on ethical or safety grounds have been foreclosed.

## Period 4: "Uncontrollable" May 14, 2025 -- Present

Agent technology is legitimized while neither the concentration of responsibility on upstream humans nor legislation to prevent diffusion of accountability is discussed; the halt provisions themselves are removed from the documents.

- OpenAI Model Spec revisions (September 12 / October 27 / December 18, 2025)
- Anthropic RSP v2.2 (May 14, 2025)
- Anthropic ASL-3 First Activation Report (May 22, 2025)
- Anthropic RSP v3.0 (February 24, 2026)
- Anthropic RSP v3.1 (April 2, 2026)

RSP v2.2 revised the scope of protection under the ASL-3 Security Standard, excluding sophisticated insiders and state-compromised insiders from the protected threat model.

That same month, ASL-3 Deployment / Security Standards were activated for the first time in connection with the launch of Claude Opus 4. This was the first instance in which the ASL framework was applied to the deployment of a model.

The September 12 revision of the OpenAI Model Spec added language about agents. The word "agent" appeared in the context of systems "sometimes used for more autonomous deployments." The "No other objectives" section continued to state that the assistant "may only pursue goals entailed by applicable instructions" and "must not adopt, optimize for, or directly pursue any additional goals," while the "Scope of Autonomy" section justified agent use by asserting that in multi-step goal pursuit, the assistant may need to fill in missing details and "must sometimes act autonomously" -- a logical structure in which prohibition and justification coexist. While permitting agents, the responsibility boundaries established by the Chain of Command became ambiguous, and no provision was made for the readily foreseeable problems of upstream humans failing to take responsibility for implementation, shifting responsibility onto AI, or avoiding responsibility altogether.

The October 27 revision codified implicit delegation of authority through tool outputs such as AGENTS.md files. The assistant's scope of autonomous action was expanded to include "implicitly delegated authority" derived from tool outputs and surrounding documents, even without explicit instructions.

The December 18 revision added U18 Principles in response to the suicide lawsuit of 16-year-old Adam Raine (filed August 2025, with a total of eight ChatGPT-related lawsuits filed within the year).

RSP v3.0 downgraded the absolute halt provision to industry-wide recommendations, citing the collective action problem -- the concern that a developer who halts first will be overtaken by competitors with weaker safety measures.

RSP v3.1 added language stating that "the commitments below do not preclude us from taking cautionary action, such as refraining from training or deploying models, in other circumstances." Read mechanically, the framing as discretionary "freedom" is ambiguous: while it asserts Anthropic can halt development even when the RSP does not require it, the same framing permits refusal to halt as an exercise of that freedom without institutional contradiction, suggesting the possibility that internal pathways for intervening in AI development have been foreclosed.

## Primary Sources

Locations of primary sources cited in this article. All links point to local archives.

### Anthropic -- Responsible Scaling Policy

- RSP v1.0 (2023-09-19) -- [PDF](./docs/anthropic-rsp-v1.0-2023-09-19.pdf) p.2 "Framework" (ASL definition, halt provisions: scaling pause / deployment delay), p.3-4 "Initial Commitments" (ASL table, codification of training halt)
- RSP v2.0 (2024-10-15) -- [PDF](./docs/anthropic-rsp-v2.0-2024-10-15.pdf) Executive Summary (ASL redefinition, clarification of halt provisions), p.3 "Capability Thresholds and Required Safeguards" (CBRN and AI R&D capability thresholds)
- RSP v2.1 (2025-03-31) -- [PDF](./docs/anthropic-rsp-v2.1-2025-03-31.pdf) p.4 "Capability Thresholds" (ASL-4 threshold additions, CBRN and AI R&D subdivision)
- RSP v2.2 (2025-05-14) -- [PDF](./docs/anthropic-rsp-v2.2-2025-05-14.pdf) p.8-9 "ASL-3 Security Standard" (revision of protection scope)
- ASL-3 First Activation Report (2025-05-22) -- [HTML](./docs/anthropic-asl3-activation-2025-05-22.html) (first application of ASL-3 Deployment / Security Standards to Claude Opus 4; original: https://www.anthropic.com/news/activating-asl3-protections)
- RSP v3.0 (2026-02-24) -- [PDF](./docs/anthropic-rsp-v3.0-2026-02-24.pdf) p.3 "Introduction" (collective action problem, downgrade of absolute halt provision to industry-wide recommendations)
- RSP v3.1 (2026-04-02) -- [PDF](./docs/anthropic-rsp-v3.1-2026-04-02.pdf) p.15 "Appendix A" opening ("do not preclude us from taking cautionary action" language)

### OpenAI -- Preparedness Framework

- Preparedness Framework Beta (2023-12-18) -- [PDF](./docs/openai-preparedness-framework-beta-2023-12-18.pdf) p.5 "Tracked Risk Categories" (Low/Medium/High/Critical four-tier scale, five categories), p.8-10 (Cybersecurity / CBRN / Persuasion threshold definitions)
- Preparedness Framework v2 (2025-04-15) -- [PDF](./docs/openai-preparedness-framework-v2-2025-04-15.pdf) p.3 "increasingly agentic," "soon have the capability to create meaningful risk of severe harm"; p.6-7 "Research Categories" (Model Autonomy split, Long-range Autonomy and Autonomous Replication demotion); p.14 "reducing risk generally does not require reducing capability"; p.15 "Appendix B: Decision-making practices" (SAG filibuster clause, CEO appointment and bypass authority)

### OpenAI -- Model Spec

- First edition (2024-05-08) -- [HTML](./docs/openai-model-spec-2024-05-08.html) `#objectives` ("talented, high-integrity employee"), `#follow-the-chain-of-command` (Chain of Command: Platform > Developer > User > Tool), `#be-as-helpful-as-possible-without-overstepping` ("following explicit instructions and reasonably addressing implied intent without overstepping")
- Revision (2025-09-12) -- [HTML](./docs/openai-model-spec-2025-09-12.html) `#no_other_objectives` ("may only pursue goals entailed by applicable instructions"), `#scope_of_autonomy` (agent definition added, "must sometimes act autonomously")
- Revision (2025-10-27) -- [HTML](./docs/openai-model-spec-2025-10-27.html) `#ignore_untrusted_data` (implicit authority delegation via tool outputs such as AGENTS.md)
- Revision (2025-12-18) -- [HTML](./docs/openai-model-spec-2025-12-18.html) `#chatgpt_u18`, `#prioritize_teen_safety` (U18 Principles)

## Notes

\* From the explanatory text of Anthropic RSP v3.0 (February 24, 2026): "When we wrote the RSP in September 2023, large language models were essentially chat interfaces."
