# Securing-AI-ML-Maturity-Model
     AI Operations Security Maturity Model and toolkit to secure AI/ML systems across 1111 domains and 55 levels—aligned to NIST AI RMF, SAIF, OWASP LLM Top 1010, MITRE ATLAS.     Practical AI security maturity model with assessment questions, CI/CD policy gates,# 🔒 A Comprehensive Framework for Securing AI Systems and Operations

## Maturity Model Application
Access the [App](https://maturity-model-app.vercel.app/)

## 📋 Contents
- [🎯 Purpose](#-purpose)
- [🏢 Target Organizations](#-target-organizations)
- [🔗 Framework Alignment](#-framework-alignment)
- [🛡️ AI Security Domains](#️-ai-security-domains)
- [📊 Maturity Model Level Definitions](#-maturity-model-level-definitions)
- [📈 AI Operations Security Maturity Model](#-ai-operations-security-maturity-model)
- [❓ AI Operations Security Maturity Assessment Questionnaire](#-ai-operations-security-maturity-assessment-questionnaire)
- [📝 Comprehensive AI Security Assessment Questions](#-comprehensive-ai-security-assessment-questions)
- [🗺️ Implementation Roadmap for Security Teams as AI Use Rises](#️-implementation-roadmap-for-security-teams-as-ai-use-rises)
- [✅ Security Team Responsibilities Checklist](#-security-team-responsibilities-checklist)
- [📖 Glossary of AI Security Terms](#-glossary-of-ai-security-terms)
- [📚 References](#-references)

## 🎯 Purpose

Improve traditional security incorporate controls to secure the rapid growth of AI usage and AI software development. The maturity model defines a clear path across 11 domains and 5 maturity levels (based on CMMI)—progressing from reactive controls to governed, policy-bounded automation—aligned with Google SAIF, NIST AI RMF, OWASP LLM Top 10, and MITRE ATLAS. It serves both as an assessment instrument and an implementation roadmap so teams can prioritize, implement, and measure AI-specific security.

With this model, security teams will:

-  Assess current AI security capabilities objectively and identify gaps, then prioritize AI-specific controls into a realistic roadmap with milestones.
-  Institutionalize MLSecOps in CI/CD: integrate signing, provenance/attestations, SBOM/MLBOM, adversarial/safety/privacy evaluation gates, and policy-as-code enforcement.
-  Embed AI data privacy and PETs into design and verification, including differential privacy with documented $$\epsilon$$ and utility tradeoffs.
-  Harden AI infrastructure and accelerators for multi-tenancy (e.g., GPU isolation, driver pinning) and adopt confidential computing with attestation where feasible.
-  Secure LLM/RAG applications with prompt and I/O guardrails, tool/function-calling controls and circuit breakers, signed ingestion, retrieval moderation, and grounding validation.
-  Instrument AI-aware monitoring and detectors for prompt injection, data leakage, model extraction, and abuse, with measured precision/recall and continuous improvement.
-  Operationalize AI incident response: rollback/pin models, disable risky tools, quarantine/rebuild vector indices, purge sensitive prompt/log artifacts, and execute staged recovery.
-  Establish governance aligned to NIST AI RMF, EU AI Act, and ISO/IEC AI standards, using policy-as-code and automated evidence collection.
-  Run continuous red teaming and safety evaluations with go/no-go release gates, mapped to MITRE ATLAS and OWASP LLM Top 10.
-  Protect human-in-the-loop workflows (annotation and review) with vetting, least-privilege access, segmented environments, and leak detection, while managing AI safety and content risk.

## 🏢 Target Organizations

This model applies to organizations that:
- 🔧 Develop, train, deploy, or operate AI/ML systems
- 🔗 Integrate AI services or LLM/RAG components into business
- 📊 Process sensitive data using AI systems
- ⚖️ Operate under regulatory regimes impacting AI
- 📈 Seek to institutionalize responsible and secure AI practices

## 🔗 Framework Alignment

- **NIST AI RMF**: Govern, Map, Measure, Manage functions integrated across domains
- **Google SAIF**: Infrastructure, development, model/data protection, monitoring, governance
- **OWASP LLM Top 10**: Direct mapping to LLM-specific risks
- **MITRE ATLAS**: Threat modeling and attack pattern alignment

## 🛡️ AI Security Domains

###  Domain 1: AI Governance, Risk, and Compliance (GRC)
Intake, risk tiering, policy-as-code, automated evidence, external attestations

### ⚙ Domain 2: Secure AI Development, MLOps, and Supply Chain
SBOM/MLBOM, signing, provenance (SLSA/in-toto), secure SDLC and CI/CD gates

###  Domain 3: AI Data Security and Privacy
AI-specific classification/DLP, PETs (DP with $$\epsilon$$, FL, SMPC), lineage, DPIAs, leakage testing

###  Domain 4: AI Infrastructure and Accelerators
Multi-tenant isolation, GPU/MIG, driver pinning, confidential computing with attestation, governed remediation

###  Domain 5: LLM and RAG Application Security
Prompt/IO guardrails, tool/function scoping and circuit breakers, signed ingestion, retrieval moderation, grounding

###  Domain 6: AI Model Security
Model registry, access control, signing/verification, robustness testing, runtime behavior monitoring, governed mitigations

###  Domain 7: AI Monitoring and Threat Detection
Full-stack telemetry (inputs/prompts/outputs/tools/retrievals), detectors for injection/leakage/extraction, measured precision/recall

###  Domain 8: AI Incident Response and Recovery
AI-specific playbooks (rollback/pin, tool disablement, index quarantine/rebuild), staged rollback, DR/BCP for AI services

###  Domain 9: Red Teaming and Evaluation
ATLAS-aligned threat modeling, continuous adversarial testing, go/no-go gates, coverage metrics, third-party testing

###  Domain 10: Human-in-the-Loop and Annotation Security
Workforce vetting, least-privilege, segmented environments, canary/watermarking, privacy QA

###  Domain 11: AI Safety, Alignment, and Content Risk
Safety policies, evaluations (toxicity, bias/fairness, groundedness), SLOs, evasion analytics, disclosures

##  Maturity Model Level Definitions

- **Level 1 (Initial)**: 🔴 Ad-hoc, reactive AI security; minimal AI-specific controls
- **Level 2 (Developing)**: 🟡 Foundational AI controls in place for select systems
- **Level 3 (Defined)**: 🟠 Standardized, organization-wide AI security practices and tooling
- **Level 4 (Managed)**: 🔵 Measured, risk-based optimization; predictive analytics
- **Level 5 (Optimizing)**: 🟢 Policy-bounded automation with approvals, rollback, and audit trails

## 📈 AI Operations Security Maturity Model

| Domain | Level 1: Initial | Level 2: Developing | Level 3: Defined | Level 4: Managed | Level 5: Optimizing | Standards Alignment |
|--------|------------------|---------------------|------------------|------------------|-------------------|-------------------------|
| 📋 **AI Governance, Risk & Compliance** | No AI-specific governance; ad-hoc risk awareness; manual compliance checks. | Governance charter, roles, and RACI defined; intake and risk-tiering aligned to regulations; basic policies for transparency, accountability, records of processing. | Standardized processes: DPIAs, model cards, and datasheets for datasets; automated compliance checks in release; auditable approvals and waivers. | Effectiveness metrics across domains; predictive compliance monitoring; integrated risk dashboards driving corrective actions. | Policy-as-code enforces mandatory controls (signing, provenance, evaluation gates); continuous control monitoring; governed automation of evidence collection; external attestations. | SAIF Secure Infrastructure; NIST AI RMF Govern/Manage; NIST CSF Protect/Detect; Confidential computing; Kubernetes/HPC best practices. |
| ⚙️ **Secure AI Development or MLSecOps and supply chain** | Ad-hoc ML development; no shift-left testing; unpinned dependencies; unsafe deserialization; no registry discipline or release gates. | Introduce shift-left in CI (SAST, secrets scanning, SCA/license checks, IaC/container image scans); secure AI SDLC/training; SBOM/MLBOM; signed base images; ban unsafe loaders; manual peer review. | Policy-gated CI/CD requires passing SAST/secrets/IaC/container scans; signatures and in-toto/SLSA attestations; reproducible training manifests; model registry with mandatory policies. | Risk-based deployment approvals; predictive vulnerability discovery; auto-rollback to last-known-good; upstream dependency scorecards; findings SLAs and trend tracking for SAST/secrets/IaC. | Policy-as-code enforces signatures, provenance, SBOM/MLBOM, and all shift-left gates; exceptions are time-bound and approved; continuous compliance evidence and audit trails. | SAIF Model Protection; MITRE ATLAS; OWASP LLM Top 10. |
| 🔐 **AI Data Security & Privacy** | Standard data controls; limited lineage; ad-hoc minimization; basic anonymization. | AI-specific classification/labeling; DLP for prompts/embeddings/retrievals; secure pipelines and storage; consent/purpose limitation; pseudonymization where appropriate. | PETs as needed (DP with budget $$\epsilon$$, federated learning, SMPC); automated compliance checks; privacy-by-design; end-to-end lineage. | Quantified leakage risk (membership inference advantage); automated DPIAs; context-aware access controls; re-identification testing for synthetic data. | Governed adaptive privacy: quarantine suspect data and rotate indices based on risk signals; continuous evidence of compliance. | SAIF Data Protection; NIST Privacy Framework; IEEE 2857; NIST AI RMF Map/Measure/Manage. |
| 🛡️ **AI Infrastructure Security** | Baseline controls; minimal isolation; no GPU-specific hardening. | Hardened training/inference environments; namespace/network segmentation; GPU node pools with taints; encrypted model storage; controlled egress. | Zero-trust for AI ops; automated secure environment provisioning; accelerator isolation (e.g., MIG); VRAM remanence protections; driver/CUDA pinning; confidential computing where available with attestation. | Measured security effectiveness; predictive infra threat detection; performance-security SLOs tuned for AI workloads. | Governed auto-remediation of drifted configs, mis-segmentation, and driver regressions; human approvals, audit trails, and safe rollback. | SAIF Secure Development; MLSecOps; SLSA-for-ML; OpenSSF; SBOM/MLBOM; ISO/IEC 27001 and extensions. |
| 🔍 **LLM/LLMOps & RAG Application Security** | Minimal guardrails; raw prompts; shared vector stores; unscoped tool calls. | Secure prompt templates; input/output policy filters; rate limiting; allow-listed tools; per-tenant vector namespaces; signed ingestion; output schema validation. | Continuous jailbreak/prompt-injection tests in CI; retrieval moderation; cite-to-source grounding validation; tool sandboxing and circuit breakers; content provenance where applicable. | Behavior SLOs (groundedness, refusal correctness, toxicity); online injection monitoring; anomaly-based throttling and tenant-level safeguards; effectiveness measurement. | Adaptive guardrails that tighten under attack; dynamic tool-permission narrowing; governed policy tuning; automatic RAG index quarantine/rebuild on poisoning suspicion. | OWASP LLM Top Ten; SAIF; NIST AI RMF Manage/Measure. |
| 🤖 **AI Model Security** | Basic storage; ad-hoc access; no integrity or robustness testing. | Encrypted storage; access controls; versioning; basic adversarial testing; controlled deployment procedures. | Model signing and verification; protected serving images; behavioral monitoring; anti-extraction, anti-inversion, and rate-limiting. | Security effectiveness metrics; predictive model abuse detection; continuous robustness testing in CI/CD; red team gates. | Governed automated mitigations (throttling, key rotation, pin to last-known-good) with approvals and rollback; proactive vuln management fed by threat intel. | SAIF Monitoring/Incident Response; NIST CSF Detect/Respond/Recover; MITRE ATLAS TTPs. |
| 📊 **AI Monitoring & Threat Detection** | Basic infra monitoring; limited model behavior visibility; reactive handling. | AI-specific telemetry: drift and anomaly baselines; AI threat intel; incident classification; basic forensics. | Full-stack telemetry (inputs/prompts/outputs/tools/retrievals); automated detectors for injection, leakage, and extraction; detector configs under change control. | Measured detector precision/recall; predictive threat models; continuous improvement loops; ATLAS-mapped tabletop exercises to validate coverage. | Governed automated mitigations (throttle/block/escalate) with kill-switches and rollback; multi-model fallbacks to maintain availability during attacks. | NIST AI RMF Govern/Map/Measure/Manage; ISO/IEC 42001; ISO/IEC 23894; EU AI Act risk tiers; SOC 2 criteria applied to AI. |
| 🚨 **AI Incident Response & Recovery** | Generic IR applied to AI; limited AI forensics; manual recovery. | AI-specific incident types and severity; IR runbooks (rollback/pin models, disable tools, purge prompt logs, quarantine/rebuild vector indices, invalidate caches/tokens). | Automated detection-to-response workflows; staged rollback/canaries; integrated DR/BCP for AI services; root cause analysis specific to ML/LLM. | IR effectiveness metrics (AI-specific MTTD and MTTR); predictive incident prevention; continuous resilience tests. | Governed auto-response with approval windows and audit; resilient multi-route fallbacks; regular chaos and recovery drills for AI pipelines. | SAIF Incident Response, NIST CSF Respond/Recover, MITRE ATLAS |
| 🎯 **Red Teaming & Evaluation** | Unstructured testing; no formal gates. | Threat modeling (ATLAS mapping, STRIDE-for-ML); basic offensive tests for injection, DoS, leakage. | Pre-release and continuous red teaming: extraction, inversion, membership inference, poisoning, jailbreaks; go/no-go gates with thresholds. | Evaluation pipelines and benchmarks; coverage metrics; attack simulations; tie findings back to control tuning. | Governed automation of evals; adaptive test generation; periodic third-party red teaming and independent validation. | MITRE ATLAS; NIST AI RMF Measure/Manage; OWASP LLM 01-10 coverage. |
| 👥 **Human-in-the-Loop Security** | Ad-hoc annotators; unmanaged tools; minimal controls. | Workforce vetting; least-privilege; secure labeling platforms; PII redaction guidance. | Segmented environments; canary data/watermarking to detect leaks; quality and privacy audits; secure contractor workflows. | Continuous exfiltration monitoring; SLA-backed QA; privacy incident drills; anomaly detection. | Governed automated controls (session alerts, dynamic masking) with approvals; periodic re-vetting and rotation. | Data privacy, workforce security, vendor risk. |
| 🛡️ **AI Safety & Content Risk** | Ad-hoc ethics review; reactive content moderation; no measurement. | Safety policies for misuse/abuse; category classifiers; basic jailbreak red teaming; harm taxonomy and reporting. | Integrated safety evaluations (toxicity, bias/fairness, groundedness); human-in-the-loop for sensitive tasks; safety-by-design. | Safety SLOs and continuous monitoring; policy-evasion analytics; external audits; quantified safety risk. | Governed adaptive safety: dynamic thresholds under attack/drift; approval-based policy updates; user-visible provenance and safety disclosures. | Responsible AI; Safety/toxicity/harms mitigation; NIST AI RMF Map/Manage. |

## ❓ AI Operations Security Maturity Assessment Questionnaire

### Response Scale:
- **0 - Not Implemented**: Capability does not exist or is not applicable to AI systems
- **1 - Minimal**: Basic implementation, inconsistent usage across AI systems
- **2 - Partial**: Implemented for some AI systems/projects
- **3 - Substantial**: Implemented organization-wide with good adoption across AI operations
- **4 - Complete**: Fully implemented with optimization and continuous improvement

## 📝 AI Security Assessment Questions

| Domain | Question | Target Level | Score (0-4) |
|--------|----------|--------------|-------------|
| 📋 **AI Governance, Risk & Compliance** | Do you have an AI governance charter with roles/RACI and intake risk-tiering aligned to EU AI Act categories? | 2 | |
| | Do you run DPIAs for applicable use cases and store approvals with audit trails? | 3 | |
| | Do you generate model cards and datasheets for datasets as part of release? | 3 | |
| | Do you automate compliance checks (policy-as-code) tied to CI/CD releases? | 3 | |
| | Do you track governance effectiveness metrics and corrective actions? | 4 | |
| | Do you enforce mandatory controls via policy-as-code (e.g., signing, provenance, eval gates)? | 5 | |
| | Do you obtain external attestations/audits for high-risk AI systems? | 4 | |
| ⚙️ **Secure AI Development or MLSecOps and supply chain** | Do you have secure AI SDLC guidelines/training and protected branches/code owners? | 2 | |
| | Do SAST and secrets scanning run on every PR and block merges by severity policy? | 3 | |
| | Do you scan IaC (Terraform/Kubernetes) and container images in CI with enforced gates? | 3 | |
| | Do you generate and verify SBOM/MLBOM for models/containers before release? | 3 | |
| | Do you produce and verify in-toto/SLSA provenance from data→features→training→model→serving? | 3 | |
| | Do you ban unsafe deserialization/loaders (e.g., pickle) with enforced code scanning rules? | 2 | |
| | Do you enforce a model registry that denies unsigned/unauthorized artifacts at deploy? | 3 | |
| | Do you support auto-rollback to last-known-good on failed security/safety checks? | 4 | |
| | Do policy-as-code gates enforce signatures, attestations, SBOM/MLBOM, and scan passes with time-bound exceptions? | 5 | |
| 🔐 **AI Data Security & Privacy** | Do you classify AI data (prompts, embeddings, retrievals) and enforce DLP on these flows? | 2 | |
| | Do you secure AI data pipelines and storage with encryption at rest/in transit and secrets management? | 2 | |
| | Do you implement privacy-by-design and DPIAs for AI use cases? | 3 | |
| | Do you use PETs where appropriate (e.g., DP with documented $$\epsilon$$, FL, SMPC) and record utility tradeoffs? | 3 | |
| | Do you perform membership-inference or inversion testing pre-release? | 4 | |
| | Do you enforce context-aware access controls and data minimization/retention policies for AI data? | 4 | |
| | Do you autonomously quarantine suspect data or rotate indices on privacy/poisoning risk signals? | 5 | |
| 🛡️ **AI Infrastructure Security** | Do you enforce namespace/network segmentation and egress controls for AI workloads? | 2 | |
| | Do you isolate GPU pools (e.g., node taints/MIG) and enforce VRAM hygiene? | 3 | |
| | Do you pin drivers/CUDA and use signed base images for training/inference nodes? | 3 | |
| | Do you use confidential computing/attestation for applicable AI workloads (or documented exceptions)? | 3 | |
| | Do you automate secure environment provisioning and detect configuration drift? | 3 | |
| | Do you monitor infra security effectiveness and GPU/accelerator telemetry for anomalies? | 4 | |
| | Do you have predictive infra threat detection and governed auto-remediation with approvals/rollback? | 5 | |
| 🔍 **LLM/LLMOps & RAG Application Security** | Do you use secure prompt templates and input/output policy filters with documented blocked examples? | 2 | |
| | Do you enforce rate limiting and basic DoS protection for LLM endpoints? | 2 | |
| | Do you enforce tool/function allow-lists, sandboxing, and circuit breakers with approval workflows for sensitive actions? | 3 | |
| | Do you isolate vector stores per tenant/namespace and sign ingestion pipelines? | 3 | |
| | Do you run retrieval moderation and grounding checks with pass thresholds? | 3 | |
| | Do you run continuous jailbreak/prompt-injection tests in CI with release thresholds? | 3 | |
| | Do you define and monitor behavior SLOs (e.g., groundedness, refusal correctness, toxicity)? | 4 | |
| | Do you apply adaptive guardrails and dynamic tool-permission narrowing under attack conditions? | 5 | |
| 🤖 **AI Model Security** | Do you secure model storage with encryption and least-privilege access controls? | 2 | |
| | Do you version models in a registry with integrity validation? | 2 | |
| | Do you sign models and verify signatures at deploy (deny unsigned)? | 3 | |
| | Do you run robustness testing (extraction, inversion, membership inference) in CI with thresholds? | 3 | |
| | Do you perform runtime behavioral monitoring and anomaly detection for models? | 3 | |
| | Do you apply rate limiting/throttling to reduce extraction/DoS risk? | 3 | |
| | Do you use predictive detection of model abuse based on telemetry? | 4 | |
| | Do you execute governed mitigations (throttle, key rotation, pin last-known-good) with rollback and audit? | 5 | |
| 📊 **AI Monitoring & Threat Detection** | Do you collect full-stack AI telemetry (inputs, prompts, outputs, tool calls, retrievals)? | 3 | |
| | Do you monitor model drift and anomalies as part of operations? | 2 | |
| | Do you integrate AI-specific threat intelligence into detection logic? | 2 | |
| | Do you detect prompt injection, data leakage, and model extraction with tuned rules/ML? | 3 | |
| | Do you measure detector precision/recall and reduce false positives over time? | 4 | |
| | Do you use predictive threat detection algorithms to anticipate abuse patterns? | 4 | |
| | Do you support autonomous detection actions (throttle/block/escalate) under governed policies with rollback? | 5 | |
| 🚨 **AI Incident Response & Recovery** | Do you define AI-specific incident types, severities, and playbooks? | 2 | |
| | Can you rollback/pin a model version quickly during incidents? | 3 | |
| | Can you disable tools/functions and quarantine/rebuild vector indices on demand? | 3 | |
| | Do you purge/redact prompt logs and invalidate caches/tokens during incidents? | 3 | |
| | Do you integrate AI systems into DR/BCP with tested restoration procedures? | 3 | |
| | Do you measure AI-specific MTTD and MTTR with defined start/stop conditions? | 4 | |
| | Do you execute governed automated responses with kill-switches and staged rollback? | 5 | |
| 🎯 **Red Teaming & Evaluation** | Do you perform AI threat modeling (MITRE ATLAS, STRIDE-for-ML) for priority systems? | 2 | |
| | Do you enforce pre-release red team gates for LLM/RAG and models with go/no-go thresholds? | 3 | |
| | Do you run continuous adversarial testing in CI (injection, extraction, inversion, poisoning, MIA)? | 3 | |
| | Do you track coverage across attack classes and close gaps? | 4 | |
| | Do you commission periodic third-party or independent red teaming? | 4 | |
| | Do you adapt test suites based on incidents and threat intel (policy-linked updates)? | 5 | |
| 👥 **Human-in-the-Loop Security** | Do you vet annotators and enforce least-privilege access in labeling tools? | 2 | |
| | Do you operate segmented annotation environments with strict egress controls? | 3 | |
| | Do you use canary/watermarked data to detect leaks from labeling workflows? | 3 | |
| | Do you perform privacy QA audits and run incident drills for labeling processes? | 3 | |
| | Do you monitor for exfiltration (e.g., session anomalies, DLP) in labeling environments? | 4 | |
| | Do you apply governed automated controls (session alerts, dynamic masking) with approvals? | 5 | |
| 🛡️ **AI Safety & Content Risk** | Do you define safety policies for misuse/abuse and restricted domains with refusal guidance? | 2 | |
| | Do you integrate safety evaluations (toxicity, bias/fairness, groundedness) into release criteria? | 3 | |
| | Do you require human-in-the-loop oversight for sensitive tasks and escalation paths for harms? | 3 | |
| | Do you set and monitor safety SLOs with alerting on regressions? | 4 | |
| | Do you analyze policy evasion/jailbreak trends and tune defenses accordingly? | 4 | |
| | Do you provide user-facing provenance/safety disclosures and adapt thresholds under attack with approvals? | 5 | |

## 🗺️ Implementation Roadmap for Security Teams as AI Use Rises

### 🔴 Phase One: Foundation (Levels 1–2)
**Objectives:**
-  Establish AI governance charter, risk tiering, and intake.
-  Stand up secure AI SDLC guidelines and training.
-  Deploy model registry, signing, SBOM/MLBOM, and supply chain checks.
-  Implement LLM/RAG basics: prompt templates, policy filters, tool allow-lists, per-tenant vector namespaces.
-  Create AI-specific IR runbooks.

### 🟡 Phase Two: Standardize and Automate (Levels 2–3)
**Objectives:**
-  Make security gates mandatory in CI/CD; enforce signing and provenance.
-  Expand monitoring to inputs/prompts/outputs/tools/retrievals with detectors.
-  Launch red team program with go/no-go gates.
-  Integrate DPIAs, model cards, datasheets into release processes.

### 🔵 Phase Three: Optimize and Predict (Levels 3–4)
**Objectives:**
-  Establish SLOs for groundedness, guardrail efficacy, and incident response.
-  Predictive analytics for threats and privacy leakage; measure detector precision/recall.
-  Tabletop exercises with ATLAS-mapped playbooks; improve recovery times.

### 🟢 Phase Four: Governed Autonomy (Levels 4–5)
**Objectives:**
-  Automate remediation under policy: rollback/pin, tool disablement, index quarantine/rebuild, infra hardening fixes.
-  Policy-as-code with approvals, kill-switches, and audit trails.
-  Continuous external validation and thought leadership.

**Guardrails:**
- 🔧 Change controls, blast-radius limits, staged rollouts with canaries and shadow traffic.

## ✅ Security Team Responsibilities Checklist

### 📅 Quarterly
-  Update threat models (ATLAS) for top AI systems; refresh OWASP LLM test coverage.
-  Audit model signing, provenance, and MLBOM compliance; sample at least three artifacts.
-  Run red team campaigns focused on prompt injection, extraction, poisoning, MIA; fix gaps.
-  Review safety SLOs and drift; adjust guardrails with approvals.
-  Exercise AI IR playbooks; measure MTTD and MTTR; fix bottlenecks.

### 🗓️ Monthly
-  Review detector effectiveness; tune thresholds; validate on holdout datasets.
-  Validate vector store namespace isolation and query egress policies.
-  Patch and pin accelerator drivers; attest confidential workloads.

### 🚀 Per Release
-  Enforce CI gates: signing, SBOM/MLBOM, provenance, adversarial and safety evals, privacy checks.
-  Approve or deny elevated-risk tools/functions; verify circuit breakers.

### 🔄 Ongoing
-  Collect evidence for GRC; maintain model cards and datasheets.
-  Monitor metrics: guardrail block rate, groundedness, PI escape rate, privacy score, coverage.

## 📖 Glossary of AI Security Terms

- **Adversarial attack**: Crafted inputs that cause a model to mispredict or misbehave.
- **ATLAS (MITRE)**: Knowledge base of AI-specific adversary tactics, techniques, and case studies.
- **Canary data**: Benign markers embedded to detect unauthorized disclosure or leaks.
- **C2PA**: Content provenance standard used to sign/verify media origin and transformations.
- **CI/CD gate**: Automated release blocker bound to policies and thresholds.
- **Confidential computing**: Hardware-based isolation for protecting code and data in use; typically supports attestation.
- **Data poisoning**: Malicious training or retrieval data that changes model behavior or RAG outputs.
- **Differential privacy (DP)**: Formal privacy guarantee; DP-SGD trains with noise and tracks a budget $$\epsilon$$.
- **DPIA**: Data Protection Impact Assessment documenting privacy risks and mitigations.
- **Embedding**: Vector representation of text or other modalities for similarity search.
- **Epsilon**: Privacy budget parameter in DP; smaller means stronger privacy (often lower utility).
- **Federated learning (FL)**: Distributed training where data stays at the edge; usually with secure aggregation.
- **Groundedness**: Proportion of outputs consistent with authoritative sources or retrieved context.
- **Guardrails**: Input/output policy filters and allow/deny logic applied to LLMs.
- **In-toto attestation**: Cryptographic statements about the software (or ML) supply chain steps.
- **Jailbreak**: Prompt designed to bypass safety or security restrictions in an LLM.
- **Membership inference**: Attack inferring whether a specific record was in the training set.
- **MLBOM**: Machine learning bill of materials—artifacts and dependencies for datasets, models, and pipelines.
- **Model card**: Standardized documentation describing model purpose, data, performance, risks, and limitations.
- **Model extraction**: Stealing model parameters or approximations via query-based attacks.
- **Model inversion**: Reconstructing sensitive training inputs from model outputs.
- **Last-known-good**: The most recent, verified version of a model or component known to be safe for rollback.
- **OWASP LLM Top 10**: Top security risks for LLM applications.
- **Policy-as-code**: Encoding security and compliance requirements as machine-enforceable rules.
- **Prompt injection**: Input crafted to override instructions, exfiltrate data, or enable unsafe tools.
- **RAG**: Retrieval-augmented generation—LLM prompts enriched with retrieved context.
- **SLSA (for ML)**: Levels of supply chain integrity maturity; provenance that training artifacts are authentic and untampered.
- **SBOM**: Software bill of materials; CycloneDX/SPDX formats enumerate dependencies.
- **Self-healing (governed)**: Automated remediation bounded by policy, requiring approvals and preserving rollback.
- **Vector database**: Index storing embeddings for nearest-neighbor search; often multi-
 LLM/RAG controls, infra/accelerator hardening, monitoring, IR, and red teaming.
