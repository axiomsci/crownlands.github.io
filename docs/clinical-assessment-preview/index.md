---
layout: bare
browser_title: Crownlands - Clinical Assessment and Outcomes Voice Data (Preview)
permalink: /docs/clinical-assessment-preview/
---

# Crownlands - Clinical Assessment and Outcomes Voice Data (Preview)
<h5>Long-form clinician-patient-caregiver visits with physician-scored clinical outcomes.</h5>

This dataset preview is designed for AI labs evaluating whether voice and multimodal models can move beyond transcription into clinical assessment. Each visit contains natural, long-duration medical conversation between a physician, patient, and caregiver, paired with structured scores produced by the physician during the visit.

The core task is to convert messy clinical dialogue into the kinds of measurements used in care and clinical trials. Some assessments are direct scoring tasks, where the model must identify answers and assign structured ratings. Others require clinical judgment: the model must follow a long interview, weigh patient and caregiver responses, and map the conversation onto a clinical rubric.

This makes the dataset useful for training and evaluating models on three capabilities that matter for medical AI: listening across long encounters, tracking multiple speakers and informants, and producing clinically meaningful outputs with physician-scored ground truth.

**What to know:** This dataset is a trove of long-duration patient visits where a doctor assesses a patient's health in a structured way. Along with real-world medical conversation, these interactions have hard outcomes. In patient care and in clinical trials, clinical scoring systems are used to standardize diagnostic staging and measure longitudinal progression. This dataset contains recorded visits where a physician scores patients on these metrics. This is a task that should be trained - correct measurement requires the application of clinical judgement, and the administration and grading of these cognitive assessments are near-term steps towards AI doctors holistically diagnosing patients. 

**Training Goal:** This dataset trains (voice) models on clinical conduct with patients and how physicians assess patient symptoms and behavior. Improvement on the clinical assessment task requires careful objective scoring of responses and holistic clinical judgement.

#### In this dataset preview:

| Included | Description |
| --- | --- |
| Compliance | First-party, de-identified |
| Speakers | Physician, patient, caregiver |
| Duration | Approximately 2-3 hours per visit |
| Assessments | Three clinical assessments per visit |
| Labels | Physician-scored ground truth |
| Modalities | Audio, with timestamped transcripts where available |

Each recording contains three clinical/cognitive assessments, conducted as structured interviews. Two are scoring tasks with direct yes/no or choice-based responses. The longest task is a clinical judgment task, where the physician uses a structured interview and expert interpretation to assign final symptom ratings.

#### Assessment Tasks:

| Assessment | What it measures | Why it matters |
| --- | --- | --- |
| NPI-Q | Caregiver-reported neuropsychiatric symptoms | Tests whether a model can track caregiver observations and convert them into structured symptom ratings |
| GDS | Patient-reported depression symptoms | Tests whether a model can follow short clinical screening questions and score patient responses |
| CDR | Dementia staging through physician judgment | Tests whether a model can reason across a long interview and map evidence to a clinical rubric |

Sample medical assessment details:

<details>
  <summary>Scoring Task A: <b>NPI-Q</b> </summary>
  <br>
  The Neuropsychiatric Inventory Questionnaire (NPI-Q) is a brief, informant-based tool used by clinicians to assess behavioral and psychological symptoms in patients with dementia and evaluate caregiver distress.<br><br>
  The NPI-Q asks the <i>informant</i> (the patient's caregiver) about 12 symptoms. Each is either rated absent (No), or present (Yes), in which case its severity is rated on a 3-point scale and the caregiver's distress is rated on a 5-point scale.<br><br>
  The NPI-Q takes 3-8 minutes to administer.
</details>

<details>
  <summary>Scoring Task B: <b>GDS</b> </summary>
  <br>
  The Geriatric Depression Scale (GDS) is a self-report screening tool to identify depressive symptoms in older adults.<br><br>
  The GDS is 15 yes or no questions. Elaboration isn't required, but since these are real clinical visits, patients often volunteer descriptions or thought processes.<br><br>
  The GDS takes 2-3 minutes to administer.
</details>

<details>
  <summary>Clinical Judgement Task: <b>CDR</b> </summary>
  <br>
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
