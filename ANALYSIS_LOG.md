# Analysis Log

Use this document as the shared, chronological record of the project's
analytical work. It should help any group member understand what has been tried,
what was learned, why decisions were made, and what should happen next.

## How to use this log

Add an entry after a significant analytical step has been completed and its
output has been checked. Significant steps include:

- inspecting a new dataset or important subset;
- making a consequential preprocessing decision;
- deciding how to handle missing values or outliers;
- creating an important exploratory visualization;
- performing a statistical test;
- fitting or comparing models;
- changing the features used in an analysis;
- performing a sensitivity or robustness analysis;
- finding that an approach is unsuccessful or inconclusive;
- obtaining a result that changes the next analytical decision;
- reaching a final interpretation.

Routine syntax fixes, package installations, file renaming, unchanged reruns,
and cosmetic figure adjustments normally do not need entries. Record a
technical correction if it changes the validity, reproducibility, or scientific
interpretation of the analysis.

Keep observed results separate from interpretations. Do not invent missing
values, numerical results, motivations, or conclusions. If an AI assistant
helps draft an entry, group members should check the numerical results and
confirm that the interpretation, limitations, and next decision reflect their
own reasoning.

### Finding an entry quickly

This file grows throughout the project, so avoid scrolling through it:

- On GitHub, use the table-of-contents button at the top right of the
  rendered file to jump to any entry.
- In VS Code, open the **Outline** view in the Explorer sidebar.
- The "Analysis overview" table below is the quick index; each row
  corresponds to one detailed entry, numbered in the same order.

---

## Project context

Complete this section near the beginning of the project. Update it if the
research question, dataset, or analytical plan changes.

- **Project title:**
- **Research question:**
- **Scientific motivation:**
- **Dataset name(s):**
- **Dataset source(s) and link(s):**
- **Date accessed:**
- **Unit of observation:**  
  What does one row, image, sample, or record represent?
- **Response or target variable, if applicable:**
- **Main predictor variables or features:**
- **Date or time range represented:**
- **Initial number of observations:**
- **Known missing-data issues:**
- **Known sampling or measurement limitations:**
- **Other important context:**

## Standing data caveats and limitations

Record here the limitations that apply to the whole project, so individual
entries do not have to repeat them. Add to this list as you discover more.

Examples of what belongs here: known measurement limitations of the dataset,
variables that are strongly correlated with each other, sampling gaps, and any
mismatch between what was measured and what you are trying to conclude.

1. 
2. 
3. 

In individual entries, note only limitations that are specific to that step.

## Reproducibility information

- **Primary script or notebook:**
- **Dependency file:**  
  For example, `requirements.txt`.
- **Python version:**
- **Random seed(s), if applicable:**
- **Raw-data location:**
- **Generated-output location:**  
  For example, `outputs/`.
- **Instructions for running the analysis:**  
  Give the exact command needed to reproduce the analysis from the
  project root.
- **Key package versions:**  
  For example, the pandas version from `python -m pip show pandas`.
- **Data snapshot check:**  
  Number of rows in the merged or cleaned dataset, and the first and
  last row values. Record these when the data is first loaded.

## Analysis overview

Add one short row for each detailed entry. This table is intended as a quick
handoff summary; keep the full reasoning in the detailed entries below.

| Entry | Date | Analysis or decision | Data/features used | Main result | Decision or next step |
|---|---|---|---|---|---|
| 1 | YYYY-MM-DD | Initial data inspection | Example: all available variables | Brief verified result | Brief reasoned decision |

---

## Detailed analysis entries

Copy the entry template below for every significant analysis. Keep entries in
chronological order and preserve earlier entries, including unsuccessful or
inconclusive work.

Keep each entry under roughly 40 lines. If an entry grows longer, move the
detail into comments in the script or into a figure caption. Write "no change"
rather than repeating information that is identical to the previous entry, and
put project-wide caveats in "Standing data caveats and limitations" above
rather than restating them each time.

### Entry N — YYYY-MM-DD — Short descriptive title

**Objective and reason**

One or two sentences: what you were trying to learn, and which earlier result,
limitation, or question prompted this step.

**Data and method**

- **Data used:**  
  Dataset or subset, variables, and observations used (e.g. "67 of 67 years").
- **Preprocessing changed from the previous entry:**  
  Write "no change" if nothing differs. Otherwise note missing-data handling,
  outlier handling, filtering, or transformations.
- **Method and key settings:**  
  Enough for a teammate to reproduce it: test or model, important parameters,
  evaluation metric, random seed, and the package or function used.

**Results**

Verified findings only. Include numbers with units, sample sizes, and any
uncertainty measures. Note null or unexpected results here too.

**Interpretation**

What the results appear to mean for the research question. Keep this clearly
separate from the observed results above.

**Limitations specific to this step**

Only what is new. Project-wide caveats belong in "Standing data caveats and
limitations" near the top of this file. Write "none beyond the standing
caveats" when that is true.

**Decision and next step**

What the group decided to do next, and which result or limitation motivated it.

**Files**

Script: | Figure(s): | Output table(s):

**Contributors and assistance**

Group member(s): | AI assistance used: | How the group verified the work:

---

## Sensitivity and model-comparison summary

Use this section when multiple preprocessing choices, feature sets, models, or
parameter values are compared. Adapt the columns to the project.

| Analysis/model | Data or features | Important settings | Evaluation result | Interpretation |
|---|---|---|---|---|
| Example baseline |  |  |  |  |
| Example sensitivity analysis |  |  |  |  |

Record whether conclusions remained stable. If results changed, state which
choice affected them and how that changes the strength of the conclusions.

## Unsuccessful or inconclusive approaches

Record scientifically useful attempts that did not produce a clear result.
Briefly state:

- what was attempted;
- why it was attempted;
- what happened;
- whether the problem was technical or analytical;
- what was learned;
- why the group stopped, modified, or replaced the approach.

An inconclusive result is not a failure and should not be removed from the
project history.

## Current conclusions

Update this section after major milestones. Keep conclusions proportional to the
evidence.

1. 
2. 
3. 

## Limitations on current conclusions

1. 
2. 
3. 

## Next planned analyses

List the next one to three planned steps. For each step, explain which current
result, uncertainty, or limitation motivates it.

1. **Planned analysis:**  
   **Reason:**
2. **Planned analysis:**  
   **Reason:**
3. **Planned analysis:**  
   **Reason:**

## Handoff checklist

Before moving the project to another group member or device, confirm that:

- [ ] The latest significant analysis has a detailed entry.
- [ ] The analysis overview table is current.
- [ ] Scripts and notebooks have been saved.
- [ ] Dependencies are recorded in the project's dependency file.
- [ ] Important outputs are saved with descriptive names.
- [ ] Links in this log point to the correct project-relative paths.
- [ ] The command needed to reproduce the analysis is documented.
- [ ] Missing data, exclusions, and preprocessing decisions are recorded.
- [ ] Interpretations and next steps have been confirmed by the group.
- [ ] Secrets, virtual environments, machine-specific files, and large raw-data
      folders have not been committed.

