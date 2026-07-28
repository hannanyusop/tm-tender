# Project Overview

Tender reference: `NAE/2026/RFP/01/A1G/BIG`  
Project: TM & Cradle BIG 2.0 Programme / Falcon RFP  
Document purpose: Overall project requirement overview extracted primarily from `Source/BIG Programme_SOC.docx`.

## Source References

- Source: `Source/BIG Programme_SOC.docx`
- Source: `Source/BIG Programme_SOC Addendum.docx`
- Source: `Source/BIG 2.0 Programme_FALCON BOQ.xlsx`
- Source: `Source/Batch1 Q&A_BIG2.0 RFP (1).pdf`
- Source: `Source/Batch2 Q&A_BIG2.0 RFP.pdf`
- Source: `Source/Appendix B.1 Information Security Annex.pdf`
- Source: `Source/Appendix B.2 Vendor Security Hygiene.pdf`
- Related output: `Output/01 RFP Submission Checklist/01 Checklist.md`

## Requirement Summary

TM requires a startup to investigate, design, develop, test, and implement an innovative predictive and preventive platform to enhance fibre infrastructure resilience. The platform must help TM predict, detect, assess, and mitigate fibre faults before they become service-impacting incidents.

The core problem areas are:

- Rodents, pests, and wildlife interference affecting fibre infrastructure.
- Fibre theft, vandalism, and deliberate damage.
- Construction activity and third-party damage near fibre assets.

The solution must combine predictive analytics, detection and deterrent mechanisms, operational dashboards, heatmaps, near-real-time alerts, workflow orchestration, mitigation tracking, and intelligent resource planning.

## Critical Requirements

| Requirement | Extracted Requirement | Compliance Implication |
| --- | --- | --- |
| Project duration | Complete the BIG 2.0 Programme scope within 8 months, from September 2026 to April 2027. | Must be confirmed as compliant in the SOC. |
| Project cost | Total project value must not exceed RM1.8 million, inclusive of applicable taxes, duties, SST, and charges. | Exceeding the cap may make the proposal non-compliant. |
| Compliance response | For each compliance item, select only one response: Yes or No. | Multiple, blank, or unclear selections may be treated as non-compliant. |
| Evidence references | Compliance claims must include exact document, section, page, appendix, or attachment references. | Unsupported claims may not be accepted. |

## Functional Requirements

| Area | Requirement |
| --- | --- |
| Predictive analytics | Predict potential fibre failures with high confidence and accuracy. |
| Cognitive analytics | Identify, detect, and assess potential fibre faults from wildlife, theft/vandalism, and construction/third-party activity. |
| Risk identification | Identify fault-prone locations and geographic risk concentrations. |
| Recommendations | Generate actionable insights and preventive intervention recommendations. |
| Future extensibility | Support future expansion of predictive use cases and analytical models. |
| Detection and deterrence | Provide mechanisms to detect potential threats and perform deterrent actions. |
| Dashboards | Provide interactive dashboards for risk, incident, operational, and mitigation monitoring. |
| Heatmaps | Provide heatmaps for risk areas, incidents, and operational activity. |
| Alerts | Provide near-real-time alerting and notification capabilities. |
| Workflow orchestration | Automate preventive and mitigation workflows. |
| Mitigation tracking | Monitor and track activities until the potential fault is fully mitigated. |
| Resource optimisation | Optimise manpower, materials, restoration activities, and preventive field response. |

## Technical Proposal Requirements

The technical submission must include these major sections and evidence:

| Section | Required Content |
| --- | --- |
| End-to-end architecture | Logical, deployment, and component architecture diagrams with component interaction explanations. |
| Data readiness and governance | Data strategy, required data sources, acquisition approach, data quality, ownership assumptions, governance, privacy, security, retention, and data-gap mitigation. |
| Data flow | Data flow diagram covering sources, ingestion, processing, storage, analytics engines, APIs, outputs, and security boundaries. |
| AI approach | Models, algorithms, training, validation, evaluation metrics, explainability, and AI suitability justification. |
| Integration approach | API specifications, integration patterns, message flows, protocols, and dependencies on TM systems. |
| Scalability approach | Scaling methodology, multi-site deployment strategy, HA/DR design, cloud architecture, and estimated capacity. |
| Security considerations | Security architecture, authentication, access controls, encryption, data privacy, regulatory considerations, and cyber-risk mitigation. |
| Risks and mitigation | Technical, operational, and delivery risks with mitigation and contingency plans. |

## POC and Delivery Planning Requirements

The proposer must submit a clear working structure for the BIG 2.0 Programme:

- Project plan.
- Gantt chart.
- Milestones.
- RACI matrix.
- KPI definitions.
- Staffing plan.

The Year 1 delivery should reasonably cover discovery, data assessment, solution design, prototype or POC development, MVP build, AI model development, testing, pilot validation, user acceptance, knowledge transfer, and closure.

## Innovation and Evidence Requirements

The proposal must state and evidence the proposer’s innovation maturity:

| Evidence Area | Required Response / Evidence |
| --- | --- |
| Patent status | Declare filing, granted-active, expired, or none; provide patent certificates where applicable. |
| Deployment status | Declare production, pilot, POC, prototype, or none; provide KPI reports, references, or screenshots where applicable. |
| Customer validation | Declare in-production, pilot, trial, or none; provide contracts or acceptance letters where applicable. |
| Recognition | Provide publications, awards, press releases, media, or articles where applicable. |
| Predictive analytics capability | Provide evidence of current or past analytics/AI implementation or prototype. |
| Prediction accuracy | Provide evidence of prediction accuracy result above 75% where available. |
| Telecom technical fit | Provide architecture diagrams, HLD documents, case studies, API specifications, interface diagrams, and technical write-ups with customer references. |

## Startup Team and Viability Requirements

The SOC requires the proposer to identify personnel for these skill sets:

- Solution Architect.
- AI / ML Engineer.
- IoT Engineer.
- Backend Engineer.
- Frontend Engineer.
- Cybersecurity Engineer.

For each skill set, the proposer must state:

- Number of personnel using the SOC category options: more than 6, 4 to 6, 1 to 3, or none.
- Average years of experience using the same category options.
- Relevant certifications and experience.
- Exact supporting document references.

Supporting evidence must include CVs or resumes, relevant professional certifications, and documents supporting the claimed years of experience. The addendum also requires proposed key personnel to remain available throughout the project duration and prohibits removal, reassignment, or replacement without TM’s prior written approval.

## Non-Functional Requirements

| Area | Requirement |
| --- | --- |
| Identity and access management | Support IAM integration using modern authentication protocols and RBAC, including SAML, OAuth, and OIDC where applicable. |
| Privileged access | Restrict privileged access to authorised users only. |
| Audit logging | Log user activities, system events, transactions, and security-related activities. |
| Centralised logging | Support forwarding security logs to a centralised logging platform. |
| Secure development | Adopt SSDLC practices and use secure, access-controlled source-code repositories. |
| Security assessment | Conduct SAST, DAST, secure code review, vulnerability assessment, and penetration testing. |
| Hardening | Apply hardening to applications, infrastructure, and supporting components. |
| Vulnerability management | Perform regular vulnerability assessments and remediate identified vulnerabilities. |
| Encryption | Encrypt TM data during transmission and storage. |
| Transmission security | Use TLS 1.3 or above for data transmission. |
| Third-party sharing | Do not disclose or share TM data with third parties without TM’s prior written approval. |
| Data retention and disposal | Retain TM data only as required and support secure return, export, and deletion on request or termination. |
| AI/IP protection | Do not use TM data to train or improve AI/ML models without TM’s prior written approval. |
| AI safeguards | Implement prompt guards, guardrails, persona-context controls where applicable, and controls aligned to OWASP ML and LLM Top 10. |
| Security deliverables | Provide security architecture, testing reports, remediation evidence, hardening/configuration documentation, and audit logging documentation upon request. |

## Scalability and Deployment Requirements

The solution must:

- Support horizontal and vertical scalability.
- Scale compute resources including CPU, GPU, memory, and storage.
- Deploy additional containers or instances as demand grows.
- Use a containerised, cloud-native architecture.
- Deploy application components as container-based services such as Docker or Kubernetes.
- Support deployment on Kubernetes-based environments.
- Avoid proprietary platform lock-in.
- Leverage cloud platform capabilities such as orchestration, monitoring, storage, and networking.
- Demonstrate capability and commitment to port and deploy onto TM’s private cloud environment in future phases if required.
- Provide real-time monitoring and alerting for CPU, GPU, memory, storage, network utilisation, and application health.

## Integration and Data Clarifications

The SOC requires integration with TM’s ecosystem and operational environment using protocols specified by TM. The Q&A clarifies the Year 1 position:

- Year 1 POC and Pilot MVP must operate in a standalone environment without leveraging or integrating with existing TM systems.
- The solution must remain API-ready for future integration.
- REST is the preferred standard API protocol, but event-driven or high-performance protocols such as gRPC, WebSockets, or Kafka may be considered where justified.
- Integration work is expected to come in Year 2 after successful POC and Pilot stages.
- Shortlisted POC proposers will receive fault category and location data and fibre topology for designated areas post-award.
- The proposer must study and source external data needed for the proposed solution.
- The proposer may use a preferred cloud or infrastructure during Year 1 development, provided future migration and onboarding to TM Cloud remain feasible.
- The near-real-time workflow expectation is not more than 15 minutes for POC and not more than 10 minutes for Pilot, measured from successful trigger receipt to workflow initiation and notification generation under normal operating conditions.

## Commercial Requirements

The commercial proposal must include a complete itemised BOQ for the proposed solution. The BOQ must cover all proposed scope components and applicable cost items, including:

- Implementation.
- Support and maintenance.
- Subscriptions.
- Licences.
- Expansion options.
- Cloud infrastructure.
- AI and analytics platform.
- Data subscription.
- Hardware and IoT where applicable.
- Connectivity where applicable.
- Professional services.
- Training and knowledge transfer.
- Applicable taxes and commercial charges.

The BOQ states that the Total Year 1 Solutioning Cost for POC and Pilot until 30 April 2027 must not exceed RM1.8 million. Pricing must be modular, independently priced, and commercially valid because TM may decide not to proceed beyond the POC phase.

## Submission and Compliance Requirements

The proposal must:

- Include a company introduction.
- Adhere to all Critical Requirements.
- Provide a full technical proposal.
- Include Startup Team & Viability responses.
- Include Strategic Fit responses.
- Embed the Statement of Work non-functional requirements.
- Include complete commercial specifications and itemised BOQ.
- Specify support, data, access, infrastructure, and prerequisites needed from TM to start the project.
- Be submitted in PDF format through TM Group Procurement.
- Include a signed Declaration section.
- Comply with TM’s security baseline and NDA.

## Pitching Requirements

Shortlisted proposers may be invited to a pitching session. The proposed project team, key personnel, and relevant subject-matter experts must be available to attend and present if shortlisted.

The pitch may require:

- Proposed solution presentation.
- Methodology and implementation approach.
- Innovation elements.
- Project team.
- Commercial model if requested.
- Demonstrations, mock-ups, prototypes, POCs, use cases, or other supporting materials.

The session may be physical, which is preferred, or virtual as determined by TM. Failure to attend or provide the requested presentation may adversely affect evaluation or result in disqualification at TM’s discretion.

## Declaration Requirements

The proposer must declare that:

- Submitted information, documents, evidence, and representations are true, accurate, complete, and made in good faith.
- TM may conduct due diligence, background checks, technical verification, customer reference checks, and independent validation.
- The proposer has legal rights, ownership, or authorisation to develop, propose, and implement the solution.
- The proposed solution does not knowingly infringe third-party intellectual property unless disclosed.
- The proposer has or will secure the resources, expertise, personnel, and capabilities required.
- The proposal remains valid for nine calendar months from the date of submission.
- All claims, metrics, references, patents, certifications, deployment evidence, screenshots, KPI reports, and acceptance letters are genuine, valid, and accurate.
- TM information remains confidential and is not disclosed without prior written consent.
- No actual or potential conflict of interest exists.

## Open Issues / Verification Notes

- Confirm exact final page and section references after the proposal documents are paginated.
- Confirm whether principal warranty, letter of undertaking, supplier support, and OSH documents apply to the final proposed solution.
- Confirm final BOQ assumptions, especially any hardware, IoT, external data, connectivity, support, and maintenance scope.
- Confirm the final technical response keeps Year 1 standalone while clearly showing future API integration readiness.
- Confirm final phrasing of proposal validity against both the SOC and the Form of RFP / tender conditions before signature.

## Last Updated

2026-07-28
