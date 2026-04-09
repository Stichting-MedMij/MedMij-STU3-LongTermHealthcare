---
topic: Encounter
---

# Retrieve Long-term Healthcare - Encounter

## Overview
| | |
| --- | --- |
| **Id** | 900000408 |
| **Data service name without version (English)** | Retrieve Long-term Healthcare - Encounter |
| **Data service name without version (Dutch)** | Verzamelen Langdurige Zorg - Contact |
| **Data service version** | 1.0.0-beta.1 |
| **System role(s)** | LZ-ENR-1.0.0-beta.1-FHIR (PHR) <br/> LZ-ENB-1.0.0-beta.1-FHIR (XIS) |
| **Used in Implementation Guide(s)** | [Long-term Healthcare](https://simplifier.net/medmij-stu3-long-term-healthcare/) |

## Functional model
| | |
| --- | --- |
| **CIM** | [zib Encounter in publication 2017](https://zibs.nl/wiki/Encounter-v3.1(2017EN)) adjusted with a pre-adopt of its counterpart in [publication 2020](https://zibs.nl/wiki/Encounter-v4.0.1(2020EN)) in the sense that future contacts are in scope as well |
| **Functional version** | 1.0.0-rc.2 |

## Technical specification
| | |
| --- | --- |
| **FHIR profile(s)** | [http://medmij.nl/fhir/StructureDefinition/lz-Encounter](https://simplifier.net/resolve?canonical=http://medmij.nl/fhir/StructureDefinition/lz-Encounter&scope=medmij.fhir.nl.stu3.longtermhealthcare@1.0.0-rc.2) |
| **FHIR package** | [medmij.fhir.nl.stu3.longtermhealthcare](https://simplifier.net/packages/medmij.fhir.nl.stu3.longtermhealthcare) version 1.0.0-rc.2 or compatible |
| **FHIR version** | STU3 |
| **Search request** | `GET [base]/Encounter` |
| **Must Support** | <ul> <li> `.identifier` <li> `.subject` <li> `.period` <li> `.participant.individual` (only reference to [http://fhir.nl/fhir/StructureDefinition/nl-core-practitioner](https://simplifier.net/resolve?canonical=http://fhir.nl/fhir/StructureDefinition/nl-core-practitioner&scope=nictiz.fhir.nl.stu3.zib2017@2.3.2), including the [practitionerrole-reference](https://simplifier.net/resolve?canonical=http://nictiz.nl/fhir/StructureDefinition/practitionerrole-reference&scope=nictiz.fhir.nl.stu3.zib2017@2.3.2) extension) <li> `.serviceProvider` <li> `.diagnosis.condition` <li> `.meta.tag` (only the [care type](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-exchange?version=1.2.0#CareType)) |
| **CapabilityStatement(s)** | [Long-term Healthcare Encounter Retrieve](https://simplifier.net/resolve?canonical=http://medmij.nl/fhir/CapabilityStatement/lz-Encounter-Retrieve&scope=medmij.fhir.nl.stu3.longtermhealthcare@1.0.0-rc.2) <br/> [Long-term Healthcare Encounter Serve](https://simplifier.net/resolve?canonical=http://medmij.nl/fhir/CapabilityStatement/lz-Encounter-Serve&scope=medmij.fhir.nl.stu3.longtermhealthcare@1.0.0-rc.2) |

The FHIR profile is included below.

<tabs>
    <tab title="Tree view" active="true">
      {{tree:http://medmij.nl/fhir/StructureDefinition/lz-Encounter, buttons}}
    </tab>
    <tab title="Xml">
      {{xml:http://medmij.nl/fhir/StructureDefinition/lz-Encounter}}
    </tab>
    <tab title="Json">
      {{json:http://medmij.nl/fhir/StructureDefinition/lz-Encounter}}
    </tab>
</tabs>