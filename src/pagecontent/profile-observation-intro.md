# CA Core Observation Profile
This Observation profile sets minimum expectations for the Observation resource to [TBC]

This profile defines core localisation concepts for use in an Canadian context.

## Mandatory Data Elements
All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.

Most elements in FHIR specification have a minimum cardinality of **0**, which means that they may be missing from a resource when it is exchanged between systems.

**Required elements:**
* category
* code
* reference to a subject

### Data Absent Reason
In situations where the minimum cardinality of an element or attribute is 1 and information is missing and the Responder knows the precise reason for the absence of data, Responders SHALL send the reason for the missing information using values (such as [NullFlavor](https://www.hl7.org/fhir/extension-iso21090-nullflavor.html)) from the value set where they exist or using the [DataAbsentReason](http://hl7.org/fhir/StructureDefinition/data-absent-reason) extension.

In addition to that an Observation without a value SHALL include a reason why the data is absent unless there are component observations or references to other Observations that are grouped within it. I.e., either _Observation.value_ or _Observation.dataAbsentReason_ SHALL be present.

## Must Support Data Elements
Some elements are labeled as MustSupport meaning that implementations that produce or consume resources SHALL provide "support" for the element in some meaningful way (see [Must Support](https://build.fhir.org/ig/scratch-fhir-profiles/CA-Core/general-guidance.html#must-support) definition).

Following elements are marked as Must Support in the Canadian Patient profile to aid record matching in databases with many pediatric records.

**Must Support elements:**
* category
* code
* reference to a subject
* effective data
* value
* dataAbsentReason	

## Usage Note

**Profile specific implementation guidance**

* Additional codes that translate or map to the Observation code or category codes are allowed (see [CodeableConcept](http://hl7.org/fhir/R4/datatypes.html#CodeableConcept) data type). 
For example: providing both a local code and LOINC code providing a more specific category codes, SNOMED CT concept, or system specific codes.
