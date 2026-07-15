# Decadal Study of Indian Exports to European Markets (2015-2025)

## About This Project
A Python project analyzing Indo-European export data from 2015 to 2025, 
covering data cleaning, visualization, and trade trend insights.

## Dataset
- **File:** `Decadal-Study-of-Indian-Exports-to-European-Markets-2015-2025-.csv`
- **Size:** ~428 MB
- **Stored using:** Git LFS (Large File Storage), since GitHub's normal 
  file limit is 100MB

## Dataset Column Details:

## Dataset Column Description

| Column | Description |
|---|---|
| `id` | Unique identifier for each record in the dataset |
| `date` | Date of the export transaction (month/year) |
| `country_name` | Full name of the destination country (e.g., Germany, France) |
| `alpha_3_code` | ISO 3-letter country code (e.g., DEU, FRA) |
| `country_code` | Internal/numeric code identifying the country |
| `region` | Broad geographical region (e.g., Europe) |
| `region_code` | Numeric code representing the region |
| `sub_region` | Finer regional grouping (e.g., Western Europe, Northern Europe) |
| `sub_region_code` | Code representing the sub-region |
| `hs_code` | Harmonized System Code — international standard for classifying traded products |
| `commodity` | Name/description of the exported product |
| `unit` | Unit of measurement for quantity (e.g., KG, MT, NOS) |
| `value_qt` | Quantity of the commodity exported, in the specified unit |
| `value_rs` | Export value in Indian Rupees (₹) |
| `value_dl` | Export value in US Dollars ($) |

## How the Dataset Was Uploaded (Git Bash Workflow)

Since the dataset exceeds GitHub's 100MB file limit, Git LFS was used 
to upload it. Here's the process:

```bash
# 1. Set up Git identity (one-time)
git config --global user.name "Varshinie13"
git config --global user.email "varshiniesivakumar13@gmail.com"

# 2. Clone the repository
git clone https://github.com/Varshinie13/Decadal-Study-of-Indian-Exports-to-European-Markets-2015-2025-.git
cd Decadal-Study-of-Indian-Exports-to-European-Markets-2015-2025-

# 3. Install and enable Git LFS
git lfs install

# 4. Track large file types
git lfs track "*.csv"
git add .gitattributes
git commit -m "Configure Git LFS tracking"

# 5. Add the dataset file
cp "/path/to/dataset.csv" .
git add Decadal-Study-of-Indian-Exports-to-European-Markets-2015-2025-.csv
git commit -m "Add exports dataset via Git LFS"

# 6. Push to GitHub
git push
```


## How the Dataset read in Python - Colab Work Space
# ============================================
# STEP 1: Install Git LFS (Large File Storage)
# Needed because our dataset files are too big for normal GitHub storage
# ============================================
!apt-get install git-lfs -y
!git lfs install

# ============================================
# STEP 2: Clone the GitHub repository into Colab
# This downloads all project files (code + datasets) from GitHub
# ============================================
!git clone https://github.com/Varshinie13/Decadal-Study-of-Indian-Exports-to-European-Markets-2015-2025-.git

# ============================================
# STEP 3: Check what files actually got downloaded
# Useful to confirm the dataset file is present and full-sized (not a tiny LFS pointer file)
# ============================================
!ls -la "/content/Decadal-Study-of-Indian-Exports-to-European-Markets-2015-2025-/"

# ============================================
# STEP 4: Import pandas
# pandas is the main library used to read, clean, and analyze tabular data (like Excel/CSV)
# ============================================
import pandas as pd

# ============================================
# STEP 5: Load the exports dataset into a DataFrame
# A DataFrame is like a table/spreadsheet that Python can work with
# ============================================
df = pd.read_csv("/content/Decadal-Study-of-Indian-Exports-to-European-Markets-2015-2025-/Decadal-Study-of-Indian-Exports-to-European-Markets-2015-2025-.csv")

# ============================================
# STEP 6: Preview the first 5 rows
# Helps confirm the data loaded correctly and shows the column names/structure
# ============================================
df.head()

# ============================================

# STEP 7: Basic info about the dataset
# Shows column names, data types, and missing values — useful first check before analysis
# ============================================
df.info()

# ============================================
# STEP 8: Summary statistics
# Gives count, mean, min, max, etc. for numeric columns — quick overview of the data
# ============================================
df.describe()

## Tools Used:

- **Python** (pandas) — data loading and analysis
- **Google Colab** — cloud-based Python environment for the project
- **Git & Git LFS** — version control and large file storage
- **GitHub** — hosting the project code and dataset

## Project Status:

🚧 In progress — data cleaning and visualization stages ongoing.
