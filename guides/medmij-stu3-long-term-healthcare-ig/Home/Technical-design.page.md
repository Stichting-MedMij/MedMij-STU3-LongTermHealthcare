---
topic: TO
---
 
# Technical design

## Introduction 

This technical design provides the technical specification of the Basic Long-term Healthcare Data Exchange+ (Dutch: Basisgegevens Langdurige Zorg+ or BgLZ+) standard based on a selection of Dutch Health Care Information Models.

The “expansion” of the long-term information standard is in first instance focused on Health Care Information Models of the information standard minimal eOverdracht version 4.0. The information standard minimal eOverdracht as published by Nictiz does not yet include a patient use case, this may change in the future. Up until then, the patient use case will be published by MedMij under the definition of Basic Long-term Healthcare Data Exchange+.  

This IG is a technical counterpart of the functional design. The FHIR version used for this IG is HL7 FHIR STU3. This implementation guide assumes that the reader is familiar with this FHIR version.  

Apart from this document, the guidelines as specified in the MedMij STU3 Core FHIR Implementation Guide apply. In particular, the reader should take note of the use case overarching principles.  

## Actors involved 
| Actor | |System | |
| --- | --- | --- | --- |
| Name | Description | Name |Description |
| Patient | The user of a personal healthcare environment | PHR | Personal health record |
| Healthcare provider | The user of a XIS | XIS | Healthcare information system |

**Table 1: Actors**

## Boundaries and relationships 
This technical design includes use cases for the exchange of the Basic Long-term Healthcare Data Exchange+ data between health care providers (e.g. nurses) and patients (e.g. in a PHR setting).

This technical design assumes that a PHR is able to make a connection to the right XIS that contains the patient's information. It does not provide information on finding the right source system nor does it provide information about security. These infrastructure and interface specifications are described in the [MedMij Afsprakenstelsel](https://afsprakenstelsel.medmij.nl/).

The Basic Long-term Healthcare Data Exchange+ is overlapping with other standards such as the [Basic Long-term Healthcare Data Exchange](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.02/OntwerpLangdurigeZorg). The Basic Long-term Healthcare Data Exchange+ uses the same Health Care Information Model (HCIM) based FHIR profiles for exchanging information as used in other standards.

## Use case: Retrieve BgLZ+ information
In this IG, BgLZ+ is provided as a combination of (1) the existing BgLZ exchange, which remains unchanged, and (2) granular exchange of an additional set of data services. Granular exchange allows the PHR to retrieve individual data services that are part of BgLZ+ through targeted search interactions, in accordance with the generic guidance and profiles defined in [MedMij STU3 Core](https://simplifier.net/medmij-stu3-core). Exchanging BgLZ together with these granular data services is optional: implementations may choose to exchange BgLZ and the granular data services, or only the granular data services.

The table below gives an overview of all granular data services that are applicable for BgLZ+.

| Id | Data service name without version (English) | Data service name without version (Dutch) | Data service version|
| --- | --- | --- | --- |
| 900000404 | [Retrieve MedMij Core - Alert (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-Alert?version=1.0.0) | Verzamelen MedMij Core - Alert (zib2017/STU3) | 1.0.0-beta.1 |
| 900000401 | [Retrieve MedMij Core - Blood pressure (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BloodPressure?version=1.0.0) | Verzamelen MedMij Core - Bloeddruk (zib2017/STU3) | 1.0.0-beta.1 |
| 900000402 | [Retrieve MedMij Core - Body height (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BodyHeight?version=1.0.0) | Verzamelen MedMij Core - Lichaamslengte (zib2017/STU3) | 1.0.0-beta.1 |
| 900000409 | [Retrieve MedMij Core - Body temperature (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BodyTemperature?version=1.0.0) | Verzamelen MedMij Core - Lichaamstemperatuur (zib2017/STU3) | 1.0.0-beta.1 |
| 900000403 | [Retrieve MedMij Core - Body weight (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-BodyWeight?version=1.0.0) | Verzamelen MedMij Core - Lichaamsgewicht (zib2017/STU3) | 1.0.0-beta.1 |
| 900000410 | [Retrieve MedMij Core - Fluid balance (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-FluidBalance?version=1.0.0) | Verzamelen MedMij Core - Vochtbalans (zib2017/STU3) | 1.0.0-beta.1 |
| 900000406 | [Retrieve MedMij Core - Living situation (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-LivingSituation?version=1.0.0) | Verzamelen MedMij Core - Woonsituatie (zib2017/STU3) | 1.0.0-beta.1 |
| 900000405 | [Retrieve MedMij Core - Nutrition advice (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-NutritionAdvice?version=1.0.0) | Verzamelen MedMij Core - Voedingsadvies (zib2017/STU3) | 1.0.0-beta.1 |
| 900000407 | [Retrieve MedMij Core - Payer (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-Payer?version=1.0.0) | Verzamelen MedMij Core - Betaler (zib2017/STU3) | 1.0.0-beta.1 |
| 900000412 | [Retrieve MedMij Core - Pulse rate (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-PulseRate?version=1.0.0) | Verzamelen MedMij Core - Polsfrequentie (zib2017/STU3) | 1.0.0-beta.1 |
| 900000411 | [Retrieve MedMij Core - Respiration (zib2017/STU3)](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index/MedMij-Core-Respiration?version=1.0.0) | Verzamelen MedMij Core - Ademhaling (zib2017/STU3) | 1.0.0-beta.1 |

**Table 2: Granular data services applicable for BgLZ+**

#### PHR: request message
For the cross-domain data services, the request parameters are defined in [MedMij STU3 Core](https://simplifier.net/medmij-stu3-core). This Long-term Healthcare IG only specifies additional guidance for the domain-specific data services. The PHR retrieves the FHIR resources using an individual search interaction. The client performs a search operation using the specified query parameters, executed as an HTTP GET:

`GET [base]/[type]{?[parameters]}`

The table below lists the sections, the CIMs that constitute those sections, and the specific content of the additional long-term care data. The last column shows the FHIR search queries to retrieve this information. At this time, only cross-domain data services are included; these can be found on this page [MedMij STU3 Core](https://simplifier.net/medmij-stu3-core).

For the HealthProfessional and HealthcareProvider HCIMs no separate data services have been defined. Instead, the corresponding Practitioner(Role) and Organization resources are secondary resources that support and contextualize the data exchanged via the granular data services listed above. Whenever these resources are referenced from other resources, they SHALL be resolvable, either by supporting a `read` interaction or by being explicitly included in the Bundle. For each granular data service, the secondary resources that have to be supported are specified in the corresponding CapabilityStatements. For the cross-domain data services, these CapabilityStatements are included on their respective page in the [MedMij STU3 Core IG](https://simplifier.net/medmij-stu3-core-ig?version=1.0.0).

#### XIS: response message
The returned data to the PHR should conform to the profiles listed in the table below.