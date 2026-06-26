## Crownlands - Clinical Assessment and Outcomes Voice Data (Preview)
##### Audio from clinician-patient visits with structured interviews → clinician's assessment of the patient.

**What to know:** This dataset is a trove of long-duration patient visits where a doctor assesses a patient's health in a structured way. Along with medical conversation, these interactions have hard outcomes. In clinical trials and in patient care, clinical scoring systems are used to standardize disease staging and measure longitudinal progression. This dataset contains recorded visits of a physician scoring patients on these metrics. This is a task that should be trained - correct measurement requires the application of clinical judgement. These cognitive assessments are a near-term step towards AI doctors assessing and diagnosing patients. 

**Training Goal:** This dataset trains (voice) models on clinical conduct with patients and how physicians assess patient symptoms and behavior. Improvement on the clinical assessment task requires careful objective scoring of responses and holistic clinical judgement.

#### Contents:
During each available clinical visit:

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

Per Crownlands policy, all users must agree not to attempt re-identification of the patients or speakers in order to access the dataset.


```
HUMAN DATA PROVENANCE

Patient consent  .----. ___ .----.   Crownlands serves
in Crownlands   (     ()   ()     )  de-ID data
study            `----' ‾‾‾ `----'
```
