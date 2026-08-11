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
| **Data service version** | 1.0.0-beta.3 |
| **System role(s)** | LZ-ENR-beta.3 (PHR) <br/> LZ-ENB-beta.3 (XIS) |
| **Used in Implementation Guide(s)** | [Long-term Healthcare](https://simplifier.net/medmij-stu3-long-term-healthcare/) |

## Functional model
| | |
| --- | --- |
| **CIM** | [zib Encounter in publication 2017](https://zibs.nl/wiki/Encounter-v3.1(2017EN)) adjusted with a pre-adopt of its counterpart in [publication 2020](https://zibs.nl/wiki/Encounter-v4.0.1(2020EN)) in the sense that future contacts are in scope as well |
| **Functional version** | 1.0.0-rc.3 |

The functional model can be found on [ART-DECOR](https://decor.nictiz.nl/pub/zib2017bbr/zib2017bbr-html-20211029T113909/tr-2.16.840.1.113883.2.4.3.11.60.7.4.2.15.1-2017-12-31T000000.html). However, note that the StartDateTime (BeginDatumTijd) concept may attain a value that lies in the future.

## Technical specification
| | |
| --- | --- |
| **FHIR profile(s)** | {{pagelink: FHIRProfilesIndex, text: <text>http://medmij.nl/fhir/StructureDefinition/lz-Encounter</text>, anchor: LzEncounter}} |
| **FHIR package** | [medmij.fhir.nl.stu3.longtermhealthcare](https://simplifier.net/packages/medmij.fhir.nl.stu3.longtermhealthcare) version 1.0.0-rc.3 or compatible |
| **FHIR version** | STU3 |
| **Search request** | `GET [base]/Encounter` |
| **Must Support** | <ul> <li> `.identifier` <li> `.subject` <li> `.period` <li> `.participant.individual` (only reference to [http://fhir.nl/fhir/StructureDefinition/nl-core-practitioner](https://simplifier.net/resolve?canonical=http://fhir.nl/fhir/StructureDefinition/nl-core-practitioner&scope=nictiz.fhir.nl.stu3.zib2017@2.3.2), including the [practitionerrole-reference](https://simplifier.net/resolve?canonical=http://nictiz.nl/fhir/StructureDefinition/practitionerrole-reference&scope=nictiz.fhir.nl.stu3.zib2017@2.3.2) extension) <li> `.serviceProvider` <li> `.diagnosis.condition` <li> `.meta.tag` (only the [care type](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-exchange?version=1.3.0#CareType)) |
| **CapabilityStatement(s)** | {{pagelink: CapabilityStatementsIndex, text: Encounter (Retrieve), anchor: EncounterRetrieve}} <br/> {{pagelink: CapabilityStatementsIndex, text: Encounter (Serve), anchor: EncounterServe}} |

The FHIR profile is included below.

<tabs>
    <tab title="Tree view" active="true">
      {{tree:http://medmij.nl/fhir/StructureDefinition/lz-Encounter, buttons}}
    </tab>
    <tab title="Mappings">
      {{page:fql-get-mappings, canonical:http://medmij.nl/fhir/StructureDefinition/lz-Encounter}}
    </tab>
    <tab title="Mappings (zib profile)">
      {{page:fql-get-mappings-zib, canonical:http://nictiz.nl/fhir/StructureDefinition/zib-Encounter}}
    </tab>
    <tab title="Xml">
      {{xml:http://medmij.nl/fhir/StructureDefinition/lz-Encounter}}
    </tab>
    <tab title="Json">
      {{json:http://medmij.nl/fhir/StructureDefinition/lz-Encounter}}
    </tab>
    <tab title="Examples">
      {{page:fql-get-examples, canonical:http://medmij.nl/fhir/StructureDefinition/lz-Encounter}}
    </tab>
</tabs>