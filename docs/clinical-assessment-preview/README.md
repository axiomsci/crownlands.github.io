---
## Crownlands - Clinical Assessment and Outcomes Voice Data (Preview)
##### Audio from clinician-patient visits with structured interviews and clinician's assessment of the patient.
#### Training Goal: 
This dataset trains (voice) models on clinical interactions with patients and how physicians assess patient symptoms and behavior. Success on this task requires careful objective scoring of responses and holistic clinical judgement.

#### Contents:
Per call:
<table>
  <tr>
    <td>Speakers</td>
    <td>3 - doctor, patient, partner </td>
  </tr>
  <tr>
    <td>Duration</td>
    <td>1-2 hours</td>
  </tr>
  <tr>
    <td>Assessments</td>
    <td>3 - see below </td>
  </tr>
</table>


Each recording contains three clinical/cognitive assessments, conducted as structured interviews. Two of these tasks are **_scoring tasks_**, which have multiple yes/no/choice questions. The longest task is a **_clinical judgement task_**, which follows a structured interview but relies un the clinician's expert judgement to determine the final symptom rating.

Task medical details:
<details>
  <summary>Scoring Task A: <b>NPI-Q</b> </summary>
  This is the hidden text or content that drops down.
</details>

<details>
  <summary>Scoring Task B: <b>GDS</b> </summary>
  This is the hidden text or content that drops down.
</details>

<details>
  <summary>Clinical Judgement Task: <b>GDS</b> </summary>
  This is the hidden text or content that drops down.
</details>

#### Health Data Provenance and Privacy: 
This dataset contains de-identified data from real patients discussing their own cases with a physician. All data is shared safely and with patient consent. Crownlands cares about transparency of the data chain-of-custody. 

In this dataset, the human health data is "first-party" - meaning Crownlands sponsored and generated the data and is providing the data to users.

Per Crownlands policy, all users must agree not to attempt re-identification of the patients or speakers in order toef access the dataset.

```
HUMAN DATA PROVENANCE

Patient consent  .----. ___ .----.   Crownlands serves
in Crownlands   (     ()   ()     )  de-ID data
study            `----' ‾‾‾ `----'
```
