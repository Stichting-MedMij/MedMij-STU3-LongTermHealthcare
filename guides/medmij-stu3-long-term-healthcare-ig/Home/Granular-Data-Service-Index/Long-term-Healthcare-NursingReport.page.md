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
| **Data service version** | 1.0.0-beta.1 |
| **System role(s)** | LZ-NRR-1.0.0-beta.1-FHIR (PHR) <br/> LZ-NRB-1.0.0-beta.1-FHIR (XIS) |
| **Relevant domain(s)** | [Long-term Healthcare](https://simplifier.net/medmij-stu3-long-term-healthcare/) |

## Functional model
| | |
| --- | --- |
| **CIM** | Nursing report (based on [ANW v2024](https://nuts-foundation.gitbook.io/bolts/anw/v2024.1#id-5.2-wegschrijven-van-informatie)) |
| **Functional version** | 1.0.0-beta.2 |

The Logical Model is included below.

<tabs>
    <tab title="Tree view" active="true">
      {{tree:http://medmij.nl/fhir/StructureDefinition/lz-lm-NursingReport, buttons}}
    </tab>
    <tab title="Xml">
      {{xml:http://medmij.nl/fhir/StructureDefinition/lz-lm-NursingReport}}
    </tab>
    <tab title="Json">
      {{json:http://medmij.nl/fhir/StructureDefinition/lz-lm-NursingReport}}
    </tab>
</tabs>

## Technical specification
| | |
| --- | --- |
| **FHIR profile(s)** | [http://medmij.nl/fhir/StructureDefinition/lz-NursingReport](https://simplifier.net/resolve?canonical=http://medmij.nl/fhir/StructureDefinition/lz-NursingReport&scope=medmij.fhir.nl.stu3.longtermhealthcare@1.0.0-beta.2) |
| **FHIR package** | [medmij.fhir.nl.stu3.longtermhealthcare](https://simplifier.net/packages/medmij.fhir.nl.stu3.longtermhealthcare) version 1.0.0-beta.2 or compatible |
| **FHIR version** | STU3 |
| **Search request** | `GET [base]/Observation?code=http://snomed.info/sct|11591000146107` |
| **Must Support** | <ul> <li> `.identifier` <li> `.subject` <li> `.effectiveDateTime` <li> `.performer` (including the [practitionerrole-reference](https://simplifier.net/resolve?canonical=http://nictiz.nl/fhir/StructureDefinition/practitionerrole-reference&scope=nictiz.fhir.nl.stu3.zib2017@2.3.2) extension) <li> `.meta.tag` (only the [care type](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-exchange?version=1.0.0#CareType)) |
| **CapabilityStatement(s)** | [Long-term Healthcare NursingReport Retrieve](https://simplifier.net/resolve?canonical=http://medmij.nl/fhir/CapabilityStatement/lz-NursingReport-Retrieve&scope=medmij.fhir.nl.stu3.longtermhealthcare@1.0.0-beta.2) <br/> [Long-term Healthcare NursingReport Serve](https://simplifier.net/resolve?canonical=http://medmij.nl/fhir/CapabilityStatement/lz-NursingReport-Serve&scope=medmij.fhir.nl.stu3.longtermhealthcare@1.0.0-beta.2) |

The FHIR profile is included below.

<tabs>
    <tab title="Tree view" active="true">
      {{tree:http://medmij.nl/fhir/StructureDefinition/lz-NursingReport, buttons}}
    </tab>
    <tab title="Xml">
      {{xml:http://medmij.nl/fhir/StructureDefinition/lz-NursingReport}}
    </tab>
    <tab title="Json">
      {{json:http://medmij.nl/fhir/StructureDefinition/lz-NursingReport}}
    </tab>
</tabs>