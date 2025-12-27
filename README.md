# Stage by Stage: Data Wrangling in *OpenRefine* Using British Library's Bibliographic "Drama" Collections

## Abstract

This project analyses the metadata of English dramas published between the seventeenth and nineteenth centuries, sourced from the British Library, in order to identify socio-cultural patterns of the period through selected methods in Digital Humanities. The first phase of the project focuses on data preparation. Using the open-source application OpenRefine, we cleaned and standardized the dataset with the dual objective of preserving as much original information as possible while extracting structured data suitable for subsequent analysis. All data processing steps are documented in a shared GitHub repository, which includes raw and cleaned datasets, OpenRefine JSON histories, and workflow documentation. This ensures transparency, version control, and reproducibility.

---

## 1. Project Overview and Scope

### 1.1 About the Project

The goal of the project is to apply digital humanities methodologies and tools to investigate patterns in titles, authorship, genres, publication, taste, and public discourse in British society. A project management plan is developed during the process of data preparation and analysis for the DH Project Management course.
This repository includes:
- data (raw & cleaned)
- Project Management Plan
- Project Management Gantt chart
- Documentation and workflow files(grel_scripts, json_history)
- cleaning protocol

### 1.2 Dataset Description

In this project we explored British Library’s bibliographic dataset of digitized British dramas from the 17th to 19th centuries, containing metadata such as authors, titles, genres, and publication details. To ensure a coherent analysis of theatrical works, the project strategically targets three specific spreadsheets within the source file: Tragedy, Comedy, and Play, while excluding the Recitation sheets, as it contained only 34 records compared to approximately 500 records each in other subgenres.
Our data wrangling process included four stages: (1) Data Discovery, involving preliminary exploration of the datasets
on OpenRefine; (2) Data Structuring, modifying the display and storage of data by developing standardized protocols
for each column; (3) Data Cleaning, creating operational workflows to clean and transform columns; and (4) Data
Enrichment, using WikiData to reconcile the authors column, thus adding contextual information for analysis.
### 1.3 Team & Context
## Team Members and Roles
| Team Member | Dataset Responsibility | Functional Role | Key Responsibilities |
|------------|------------------------|-----------------|----------------------|
| Liangyu Gan | Play | Project Coordinator | Oversees timeline and Gantt chart; coordinates meetings; manages final submission |
| Chahna Paresh Ahuja | Comedy | Technical Lead | Develops and validates GREL transformations; ensures schema consistency |
| Xinran Liu | Tragedy | QA & Documentation Lead | Manages version control; conducts peer review; compiles final documentation |

[Describe briefly how the dataset relates to British-era drama or the cultural focus of your project.]


### 1.4 Project Scope & Research Questions
**Scope of the project:**

This group project focuses on preparing the British dramas dataset for DH analysis and covers data cleaning, documentation, and project management. Data wrangling was carried out using OpenRefine to clean and standardize the data. 
Project management tasks were coordinated through clearly defined roles and shared timelines. GitHub was used as the main platform for collaboration, task tracking, and final submission.

**Individual research questions:**
- [Member 1 research question]  
- [Member 2 research question]  
- [Member 3 research question]

---

## 2. Project Outcomes

### 2.1 Deliverables
- data cleaned
- Project Management Plan
- Project Management Gantt chart
- Documentation and workflow files(grel_scripts, json_history)
- cleaning protocol

### 2.2 Tools & Packages Used
**Software:**  
We used OpenRefine for data cleaning, Python for further analysis, and GitHub for version control.

**Python packages (if applicable):**  
[pandas, numpy, re, etc.]


**Project management tools:**  
We used OpenRefine for cleaning, OneDrive/GitHub for version control, and Notion for task
tracking.

---

## 3. Project Workflow and Documentation

### 3.1 Workflow Summary

The workflow began with acquiring the British Library drama dataset and inspecting it in OpenRefine to identify structural and data quality issues. Data cleaning focused on removing redundant columns, standardizing text, and transforming key metadata fields using facets and GREL. Quality checks were conducted through iterative faceting, clustering, and manual review. Author data was further enriched through WikiData reconciliation. All processes and outputs were documented in GitHub, resulting in cleaned and analysis-ready datasets.

### 3.2 Work Breakdown Structure (WBS)
**Phase 1: Initiation and Protocol Definition (13 Oct – 26 Oct)**  
A shared cleaning and standardization protocol is defined, covering column selection, author name
normalization, date extraction, handling of missing values, and character encoding. 
We set up the collaborative working environment, including shared repositories and agreed
communication channels.

**Phase 2: Distributed Data Cleaning (27 Oct – 23 Nov)**  
During this phase, each member cleans one spreadsheet using OpenRefine, strictly following the shared protocol. Clustering functions and GREL transformations are applied to address inconsistencies. 

**Phase 3: Quality Assurance and Integration (24 Nov – 1 Dec)**  
Quality assurance is carried out through peer review and semi-automated sampling of approximately 10% of the
records in each dataset. 

**Phase 4: Documentation & Reporting**  
OpenRefine operation histories (JSON) and GREL scripts are compiled, and the final cleaned datasets and documentation package are prepared.

### 3.3 Team Roles & Responsibilities
- **Project Coordinator: Liangyu Gan**
- **Data Lead: Chahna Paresh Ahuja**
- **Documentation Lead: Xinran Liu** 

We utilize OpenRefine for cleaning, OneDrive/GitHub for version control, and Notion for task
tracking. Weekly synchronization meetings complement real-time messaging

### 3.4 Project Schedule (Gantt Chart) 
See deliverables(Project_Mangement/PM_Gantt_Chart.xlsx) for more details

---

## 4. Documentation & Collaboration

### 4.1 Documentation Practices

To preserve the original data for comparison, we keep the original columns while creating new columns for cleaned data: Columns marked with (o) represent the original values, while those indicated by (n) contain their cleaned or standardised counterparts.

The summary of our protocol framework as as follows: 

**Null Handling:**	
- Keep empty cells; do not delete rows

**General Standards:**
- Convert all text to UTF-8
- Lowercase and trim whitespace
- Retain essential columns: DOM ID, Author, Title, Imprint, Editions
- Remove non-informative columns: DDC, Language, Country

More details are shown in the deliverables: workflow.md
### 4.2 Collaboration & Communication

The project was coordinated through weekly online meetings and continuous communication via a messaging group. OpenRefine was used for data processing, GitHub and OneDrive for version control and file sharing, and Notion for task tracking. Shared documents supported collaboration and ensured consistent project documentation.

### 4.3 Connection to Individual Assignment
[Note that Task 2 builds on this dataset and includes personal analysis and a reflective report.]

---

## 5. Folder Structure

---

## 6. Citation / Licensing (Optional)
[Insert dataset license, citation, or reuse guidelines if relevant.]

---

## 7. Acknowledgements (Optional)
[Add any acknowledgements for tools, instructors, or collaborators.]
