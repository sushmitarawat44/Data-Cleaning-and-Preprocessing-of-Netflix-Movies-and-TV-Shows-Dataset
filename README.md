# 🎬 Netflix Movies and TV Shows Dataset Cleaning (Excel-Based Project)

This project documents the data cleaning process I followed using **Microsoft Excel** and **Power Query** to prepare the Netflix Movies and TV Shows dataset (sourced from Kaggle) for analysis.

---

## 📥 Step 1: Download the Dataset
- Dataset was downloaded from Kaggle (https://www.kaggle.com/datasets).
- File format: CSV (Comma-Separated Values)

---

## 🧾 Step 2: Organize Columns
- Highlighted headers and adjusted column widths for better readability.
- Ensured each column had appropriate titles and was clearly distinguishable.

---

## 🔍 Step 3: Identify and Handle Missing Values

### ➤ Example: `director` Column
- Found **2,389 missing values** (~31% of all entries).
- Deleting those rows would result in significant data loss.
- ✅ Solution: Replaced missing values with `"Unknown"`.

#### 🛠️ Process in Excel:
1. Select the `director` column.
2. Go to **Data → Filter**.
3. Filter by **(Blanks)**.
4. Select all visible blank cells.
5. Type `Unknown` and press **Ctrl + Enter** to fill all at once.

✅ Repeated similar steps for other columns like `cast`, `country`, and `rating`.

---

## 🧼 Step 4: Highlight All Blank Cells
To identify and clean blank values across the sheet:

1. Press **Ctrl + A** to select all data.
2. Press **F5** (or **Alt + F5**) → Click **Special**.
3. Choose **Blanks** → Click **OK**.
4. Fill blank values with placeholders like `"Not Available"`.

---

## 🔁 Step 5: Remove Duplicate Rows
- Selected the full data range.
- Went to **Data → Remove Duplicates**.
- ✅ Result: No duplicate entries found.

---

## 🛠️ Step 6: Standardize and Transform Data
- Opened the file in **Power Query** for better control.

### 🔧 Process:
1. Created a new worksheet.
2. Went to **Data → Get Data → From File → From Workbook/CSV**.
3. Selected the current Excel file → Clicked **Transform Data**.
4. Performed:
   - Trimming spaces
   - Case formatting (Proper/Upper/Lower)
   - Replacing inconsistent text values (e.g., US → United States)
5. Closed & reloaded the cleaned data.
6. Deleted the original, uncleaned sheet.

---

## 📅 Step 7: Format Dates Consistently
- Selected the `date_added` column.
- Right-click → **Format Cells → Number → Custom**
- Used format: `dd-mm-yyyy`

---

## 🧪 Step 8: Verify Data Types
- Used **Power Query Editor** to inspect and correct data types.
- Ensured:
  - Dates were not stored as text
  - Numerical fields had correct formats
  - Text columns were consistent

---

## ✅ Final Outcome
- Cleaned, structured, and standardized Netflix dataset ready for analysis.
- All missing values addressed appropriately.
- Consistent formatting across:
  - Dates (`dd-mm-yyyy`)
  - Text values (proper casing, cleaned spacing)
- No duplicate or mismatched data types remain.

---

## 📎 Dataset Source
- [Netflix Movies and TV Shows on Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)
