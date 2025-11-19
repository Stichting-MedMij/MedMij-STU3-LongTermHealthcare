---
topic: TO
---
 
# Technisch ontwerp 

## Introduction 

This Implementation Guide (IG) provides the technical specification of the Basic Long-term Healthcare Data Exchange+ (Dutch: Basisgegevens Langdurige Zorg+ or BgLZ+) standard based on a selection of Dutch Health Care Information Models. The “expansion” of the long-term information standard is in first instance focused on Health Care Information Models of the information standard minimal eOverdracht version 4.0. The information standard minimal eOverdracht as published by Nictiz does not yet include a patient use case, this may change in the future. Up until then, the patient use case will be published by MedMij under the definition of Basic Long-term Healthcare Data Exchange+.  

This IG is a technical counterpart of the functional design. The FHIR version used for this IG is HL7 FHIR STU3. This implementation guide assumes that the reader is familiar with this FHIR version.  

Apart from this document, the guidelines as specified in general FHIR Implementation Guide apply. In particular, the reader should take note of the Use case overarching principles.  

## Actors involved
| Actor | | System | | FHIR CapabilityStatement |
| --- | --- | --- | --- | --- | --- |
| **Name** | **Description** | **Name** | **Description** | **Name** | **Description** |
| Patient | The user of a personal healthcare environment | PHR | Personal health record | [CapabilityStatement Retrieve](http://medmij.nl/fhir/CapabilityStatement/lz-Retrieve) | FHIR client requirements |
| Healthcare provider | The user of a XIS | XIS | Healthcare information system | [CapabilityStatement Serve](http://medmij.nl/fhir/CapabilityStatement/lz-Serve) | FHIR server requirements |

## Boundaries and relationships 

This FHIR IG includes use cases for the exchange of the Basic Long-term Healthcare Data Exchange+ data between health care providers (e.g. nurses) and patients e.g. in a Personal Health Record setting (PHR). In this Implementation Guide we focus on exchange of healthcare data between an healthcare povider to a Personal Health Record (PHR) or in Dutch: persoonlijke gezondheidsomgeving or PGO.

This IG guide assumes that a PHR is able to connect with a XIS. It does not provide information on finding the right source system nor does it provide information about security. These infrastructure and interface specifications are described in the ['MedMij Afsprakenstelsel'](https://afsprakenstelsel.medmij.nl/).

The Basic Long-term Healthcare Data Exchange+ is overlapping with other standards such as the Basic Long-term Healthcare Data Exchange. The Basic Long-term Healthcare Data Exchange+ uses the same HCIM based FHIR profiles for exchanging information as used in other standards.

## Use cases 

The use cases in this IG are based as much as possible on the specifications described in the [Nictiz information standard Minimale eOverdracht](https://informatiestandaarden.nictiz.nl/wiki/MedMij:V2020.02/FHIR_BGLZ).

We are not using the infrastructure profiles since we do not transfer messages between healthcare providers. In this Implementation Guide we focus op exchange of healthcare data between an healthcare povider to a Personal Health Record (PHR) or in Dutch: persoonlijke gezondheidsomgeving or PGO.  
 
#### PHR: request Parameters

The PHR system requests the addditional data long-term care using individual search interactions. The addditional data long-term care consists of multiple FHIR resources with certain constraints. To obtain the patient's addditional data long-term care, the client can use multiple individual search operations based on specified search queries. The interactions are performed by an HTTP GET as shown: 

GET [base]/[type]{?[parameters]} 

The table below shows in the first four columns the  sections, the HCIMs that constitute those sections and the specific content of the addditional data long-term care. The last column shows the FHIR search queries to obtain the long-term care information. These queries and expected responses are based on StructureDefinitions listed in ([TO DO] link)

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
                    <th>ZIB NL</th>
                    <th>HCIM EN</th>
                    <th>FHIR Resource</th>
                    <th>FHIR Profile </th>
                    <th>Search URL</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>1</td>
                    <td>zib Betaler</td>
                    <td>Payer</td>
                    <td> Coverage </td>
                    <td> <a href="https://simplifier.net/resolve?target=simplifier&canonical=http://nictiz.nl/fhir/StructureDefinition/zib-Payer&scope=nictiz.fhir.nl.stu3.zib2017@2.2.18">Payer</a> </td>
                    <td class="monospace"> GET [base]/Coverage</td>
                </tr>
                <tr>
                    <td>2</td>
                    <td>zib Contact</td>
                    <td>Contact</td>
                    <td>Encounter</td>
                    <td><a href="https://simplifier.net/resolve?target=simplifier&canonical=http://nictiz.nl/fhir/StructureDefinition/eOverdracht-Encounter&scope=nictiz.fhir.nl.stu3.eoverdracht@4.0.0">Encounter</a> </td>
                    <td class="monospace">GET [base]/Encounter </td>
                </tr>
                <tr>
                    <td>3</td>
                    <td>zib Bloeddruk</td>
                    <td>BloodPressure </td>
                    <td>Observation</td>
                    <td><a href="https://simplifier.net/resolve?target=simplifier&canonical=http://nictiz.nl/fhir/StructureDefinition/zib-BloodPressure&scope=nictiz.fhir.nl.stu3.zib2017@2.2.18">BloodPressure</a> </td>
                    <td class="monospace">GET [base]/Observation?code=http://loinc.org|85354-9  </td>
                </tr>
                <tr>
                    <td>4</td>
                    <td>zib Lichaamsgewicht</td>
                    <td>BodyWeigth </td>
                    <td>Observation</td>
                    <td><a href="https://simplifier.net/resolve?target=simplifier&canonical=http://nictiz.nl/fhir/StructureDefinition/zib-BodyWeight&scope=nictiz.fhir.nl.stu3.zib2017@2.2.18">BodyWeight</a> </td>
                    <td class="monospace">GET [base]/Observation?code=http://loinc.org|29463-7  </td>
                </tr>
                <tr>
                    <td>5</td>
                    <td>zib Lichaamslengte</td>
                    <td>BodyHeight </td>
                    <td>Observation</td>
                    <td><a href="https://simplifier.net/resolve?target=simplifier&canonical=http://nictiz.nl/fhir/StructureDefinition/zib-BodyHeight&scope=nictiz.fhir.nl.stu3.zib2017@2.2.18">BodyHeight</a> </td>
                    <td class="monospace">GET [base]/Observation?code=http://loinc.org|8302-2 </td>
                </tr>
                <tr>
                    <td>6</td>
                    <td>zib Alert</td>
                    <td>Alert</td>
                    <td>Flag</td>
                    <td><a href="https://simplifier.net/resolve?target=simplifier&canonical=http://nictiz.nl/fhir/StructureDefinition/zib-Alert&scope=nictiz.fhir.nl.stu3.zib2017@2.2.18">Alert</a> </td>
                    <td class="monospace">GET [base]/Flag </td>
                </tr>
                <tr>
                    <td>7</td>
                    <td>zib Woonsituatie</td>
                    <td>LivingSituation</td>
                    <td>Observation</td>
                    <td><a href="https://simplifier.net/resolve?target=simplifier&canonical=http://nictiz.nl/fhir/StructureDefinition/zib-LivingSituation&scope=nictiz.fhir.nl.stu3.zib2017@2.2.18">LivingSituation</a> </td>
                    <td class="monospace">GET [base]/Observation?code=http://snomed.info/sct|365508006 </td>
                </tr>
                <tr>
                    <td>8</td>
                    <td>zib Voedingsadvies</td>
                    <td>NutritionAdvice </td>
                    <td>NutritionOrder</td>
                    <td><a href="https://simplifier.net/resolve?target=simplifier&canonical=http://nictiz.nl/fhir/StructureDefinition/zib-NutritionAdvice&scope=nictiz.fhir.nl.stu3.zib2017@2.2.18">NutritionAdvice</a> </td>
                    <td class="monospace">GET [base]/NutritionOrder </td>
                </tr>
                    <tr>
                    <td>9</td>
                    <td>zib Lichaamstemperatuur</td>
                    <td> BodyTemperature</td>
                    <td>Observation</td>
                    <td><a href="https://simplifier.net/packages/nictiz.fhir.nl.stu3.zib2017/2.2.18/files/2317151">BodyTemperature</a> </td>
                    <td class="monospace">GET [base]/Observation?code=http://loinc.org|8310-5 </td>
                </tr>
                <tr>
                    <td>10</td>
                    <td>zib Vochtbalans</td>
                    <td>FluidBalance </td>
                    <td>Observation</td>
                    <td><a href="https://simplifier.net/packages/nictiz.fhir.nl.stu3.zib2017/2.2.18/files/2317199">FluidBalance</a> </td>
                    <td class="monospace">GET [base]/Observation?code=http://snomed.info/sct|364396009 </td>
                </tr>
                <tr>
                    <td>11</td>
                    <td>zib Ademhaling</td>
                    <td>Respiration </td>
                    <td>Observation</td>
                    <td><a href="https://simplifier.net/packages/nictiz.fhir.nl.stu3.zib2017/2.2.18/files/2317350">Respiration</a> </td>
                    <td class="monospace">GET [base]/Observation?code=http://snomed.info/sct|422834003</td>
                </tr>
                    <tr>
                    <td>12</td>
                    <td>zib Polsfrequentie</td>
                    <td>PulseRate </td>
                    <td>Observation</td>
                    <td><a href="https://simplifier.net/packages/nictiz.fhir.nl.stu3.zib2017/2.2.18/files/2317348">PulseRate</a> </td>
                    <td class="monospace">GET [base]/Observation?code=http://loinc.org|8893-0 </td>
                </tr>
                    <tr>
                    <td>13</td>
                    <td>CIM Dagrapportage</td>
                    <td>Nursing Report </td>
                    <td>Observation</td>
                    <td><a href="https://simplifier.net/anw/nl-core-nursingreport">Nursing Report</a> </td>
                    <td class="monospace">GET [base]/Observation?code=http://snomed.info/sct|11591000146107</td>
                </tr>
                </tr>
            </tbody>
        </table>
    </body>
</html>