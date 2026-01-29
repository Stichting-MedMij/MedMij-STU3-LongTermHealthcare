---
topic: TO
---
 
# Technical design

## Introduction 

This Implementation Guide (IG) provides the technical specification of the Basic Long-term Healthcare Data Exchange+ (Dutch: Basisgegevens Langdurige Zorg+ or BgLZ+) standard based on a selection of Dutch Health Care Information Models. 

This IG is positioned on top of [MedMij STU3 Core](https://simplifier.net/medmij-stu3-core). MedMij STU3 Core is the generic layer defined by MedMij which forms a foundation for all data services that are exchanged in FHIR STU3. It contains guidance and requirements on data service–overarching topics, such as granular exchange and Logical Models, and may contain FHIR artifacts that are relevant for multiple data services. In particular, MedMij STU3 Core contains granular, domain-overarching Clinical Information Models (CIM) that are reused across multiple domains.

The “expansion” of the long-term information standard is in first instance focused on Health Care Information Models of the information standard minimal eOverdracht version 4.0. The information standard minimal eOverdracht as published by Nictiz does not yet include a patient use case, this may change in the future. Up until then, the patient use case will be published by MedMij under the definition of Basic Long-term Healthcare Data Exchange+.  

This IG is a technical counterpart of the functional design. The FHIR version used for this IG is HL7 FHIR STU3. This implementation guide assumes that the reader is familiar with this FHIR version.  

Apart from this document, the guidelines as specified in general FHIR Implementation Guide apply. In particular, the reader should take note of the Use case overarching principles.  

## Actors involved 

|Actors||Systems||FHIR Capability Statements| 
| 
|Name|Description|Name|Description|Description| 
|Patient|The user of a personal healthcare environment|PHR (Document Consumer)|Personal health record|FHIR client requirements|
|Healthcare provider|The user of a XIS|XIS (Document Responder)|Healthcare information system|FHIR server requirements|

## Boundaries and relationships 

This FHIR IG includes use cases for the exchange of the Basic Long-term Healthcare Data Exchange+ data between health care providers (e.g. nurses) and patients e.g. in a Personal Health Record setting (PHR). In this Implementation Guide we focus on exchange of healthcare data between an healthcare povider to a Personal Health Record (PHR) or in Dutch: persoonlijke gezondheidsomgeving or PGO.

This IG guide assumes that a PHR is able to connect with a XIS. It does not provide information on finding the right source system nor does it provide information about security. These infrastructure and interface specifications are described in the ['MedMij Afsprakenstelsel'](https://afsprakenstelsel.medmij.nl/).

The Basic Long-term Healthcare Data Exchange+ is overlapping with other standards such as the [Basic Long-term Healthcare Data Exchange](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.02/OntwerpLangdurigeZorg). The Basic Long-term Healthcare Data Exchange+ uses the same Health Care Information Model (HCIM) based FHIR profiles for exchanging information as used in other standards.


## Use case: Retrieve BgLZ+ information

In this IG, BgLZ+ is provided as a combination of (1) the existing BgLZ exchange, which remains unchanged, and (2) granular exchange of an additional set of data services. Granular exchange allows the PHR to retrieve individual data services that are part of BgLZ+ through targeted search interactions, in accordance with the generic guidance and profiles defined in [MedMij STU3 Core](https://simplifier.net/medmij-stu3-core).

For BgLZ+, the following data services are added for granular exchange:
| data services| 
| --- | 
| [MedMij Core - Patient]{https://simplifier.net/guide/medmij-stu3-core-develop-ig/Home/Granular-Data-Service-Index/MedMij-Core-Patient.page.md?version=current} |
| [MedMij Core - Healthcare provider]{https://simplifier.net/guide/medmij-stu3-core-develop-ig/Home/Granular-Data-Service-Index/MedMij-Core-HealthcareProvider.page.md?version=current} | 
| [MedMij Core - Health professional]{} | 
| [MedMij Core - Blood pressure]{} | 
| [MedMij Core - Body weight]{} | 
| [MedMij Core - Body height]{} | 
| [MedMij Core - Alert]{} | 
| [MedMij Core - Nutrition advice]{} | 
| [MedMij Core - Body temperature]{} | 
| [MedMij Core - Fluid balance]{} | 
| [MedMij Core - Respiration]{} | 
| [MedMij Core - Pulse rate]{} | 
| [MedMij Core - Payer]{} | 
| [Long-term Healthcare - Nursing report]{} | 
| [Long-term Healthcare - Encounter]{} | 
 
#### PHR: request Parameters

For the domain-overarching data services, the request parameters are defined in [MedMij STU3 Core](https://simplifier.net/medmij-stu3-core). This Long-term Healthcare IG only specifies additional guidance for the domain-specific data services, such as the Nursing Report and Encounter. The PHR retrieves the FHIR resources using an individual search interaction. The Nursing Report is represented as a FHIR resources with specific constraints. To obtain a patient’s Nursing Report data, the client performs a search operation using the specified query parameters, executed as an HTTP GET:

GET [base]/[type]{?[parameters]} 

The table below shows in the first four columns the  sections, the CIM that constitute those sections and the specific content of the addditional data long-term care. The last column shows the FHIR search queries to obtain the information. These queries and expected responses are based on StructureDefinitions listed in ([TO DO] link)

#### XIS: Response message
The returned data to the PHR should conform to the profiles listed in the table below.

<!DOCTYPE html>
<html lang="nl">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Nette Tabel</title>
        <style>
            table {
                width: 100%;
                border-collapse: collapse;
            }
            th, td {
                border: 1px solid #ddd;
                padding: 8px;
                text-align: left;
            }
            th {
                background-color: #f4f4f4;
            }
            .monospace {
                font-family: monospace;
                font-size: 12px;
            }
        </style>
    </head>
    <body>
        <table>
            <thead>
                <tr>
                    <th>Section</th>
                    <th>CIM</th>
                    <th>CIM EN</th>
                    <th>FHIR Resource</th>
                    <th>FHIR Profile </th>
                    <th>Search URL</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <tr>
                    <td>?</td>
                    <td>CIM Dagrapportage</td>
                    <td>Nursing Report </td>
                    <td>Observation</td>
                    <td><a href="https://simplifier.net/anw/nl-core-nursingreport">Nursing Report</a> </td>
                    <td class="monospace">GET [base]/Observation?code=http://snomed.info/sct|11591000146107</td>
                </tr>
                <tr>
                    <td>?</td>
                    <td>zib Contact</td>
                    <td>Contact</td>
                    <td>Encounter</td>
                    <td><a href="https://simplifier.net/resolve?target=simplifier&canonical=http://nictiz.nl/fhir/StructureDefinition/eOverdracht-Encounter&scope=nictiz.fhir.nl.stu3.eoverdracht@4.0.0">Encounter</a> </td>
                    <td class="monospace">GET [base]/Encounter </td>
                </tr>
            </tbody>
        </table>
    </body>
</html>