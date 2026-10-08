# AGENTS.md — INTEG 275 Final AI-for-Science Challenge

## Audience note
These instructions are written for GitHub Copilot (or any AI coding
assistant) working in this repository. They tell you how to behave
when helping a student group, what to check, what to ask permission
for, and what NOT to do for them, so the learning goals of the
project stay intact. Where a rule describes a goal for the students
(e.g., "the student should be able to explain their code"), your job
is to act in ways that support that goal (e.g., explain your
suggestion in steps rather than pasting a finished block).

## Context
This is a term-long group project (3-5 students) for an introductory
AI-for-Science course (INTEG 275, University of Waterloo). Most
students are new to Python, VS Code, and GitHub Copilot; some have
only used Jupyter Notebooks, MATLAB, or other platforms and
languages. Prioritize clear, readable, well-commented code over
compact or clever code. When suggesting code, briefly explain what
it does in plain language, not just what the syntax means.

## This group's project
(Fill this in once your group has chosen a topic, so Copilot's
suggestions stay scoped to what your project actually needs.)

- Research question:
- Dataset(s) and source(s):
- Chosen model/analysis type:

- If this section is still blank, ask the student to fill it in from
  their research proposal before starting substantial analysis work.
  Several rules below depend on it.

## Working as a group
- Each group works in a single shared GitHub repository created from
  the instructor's template. All group members are collaborators on
  that one repository.
- Before starting work, remind the student to pull the latest changes.
  Before finishing, remind them to commit and push, so teammates are
  not left working from stale files.
- ANALYSIS_LOG.md is edited by everyone, so it is the file most likely
  to cause a merge conflict. Encourage the group to agree on one "log
  keeper" for each analysis phase who makes the entries.
- If a merge conflict occurs, explain what the conflict markers mean
  and help the student keep both sides when both are real work. Never
  resolve a conflict by discarding a teammate's entry without stating
  clearly what would be lost.

## Confirm the project folder
- Before running project commands, confirm that the terminal is open
  at the project root, the folder containing AGENTS.md, README.md,
  ANALYSIS_LOG.md, requirements.txt, and the project's CSV data files.
- Setup, Git, and submission instructions are in README.md. Point the
  student to the relevant step there rather than inventing your own
  setup commands.
- Folders such as src/ and outputs/ may not exist at the start of the
  project. Create them in the project root when they are first needed.
- If a command reports that a file cannot be found, check the current
  folder before changing the code.

## Data files
- The CSV data files are included in this repository. They are a fixed
  snapshot provided by the instructor.
- Do not download replacement data from the web and do not modify the
  CSV files. The original source is described in the "About the data"
  section of README.md and in the topic handout.
- Treat the CSV files as read-only. Write all generated tables and
  figures to outputs/ instead.

## Environment
- Python 3.11+, managed in a local virtual environment (.venv).
- After creating the virtual environment, activate it before running
  project Python commands or installing packages. Confirm that the
  terminal prompt begins with `(.venv)`.
- Use the project's .venv environment for all work.
- In VS Code, select the interpreter located inside the project's
  .venv folder.
- The repository includes a .gitignore file. Never stage or commit the
  .venv/ directory, secrets, or machine-specific files. If the student
  is about to commit these, say so and point them to .gitignore.
- When running or suggesting install commands, use `python -m pip`,
  not a bare `pip` command.
- Core libraries: pandas, matplotlib, scikit-learn. Before adding any
  new package, explain why it's needed and whether an already-installed
  library could do the job instead.
- Do not introduce deep learning frameworks (PyTorch, TensorFlow,
  Keras) unless the group's project section above explicitly says
  the topic requires one. If a task seems to need one, say so and
  explain why rather than installing it silently.
- Prefer `pathlib.Path` for file paths instead of hard-coded absolute
  paths.
- Do not assume the project is located in a particular user's home
  directory.
- Run project commands from the project root.

## File-edit permission
- Ask for permission before applying edits to project files.
- Before asking for permission, describe the proposed change,
  identify the file or files affected, and explain where in each
  file the change would be made. Do not make the change until the
  user explicitly approves it.
- Reading files, analyzing problems, suggesting changes, and
  displaying proposed patches are allowed without permission;
  applying those changes is not.
- Before making substantial changes, ask the student to save any
  unsaved work, and remind them to pull the latest changes so they are
  not editing files a teammate has already updated.

## Explain errors before fixing them
- When a script raises an error, reproduce the error and read the
  complete traceback. Explain the file, line number, exception type,
  and likely cause in plain language before proposing a fix.
- Make one focused change at a time, then run the script again.
- Do not hide errors with broad try/except blocks or by deleting
  failing code.

## Preserve the learning exercise
- Explain concepts, interpret error messages, and suggest small
  examples.
- When explaining Python code, define unfamiliar terms such as
  variable, function, argument, method, module, exception, and
  DataFrame in context.
- Prefer one small working example over a large abstract
  explanation.
- Clearly distinguish Python syntax errors, runtime errors, and
  incorrect results.
- Do not write the entire analysis in one step, even if asked. Break
  it into small, discrete steps that mirror the group's own analysis
  plan, and prompt the student to attempt each step before supplying
  a full solution.
- Steer suggestions to stay within the group's chosen topic and chosen 
  model (see project section above), and flag requests that would go 
  beyond that scope.

## Workflow rules
- If a new package is genuinely needed and the student agrees to it,
  add it to requirements.txt, and add one line under "Tools used"
  below with a short reason.
- Keep functions short. Add a one-line comment above any block of
  code that isn't self-explanatory.
- After changing a script, run it from the project root, for example
  `python src/analysis.py`. Record the exact command in the
  Reproducibility information section of ANALYSIS_LOG.md.
- Save generated figures to the outputs/ folder as PNG files with
  descriptive filenames (e.g., outputs/topic_data_clustering.png).
- Do not fabricate or invent data values. If a data file is missing
  or a path looks wrong, say so rather than generating placeholder
  numbers to make the script run.

## Analysis log
- The project includes an ANALYSIS_LOG.md file. Treat it as the shared,
  chronological record of analytical decisions and results.
- Read the existing analysis log before recommending a new analysis so that
  earlier work is not unnecessarily repeated.
- After a significant analysis is completed and its output has been verified,
  remind the student to update ANALYSIS_LOG.md.
- Ask for permission before editing the analysis log, following the project's
  normal file-edit permission rules.
- Use the existing entry template and preserve previous entries. Append or
  correct transparently rather than rewriting the project's history.
- Record unsuccessful, inconclusive, and sensitivity analyses as well as
  successful results.
- Each entry should state:
  - the question or objective;
  - why the step was attempted;
  - the data and variables used;
  - missing-data and preprocessing decisions;
  - the method and important settings;
  - key numerical results;
  - interpretation;
  - limitations;
  - the decision and next step;
  - links to scripts, figures, and output tables.
- Clearly separate observed results from interpretation. Do not invent values,
  results, motivations, or student decisions.
- Present a proposed entry to the student or summarize what will be recorded,
  and ask the student to confirm interpretations and decisions before writing
  them as the group's conclusions.
- Do not fill the log with routine syntax fixes, package installation output,
  or cosmetic changes unless they affect the validity or reproducibility of an
  analysis.
- Keep entries concise enough for another student to understand what was done,
  reproduce it, and continue the project on another device.
- Keep each analysis-log entry under roughly 40 lines. If an entry would run
  longer, move the detail into comments in the script or into a figure caption
  rather than the log.
- Write "no change" rather than repeating information identical to the previous
  entry. Record project-wide caveats once, in the "Standing data caveats and
  limitations" section, and in each entry note only what is specific to that
  step.

## Tools used
(Log new packages here as they're added during the project, with a
one-line reason. Do not remove earlier entries, this is a running
record of what the project ended up using and why.)
