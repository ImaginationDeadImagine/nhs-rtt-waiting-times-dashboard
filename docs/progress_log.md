# Progress Log

## Tue 20 Oct 2026

- Done: Chose NHS England RTT waiting times (Aug 2026, national file) for the project. Defined the audience (public/patients), i.e. non-technical, and the headline statistic (percentiles of weeks waited so far, by specialty and ICB). Created the repo from the Code Institute template, removed outer dashboard nested-folder layout, built the venv, trimmed and pinned requirements.txt (NumPy 1.26.1, SciPy 1.16.3) and committed both pieces (Set up structure and Trim requirements) separately. Raw data files (.csv and .zip) are git-ignored.
- Next: Deploy a “hello world” Streamlit app to Render. Then load the CSV, keep Part_2 and exclude Total rows, and save the slim file to data/processed/v1/.
- Stuck or unsure: Haematology (C_303), my first choice for demonstrating how to handle data, is not published as its own specialty (may be inside “Other - Medical Services”), so T&O is the worked example. Still to confirm: how to handle the 5% of rows with a blank commissioner parent.