# Ex. No. 5 — Use Autopsy to Create a Case and Import Evidence

## Digital Forensics Lab

### Aim / Description

**Autopsy** is an open-source digital forensics platform used for analyzing and extracting data from digital devices.

This experiment demonstrates how to use Autopsy to create a forensic case, import evidence, analyze artifacts, and generate a forensic report.

---

## Evidence Files

The evidence files used for this experiment are:

* `4Dell Latitude CPi.E01`
* `4Dell Latitude CPi.E02`

---

# Procedure

## 1. Installation

### Download and Install Autopsy

Download and install **Autopsy** from its official website.

Follow the installation instructions according to the operating system being used.

---

## 2. Starting a New Case

### Open Autopsy

Launch the Autopsy application after installation.

### Create a New Case

1. Click **New Case**.
2. Enter the **Case Name**.
3. Select the **Location** where the case data will be stored.
4. Enter the required case details such as:

   * Case Number
   * Examiner's Name
   * Other relevant information
5. Click **Next**.

---

## 3. Adding a Data Source

### Choose the Type of Data Source

After creating a case, Autopsy prompts you to add a data source.

Autopsy supports different types of data sources, including:

* Disk Images
* Directories
* Logical Files
* Local Disks

### Select the Data Source

Browse to the location of the evidence file or disk that needs to be analyzed.

Supported examples include:

* `.E01`
* `.dd`
* `.raw`
* Physical Disk
* Directory

For this experiment, import:

```text
4Dell Latitude CPi.E01
4Dell Latitude CPi.E02
```

### Configure Ingest Modules

Autopsy provides several analysis modules that can be enabled or disabled depending on the investigation requirements.

Examples include:

* File Type Identification
* Keyword Search
* Hash Lookup
* Other available analysis modules

Select the required modules and click **Next** to start the analysis.

---

# 4. Initial Analysis and Overview

## Ingest Progress

As Autopsy processes the data source, the ingestion progress can be monitored from the application interface.

## Explore the Resulting Artifacts

Autopsy automatically categorizes the findings into different artifact categories, including:

* Web Artifacts
* File System Metadata
* Communication Records

## Use the Tree Viewer

The left-side tree viewer allows the investigator to navigate through different sections of the evidence.

Examples include:

* File System
* Web History
* Email
* Other forensic artifacts

---

# 5. Detailed Analysis

## Keyword Search

The **Keyword Search** module can be used to search for specific words or phrases within the evidence.

You can:

* Use pre-configured keyword lists
* Enter custom keywords
* Search for investigation-specific terms

---

## File Analysis

Navigate through files and folders using the **File Types** or **File System** sections.

You can:

* Open files
* View files
* Examine file information
* Export files for further analysis

---

## Timeline Analysis

Use the **Timeline** module to visualize events according to their timestamps.

Timeline analysis can help investigators understand and track user activity over time.

---

## Hash Analysis

Hash analysis can be used to compare file hashes against known databases.

This helps identify:

* Known good files
* Known bad files
* Previously identified files

---

# 6. Reporting

## Generate a Report

After completing the analysis:

1. Click **Generate Report** from the toolbar.
2. Select the required report format.
3. Choose the information and artifacts that should be included.
4. Generate the report.

Possible report formats include:

* HTML
* CSV
* Excel
* Other supported formats

---

## Export Findings

Individual files or forensic artifacts can be exported for:

* Inclusion in the final report
* Further forensic examination
* Evidence preservation

---

## Final Review

Review the generated report carefully to ensure that all relevant information has been included.

Save or print the report for use in the forensic case.

---

# 7. Case Closure

## Close the Case

Once the investigation has been completed, close the case within Autopsy.

## Archiving

Ensure that all relevant:

* Evidence
* Reports
* Case information

are properly archived according to the organization's policies.

---

# 8. Advanced Features (Optional)

## Custom Ingest Modules

Autopsy supports custom ingest modules that can be added when specific analysis capabilities are required beyond the default modules.

## Collaboration

Autopsy can be configured to support multi-user cases when working as part of a team environment.

---

# Result

The forensic evidence was successfully imported into **Autopsy**, analyzed using various forensic modules, and the relevant findings were reviewed and prepared for reporting.

## Output Screenshots
<img width="1005" height="622" alt="Screenshot 2026-08-30 221654" src="https://github.com/user-attachments/assets/0bc55c95-3137-4aea-b93c-dece410197e1" />
<img width="1920" height="1080" alt="Screenshot 2026-08-30 221735" src="https://github.com/user-attachments/assets/8eebe6bf-a849-4e9c-8eae-29c06ad2d751" />
<img width="1920" height="1080" alt="Screenshot 2026-08-30 221750" src="https://github.com/user-attachments/assets/3727a70f-f9d8-4f8c-9a71-3c84315968a0" />
<img width="1920" height="1080" alt="Screenshot 2026-08-30 221916" src="https://github.com/user-attachments/assets/05141bca-e4f4-4a3c-8522-25fc8658c3b6" />
<img width="1920" height="1080" alt="Screenshot 2026-08-30 221956" src="https://github.com/user-attachments/assets/2f52bd59-e8c3-497b-9065-d0787b2c759e" />
<img width="1920" height="1080" alt="Screenshot 2026-08-30 222006" src="https://github.com/user-attachments/assets/d384fd55-be26-4258-a7e8-69b8135a7035" />
<img width="1920" height="1080" alt="Screenshot 2026-08-30 222205" src="https://github.com/user-attachments/assets/f2191de6-1472-430d-a8fa-47bd3062b22e" />
<img width="1920" height="1080" alt="Screenshot 2026-08-30 222232" src="https://github.com/user-attachments/assets/c1db6f00-04e1-4c83-842b-74f67dd05cc2" />
