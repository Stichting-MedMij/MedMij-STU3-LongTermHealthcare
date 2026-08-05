---
topic: NursingReport
---

# Retrieve Long-term Healthcare - Nursing report

## Overview
| | |
| --- | --- |
| **Id** | 900000413 |
| **Data service name without version (English)** | Retrieve Long-term Healthcare - Nursing report |
| **Data service name without version (Dutch)** | Verzamelen Langdurige Zorg - Dagrapportage |
| **Data service version** | 1.0.0-rc.3 |
| **System role(s)** | LZ-NRR-rc.3 (PHR) <br/> LZ-NRB-rc.3 (XIS) |
| **Used in Implementation Guide(s)** | [Long-term Healthcare](https://simplifier.net/medmij-stu3-long-term-healthcare/) |

## Functional model
| | |
| --- | --- |
| **CIM** | NursingReport (based on the [ANW v2024.1](https://nuts-foundation.gitbook.io/bolts/anw/v2024.1#id-5.2-wegschrijven-van-informatie) specification) |
| **Functional version** | 1.0.0-rc.3 |

The Logical Model is included below.

{{page:resource-lm-view-tree, canonical:http://medmij.nl/fhir/StructureDefinition/lz-lm-NursingReport}}

## Technical specification
| | |
| --- | --- |
| **FHIR profile(s)** | [http://medmij.nl/fhir/StructureDefinition/lz-NursingReport](https://simplifier.net/resolve?canonical=http://medmij.nl/fhir/StructureDefinition/lz-NursingReport&scope=medmij.fhir.nl.stu3.longtermhealthcare@1.0.0-rc.3) |
| **FHIR package** | [medmij.fhir.nl.stu3.longtermhealthcare](https://simplifier.net/packages/medmij.fhir.nl.stu3.longtermhealthcare) version 1.0.0-rc.3 or compatible |
| **FHIR version** | STU3 |
| **Search request** | `GET [base]/Observation?code=http://snomed.info/sct|11591000146107` |
| **Must Support** | <ul> <li> `.identifier` <li> `.subject` <li> `.effectiveDateTime` <li> `.performer` (including the [practitionerrole-reference](https://simplifier.net/resolve?canonical=http://nictiz.nl/fhir/StructureDefinition/practitionerrole-reference&scope=nictiz.fhir.nl.stu3.zib2017@2.3.2) extension) <li> `.valueString` <li> `.meta.tag` (only the [care type](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-exchange?version=1.3.0#CareType)) |
| **CapabilityStatement(s)** | {{pagelink: CapabilityStatementsIndex, text: Nursing Report (Retrieve), anchor: NursingReportRetrieve}} <br/> {{pagelink: CapabilityStatementsIndex, text: Nursing Report (Serve), anchor: NursingReportServe}} |

The FHIR profile is included below.

{{page:resource-view-tree, canonical:http://medmij.nl/fhir/StructureDefinition/lz-NursingReport}}