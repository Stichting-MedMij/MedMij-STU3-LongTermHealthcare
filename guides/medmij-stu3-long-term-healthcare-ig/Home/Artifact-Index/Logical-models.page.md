---
topic: LM
---

# Logical Models

Logical Models represent data structures, and contain data elements and their constraints and relationships. They allow data requirements to be described from a functional perspective. In this IG, the functional dataset and the underlying use cases are represented by [FHIR Logical Models](https://build.fhir.org/logical.html) (only for the information models that are not yet present in ART-DECOR). These use FHIR to capture the data structures (namely by specifying a [StructureDefinition](https://hl7.org/fhir/STU3/structuredefinition.html) and underlying [ElementDefinitions](https://hl7.org/fhir/STU3/elementdefinition.html), for each data structure), but they are not (directly) attached to FHIR resources.

- The Logical Models corresponding to the dataset, which we will refer to as *base Logical Models*, contain all functional concepts, including corresponding datatype, terminology binding (if applicable) and an id.
  - For each concept, an id is assigned by MedMij. These ids are also added as mappings in the FHIR profiles (provided these are maintained by MedMij), and therefore form the linking pin between Logical Models and FHIR profiles.
  - For each concept it is indicated whether it is repeating (i.e. by setting its maximum cardinality to `1` or `*`).
  - The [FHIR datatypes](https://hl7.org/fhir/STU3/datatypes.html) are used in the Logical Models, even though these might bring 'physical' constraints, formats, etc. into the abstract logical data models which are not intended or applicable on the logical level. For instance, elements of the Attachment datatype need to satisfy the *att-1* constraint, which states that the element SHALL have a `contentType`, provided the element has non-empty `data`. Even though this constraint makes sense on a technical level, the aforementioned attributes `contentType` and `data` are not present in a logical data model. Therefore, such constraints may be 'ignored' in the Logical Models; instead, these constraints are taken into account in the corresponding FHIR profiles.
- The Logical Models corresponding to a use case are derived from the base Logical Models, and are therefore called *derived Logical Models*.
  - These indicate which concepts are (conditionally) required in the respective use case by setting the minimum cardinality to `1` (or adding a constraint which specifies when the concept is required).
  - All concepts from the dataset that are part of the use case are indicated with a so-called *Must Support* flag. Systems that exchange data in the context of the respective use case SHALL be able to convey these concepts. Concepts in the derived Logical Model that are not flagged in this way are technically not part of the use case, but MAY be conveyed in the context of that use case, nonetheless. Note that, strictly speaking, [the Must Support flag is prohibited in type definitions](https://hl7.org/fhir/STU3/elementdefinition.html#interpretation). However, [it is yet unclear whether this applies to (derived) Logical Models](https://chat.fhir.org/#narrow/channel/215610-shorthand/topic/Logical.20Models.20and.20not.20permitting.20MustSupport.20flag). Since we are mainly interested in a clear and concise way of depicting the functional model, we still opted to use this flag (instead of e.g. using extensions).

Base Logical Models and derived Logical Models can (also) be distinguished from each other by the value of `.abstract`, as this element attains the value *true* and *false* for these Logical Models, respectively.

## Dataset
### NursingReport
<tabs>
    <tab title="Tree view" active="true">
      {{tree:http://medmij.nl/fhir/StructureDefinition/nl-core-lm-NursingReport, buttons}}
    </tab>
    <tab title="Xml">
      {{xml:http://medmij.nl/fhir/StructureDefinition/nl-core-lm-NursingReport}}
    </tab>
    <tab title="Json">
      {{json:http://medmij.nl/fhir/StructureDefinition/nl-core-lm-NursingReport}}
    </tab>
</tabs>