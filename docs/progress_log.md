# Progress Log

## Wed 21 Oct 2026 (evening)

- Done:
  - Deployed minimal Streamlit app to Render (#3).
  - Loaded the national RTT CSV in notebook 01, kept Part_2 and removed the Total rows (#4).
  - Validated the filter two ways, in pandas and an Excel pivot: both give 7,189,213 patients.
  - Investigated blank commissioner parents (2.24% of patients): commissioning hubs, NHS England regions and non-English commissioners (NONC).
  - Built a commissioner_group column with 59 groups and no patients lost.
- Next:
  - Decide the shape of the slim processed file and save it to data/processed/v1/ (#5).
  -  Percentiles and the T&O worked example.
  -  Tutor (Vasi Pavaloi) has confirmed project extension time to end of Sunday.
- Stuck or unsure:
  - Blank commissioner parents were a lookup gap, not bad data.
  - Still deciding how ICB comparisons should show groups that aren’t ICBs.

## Wed 21 Oct 2026

- Done (late Tue / early Wed): Created issues #1 to #7 and a public Kanban board; #1 and #2 closed.
    Commit mistakenly labelled #3 was for the progress log (#7).
- Next: Render “Hello, world!” (#3), then notebook 01 (#4, #5).

## Tue 20 Oct 2026

- Done: Chose NHS England RTT waiting times (Aug 2026, national file) for the project. Defined the audience (public/patients), i.e. non-technical, and the headline statistic (percentiles of weeks waited so far, by specialty and ICB). Created the repo from the Code Institute template, removed outer dashboard nested-folder layout, built the venv, trimmed and pinned requirements.txt (NumPy 1.26.1, SciPy 1.16.3) and committed both pieces (Set up structure and Trim requirements) separately. Raw data files (.csv and .zip) are git-ignored.
- Next: Deploy a “hello world” Streamlit app to Render. Then load the CSV, keep Part_2 and exclude Total rows, and save the slim file to data/processed/v1/.
- Stuck or unsure: Haematology (C_303), my first choice for demonstrating how to handle data, is not published as its own specialty (may be inside “Other - Medical Services”), so T&O is the worked example. Still to confirm: how to handle the 5% of rows with a blank commissioner parent.