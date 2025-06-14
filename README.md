# Angela-Irungu

# ETL Extract Lab - Patient Data (Lab 3 & Lab 4)

Name: Angela Irungu
Student ID:669289


## Project Overview

This project demonstrates a complete ETL (Extract, Transform, Load) pipeline using patient data.

The dataset used is `Patient data.xlsx`, which includes patient visit records.

Tools & Technologies

* Python 3
* pandas
* Jupyter Notebook

Dataset Fields

 `ID`: Patient identifier
 `age`: Patient age
 `gender`: Patient gender
 `condition`: Reason for visit
 `visit_date`: Date of patient visit
 `doctor`: Attending physician

Notebook Sections

Section 1: Full Extraction

* Loads all records from the Excel file
* Displays shape and sample

Section 2: Incremental Extraction

* Uses timestamp in `last_extraction.txt`
* Extracts only new records with `visit_date` after that timestamp

Section 3: Save New Timestamp

* Updates `last_extraction.txt` with the current timestamp

Section 4: Transform Full Data

* Removes duplicates
* Drops rows with missing `age`
* Converts date fields
* Adds:

  * `is_senior` (True if age ≥ 65)
  * `age_group` (categorized: child, teen, adult, senior)

Section 5: Transform Incremental Data

 Applies the same cleaning and enrichment logic to incremental data


 How to Run

1. Open the `etl_extract.ipynb` notebook in Jupyter.
2. Run all cells in order.
3. The transformed datasets will be saved automatically.


