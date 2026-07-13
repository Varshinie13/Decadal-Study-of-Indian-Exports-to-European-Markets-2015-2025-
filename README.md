# Decadal Study of Indian Exports to European Markets (2015-2025)

## About This Project
A Python project analyzing Indo-European export data from 2015 to 2025, 
covering data cleaning, visualization, and trade trend insights.

## Dataset
- **File:** `Decadal-Study-of-Indian-Exports-to-European-Markets-2015-2025-.csv`
- **Size:** ~428 MB
- **Stored using:** Git LFS (Large File Storage), since GitHub's normal 
  file limit is 100MB

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

## Tools Used
- **Python** (pandas) — data loading and analysis
- **Google Colab** — cloud-based Python environment for the project
- **Git & Git LFS** — version control and large file storage
- **GitHub** — hosting the project code and dataset

## Project Status
🚧 In progress — data cleaning and visualization stages ongoing.
