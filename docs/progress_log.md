# Progress Log

## Thu 22 Oct 2026

- Done:
  - Built the slim processed table (ICB group × specialty, 1,181 rows × 110 columns) and saved it as data/processed/v1/icb_specialty_waits.csv (#5). Validated it with four checks: no duplicate groups, a spot check against the full table (NW hub T&O = 12; a large London ICB = 38,478), Total All unchanged at 7,189,213, and week bands equal to the total, so every patient has a known clock start.
  - Wrote and tested percentile_band (calculated T&O, England: 25th percentile in the 6-7 week band, median in 13-14, 75th in 25-26; empty group returns “No data”) (#8).
  - Decided to test H1 and H2, and to treat H3 (trust-level list size) as a stretch goal
  - Deadline confirmed by tutor as elastic to the end of Sunday.
- Next:
  - Check whether the 36 ICB parent names in the data match the 36 ICBs on the NHS.uk list.
  - Create 02_percentiles.ipynb that reads the processed file.
  - Helper to get the band counts for a specialty and area.
  - Friendly band labels. % waiting under 18 weeks.
  - First version of the app with dropdowns.
  - Write H1 and H2 in the README.
- Stuck or unsure:
  - GitHub board: #8 repeatedly disappears after being added or moved to Done; suspect a workflow or view filter (columns showed counts like 3/3).
  - Recreated the issue by mistake (#9, closed as duplicate).
  - #3 and #4 are finished but still open in In progress.

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