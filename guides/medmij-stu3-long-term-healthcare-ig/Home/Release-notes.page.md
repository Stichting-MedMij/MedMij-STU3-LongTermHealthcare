# {{page-title}}
 
## 1.0.0-beta.2
 
| Component             | Description  | Ticket    |
| --------------------- | ------------ | --------- |
| Functional design     | The cross-domain data service Respiration has been updated to version 1.0.0-beta.2. | [DOSINZAGE1-851](https://medmij.atlassian.net/browse/DOSINZAGE1-851) |
| Technical design      | The cross-domain data service Respiration has been updated to version 1.0.0-beta.2. | [DOSINZAGE1-851](https://medmij.atlassian.net/browse/DOSINZAGE1-851) |
| Test material         | Several test instances corresponding to the Respiration CIM have been updated. Moreover, test instances corresponding to the AdministrationDevice concept have been added. | [DOSINZAGE1-851](https://medmij.atlassian.net/browse/DOSINZAGE1-851) |

## 1.0.0-beta.1
 
| Component             | Description  | Ticket    |
| --------------------- | ------------ | --------- |
| Functional design     | The cross-domain data services have been moved to the [MedMij STU3 Core IG](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index?version=1.0.0), while the domain-specific data services (i.e. Encounter and Nursing Report) have been removed. | [DOSINZAGE1-806](https://medmij.atlassian.net/browse/DOSINZAGE1-806), [DOSINZAGE1-821](https://medmij.atlassian.net/browse/DOSINZAGE1-821) |
| Technical design      | The cross-domain data services have been moved to the [MedMij STU3 Core IG](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-Data-Service-Index?version=1.0.0), while the domain-specific data services (i.e. Encounter and Nursing Report) have been removed. | [DOSINZAGE1-806](https://medmij.atlassian.net/browse/DOSINZAGE1-806), [DOSINZAGE1-825](https://medmij.atlassian.net/browse/DOSINZAGE1-825) |
| FHIR artifacts        | <ul> <li> The zib2017 dependency has been updated to 2.3.2. <li> A dependency on version 1.0.0 of MedMij STU3 Core has been added. | [DOSINZAGE1-825](https://medmij.atlassian.net/browse/DOSINZAGE1-825) |
| Test material         | The `.meta.tag`s corresponding to the care type have been added to all test instances. | [DOSINZAGE1-825](https://medmij.atlassian.net/browse/DOSINZAGE1-825) |
| Test material         | The test instances corresponding with the Encounter and NursingReport CIMs have been removed. | [DOSINZAGE1-825](https://medmij.atlassian.net/browse/DOSINZAGE1-825) |
| Test material         | The wrong `.system` for `.code` *MC* has been corrected in the Practitioner instance with `.id` *Practitioner-bglz-av-test-Pinxteren*. | [DOSINZAGE1-825](https://medmij.atlassian.net/browse/DOSINZAGE1-825) |
| Test material         | Several references that could not be resolved in the test material have been corrected. | [DOSINZAGE1-846](https://medmij.atlassian.net/browse/DOSINZAGE1-846) |
 
## 1.0.0-alpha.1
 
Initial version, intended for a Proof of Concept (PoC).