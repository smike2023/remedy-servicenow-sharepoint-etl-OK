# Remedy-to-ServiceNow: 3-Zone ETL Governance Model

This repository contains artifacts to support the reorganization of fragmented SharePoint folders during the Remedy-to-ServiceNow migration. It introduces a practical 3-Zone governance model inspired by ETL principles: Extract, Transform, Load.

---

## 📊 3-Zone Model Overview

- **Zone A - SOURCE**  
  Raw exports (SRXML, SQL dumps, historical records)

- **Zone B - TRANSFORMATION**  
  Working files: mappings, test logs, transformation logic

- **Zone C - LOADED**  
  Finalized XMLs and transform maps ready for ServiceNow import

---

## 📁 Repository File Descriptions

| File Name | Description |
|-----------|-------------|
| `3-Zone_ETL_Governance_Model_Explainer_FIXED.pdf` | 1-page PDF overview of the 3-Zone model |
| `3-Zone_SharePoint_Reorg_PitchDeck.pptx` | Pitch deck for explaining the structure to leadership |
| `3-Zone_SharePoint_Notion_Tracker.csv` | Tracker board for folder ownership, status, and purpose |
| `A_flowchart-style_digital_diagram_illustrates_a_pr.png` | High-level flowchart of SharePoint reorganization |
| `A_PowerPoint_slide_presentation_displays_the_propo.png` | Slide-optimized layout visual of the 3-Zone concept |
| `.gitignore` | Git exclusions for temporary or system-specific files |
| `Suggested_Folder_Structure_CLEAN.txt` | Sample folder layout for organizing the SharePoint migration files |
| `.github/workflows/upload-etl-project-kit.yml` | GitHub Actions workflow to auto-import zipped project kit |

---

## 🔄 GitHub Actions: Auto-Unzip and Commit Project Kit

This repository includes a GitHub Actions workflow that automatically unzips the `3-Zone_ETL_Project_Kit.zip` file and commits its contents into the repository.

### 📂 Workflow File
- `.github/workflows/upload-etl-project-kit.yml`

### 🧠 What It Does (Step-by-Step)
1. Watches the `main` branch for new pushes.
2. Unzips `3-Zone_ETL_Project_Kit.zip` into a temporary folder.
3. Copies the unzipped contents to the root of the repo.
4. Automatically commits and pushes the updated files.

> This saves time, keeps things consistent, and supports teams working without full Git privileges.

---

## 📦 Setup Instructions

1. **Upload the following to your GitHub repository root:**
   - `3-Zone_ETL_Project_Kit.zip`
   - This `README.md` file
   - `.gitignore` and `Suggested_Folder_Structure_CLEAN.txt` for internal reference

2. **Place the GitHub Actions file here:**
   - `.github/workflows/upload-etl-project-kit.yml`

3. **On your next commit/push to `main`, GitHub will:**
   - Unzip the kit
   - Move files into place
   - Commit them automatically

---

## 🙌 Credit

Created by: **[Your Name]**  
Mission: Bring order to SharePoint chaos using ETL-driven governance
