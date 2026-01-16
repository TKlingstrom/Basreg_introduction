# Basreg introduction: using BasregDWH

This repository contains a short step-by-step user guide for accessing the SLU Basreg data warehouse (**basregDWH**) from **R / RStudio** using `odbc`, `DBI`, `dplyr`, and `dbplyr`.

**Audience:** Biologists and other researchers who are familiar with the idea of programming but are new to R packages and database workflows.

---

## What is included

- `Basreg_introduction.Rproj` — RStudio project file (recommended way to open this repo)
- `basreg_userguide.Rmd` — the main tutorial (run code step-by-step)
- `basreg_userguide.html` — a pre-rendered HTML version you can read in a browser
- `basreg_userguide.pdf` — a PDF version (A4, shortened where needed)

---

## Prerequisites

1. **RStudio**  
   Official getting started guide: https://posit.co/resources/videos/getting-started-with-rstudio/

2. **Access to SLU Basreg / basregDWH**  
   For permissions, contact **Eva Rundlöf**.

> If you have an SLU-issued Windows laptop, ODBC will normally verify your identity automatically when connecting.  
> Linux and macOS users need a separate ODBC setup.

---

## Download this repository

### Option A: Clone with Git in RStudio (recommended)

1. In RStudio: **File → New Project → Version Control → Git**
2. Paste the repository URL:
   https://github.com/TKlingstrom/Basreg_introduction
3. Choose a folder and click **Create Project**

### Option B: Download as ZIP

1. Open the repository in your browser
2. Click **Code → Download ZIP**
3. Unzip the folder
4. Open `Basreg_introduction.Rproj` in RStudio

---

## Where to start

### If you want to *run the tutorial*
1. Open `basreg_userguide.Rmd` in RStudio
2. Read the introduction, then start at **Step 1** and run each code chunk in order
   - In an R Markdown chunk, click the green ▶ button in the top-right corner of the chunk
   - Or select code and press **Ctrl + Enter**

### If you only want to *read the tutorial*
- Open `basreg_userguide.html` in your web browser (recommended)
- Or read `basreg_userguide.pdf`

You can also copy each code segment from the HTML document or PDF into your own R-script to run the tutorial step by step. 
---

## Notes

- Users have **read-only access**. You can view and download data, but you are not at risk of changing the database, you should however not run very large and complex matching operations serverside to generate datasets as it may impact other users.
- The guide saves example output (CSV) to your current working directory (`getwd()`).

---

## Author

Tomas Klingström
