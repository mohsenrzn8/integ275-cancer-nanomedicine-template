# INTEG 275 — Final AI-for-Science Challenge: {TOPIC NAME}

This repository is the starting point for your group's final project.
Unlike the warm-up exercise, there is no single correct answer here.
Your group chooses the analysis, carries it out, and records your
reasoning as you go.

Your topic handout and your completed research proposal describe the
scientific question. This README covers the technical setup and the
working routine.

## What's in this repository

```
{your topic's CSV data file(s)}  the dataset (see "About the data")
AGENTS.md                        instructions Copilot reads automatically
ANALYSIS_LOG.md                  your group's shared record of decisions
                                 and results — you will edit this often
README.md                        this file
requirements.txt                 the Python packages this project needs
.gitignore                       tells Git which files not to save
```

You will create these yourselves as the project develops:

```
src/                             your analysis scripts or notebooks
outputs/                         your generated figures and result tables
```

## Step 1: Install the tools

This is the same setup as the warm-up exercise. If yours still works,
skip to Step 2.

1. Install [VS Code](https://code.visualstudio.com/).
2. Install [Python](https://www.python.org/downloads/) 3.11 or newer.
   On Windows, check the box that says "Add python.exe to PATH" during
   installation.
3. Open VS Code, go to the Extensions panel (the icon that looks like
   four squares on the left sidebar, or Ctrl+Shift+X / Cmd+Shift+X),
   and install:
   - **Python** (by Microsoft)
   - **GitHub Copilot Chat** (by GitHub)
4. Sign in to GitHub Copilot with your GitHub account.

## Step 2: Create your group's repository — ONE person only

Decide as a group who will do this. Only that person performs Step 2.
Everyone else waits for the invitation in Step 3.

1. On this repository's GitHub page, click the green **"Use this
   template"** button, then **"Create a new repository"**.
2. Name it so your group is identifiable, for example
   `integ275-group7-{topic}`.
3. Set the visibility to **Private**. Your group's work should not be
   visible to other groups.
4. Click **Create repository**.
5. In your new repository, go to **Settings > Collaborators >
   Add people** and add:
   - every other member of your group, by GitHub username
   - your instructors: **luciedelobel**, **aelsamma**, and **mohsenrzn8**

Adding your instructor is required. Because the repository is private,
nobody can see your work for grading unless they have been added.

This one repository is where all of your group's work will live. Do not
create a separate repository for each person.

## Step 3: Everyone else joins and clones

Each remaining group member:

1. Accept the collaborator invitation. It arrives by email, and also
   appears at https://github.com/notifications.
2. Open your group's repository on GitHub, click the green **Code**
   button, and copy the HTTPS URL. Check that this is your *group's*
   repository, not the instructor's template.
3. In VS Code, open the Command Palette (Ctrl+Shift+P / Cmd+Shift+P),
   type "Git: Clone", paste the URL, and choose a folder on your
   computer to save it in.
4. Once it's cloned, open the folder in VS Code (File > Open Folder...).

Do not save the project inside a cloud-synced folder such as OneDrive,
Dropbox, or Google Drive. Git and cloud sync interfere with each other
and can create duplicate or corrupted files.

## Step 4: Set up your Python environment

Every group member does this on their own computer. The virtual
environment is not shared through Git, so each person creates their own.

Open a terminal in VS Code (Terminal > New Terminal). The terminal must
be at the project root — the folder that contains `AGENTS.md`,
`README.md`, `ANALYSIS_LOG.md`, `requirements.txt`, and your topic's
CSV data files — before running the commands below.

On Windows, you can verify the location with:

```
Get-Location
Test-Path .\requirements.txt
```

The second command should print `True`. If it prints `False`, change to
the project root before continuing, or reopen that folder in VS Code.

Then run, on **Windows (PowerShell)**:

```
python -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

Or on **macOS / Linux**:

```
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -r requirements.txt
```

If VS Code asks whether to use this environment as your workspace's
Python interpreter, say yes. You'll know the virtual environment is
active when `(.venv)` appears at the start of your terminal prompt.

## Step 5: Fill in your project details

Before starting any analysis, open `AGENTS.md` and complete the
"This group's project" section using your research proposal. Copilot
reads this file automatically, and several of its guardrails do nothing
while that section is blank.

Then open `ANALYSIS_LOG.md` and fill in the "Project context" and
"Reproducibility information" sections.

## Step 6: Work in small steps

There is no list of TODOs to complete. Your group decides what to do
next, guided by your research question.

A reasonable working loop:

1. Decide the next small step — load the data, check for missing
   values, make one plot, fit one simple model.
2. Attempt it yourselves first. Ask Copilot to explain or unblock you
   rather than to produce the finished step.
3. Run your script from the project root and check that the output
   is sensible before trusting it.
4. Save figures to `outputs/` with descriptive names, for example
   `outputs/rainfall_by_month.png`.
5. Record what you did and what you concluded in `ANALYSIS_LOG.md`.

Resist the temptation to ask for the whole analysis at once. You are
assessed on your reasoning, and you need to be able to explain every
line you submit.

## Step 7: Keep the analysis log current

`ANALYSIS_LOG.md` is the heart of this project. It records what you
tried, what you found, what you decided, and why — including approaches
that did not work. Unsuccessful and inconclusive attempts belong there;
they are a normal part of real scientific work.

Because everyone edits this one file, agree on a **log keeper** for each
phase of the analysis. That person writes the entries. This avoids two
people editing the same lines and creating a merge conflict.

Copilot can help draft an entry, but the interpretation, limitations,
and next steps must be your group's own reasoning. Check every number
before it goes in.

## Step 8: Work together without overwriting each other

Because you share one repository, get into this habit.

**Before you start working:**

```
git pull
```

**When you finish a working session:**

```
git add .
git status
git commit -m "Short description of what you did"
git push
```

`git pull` brings in your teammates' latest work. `git add .` prepares
your changed files, `git status` lets you check what is prepared,
`git commit` records a snapshot of those files, and `git push` uploads
it to GitHub so your teammates can see it.

If Git reports a **merge conflict**, don't panic and don't delete
anything. It means two people changed the same lines of the same file.
Ask Copilot Chat to explain what the conflict markers mean, and keep
both sides when both are real work. Never resolve a conflict by
discarding a teammate's work without checking with them first.

## Step 9: Submit

Submit your group's repository URL as instructed on LEARN.

Before submitting, confirm that:

- your instructors, **luciedelobel**, **aelsamma**, and **mohsenrzn8** 
have been added as a   collaborator — without this your work cannot be graded
- every group member has accepted their invitation
- `ANALYSIS_LOG.md` is current, and its handoff checklist is satisfied
- your figures are in `outputs/` with descriptive filenames
- all of your work has been committed **and pushed** — check the file
  list on GitHub, not just your own computer
- `.venv/` does **not** appear in the repository on GitHub

Keep the repository **Private**. Do not share it with other groups.

## About the data

{Replace this section for each topic.}

- **Dataset:**
- **Source and link:**
- **Collected by / citation:**
- **Licence or terms of use:**

The data files in this repository are a fixed copy provided for this
course. Do not download replacement data and do not edit the data files.
Treat them as read-only, and write all generated output to `outputs/`.

## Using Copilot well

Copilot works best when you describe what you want in plain language,
one step at a time, rather than asking it to write a whole analysis at
once. If a suggestion looks confusing, ask Copilot Chat to explain it
line by line before accepting it. You are responsible for understanding
every line of code you submit, not just for getting it to run.

This repository includes an `AGENTS.md` file, which Copilot reads
automatically to understand this course's expectations — for example,
asking your permission before editing files, explaining errors before
fixing them, and breaking work into small steps. You don't need to do
anything with it beyond Step 5, but feel free to open it and see what
Copilot "sees" before you even ask a question.

One warning worth taking seriously: Copilot will happily produce a
complete analysis if you ask for one. That shortcut costs you the
understanding you are being assessed on, and it tends to produce work
you cannot defend.
