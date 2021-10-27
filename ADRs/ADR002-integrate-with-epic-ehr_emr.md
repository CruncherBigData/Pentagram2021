# ADR_002: Integrate with Epic EHR/EMR API to pull Farmacy Family EMR data


# Status:
Proposed


# Rationale:
EPIC EMR API adheres to the latest standards and has a free tier that will allow us to pull data from EPIC EMR. EPIC is one of the largest EHR in the US. The free tier allows access to the following data

- Observation (Vitals) — all the vital signs
- Observation (Labs) — lab test results
- DiagnosticReport — for example, results of MRI scans in the form of radiologist reports (images per se are not included)
- DocumentReference (Clinical Notes) — notes by nurses, physicians, or other healthcare professionals
- Binary (Clinical Notes) — part of DocumentReference
- MedicationRequest — lists prescribed medications
- Device — describes information about implantable medical devices
- AllergyIntolerance — info about the patient’s allergy or intolerance to a specific substance
- Condition – patient data from problem list records
- Procedure – surgeries, endoscopies, biopsies, counseling, physiotherapy, etc.
- Patient — demographics, care providers, and other administrative information about a patient
- Immunization — info about vaccine and vaccine administration details

This has all the data a dietician could require to provide guidance on diet changes. However, the following are the drawbacks

1. This is a one way action. We cannot push data back. So if a dietician wanted to order more tests this is not going to allow that

2. The patient needs to have an EPIC ID (unique ID) 

The communication via messages will have to be outside of this


# Decision


# Consequences
