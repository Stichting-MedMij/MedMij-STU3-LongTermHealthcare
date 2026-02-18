---
topic: FHIRProfilesIndex
---

# FHIR profiles
## Profiling guidelines
- The [Nictiz Profiling Guidelines for FHIR STU3](https://informatiestandaarden.nictiz.nl/wiki/FHIR:V1.0_FHIR_Profiling_Guidelines_STU3) have been used as guidelines for creating the profiles.
- The (element) descriptions present in the profiles are taken from the respective Logical Model the mapped concept originates from.
- The ['open world' modeling](https://informatiestandaarden.nictiz.nl/wiki/FHIR:V1.0_FHIR_Profiling_Guidelines_STU3#Open_vs._Closed_Modeling) approach is adopted as much as possible. Notable exceptions are cardinalities that have been restricted based on the functional dataset of the MedMij use case, such as several minimum cardinalities.

## Other profiles
FHIR STU3 conformance resources developed by Nictiz (based on zib publication 2017) from the [zib2017 2.3.2 package](https://simplifier.net/packages/nictiz.fhir.nl.stu3.zib2017/2.3.2) are used and referenced where possible. In particular, the zibs and corresponding nl-core profiles collected in the table below are used.

| Zib | FHIR resource/data type | FHIR profile |
| --- | --- | --- |
| [Patient](https://zibs.nl/wiki/Patient-v3.1(2017EN)) | Patient | [nl-core-patient](https://simplifier.net/resolve?canonical=http://fhir.nl/fhir/StructureDefinition/nl-core-patient&scope=nictiz.fhir.nl.stu3.zib2017@2.3.2) |
| [HealthProfessional](https://zibs.nl/wiki/HealthProfessional-v3.2(2017EN)) | PractitionerRole <br/> Practitioner | [nl-core-practitionerrole](https://simplifier.net/resolve?canonical=http://fhir.nl/fhir/StructureDefinition/nl-core-practitionerrole&scope=nictiz.fhir.nl.stu3.zib2017@2.3.2) <br/> [nl-core-practitioner](https://simplifier.net/resolve?canonical=http://fhir.nl/fhir/StructureDefinition/nl-core-practitioner&scope=nictiz.fhir.nl.stu3.zib2017@2.3.2) |
| [HealthcareProvider](https://zibs.nl/wiki/HealthcareProvider-v3.1.1(2017EN)) | Organization | [nl-core-organization](https://simplifier.net/resolve?canonical=http://fhir.nl/fhir/StructureDefinition/nl-core-organization&scope=nictiz.fhir.nl.stu3.zib2017@2.3.2) |

**Table 1: Relevant nl-core profiles**