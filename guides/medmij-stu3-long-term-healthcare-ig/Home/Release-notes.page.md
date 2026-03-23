# {{page-title}}

## 1.0.0-rc.1

| Component              | Description  | Ticket    |
| ---------------------- | ------------ | --------- |
| Technical design       | Guidance on both patient identification, and the relation between FHIR profiles and Logical Models, has been added. | [DOSINZAGE1-927](https://medmij.atlassian.net/browse/DOSINZAGE1-927) |
| FHIR artifacts         | The MedMij STU3 Core dependency has been updated to version 1.1.1. | [DOSINZAGE1-928](https://medmij.atlassian.net/browse/DOSINZAGE1-928) |

## 1.0.0-beta.2

| Component              | Description  | Ticket    |
| ---------------------- | ------------ | --------- |
| Dataset                | A Logical Model corresponding to the NursingReport information model has been added. | [DOSINZAGE1-809](https://medmij.atlassian.net/browse/DOSINZAGE1-809) |
| Functional design      | The domain-specific data services Encounter and Nursing report have been added. | [DOSINZAGE1-809](https://medmij.atlassian.net/browse/DOSINZAGE1-809) |
| Functional design      | The cross-domain data services Alert, Blood pressure, Body height, Body temperature, Body weight, Fluid balance, Living situation, Pulse rate and Respiration have been updated to version 1.0.0-beta.2. | [DOSINZAGE1-851](https://medmij.atlassian.net/browse/DOSINZAGE1-851), [DOSINZAGE1-875](https://medmij.atlassian.net/browse/DOSINZAGE1-875) |
| Functional design      | The display guideline (weergaverichtlijn) has been added to the functional design. | [DOSINZAGE1-786](https://medmij.atlassian.net/browse/DOSINZAGE1-786) |
| Technical design       | The domain-specific data services Encounter and Nursing report have been added. | [DOSINZAGE1-809](https://medmij.atlassian.net/browse/DOSINZAGE1-809) |
| Technical design       | The cross-domain data services Alert, Blood pressure, Body height, Body temperature, Body weight, Fluid balance, Living situation, Pulse rate and Respiration have been updated to version 1.0.0-beta.2. | [DOSINZAGE1-851](https://medmij.atlassian.net/browse/DOSINZAGE1-851), [DOSINZAGE1-875](https://medmij.atlassian.net/browse/DOSINZAGE1-875) |
| FHIR artifacts         | The profiles lz-Encounter, lz-NursingReport and ext-NursingReport.ReportTitle have been created and added to the IG. | [DOSINZAGE1-809](https://medmij.atlassian.net/browse/DOSINZAGE1-809) |
| FHIR artifacts         | CapabilityStatements for the domain-specific data services Encounter and Nursing report have been added. | [DOSINZAGE1-809](https://medmij.atlassian.net/browse/DOSINZAGE1-809) |
| FHIR artifacts         | The MedMij STU3 Core dependency has been updated to version 1.1.0. | [DOSINZAGE1-829](https://medmij.atlassian.net/browse/DOSINZAGE1-829) |
| Granular data services | The data services Encounter and Nursing report have been added. | [DOSINZAGE1-809](https://medmij.atlassian.net/browse/DOSINZAGE1-809), [DOSINZAGE1-875](https://medmij.atlassian.net/browse/DOSINZAGE1-875) |
| Test material          | Test instances corresponding with the Encounter and NursingReport CIMs have been added. | [DOSINZAGE1-809](https://medmij.atlassian.net/browse/DOSINZAGE1-809) |
| Test material          | Several test instances corresponding to the Respiration CIM have been updated. Moreover, test instances corresponding to the AdministrationDevice concept have been added. | [DOSINZAGE1-851](https://medmij.atlassian.net/browse/DOSINZAGE1-851) |

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