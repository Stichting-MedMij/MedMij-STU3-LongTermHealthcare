# {{page-title}}

## 1.0.0-rc.3

| Component                   | Description  | Ticket    |
| --------------------------- | ------------ | --------- |
| Dataset                     | The explicit modeling of the HealthProfessional and HealthcareProvider within the Performer concept of the NursingReport Logical Model has been replaced by references to the MedMij Core Logical Models for HealthProfessional and HealthcareProvider. In particular, several cardinalities have been relaxed and some (optional) concepts have been added. Moreover, the binding on OrganizationType has been changed from *extensible* to *required*. | [DOSINZAGE1-1041](https://medmij.atlassian.net/browse/DOSINZAGE1-1041) |
| Functional design           | The display guideline has been updated: <br/> <ul> <li> Guidance on the exchange of the CIM Encounter with other contact types (i.e. with ContactType equal to NullFlavor *OTH*) has been added. <li> The acceptance criteria for the overview have been updated, while the acceptance criteria for the detail view have been added. <li> The definition of 'Won't have' in the MoSCoW method has been finetuned. | [DOSINZAGE1-1003](https://medmij.atlassian.net/browse/DOSINZAGE1-1003) |
| Functional design           | The cross-domain data services Alert, Blood pressure, Body height, Body temperature, Body weight, Fluid balance, Living situation, Nutrition advice, Payer, Pulse rate and Respiration have been updated to version 1.0.0-rc.3. | [MC-4](https://medmij.atlassian.net/browse/MC-4), [DOSINZAGE1-1041](https://medmij.atlassian.net/browse/DOSINZAGE1-1041) |
| Functional design           | Updated guidance on and links to the relevant transactions. | [DOSINZAGE1-1041](https://medmij.atlassian.net/browse/DOSINZAGE1-1041) |
| Technical design            | The cross-domain data services Alert, Blood pressure, Body height, Body temperature, Body weight, Fluid balance, Living situation, Nutrition advice, Payer, Pulse rate and Respiration have been updated to version 1.0.0-rc.3. | [MC-4](https://medmij.atlassian.net/browse/MC-4), [DOSINZAGE1-1041](https://medmij.atlassian.net/browse/DOSINZAGE1-1041) |
| FHIR artifacts              | The MedMij STU3 Core dependency has been updated to version 1.3.0. | [MC-4](https://medmij.atlassian.net/browse/MC-4), [DOSINZAGE1-1041](https://medmij.atlassian.net/browse/DOSINZAGE1-1041) |
| FHIR artifacts              | For each Logical Model and FHIR profile, the mappings have been added in the IG. Moreover, for each FHIR profile, (links to) the corresponding examples have been added in the IG. | [DOSINZAGE1-1015](https://medmij.atlassian.net/browse/DOSINZAGE1-1015) |
| FHIR artifacts              | The CapabilityStatements have been added to the Artifact index. | [DOSINZAGE1-1087](https://medmij.atlassian.net/browse/DOSINZAGE1-1087) |
| Granular data service index | The following granular data services have been updated: <br/> <ul> <li> Retrieve Long-term Healthcare - Encounter, version 1.0.0-beta.3 <ul> <li> The link to the functional model on ART-DECOR has been updated, which now includes the applicable cardinalities. <li> The FHIR profile mappings have been added. </ul> <li> Retrieve Long-term Healthcare - Nursing report, version 1.0.0-rc.3 <ul> <li> The explicit modeling of the HealthProfessional and HealthcareProvider within the Performer concept has been replaced by references to MedMij Core Logical Models. <li> The Logical Model and FHIR profile mappings have been added. </ul> | [DOSINZAGE1-1041](https://medmij.atlassian.net/browse/DOSINZAGE1-1041), [DOSINZAGE1-1087](https://medmij.atlassian.net/browse/DOSINZAGE1-1087) |
| Test material               | Several (incorrect) `.display`s of LOINC and SNOMED CT codes have been corrected, and translated to Dutch (if possible). | [DOSINZAGE1-1013](https://medmij.atlassian.net/browse/DOSINZAGE1-1013) |

## 1.0.0-rc.2

| Component                   | Description  | Ticket    |
| --------------------------- | ------------ | --------- |
| Functional design           | The cross-domain data services Alert, Blood pressure, Body height, Body temperature, Body weight, Fluid balance, Living situation, Nutrition advice, Payer, Pulse rate and Respiration have been updated to version 1.0.0-rc.2. | [DOSINZAGE1-986](https://medmij.atlassian.net/browse/DOSINZAGE1-986) |
| Technical design            | The cross-domain data services Alert, Blood pressure, Body height, Body temperature, Body weight, Fluid balance, Living situation, Nutrition advice, Payer, Pulse rate and Respiration have been updated to version 1.0.0-rc.2. | [DOSINZAGE1-986](https://medmij.atlassian.net/browse/DOSINZAGE1-986) |
| FHIR artifacts              | The MedMij STU3 Core dependency has been updated to version 1.2.1. | [DOSINZAGE1-986](https://medmij.atlassian.net/browse/DOSINZAGE1-986) |
| Granular data service index | The following granular data services have been updated: <br/> <ul> <li> Retrieve Long-term Healthcare - Encounter, version 1.0.0-beta.2 <ul> <li> The system roles have been updated to conform to the 30-character limit. </ul> <li> Retrieve Long-term Healthcare - Nursing report, version 1.0.0-rc.2 <ul> <li> The system roles have been updated to conform to the 30-character limit. </ul> | [DOSINZAGE1-987](https://medmij.atlassian.net/browse/DOSINZAGE1-987) |

## 1.0.0-rc.1

| Component                   | Description  | Ticket    |
| --------------------------- | ------------ | --------- |
| Functional design           | The cross-domain data services Alert, Blood pressure, Body height, Body temperature, Body weight, Fluid balance, Living situation, Nutrition advice, Payer, Pulse rate and Respiration have been updated to version 1.0.0-rc.1. | [DOSINZAGE1-915](https://medmij.atlassian.net/browse/DOSINZAGE1-915), [DOSINZAGE1-968](https://medmij.atlassian.net/browse/DOSINZAGE1-968) |
| Functional design           | The display guidelines has been updated. | [DOSINZAGE1-923](https://medmij.atlassian.net/browse/DOSINZAGE1-923) |
| Technical design            | The cross-domain data services Alert, Blood pressure, Body height, Body temperature, Body weight, Fluid balance, Living situation, Nutrition advice, Payer, Pulse rate and Respiration have been updated to version 1.0.0-rc.1. | [DOSINZAGE1-915](https://medmij.atlassian.net/browse/DOSINZAGE1-915), [DOSINZAGE1-968](https://medmij.atlassian.net/browse/DOSINZAGE1-968) |
| Technical design            | Guidance on both patient identification, and the relation between FHIR profiles and Logical Models, has been added. | [DOSINZAGE1-927](https://medmij.atlassian.net/browse/DOSINZAGE1-927) |
| FHIR artifacts              | The MedMij STU3 Core dependency has been updated to version 1.2.0. | [DOSINZAGE1-928](https://medmij.atlassian.net/browse/DOSINZAGE1-928) |
| Granular data service index | The following granular data services have been updated: <br/> <ul> <li> Retrieve Long-term Healthcare - Nursing report, version 1.0.0-rc.1 | [DOSINZAGE1-968](https://medmij.atlassian.net/browse/DOSINZAGE1-968) |
| Test material               | Several small errors in the test material have been corrected. | [DOSINZAGE1-924](https://medmij.atlassian.net/browse/DOSINZAGE1-924) |
| Test material               | The test material has been relocated to the IG. | [DOSINZAGE1-924](https://medmij.atlassian.net/browse/DOSINZAGE1-924) |

## 1.0.0-beta.2

| Component                   | Description  | Ticket    |
| --------------------------- | ------------ | --------- |
| Dataset                     | A Logical Model corresponding to the NursingReport information model has been added. | [DOSINZAGE1-809](https://medmij.atlassian.net/browse/DOSINZAGE1-809) |
| Functional design           | The domain-specific data services Encounter and Nursing report have been added. | [DOSINZAGE1-809](https://medmij.atlassian.net/browse/DOSINZAGE1-809) |
| Functional design           | The cross-domain data services Alert, Blood pressure, Body height, Body temperature, Body weight, Fluid balance, Living situation, Pulse rate and Respiration have been updated to version 1.0.0-beta.2. | [DOSINZAGE1-851](https://medmij.atlassian.net/browse/DOSINZAGE1-851), [DOSINZAGE1-875](https://medmij.atlassian.net/browse/DOSINZAGE1-875) |
| Functional design           | The display guideline (weergaverichtlijn) has been added to the functional design. | [DOSINZAGE1-786](https://medmij.atlassian.net/browse/DOSINZAGE1-786) |
| Technical design            | The domain-specific data services Encounter and Nursing report have been added. | [DOSINZAGE1-809](https://medmij.atlassian.net/browse/DOSINZAGE1-809) |
| Technical design            | The cross-domain data services Alert, Blood pressure, Body height, Body temperature, Body weight, Fluid balance, Living situation, Pulse rate and Respiration have been updated to version 1.0.0-beta.2. | [DOSINZAGE1-851](https://medmij.atlassian.net/browse/DOSINZAGE1-851), [DOSINZAGE1-875](https://medmij.atlassian.net/browse/DOSINZAGE1-875) |
| FHIR artifacts              | The profiles lz-Encounter, lz-NursingReport and ext-NursingReport.ReportTitle have been created and added to the IG. | [DOSINZAGE1-809](https://medmij.atlassian.net/browse/DOSINZAGE1-809) |
| FHIR artifacts              | CapabilityStatements for the domain-specific data services Encounter and Nursing report have been added. | [DOSINZAGE1-809](https://medmij.atlassian.net/browse/DOSINZAGE1-809) |
| FHIR artifacts              | The MedMij STU3 Core dependency has been updated to version 1.1.0. | [DOSINZAGE1-829](https://medmij.atlassian.net/browse/DOSINZAGE1-829) |
| Granular data service index | The following granular data services have been added: <br/> <ul> <li> Retrieve Long-term Healthcare - Encounter, version 1.0.0-beta.1 <li> Retrieve Long-term Healthcare - Nursing report, version 1.0.0-beta.1 | [DOSINZAGE1-809](https://medmij.atlassian.net/browse/DOSINZAGE1-809), [DOSINZAGE1-875](https://medmij.atlassian.net/browse/DOSINZAGE1-875) |
| Test material               | Test instances corresponding with the Encounter and NursingReport CIMs have been added. | [DOSINZAGE1-809](https://medmij.atlassian.net/browse/DOSINZAGE1-809) |
| Test material               | Several test instances corresponding to the Respiration CIM have been updated. Moreover, test instances corresponding to the AdministrationDevice concept have been added. | [DOSINZAGE1-851](https://medmij.atlassian.net/browse/DOSINZAGE1-851) |

## 1.0.0-beta.1

| Component             | Description  | Ticket    |
| --------------------- | ------------ | --------- |
| Functional design     | The cross-domain data services have been moved to the [MedMij STU3 Core IG](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index?version=1.0.0), while the domain-specific data services (i.e. Encounter and Nursing report) have been removed. | [DOSINZAGE1-806](https://medmij.atlassian.net/browse/DOSINZAGE1-806), [DOSINZAGE1-821](https://medmij.atlassian.net/browse/DOSINZAGE1-821) |
| Technical design      | The cross-domain data services have been moved to the [MedMij STU3 Core IG](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index?version=1.0.0), while the domain-specific data services (i.e. Encounter and Nursing report) have been removed. | [DOSINZAGE1-806](https://medmij.atlassian.net/browse/DOSINZAGE1-806), [DOSINZAGE1-825](https://medmij.atlassian.net/browse/DOSINZAGE1-825) |
| FHIR artifacts        | <ul> <li> The zib2017 dependency has been updated to 2.3.2. <li> A dependency on version 1.0.0 of MedMij STU3 Core has been added. | [DOSINZAGE1-825](https://medmij.atlassian.net/browse/DOSINZAGE1-825) |
| Test material         | The `.meta.tag`s corresponding to the care type have been added to all test instances. | [DOSINZAGE1-825](https://medmij.atlassian.net/browse/DOSINZAGE1-825) |
| Test material         | The test instances corresponding with the Encounter and NursingReport CIMs have been removed. | [DOSINZAGE1-825](https://medmij.atlassian.net/browse/DOSINZAGE1-825) |
| Test material         | The wrong `.system` for `.code` *MC* has been corrected in the Practitioner instance with `.id` *Practitioner-bglz-av-test-Pinxteren*. | [DOSINZAGE1-825](https://medmij.atlassian.net/browse/DOSINZAGE1-825) |
| Test material         | Several references that could not be resolved in the test material have been corrected. | [DOSINZAGE1-846](https://medmij.atlassian.net/browse/DOSINZAGE1-846) |

## 1.0.0-alpha.1

Initial version, intended for a Proof of Concept (PoC).