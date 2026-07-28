# Proposer's Specifications And Supporting Literature

Tender reference: `NAE/2026/RFP/01/A1G/BIG`  
Submission volume: Volume III — Technical Proposal  
Checklist item: Proposer's Specifications and any other literature deemed necessary  
Draft status: Working draft for technical team review

## Source References

- `Source/01 PART III - Appendix A_Checklist of Tender Submission_amend.docx`
- `Source/BIG Programme_SOC.docx`
- `Source/BIG Programme_SOC Addendum.docx`
- `Source/Appendix B.1 Information Security Annex.pdf`
- `Source/Appendix B.2 Vendor Security Hygiene.pdf`
- `Source/Batch1 Q&A_BIG2.0 RFP (1).pdf`
- `Source/Batch2 Q&A_BIG2.0 RFP.pdf`
- `Source/PART I - Instructions to Proposers RFP Falcon (Ver1.0) (1).pdf`

## Usage Notes

- This document supports the Part V Statement of Compliance and should be submitted in Volume III with no pricing information.
- Final submission should be exported to the format required by TM and cross-referenced from `Source/BIG Programme_SOC.docx`.
- Replace all bracketed placeholders before submission.
- Do not include priced BOQ details, commercial totals, rate cards, discounts, or other price information in this technical package.

## 1. Purpose Of This Supporting Literature

This document provides supporting specifications and technical literature for the proposed predictive and preventive fibre resilience platform for the TM & Cradle BIG 2.0 Programme. It supplements the completed Part V Statement of Compliance by describing the proposed solution design, technical components, data and AI methodology, operational workflows, security approach, scalability considerations, implementation evidence, and supporting attachments.

The proposed solution is intended to help TM predict, detect, assess, and mitigate fibre disruption risks associated with:

- Rodents, pests, and wildlife.
- Theft and vandalism affecting fibre network infrastructure.
- Construction, excavation, and third-party activity near fibre routes.

## 2. Proposed Solution Summary

Proposer: `[Krenovator Technology Sdn Bhd / confirm legal proposer name]`  
Solution name: `[Insert solution/platform name]`  
Deployment model for Year 1: Standalone POC and Pilot platform, API-ready for future integration  
Target project window: September 2026 to April 2027  
Primary outcome: Improve fibre infrastructure resilience through predictive analytics, risk prioritisation, automated workflow initiation, and preventive mitigation tracking.

The proposed platform combines geospatial intelligence, predictive analytics, alerting, dashboard visualisation, workflow orchestration, and resource planning into a single operational environment. For Year 1, the platform is designed to operate independently from TM production systems while preparing standard API interfaces for future integration if the POC and Pilot progress to subsequent phases.

## 3. Functional Specifications

| Capability | Proposed Specification | Supporting Evidence To Attach |
| --- | --- | --- |
| Risk prediction | Predict high-risk fibre route segments using historical fault records, geospatial context, environmental indicators, activity patterns, and external risk signals. | Model methodology note, prototype report, validation metrics, sample risk output. |
| Risk heatmaps | Present map-based heatmaps showing route-level or area-level risk concentration by cause category and severity. | Dashboard screenshot, map layer sample, user guide extract. |
| Incident and risk dashboard | Provide operational views for risk trends, active alerts, mitigation status, route priority, and management reporting. | Dashboard screenshots, feature list, role-based view examples. |
| Near-real-time alerting | Initiate preventive workflow and notification after receipt of triggering events within the required POC/Pilot response thresholds. | Alert flow diagram, timing test result, notification screenshot. |
| Workflow orchestration | Convert detected or predicted risks into assigned preventive actions, escalation tasks, and closure tracking. | Workflow diagram, sample task lifecycle, audit trail screenshot. |
| Mitigation tracking | Track mitigation action owner, status, timestamps, evidence, resolution notes, and open ageing. | Sample work order screen, report template, closure evidence. |
| Resource planning | Recommend manpower, materials, equipment, and dispatch prioritisation based on risk severity, location, resource constraints, and operational impact. | Resource optimisation logic, sample planner view, assumptions list. |
| API readiness | Provide documented API specifications and integration patterns for future REST-based or event-driven integration. | API catalogue, OpenAPI draft, message flow diagram. |
| Reporting | Generate periodic management, technical, KPI, and pilot learning reports. | Report templates, KPI table, sample export. |

## 4. Technical Architecture

The proposed architecture consists of the following logical layers:

| Layer | Description | Key Components |
| --- | --- | --- |
| Data source layer | Receives TM-provided post-award data and proposer-sourced external data required for risk modelling. | Fault category/location data, fibre topology for designated areas, weather/geospatial/activity data, sensor or hardware feeds if proposed. |
| Ingestion layer | Loads batch, offline, API, or event-based datasets into the platform with validation and provenance controls. | File ingestion, API connectors, schema validation, ingestion logs, data quality checks. |
| Processing layer | Cleans, normalises, labels, enriches, and correlates data for analytics and visualisation. | ETL/ELT jobs, geospatial joins, feature engineering, quality scoring. |
| Analytics layer | Produces prediction, classification, anomaly detection, severity scoring, and recommendation outputs. | AI/ML models, rules engine, explainability module, validation metrics. |
| Application layer | Provides dashboards, heatmaps, alerting, workflow management, mitigation tracking, and reporting. | Web dashboard, notification service, task/workflow engine, report generator. |
| Security and governance layer | Protects data, access, logs, configuration, and application delivery. | IAM/RBAC, encryption, audit logs, secrets management, vulnerability management, incident response. |
| Integration layer | Exposes future integration points while maintaining standalone Year 1 operation. | REST APIs, event interfaces, OpenAPI documentation, adapter pattern. |

Required architecture attachments:

- [ ] Logical architecture diagram.
- [ ] Deployment architecture diagram.
- [ ] Component interaction diagram.
- [ ] Data flow diagram.
- [ ] Security boundary diagram.
- [ ] Future integration sequence diagram.

## 5. Data Strategy And Governance

The Year 1 proposal assumes TM will provide designated post-award data for the POC and Pilot, including fault category/location data and fibre topology for the relevant designated areas. The proposer will identify and source suitable external datasets needed to improve prediction quality, subject to legality, availability, cost inclusion, and data quality suitability.

| Data Category | Expected Source | Intended Use | Governance Considerations |
| --- | --- | --- | --- |
| Historical fibre fault category and location | TM post-award dataset | Train, validate, and test risk prediction models. | Confidential handling, access control, approved storage, data minimisation. |
| Fibre topology for designated areas | TM post-award dataset | Route segmentation, geospatial mapping, risk localisation. | Security controls, restricted access, topology sensitivity. |
| Weather and environmental data | Proposer-sourced external data | Correlate environmental factors with fault likelihood. | Licence compliance, refresh frequency, quality validation. |
| Construction or third-party activity indicators | Proposer-sourced or partner-sourced data | Identify third-party damage risk and preventive actions. | Source reliability, update cadence, lawful usage. |
| Sensor or hardware feeds, if proposed | Proposed field devices or partners | Detect physical events or environmental changes. | Device identity, secure transmission, maintenance responsibility. |
| Operational workflow data | Platform-generated | Track mitigation actions, closure, ageing, and performance. | Auditability, retention, access control. |

Data controls:

- [ ] Define data ownership and usage assumptions.
- [ ] Maintain source lineage and ingestion logs.
- [ ] Apply data quality checks before analytics use.
- [ ] Use least-privilege access for TM/customer data.
- [ ] Encrypt sensitive data in transit and at rest.
- [ ] Define retention and secure disposal rules.
- [ ] Document mitigation plans for unavailable, incomplete, or low-quality datasets.

## 6. AI And Analytics Methodology

The proposed AI approach should combine supervised learning, geospatial analytics, anomaly detection, and rules-based prioritisation where appropriate. Final model selection should be validated during ideation and MVP development after receiving TM's post-award data.

Candidate methods:

- Classification models for risk category and likelihood prediction.
- Geospatial clustering to identify recurring high-risk route areas.
- Time-series and trend analysis for fault recurrence and seasonality.
- Anomaly detection for unusual route, sensor, or activity patterns.
- Rules-based business logic for severity thresholds, escalation paths, and action recommendations.
- Explainability methods to show the key factors behind risk scores and recommendations.

Target evaluation metrics:

| Metric | Purpose | Draft Target / Note |
| --- | --- | --- |
| Accuracy | Overall prediction correctness. | Align with Part V evidence expectation; insert validated result. |
| Precision | Reduce false positives for operational alerts. | Insert result from prototype, simulation, POC, or pilot. |
| Recall | Capture likely fault/disruption risks before service impact. | Insert result from prototype, simulation, POC, or pilot. |
| F1-score | Balance precision and recall. | Insert result from prototype, simulation, POC, or pilot. |
| Prediction accuracy | Demonstrate analytics performance. | Part V references prediction accuracy result above 75%; insert evidence. |
| Workflow initiation time | Confirm near-real-time threshold. | POC: not more than 15 minutes; Pilot: not more than 10 minutes. |

Evidence to attach:

- [ ] AI methodology paper or technical note.
- [ ] Prototype or simulation test report.
- [ ] Model validation report with assumptions and dataset scope.
- [ ] Screenshots of prediction output, heatmap, alert, and workflow.
- [ ] Explainability sample showing why a route/location was scored as high-risk.

## 7. Integration Approach

For Year 1, the platform will operate as a standalone environment without dependency on existing TM production systems. The proposed design remains API-ready so TM may consider future integration after successful POC and Pilot stages.

Planned integration specifications:

| Interface | Year 1 Approach | Future Integration Readiness |
| --- | --- | --- |
| TM fault/category and topology data | Offline or approved post-award data transfer. | REST API or secure data pipeline adapter. |
| Dashboard access | Web-based controlled access for approved TM users. | SSO/IAM integration subject to TM approval. |
| Alert notification | Configurable notification channels for POC/Pilot. | Integration to NOC/OSS/workforce tools if requested in future phases. |
| Workflow data | Platform-managed workflow records. | Work order or ticketing API adapter. |
| Reporting exports | PDF/CSV/XLSX or approved export method. | BI/reporting API integration. |

API design principles:

- REST as the preferred standard API pattern.
- Event-driven options such as WebSockets, Kafka, or similar protocols where justified by scalability or real-time requirements.
- Versioned endpoints and backward-compatible changes.
- Secure authentication, authorisation, rate limiting, logging, and input validation.
- Clear API ownership, error handling, and audit traceability.

## 8. Security Specifications

The proposed platform will be designed to align with TM's Information Security Annex and Vendor Security Hygiene requirements. Security controls should be implemented across people, process, application, infrastructure, data, and third-party components.

| Security Area | Proposed Control |
| --- | --- |
| Security governance | Maintain documented security policies and nominated security contact points for the project. |
| Access control | Use unique user accounts, role-based access control, least privilege, strong authentication, and timely removal of users who no longer need access. |
| Data protection | Encrypt sensitive data in transit and at rest using industry-standard encryption and controlled key management. |
| Application security | Apply secure development practices, code review, dependency checks, application security testing, and remediation tracking. |
| Vulnerability management | Perform vulnerability scanning and remediate critical/high findings within required timelines or agreed remediation plans. |
| Logging and monitoring | Enable audit logs for system access, administrative activity, ingestion activity, model output, workflow actions, and security events. |
| Incident response | Maintain incident detection, escalation, notification, root-cause analysis, and remediation procedures. |
| Backup and recovery | Define backup frequency, recovery objectives, restoration testing, and secure retention where applicable. |
| Third-party controls | Ensure any subcontractor, hardware provider, cloud provider, data provider, or startup/SME partner follows equivalent confidentiality and security obligations. |

Required security attachments:

- [ ] Security architecture diagram.
- [ ] Access control matrix.
- [ ] Data protection and encryption statement.
- [ ] Secure development lifecycle summary.
- [ ] Vulnerability management approach.
- [ ] Incident response procedure summary.
- [ ] Backup, HA, DR, and recovery assumptions.
- [ ] Third-party security responsibility matrix, if applicable.

## 9. Scalability, Availability, And Portability

The platform should be designed to scale beyond the Year 1 POC and Pilot without requiring fundamental rework. The proposed architecture should support multi-site deployment, additional datasets, additional users, higher data volumes, and future integration to TM systems if requested.

Scalability specifications:

- Modular application components that can scale independently.
- Container-ready deployment approach where feasible.
- Separation between ingestion, analytics, application, and reporting workloads.
- Configurable site/route onboarding process.
- API-first design to avoid unnecessary proprietary lock-in.
- Monitoring and alerting for platform health and operational performance.

Availability and resilience specifications:

- Defined backup and restoration approach.
- Defined failure handling for ingestion, analytics, dashboard, and notification services.
- Documented HA/DR approach for Pilot and future scale-up.
- Operational runbook for support, escalation, and maintenance.

## 10. Hardware, Sensor, And Connectivity Literature

If hardware, sensors, IoT devices, DAS, camera, vibration, motion, environmental, connectivity, or field components are included in the proposal, attach product specifications and partner literature here.

| Component | Proposed Role | Required Literature |
| --- | --- | --- |
| `[Insert hardware/sensor item]` | `[Detection, deterrence, environmental sensing, gateway, edge processing, etc.]` | Datasheet, technical specification, operating conditions, warranty, country of origin, principal name/address. |
| `[Insert connectivity service]` | `[Cellular, LoRaWAN, NB-IoT, satellite, fixed broadband, etc.]` | Coverage assumptions, bandwidth, latency, installation requirement, support responsibility. |
| `[Insert cloud/hosting service]` | `[Application hosting, analytics, storage, backup, etc.]` | Service specification, region, security controls, resilience, support model. |
| `[Insert data source/subscription]` | `[Weather, geospatial, construction, activity, etc.]` | Licence, coverage, refresh interval, data fields, usage restrictions. |

Submission checks:

- [ ] Confirm whether any principal warranty is required.
- [ ] Confirm whether any letter of undertaking is required.
- [ ] Confirm whether each supplier/subcontractor role is declared.
- [ ] Confirm whether each party accessing confidential information is covered by appropriate NDA obligations.
- [ ] Confirm all relevant hardware, software, licences, subscriptions, and tools are included in the BOQ without prices for Volume III and priced only in the commercial/price submission where required.

## 11. Operational Workflow Specifications

The proposed operating workflow should convert data and model outputs into clear preventive action.

| Step | Description | Output |
| --- | --- | --- |
| 1. Ingest | Load TM-provided and external datasets through approved methods. | Validated data records and ingestion audit trail. |
| 2. Enrich | Clean, geocode, segment, label, and enrich data for analytics. | Analytics-ready dataset. |
| 3. Predict | Generate risk score, risk cause, severity, and confidence. | Risk-ranked fibre route/location list. |
| 4. Visualise | Display risks on dashboard and heatmap by geography, category, and severity. | Operational risk view. |
| 5. Alert | Trigger notifications based on threshold, confidence, and operational rules. | Alert record and notification evidence. |
| 6. Orchestrate | Create preventive workflow, assign owner, define action, and set SLA/target date. | Mitigation task/work order. |
| 7. Track | Monitor progress until closure, including evidence and remarks. | Closure record and KPI history. |
| 8. Learn | Feed closure outcomes and confirmed incidents back into the model improvement cycle. | Updated model features and performance report. |

## 12. Project Delivery Literature

Attach or cross-reference the following delivery documents:

- [ ] Project plan.
- [ ] Gantt chart covering September 2026 to April 2027.
- [ ] Milestone and deliverables table.
- [ ] RACI matrix.
- [ ] KPI definitions.
- [ ] POC plan.
- [ ] Pilot validation plan.
- [ ] Training and knowledge transfer plan.
- [ ] Support and maintenance approach.
- [ ] Risk register and mitigation plan.

## 13. Startup Team And Viability Evidence

The proposed personnel should remain available and committed throughout the project duration. Any replacement should be subject to TM's prior written approval and should have equivalent or better qualifications, experience, competencies, and certifications.

| Role / Skill Set | Proposed Personnel | Evidence To Attach |
| --- | --- | --- |
| Project Manager | `[Insert name]` | CV, relevant delivery record, certification if any. |
| Solution Architect | `[Insert name]` | CV, architecture experience, cloud/platform certifications. |
| AI / ML Engineer | `[Insert name]` | CV, model development evidence, AI/ML project references. |
| Data Engineer | `[Insert name]` | CV, ETL/data platform experience, data governance evidence. |
| Geospatial / GIS Specialist | `[Insert name]` | CV, GIS/geospatial analytics examples. |
| Software Engineer | `[Insert name]` | CV, application/API development evidence. |
| Cybersecurity Engineer | `[Insert name]` | CV, security certification, security implementation evidence. |
| Field / IoT Specialist, if applicable | `[Insert name or partner]` | CV, hardware deployment records, supplier support letter. |

Personnel evidence checks:

- [ ] Include CV/resume for each named person.
- [ ] Include certifications claimed in the Part V response.
- [ ] Include project references supporting years of experience.
- [ ] Confirm named personnel availability for the full project period.
- [ ] Align subcontractor/partner personnel with declaration and NDA requirements.

## 14. Innovation And Past Implementation Evidence

Attach evidence relevant to innovation merit, predictive analytics capability, and telecom technical fit.

| Evidence Type | Description | Attachment Reference |
| --- | --- | --- |
| Prototype demonstration | Workable prototype showing dashboard, heatmap, prediction, alerting, workflow, or analytics capability. | `[Insert filename]` |
| Simulated result | Simulation output demonstrating methodology and measurable result where production KPI is unavailable. | `[Insert filename]` |
| KPI report | Measured performance from prototype, POC, pilot, customer deployment, or internal test. | `[Insert filename]` |
| Customer reference | Reference letter or project profile for similar analytics, telecom, IoT, geospatial, or AI delivery. | `[Insert filename]` |
| Architecture / HLD | High-level design and architecture diagram showing telecom technical fit. | `[Insert filename]` |
| Screenshots | Product or prototype screenshots showing actual capability. | `[Insert filename]` |
| Patent / IP evidence, if any | Patent certificates, filings, proprietary modules, or IP declaration. | `[Insert filename]` |

## 15. Compliance Cross-Reference

| Part V Area | Supporting Literature Section | Evidence Status |
| --- | --- | --- |
| End-to-end architecture | Sections 4, 7, 9 | Draft; diagrams required. |
| Data readiness and governance | Section 5 | Draft; data assumptions to confirm. |
| Data flow | Sections 4 and 5 | Draft; data flow diagram required. |
| AI approach | Section 6 | Draft; model evidence required. |
| Integration approach | Section 7 | Draft; API catalogue required. |
| Scalability approach | Section 9 | Draft; deployment architecture required. |
| Security considerations | Section 8 | Draft; security attachments required. |
| Project plan, Gantt, milestone, RACI, KPI | Section 12 | Draft; delivery documents required. |
| Innovation merit | Section 14 | Draft; prototype/customer evidence required. |
| Predictive analytics capability | Section 6 and Section 14 | Draft; validation metrics required. |
| Technical fit and integration | Sections 4, 7, 9, 14 | Draft; HLD and screenshots required. |
| Startup team and viability | Section 13 | Draft; CVs/certifications required. |

## 16. Attachment Register

| Ref | Attachment | Purpose | Status |
| --- | --- | --- | --- |
| A1 | Logical Architecture Diagram | Shows solution components and interactions. | To attach |
| A2 | Deployment Architecture Diagram | Shows hosting, network, security, and runtime environment. | To attach |
| A3 | Data Flow Diagram | Shows sources, ingestion, processing, storage, analytics, API, and outputs. | To attach |
| A4 | Security Architecture Diagram | Shows trust boundaries and security controls. | To attach |
| A5 | API Catalogue / OpenAPI Draft | Supports future integration readiness. | To attach |
| A6 | Prototype / Simulation Report | Supports innovation and analytics evidence. | To attach |
| A7 | Dashboard And Workflow Screenshots | Demonstrates operational platform capability. | To attach |
| A8 | AI Model Methodology And Validation Note | Supports AI approach and predictive analytics capability. | To attach |
| A9 | Hardware / Sensor Datasheets, If Applicable | Supports proposed hardware or IoT components. | To attach / N/A |
| A10 | Third-Party Brochures, Certifications, Or Partner Literature | Supports supplier, principal, cloud, data, or implementation partners. | To attach / N/A |
| A11 | CVs And Certifications | Supports startup team and viability. | To attach |
| A12 | Support, Maintenance, HA/DR, And Backup Note | Supports operational readiness. | To attach |

## 17. Open Issues Before Submission

- [ ] Confirm final solution name and product branding.
- [ ] Confirm whether any hardware, sensor, IoT, DAS, connectivity, cloud, or data subscription component is proposed.
- [ ] Confirm all third-party technology, supplier, principal, subcontractor, or SME/startup partner roles.
- [ ] Insert final diagrams, page numbers, attachment filenames, and evidence references.
- [ ] Confirm no pricing information appears in this Volume III literature document or its attachments.
- [ ] Cross-reference the final attachment names and page numbers into the Part V Statement of Compliance reference column.
- [ ] Verify final wording against the original tender documents before submission.
