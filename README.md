# ETL Mini Project: Contacts and Campaign Data Processing

## Overview

This project demonstrates the process of extracting, transforming, and loading (ETL) data for creating a clean and structured dataset from raw data. The project involved processing crowdfunding and contacts data stored in spreadsheets to create standardized CSV files for further analysis.

## Key Concepts Learned

1. **Extract, Transform, Load (ETL):**
   - Extracting raw data from spreadsheets.
   - Transforming data into clean, usable formats.
   - Exporting the transformed data into standardized CSV files.

2. **Pandas Library for Data Processing:**
   - Using Pandas to read, manipulate, and export data.
   - Handling missing or malformed data.
   - Creating new columns by extracting values from existing ones.

3. **Regex for Data Extraction:**
   - Using regular expressions to extract specific patterns (e.g., IDs, names, and emails) from raw text.

4. **Data Cleaning:**
   - Handling `None` values and converting data types.
   - Splitting concatenated fields into separate columns.
   - Reordering and renaming columns for consistency.

## Process Breakdown

### Step 1: Process Contacts Data
- **Input:** `contacts.xlsx` file with dictionary-like strings in a single column.
- **Output:** `contacts.csv` file with clean columns:
  - `contact_id` (integer)
  - `first_name` (string)
  - `last_name` (string)
  - `email` (string)
- **Steps:**
  1. Extract `contact_id`, `name`, and `email` using regex.
  2. Split the `name` into `first_name` and `last_name`.
  3. Handle missing values by replacing with defaults (e.g., `0` for IDs).
  4. Reorder columns and export as `contacts.csv`.

### Step 2: Process Campaign Data
- **Input:** `crowdfunding.xlsx` file with raw data including categories and subcategories.
- **Output:** `campaign.csv`, `category.csv`, and `subcategory.csv` files.
- **Steps:**
  1. Split combined `category & sub-category` column into separate fields.
  2. Create `category_id` and `subcategory_id` mappings.
  3. Merge data to assign proper IDs to each campaign.
  4. Format columns (e.g., convert dates to datetime format, goals to floats).
  5. Export cleaned data to CSV files.

## Tools Used
- **Python**: Core programming language.
- **Pandas**: For data manipulation and cleaning.
- **Regex (re module)**: For extracting specific patterns.
- **Excel**: Source format for the raw data.

## Final Outputs
- `contacts.csv`: A cleaned and structured file of contact data.
- `campaign.csv`: A cleaned dataset for crowdfunding campaigns.
- `category.csv`: A mapping of unique campaign categories.
- `subcategory.csv`: A mapping of unique campaign subcategories.

## Reflection
This project provided hands-on experience with the full ETL process, highlighting the importance of structured workflows and robust error handling when working with raw and messy data. Mastery of Python libraries like Pandas and Regex proved essential for efficient data transformation.
