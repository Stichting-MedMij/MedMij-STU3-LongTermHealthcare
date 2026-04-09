---
topic: TD
---

# Technical design

## Introduction
This technical design provides the technical specification of the Basic Long-term Healthcare Data Exchange+ (Dutch: Basisgegevens Langdurige Zorg+ or BgLZ+) standard. This 'expansion' of the [BgLZ](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.02/FHIR_BGLZ) information standard is initially focused on Health and Care Clinical Information Models (HCIMs) of the information standard [Minimal eOverdracht (MeO), version 4.0](https://informatiestandaarden.nictiz.nl/wiki/vpk:V4.0_FHIR_eOverdracht), which is published by Nictiz. The MeO does not yet include a patient use case, however, this may change in the future. Up until then, the patient use case will be published by MedMij under the definition of Basic Long-term Healthcare Data Exchange+.

This technical design is the technical counterpart of the {{pagelink: FO, text: functional design}}. The FHIR version used for this IG is STU3 (3.0.2).

Note that in addition to this design, the (technical) guidelines as specified in the [MedMij STU3 Core IG](https://simplifier.net/guide/medmij-stu3-core-ig?version=1.2.1) and the [MedMij FHIR IG for STU3, version 2020.02](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.02/FHIR_IG) apply, the latter of which is published by Nictiz.

## Actors involved
| Actor | | System | |
| --- | --- | --- | --- |
| **Name** | **Description** | **Name** | **Description** |
| Patient | The user of a personal healthcare environment | PHR | Personal health record |
| Healthcare provider | The user of a XIS | XIS | Healthcare information system |

**Table 1: Actors**

## Boundaries and relationships
This technical design includes use cases for the exchange of long-term healthcare data (specifically, data that is part of the BgLZ+) between healthcare providers (e.g. nurses) and patients (e.g. in a PHR setting).

This technical design assumes that a PHR is able to make a connection to the right XIS that contains the patient's information. It does not provide information on finding the right source system nor does it provide information about security. These infrastructure and interface specifications are described in the [MedMij Afsprakenstelsel](https://afsprakenstelsel.medmij.nl/). In particular, each transaction is performed in the context of a specific authenticated patient, which has been established using the authentication mechanisms outlined in the MedMij Afsprakenstelsel (also see the [MedMij FHIR IG by Nictiz](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.02/FHIR_IG#Afsprakenstelsel)), i.e. via an OAuth2 token. Each XIS gateway is required to perform filtering based on the patient associated with the context for the request, so only the records associated with the authenticated patient are returned. For this reason, search parameters for patient identification SHALL NOT be included.

The BgLZ+ is related to several other information standards, since it is an expansion of the [BgLZ](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.02/OntwerpLangdurigeZorg) and has overlap with the [MeO](https://informatiestandaarden.nictiz.nl/wiki/vpk:V4.0_FHIR_eOverdracht). In particular, these standards make use of the same set of HCIM-based FHIR profiles, which are bundled in the [nictiz.fhir.nl.stu3.zib2017](https://simplifier.net/packages/nictiz.fhir.nl.stu3.zib2017) package.

## <a name="RelatingFHIRToFunctionalCounterpart"></a> Relating FHIR (profiles) to its functional counterpart
The functional model used in the BgLZ+ consists of zibs from [publication 2017](https://zibs.nl/wiki/HCIM_Release_2017(EN)), as well as Clinical Information Models (CIMs) defined by MedMij, the latter of which are represented by {{pagelink: LogicalModelsIndex, text: Logical Models}}.
- For each concept in these Logical Models, an id is assigned by MedMij. These ids are also added as mappings in the {{pagelink: FHIRProfilesIndex, text: FHIR profiles}} on the corresponding elements, i.e. by specifying `.mapping.map` on each element accordingly. Therefore, these ids form the linking pin between the Logical Models and FHIR profiles. If no such mapping is possible for a certain element in a FHIR profile, guidance is provided to indicate how that element should be handled.
- The zibs are technically implemented via nl-core profiles, which are bundled in the [nictiz.fhir.nl.stu3.zib2017](https://simplifier.net/packages/nictiz.fhir.nl.stu3.zib2017) package. In these profiles, mappings to the corresponding zib (concepts) have been added.

## Use cases
As the BgLZ+ is an expansion of the BgLZ, long-term healthcare data is exchanged by a combination of the BgLZ (whose use case remains unchanged) and BgLZ+. Note that the exchange of the BgLZ is not a prerequisite for exchanging the BgLZ+: implementations may choose to exchange both the BgLZ and the BgLZ+, only the BgLZ (which is not in scope of this IG) or only (part of) the BgLZ+.

### Use case: Retrieve BgLZ+ data
The BgLZ+ data is defined and exchanged in a granular manner, which means that for each CIM that is part of the BgLZ+, a separate (granular) data service is defined. Granular exchange allows the PHR to retrieve individual data services that are part of BgLZ+ through targeted search interactions, in accordance with the general guidance and profiles defined in the [MedMij STU3 Core IG](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-exchange?version=1.2.1).

The table below gives an overview of all granular data services that are applicable for BgLZ+. Note that cross-domain data services are defined in the MedMij STU3 Core IG, while domain-specific data services are defined in this IG.

| Id | Data service name without version (English) | Data service name without version (Dutch) | Data service version |
| --- | --- | --- | --- |
| 900000404 | [Retrieve MedMij Core - Alert (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-Alert?version=1.2.1) | Verzamelen MedMij Core - Alert (zib2017/STU3) | 1.0.0-rc.2 |
| 900000401 | [Retrieve MedMij Core - Blood pressure (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BloodPressure?version=1.2.1) | Verzamelen MedMij Core - Bloeddruk (zib2017/STU3) | 1.0.0-rc.2 |
| 900000402 | [Retrieve MedMij Core - Body height (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BodyHeight?version=1.2.1) | Verzamelen MedMij Core - Lichaamslengte (zib2017/STU3) | 1.0.0-rc.2 |
| 900000409 | [Retrieve MedMij Core - Body temperature (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BodyTemperature?version=1.2.1) | Verzamelen MedMij Core - Lichaamstemperatuur (zib2017/STU3) | 1.0.0-rc.2 |
| 900000403 | [Retrieve MedMij Core - Body weight (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BodyWeight?version=1.2.1) | Verzamelen MedMij Core - Lichaamsgewicht (zib2017/STU3) | 1.0.0-rc.2 |
| 900000410 | [Retrieve MedMij Core - Fluid balance (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-FluidBalance?version=1.2.1) | Verzamelen MedMij Core - Vochtbalans (zib2017/STU3) | 1.0.0-rc.2 |
| 900000406 | [Retrieve MedMij Core - Living situation (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-LivingSituation?version=1.2.1) | Verzamelen MedMij Core - Woonsituatie (zib2017/STU3) | 1.0.0-rc.2 |
| 900000405 | [Retrieve MedMij Core - Nutrition advice (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-NutritionAdvice?version=1.2.1) | Verzamelen MedMij Core - Voedingsadvies (zib2017/STU3) | 1.0.0-rc.2 |
| 900000407 | [Retrieve MedMij Core - Payer (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-Payer?version=1.2.1) | Verzamelen MedMij Core - Betaler (zib2017/STU3) | 1.0.0-rc.2 |
| 900000412 | [Retrieve MedMij Core - Pulse rate (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-PulseRate?version=1.2.1) | Verzamelen MedMij Core - Polsfrequentie (zib2017/STU3) | 1.0.0-rc.2 |
| 900000411 | [Retrieve MedMij Core - Respiration (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-Respiration?version=1.2.1) | Verzamelen MedMij Core - Ademhaling (zib2017/STU3) | 1.0.0-rc.2 |
| 900000408 | {{pagelink: Encounter, text: Retrieve Long-term Healthcare - Encounter}} | Verzamelen Langdurige Zorg - Contact | 1.0.0-beta.2 |
| 900000413 | {{pagelink: NursingReport, text: Retrieve Long-term Healthcare - Nursing report}} | Verzamelen Langdurige Zorg - Dagrapportage | 1.0.0-rc.2 |

**Table 2: Granular data services applicable for BgLZ+**

The technical specifications with respect to the request message executed by the PHR and the response message of the XIS are detailed in the [MedMij STU3 Core IG](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-exchange?version=1.2.1#GeneralTechnicalSpecifications).