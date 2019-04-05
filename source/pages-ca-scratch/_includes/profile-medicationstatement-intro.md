<!--- Text entered into this file will appear at the top of the profiles page before the Formal Views of the profile content. -->

This profile was generated from [HL7 StructureDefinition](https://www.hl7.org/fhir/medicationstatement.profile.json) on 2019-03-28 and constrained during a review of US Core against Canadian sources.

Key differences from [USCoreR4 MedicationStatement](https://build.fhir.org/ig/HL7/US-Core-R4/StructureDefinition-us-core-medicationstatement.html):
- MedicationStatement.medication updated:
  - CodeableConcept binding to ValueSet-prescriptionmedicinalproduct
  - Reference to profile-medication
- MedicationStatement.subject reference updated to profile-patient

**[ToDo]:**

[x] review USCoreR4 profile and draft extensions and restrictions

[] review structure against pan-CDN HL7 v3

[] review structure against existing CAD FHIR specs
- review against PrescribeIT and DHDR **<< outstanding**

[] review and update terminology bindings

[] add constraints (cross element) from USCoreR4

[] refine constraints (cross element) to CAD requirements ?

[] ?

{% include link-list.md %}