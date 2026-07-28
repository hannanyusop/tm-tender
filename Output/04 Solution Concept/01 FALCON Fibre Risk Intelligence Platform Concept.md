# FALCON Fibre Risk Intelligence Platform Concept

Tender reference: `NAE/2026/RFP/01/A1G/BIG`  
Working output type: Solution concept draft for technical proposal development  
Related submission volume: Volume III — Technical Proposal  
Draft status: Working draft for proposer review

## Source References

- `Source/BIG Programme_SOC.docx`
- `Source/BIG Programme_SOC Addendum.docx`
- `Source/Batch1 Q&A_BIG2.0 RFP (1).pdf`
- `Source/Batch2 Q&A_BIG2.0 RFP.pdf`
- `Source/Reference Baseline for Solution Design and BOQ.pptx`
- `Source/Appendix B.1 Information Security Annex.pdf`
- `Source/Appendix B.2 Vendor Security Hygiene.pdf`
- `Output/03 Technical Supporting Literature/01 Proposers Specifications And Supporting Literature.md`

## Usage Notes

- This is a concept-development document, not final submission wording.
- Use this document to refine the proposer narrative, architecture, POC plan, IoT assumptions, workflow design, and supporting literature.
- Verify final contractual, technical, acceptance, security, data, pricing, and submission-critical statements against the original tender source files before incorporating them into the final proposal.
- Do not include priced BOQ details, commercial totals, rate cards, discounts, or other price information in this document.
- Keep POC device quantities, selected sites, power availability, camera permission, connectivity, and installation method as assumptions until confirmed with TM.

## 1. Recommended Concept

The recommended direction is the **FALCON Fibre Risk Intelligence Platform**.

The strongest proposal position is not to build only an IoT monitoring system. The solution should be positioned as an end-to-end preventive operations platform:

```text
Data and sensors -> risk detection -> AI prediction -> verification -> alert -> field action -> escalation -> closure -> model learning
```

This direction directly supports the tender objective to address construction activity, theft/vandalism, and rodents/wildlife while tracking preventive action rather than merely displaying alerts on a dashboard.

## 2. Proposed System Modules

### 2.1 Command Dashboard

A central dashboard should support TM operations and management users.

Main components:

- Overall network risk score.
- Active high-risk locations.
- Open preventive cases.
- Alerts awaiting acknowledgement.
- Cases exceeding SLA.
- Risk breakdown by construction, theft/vandalism, and rodent/wildlife.
- Device and communication status.
- Map showing fibre routes and risk hotspots.
- Trend comparison by day, week, and month.

The dashboard should clearly distinguish:

| Event Type | Meaning |
| --- | --- |
| Predicted risk | Something may happen. |
| Detected activity | A sensor or external data source identified an event. |
| Confirmed incident | A human user or field team verified the event. |
| Actual fibre fault | Fibre service was affected. |

This distinction is important for calculating model accuracy and operational value.

### 2.2 GIS Fibre Risk Map

The GIS fibre risk map should be the core operational screen.

Potential map layers:

- Fibre route.
- Fibre joints, cabinets, manholes, and poles.
- Historical fault locations.
- Construction activity.
- High-risk theft zones.
- Rodent recurrence areas.
- Sensor locations.
- Camera coverage.
- Active cases.
- Field team locations, where permitted.
- Weather and flood information.
- Land-use or vegetation zones.

Each fibre route may be divided into segments such as:

- 100 metres.
- 250 metres.
- 500 metres.

Each segment should receive a risk score:

| Score | Classification | Recommended Response |
| --- | --- | --- |
| 0–30 | Low | Continue monitoring. |
| 31–60 | Medium | Review and schedule inspection. |
| 61–80 | High | Verify and assign preventive action. |
| 81–100 | Critical | Immediate notification and escalation. |

The score should explain why the location is high risk.

Example:

> Risk score: 87 — Critical  
> Primary cause: Excavation activity  
> Distance from fibre: 8 metres  
> Supporting factors: Repeated vibration, active construction permit, and two historical faults within 500 metres.

### 2.3 Alert And Event Management

The platform should include a unified alert centre.

Each alert should contain:

- Alert ID.
- Date and time.
- Location.
- Fibre segment.
- Threat category.
- Risk score.
- Confidence score.
- Source of detection.
- Related sensor readings.
- Images or video evidence.
- Recommended action.
- Assigned team.
- Acknowledgement status.
- SLA deadline.
- Escalation level.
- Full audit trail.

Suggested alert lifecycle:

```text
New -> Awaiting verification -> Verified -> Assigned -> In progress -> Mitigated -> Closed
```

Other statuses:

- False alarm.
- Duplicate.
- Monitoring only.
- Unable to verify.
- Escalated.
- Converted to actual incident.

### 2.4 Preventive Case And Work-Order Module

When a risk exceeds a defined threshold, the platform should automatically create a preventive case.

Example construction actions:

- Contact contractor.
- Verify permit.
- Mark fibre alignment at site.
- Dispatch technician.
- Install warning sign.
- Conduct site patrol.
- Escalate to local authority.

Example theft or vandalism actions:

- Review camera evidence.
- Dispatch security team.
- Notify police.
- Inspect cabinet or manhole.
- Secure access cover.
- Increase patrol frequency.
- Install temporary surveillance.

Example rodent or wildlife actions:

- Inspect cable route.
- Install rodent protection.
- Seal entry points.
- Replace exposed ducting.
- Clear vegetation.
- Add bait station where legally and operationally appropriate.
- Schedule recurring inspection.

Every action should capture:

- Owner.
- Target date.
- SLA.
- Notes.
- Before-and-after photographs.
- GPS location.
- Materials used.
- Closure reason.
- Supervisor approval.

### 2.5 SLA And Escalation Engine

Suggested SLA levels:

| Severity | Acknowledge | Verify | Action Started |
| --- | --- | --- | --- |
| Critical | 5 minutes | 15 minutes | 30 minutes |
| High | 10 minutes | 30 minutes | 1 hour |
| Medium | 30 minutes | 2 hours | 4 hours |
| Low | 4 hours | 1 working day | Scheduled |

These values should remain configurable until confirmed with TM.

Escalation example:

1. Notify operational officer.
2. If not acknowledged, notify team leader.
3. If still unacknowledged, notify regional manager.
4. For critical threats, notify NOC or relevant emergency contact.
5. Continue escalating until acknowledgement or case reassignment.

The system should measure the tender workflow-initiation threshold separately:

- POC: workflow initiated within 15 minutes.
- Pilot: workflow initiated within 10 minutes.

### 2.6 AI Risk Engine

The recommended approach is hybrid AI and configurable rules, not AI alone.

AI components:

- Route-level risk prediction.
- Historical hotspot clustering.
- Time-of-day and seasonal analysis.
- Event classification.
- Sensor anomaly detection.
- Image or video object detection.
- False-alarm reduction.
- Recommended preventive action.

Rules components:

- Risk thresholds.
- Fibre proximity rules.
- Escalation rules.
- SLA calculations.
- Known contractor whitelist.
- Working-hour rules.
- Repeated event logic.
- Critical infrastructure prioritisation.

Possible combined score:

| Component | Draft Weight |
| --- | ---: |
| Historical risk | 25% |
| Real-time sensor risk | 25% |
| Location proximity | 20% |
| External activity | 15% |
| Asset criticality | 10% |
| Environmental risk | 5% |

Weights should later be calibrated using TM data.

The model should provide explainability, such as:

- Construction equipment detected.
- Activity is within 12 metres of fibre.
- Route experienced three related faults previously.
- Vibration exceeded baseline by 65%.
- Event occurred outside approved working hours.

### 2.7 Resource Planning Module

The tender mentions manpower, material, and dispatch planning, so this should be visible in the platform rather than only described.

The module can recommend:

- Nearest available field team.
- Required skill set.
- Recommended tools.
- Replacement materials.
- Estimated travel time.
- Priority compared with other cases.
- Expected operational impact.
- Whether security or authority involvement is needed.

Example:

> Recommended response: Fibre patrol team  
> Personnel: 2 technicians  
> Equipment: Fibre locator, route marker, camera  
> Supporting party: Contractor liaison officer  
> Dispatch priority: 1 of 6 active cases.

For POC, this can initially be rule-based rather than a sophisticated optimisation engine.

### 2.8 Mobile Field Application Or PWA

Field teams should be able to:

- Receive assignments.
- Navigate to the location.
- View fibre route and alert details.
- Acknowledge a task.
- Upload photographs and video.
- Record findings.
- Update work status.
- Capture GPS coordinates.
- Record materials used.
- Request escalation.
- Submit closure evidence.
- Work temporarily offline.

For Year 1, a mobile-responsive PWA may be more practical than separate Android and iOS applications.

### 2.9 Reporting And Analytics

Suggested reports:

- High-risk fibre segments.
- Alert response time.
- Preventive workflow initiation time.
- SLA compliance.
- Number of risks mitigated before disruption.
- False-positive rate.
- Risk category distribution.
- Fault recurrence.
- Construction-risk report.
- Theft hotspot report.
- Rodent hotspot report.
- Field team performance.
- Device uptime and offline duration.
- AI model precision, recall, and F1 score.
- POC versus Pilot KPI comparison.

Reports should support PDF, CSV, and XLSX exports where required by the source documents.

## 3. IoT Design By Threat Category

One device type should not be proposed as the solution for all three risk families.

### 3.1 Construction And Excavation Detection

Recommended devices:

| Device | Purpose |
| --- | --- |
| Ground vibration sensor or geophone | Detects digging, drilling, and heavy machinery vibration near critical underground fibre routes. |
| Acoustic sensing device | Identifies unusual excavation or impact patterns, useful where vibration alone produces too many false alarms. |
| AI camera | Detects excavators, backhoes, trucks, and human activity, and provides evidence before dispatching a team. |
| GNSS-enabled IoT gateway | Sends events to the central platform and maintains device identity and location. |
| Optional DAS integration | Uses existing fibre as a sensing medium for long-route coverage, but should be treated as an optional advanced pilot track due to complexity and cost. |

Recommended detection logic:

```text
High vibration
+ equipment detected by camera
+ event within 20 metres of fibre
+ no approved work record
= Critical construction alert
```

### 3.2 Theft And Vandalism Detection

Recommended devices:

| Device | Purpose |
| --- | --- |
| Low-light AI camera | Supports human, vehicle, and loitering detection at night. |
| Door or cabinet contact sensor | Detects unauthorised cabinet opening. |
| Manhole cover tamper sensor | Detects lifting, movement, or removal. |
| Tilt and vibration sensor | Detects impact, cutting, or forced access. |
| Passive infrared or microwave motion sensor | Detects presence around restricted infrastructure. |
| Acoustic sensor | Detects cutting, drilling, or repeated metallic impact. |
| Siren or strobe deterrent | Optional local deterrence after central verification and defined activation rules. |
| Solar-powered edge gateway | Suitable for locations without stable utility power. |

Recommended detection logic:

```text
Cabinet opened
+ no authorised maintenance ticket
+ event outside working hours
+ person detected
= Critical tampering alert
```

### 3.3 Rodents, Pests, And Wildlife

Rodent and wildlife risk is more difficult to detect directly. The primary strategy should be predictive maintenance, supported by targeted sensing at selected sites.

Possible devices:

| Device | Purpose |
| --- | --- |
| Environmental sensor | Measures temperature, humidity, water ingress, and enclosure conditions. |
| PIR or thermal sensor | Detects movement inside cabinets or chambers. |
| Small inspection camera | Used at high-recurrence sites rather than throughout the network. |
| Acoustic sensor | Experimental detection of scratching or chewing patterns. |
| Smart bait or trap monitoring | Useful only where operationally and legally suitable. |
| Cable or enclosure tamper/continuity sensor | Detects physical disturbance before full cable failure. |

For Year 1, rodent/wildlife prediction should prioritise:

- Historical recurrence.
- Vegetation.
- Drainage and water exposure.
- Nearby food premises or waste sites.
- Underground chamber condition.
- Cable protection type.
- Past maintenance records.
- Seasonal patterns.

This risk family may initially be predicted mainly through data analytics instead of widespread IoT installation.

## 4. Common IoT Architecture

```text
Sensor / Camera
      ↓
Edge Controller or IoT Gateway
      ↓
4G/5G, NB-IoT, LoRaWAN or Fixed Network
      ↓
Secure IoT Ingestion Service
      ↓
Device Registry and Message Broker
      ↓
Rules Engine + AI Analytics
      ↓
FALCON Alert and Workflow Platform
      ↓
Dashboard / PWA / Notification
```

Edge gateway responsibilities:

- Register and authenticate devices.
- Buffer readings when the network is unavailable.
- Filter unnecessary raw data.
- Perform simple local event detection.
- Encrypt transmitted data.
- Send device health information.
- Synchronise time.
- Support remote configuration.
- Support firmware updates.
- Store limited evidence locally.
- Retry failed transmissions.

For cameras, the recommended approach is to transmit event clips or snapshots rather than continuous video unless continuous streaming is specifically required.

## 5. Connectivity Options

| Connectivity | Best Use | Concern |
| --- | --- | --- |
| 4G/5G | Camera sites and high-volume data. | Recurring SIM cost and coverage. |
| NB-IoT | Low-bandwidth sensors. | Not suitable for video. |
| LoRaWAN | Multiple low-power sensors in an area. | Requires gateway coverage. |
| Fixed broadband | Permanent sites with existing connectivity. | Not available everywhere. |
| Satellite | Remote areas with no cellular coverage. | Higher equipment and service cost. |
| Store-and-forward | Temporary loss of connectivity. | Alerts may be delayed. |

A hybrid connectivity model is more realistic than selecting a single technology.

## 6. Device Management Module

The application should include an IoT device registry with:

- Device ID.
- Device type.
- Serial number.
- Installation location.
- Associated fibre segment.
- Firmware version.
- Connectivity type.
- SIM or gateway information.
- Last communication time.
- Battery level.
- Signal strength.
- Sensor health.
- Installation date.
- Warranty.
- Maintenance schedule.
- Assigned supplier.
- Calibration history.

Device states:

- Online.
- Offline.
- Degraded.
- Low battery.
- Communication failure.
- Sensor fault.
- Maintenance mode.
- Decommissioned.

## 7. Recommended Year 1 POC Scope

Avoid deploying too many device types in the POC. A focused design is easier to deliver and validate.

Suggested POC:

| Site | Risk Focus | Indicative Components | Workflow Focus |
| --- | --- | --- | --- |
| Site 1 | Construction risk | One vibration sensor, one AI camera, one cellular gateway. | Construction-risk detection workflow. |
| Site 2 | Theft/vandalism risk | One AI camera, one cabinet/manhole tamper sensor, one motion or vibration sensor, one gateway. | Security verification workflow. |
| Site 3 | Rodent/wildlife risk | Environmental sensor, internal movement or inspection sensor, historical-risk prediction model. | Preventive maintenance workflow. |

Exact quantities must remain assumptions until TM confirms designated routes, site conditions, power availability, permitted installation methods, and installation responsibilities.

## 8. POC Demonstration Scenario

During the demonstration:

1. Simulate excavation near a selected fibre segment.
2. Vibration sensor detects the activity.
3. Camera identifies construction equipment.
4. Gateway sends the event.
5. Platform associates the event with the fibre route.
6. AI/rules calculate the risk score.
7. Alert appears on the heatmap.
8. Preventive task is automatically created.
9. Operations user acknowledges it.
10. Field officer receives the assignment.
11. Officer uploads site evidence.
12. Supervisor verifies mitigation.
13. Case is closed.
14. Response-time and model evidence appear in the KPI report.

This demonstrates the complete tender value chain rather than merely showing sensor readings.

## 9. Potential Differentiators

Potential innovation features:

- Digital representation of each fibre route segment.
- What-if risk simulation.
- AI-generated incident summary.
- Automatic recommended mitigation.
- Duplicate alert correlation.
- Risk confidence and explainability.
- Contractor activity geofencing.
- Permit or planned-work matching.
- Offline field operations.
- Edge AI to reduce data transfer.
- Device battery prediction.
- Predictive maintenance for sensors.
- Automatic model-drift monitoring.
- Pre- and post-mitigation risk comparison.
- Evidence-based closure approval.
- Route criticality based on affected customers or services.
- Risk simulation during heavy rain or major construction periods.

## 10. Key Decisions For Technical Workshop

The next design workshop should finalise:

- [ ] Whether the POC will use real field devices, simulated feeds, or both.
- [ ] Number and characteristics of POC sites.
- [ ] Whether TM permits cameras near its infrastructure.
- [ ] Power availability at each location.
- [ ] Cellular coverage at the selected sites.
- [ ] Whether construction permit data can be obtained.
- [ ] Whether TM will provide asset criticality and customer-impact data.
- [ ] Whether GIS fibre geometry can be loaded into the standalone platform.
- [ ] Whether field users require a PWA or dashboard only.
- [ ] Whether DAS is included, optional, or excluded.
- [ ] Whether video is stored centrally or only event snapshots are retained.
- [ ] Who performs physical installation and device maintenance.
- [ ] What constitutes a successful prediction.
- [ ] How false positives will be measured.
- [ ] Exact acceptance thresholds for POC and Pilot.

## 11. Initial Recommendation

Use a hybrid architecture with:

- Web-based command platform.
- GIS fibre-risk map.
- AI plus configurable rules.
- Preventive workflow and SLA engine.
- Mobile PWA for field teams.
- IoT device management.
- Targeted sensors only at selected critical sites.
- External datasets for broader route coverage.
- API-ready standalone deployment.
- Optional DAS as an advanced future component.

This keeps the Year 1 scope achievable while presenting a credible path toward national-scale fibre resilience.

