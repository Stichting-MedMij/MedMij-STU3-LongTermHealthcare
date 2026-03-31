---
topic: GranularDataServiceIndex
---

# Granular data service index

This index contains all active domain-specific granular data services within Long-term Healthcare. The following is specified for each data service:

- **Overview**
    - **Id** - the id of the data service that is used to uniquely define it in the [MedMij Catalogus](https://catalogus.medmij.nl/overzicht/actueel/actuele-catalogus).
    - **Data service name without version** - the name of the data service, both in English and Dutch, of which the Dutch one, appended with the data service version, is used in the MedMij Catalogus.
    - **Data service version** - the version assigned to the data service as a whole (not to be confused with the version of the corresponding functional model or the package version of the corresponding FHIR profiles).
    - **System role(s)** - the system roles corresponding to the different transactions within each data service. Each system is of the form 'LZ-[CIM abbreviation]\[Transaction indicator\](-[Suffix])-[Data service version]-FHIR', where:
        - 'LZ' refers to Long-term Healthcare (Dutch: Langdurige Zorg);
        - the CIM abbreviation consists of exactly two capital letters indicating the English name of the CIM;
        - the Suffix is an optional addition, and is described in more detail [here](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-exchange?version=1.1.1#PublicationGranularDataServices);
        - the Transaction indicator is either 'R' or 'B', indicating a Retrieve (Dutch: Raadplegen) or Serve (Dutch: Beschikbaar stellen) transaction, respectively. The former transaction is intended for the PHR, while the latter is relevant for the XIS. As the corresponding transaction (group) can be derived from the system role, the transactions and transaction groups are not specified on the respective data service pages. Instead, these can be found in the [MedMij Catalogus](https://catalogus.medmij.nl/overzicht/actueel/actuele-catalogus).
    - **Used in Implementation Guide(s)** - the IGs (and corresponding domains) in which the granular data service is used, which is always *Long-term Healthcare* in this IG.
- **Functional model**
    - **CIM** - the underlying Clinical Information Model, which is often a zib.
    - **Functional version** - the version of the CIM. For a CIM that is a zib, this version is of the form '*x.y*([zib publication])', e.g. '3.1(2017)'. For CIMs that are defined by MedMij as a Logical Model, the version of the corresponding FHIR package is suitable as the functional version.
    - Moreover, either a link to the functional model in ART-DECOR, or a Logical Model is included in this section.
- **Technical specification**
    - **FHIR profile(s)** - the FHIR profiles that are used to exchange the CIM.
    - **FHIR package** - the FHIR package in which the FHIR profiles have been published.
    - **FHIR version** - the version of FHIR in which the profiles corresponding to the CIM have been created, which is always *STU3* in this IG.
    - **Search request** - the request to be executed by the PHR to retrieve the data corresponding to the granular data service.
    - **Must Support** - the elements that have to be supported in the manner described [here](https://simplifier.net/guide/medmij-stu3-core-ig/Home/Granular-exchange?version=1.1.1#MustSupport).
    - **CapabilityStatement(s)** - the FHIR CapabilityStatements that describe the minimal requirements for a client or server to fulfill the corresponding transaction(s) defined within the data service.
    - Moreover, the relevant FHIR profiles are added in this section.