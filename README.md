**Dependencies:**

pandas (for data manipulation)
numpy (not strictly necessary in this script, but potentially used elsewhere)
Input Files:

mark.csv: Assumed to contain student marks (e.g., exam scores).
student.csv: Assumed to contain additional student information (e.g., age, gender, employment status, grades).
Output:

The script modifies the in-memory DataFrame (combined_df) but doesn't save any output files.

**Steps Performed:**

**Data Loading**:

Imports pandas and numpy libraries.
Reads data from mark.csv and student.csv into DataFrames df1 and df2 respectively.

**Data Merging:**

Merges df1 and df2 based on the assumption that they share a common Student_id column.
The merged DataFrame is stored in combined_df.

**Missing Value Check**:

Checks for missing values in combined_df using isnull().sum().
This script assumes there are no missing values, but you might need to implement handling if necessary.

**Handling Categorical Data (Employment)**:

Creates a new column Employed by converting "yes" in the original Employed column to 1 and other values to 0.
This transforms the categorical data into a numerical format suitable for some machine learning algorithms or statistical analysis.

**Handling Categorical Data (Grades)**:

Defines a dictionary grade_mapping to map textual grades ("1st Class", etc.) to numerical values (3, 2, 1).
Creates a new column Numeric Grade by applying the grade_mapping to the Grade column.
This provides a numerical representation of grades for potential use in further analysis.
