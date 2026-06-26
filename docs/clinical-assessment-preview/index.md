---
layout: bare
browser_title: Crownlands - Clinical Assessment and Outcomes Voice Data (Preview)
permalink: /docs/clinical-assessment-preview/
---

# Crownlands - Clinical Assessment and Outcomes Voice Data (Preview)
<h5>Audio from clinician-patient visits with structured interviews → clinician's assessment of the patient.</h5>

**What to know:** This dataset is a trove of long-duration patient visits where a doctor assesses a patient's health in a structured way. Along with real-world medical conversation, these interactions have hard outcomes. In patient care and in clinical trials, clinical scoring systems are used to standardize diagnostic staging and measure longitudinal progression. This dataset contains recorded visits where a physician scores patients on these metrics. This is a task that should be trained - correct measurement requires the application of clinical judgement, and the administration and grading of these cognitive assessments are near-term steps towards AI doctors holistically diagnosing patients. 

**Training Goal:** This dataset trains (voice) models on clinical conduct with patients and how physicians assess patient symptoms and behavior. Improvement on the clinical assessment task requires careful objective scoring of responses and holistic clinical judgement.

#### In this dataset preview:
With each available clinical visit:

<table>
  <tr>
    <td>Three speakers: doctor, patient, caregiver </td>
  </tr>
  <tr>
    <td>1-2 hours duration per visit</td>
  </tr>
  <tr>
    <td>Three clinical assessments: see below </td>
  </tr>
</table>


Each recording contains three clinical/cognitive assessments, conducted as structured interviews. Two of these tasks are **_scoring tasks_**, which have multiple yes/no/choice questions. The longest task is a **_clinical judgement task_**, which follows a structured interview but relies un the clinician's expert judgement to determine the final symptom rating.

Sample medical assessment details:

<details>
  <summary>Scoring Task A: <b>NPI-Q</b> </summary>
  The Neuropsychiatric Inventory Questionnaire (NPI-Q) is a brief, informant-based tool used by clinicians to assess behavioral and psychological symptoms in patients with dementia and evaluate caregiver distress.<br><br>
  The NPI-Q asks the <i>informant</i> (the patient's caregiver) about 12 symptoms. Each is either rated absent (No), or present (Yes), in which case its severity is rated on a 3-point scale and the caregiver's distress is rated on a 5-point scale.<br><br>
  The NPI-Q takes 3-8 minutes to administer.
</details>

<details>
  <summary>Scoring Task B: <b>GDS</b> </summary>
  The Geriatric Depression Scale (GDS) is a self-report screening tool to identify depressive symptoms in older adults.<br><br>
  The GDS is 15 yes or no questions. Elaboration isn't required, but since these are real clinical visits, patients often volunteer descriptions or thought processes.<br><br>
  The GDS takes 2-3 minutes to administer.
</details>

<details>
  <summary>Clinical Judgement Task: <b>CDR</b> </summary>
  The Clinical Dementia Rating (CDR) Scale stages dementia and Alzheimer's disease. It is the primary outcome measurement in most late-stage clinical trials of Alzheimer's disease therapeutics.<br><br>
  The CDR requires a trained clinician to administer, interpret, and score. It is conducted in a structured interview with the patient and the <i>informant</i> (the patient's caregiver). It follows a standardized format but the clinician asks follow-up questions or changes the flow based on the conversation. The notetaking standard has ~100 fields, including yes/no, likert questions, and short written notes.<br><br>
  Clinical judgement is used to turn these interviews into a final score, which uses a 6-category rubric. For example, "Memory" is rated 0 for "No memory loss, or slight inconsistent forgetfulness," 0.5 for "Consistent slight forgetfulness; partial recollection of events; "benign" forgetfulness," ..., 2 for "Severe memory loss; only highly learned material retained; new material rapidly lost," and 3 for "Severe memory loss; only fragments remain." You can see the rubric (here)[https://knightadrc.wustl.edu/app/uploads/2021/06/CDR-Table.pdf]. These six scores or "boxes" can be converted into a final score, for example with a sum (sum of boxes, CDR-SB).<br><br>
  The CDR takes 50-75 minutes to administer. 
</details>


#### Sample Download:
The preview sample includes nine scored clinical assessments across three patients, with one complete, de-identified clinical visit recording per patient. Each recording includes audio. Timestamped transcripts with tracked speaker labels are included where available, but the full transcript and speaker attribution are not guaranteed.

Sample cases:

| Full Visit | Duration | Assessments |
| --- | --- | --- |
| case_714 | 166.2 min / 2.77 hr | Three |
| case_754 | 145.5 min / 2.42 hr | Three |
| case_214 | 117.3 min / 1.96 hr | Three |

Each assessment is conducted and scored by a highly trained, experienced physician, with ground truth available for every assessment.

The sample is delivered as a data file, available after a privacy agreement, and a Python evaluation package. In the evaluation package, audio and transcripts can be subsegmented by assessment task and scored against ground truth. Onboarding data is available separately.

Please contact your organization's point of contact with Crownlands if you do not have the org-specific download link.


#### Health Data Provenance and Privacy: 
This dataset contains de-identified data from real patients discussing their own cases with a physician. All data is shared safely and with patient consent. Crownlands cares about transparency of the data chain-of-custody. 

In this dataset, the human health data is "first-party" - meaning Crownlands sponsored and generated the data and is providing the data to users.

Per Crownlands policy, all users must agree not to attempt re-identification of the patients or speakers in order to access the dataset.


<pre><code>
HUMAN DATA PROVENANCE

Patient consent  .----. ___ .----.   Crownlands serves
in Crownlands   (     ()   ()     )  de-ID data
study            &#96;----' ‾‾‾ &#96;----'
</code></pre>
