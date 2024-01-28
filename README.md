# awesome-healthcare-analytics

This repository is a curated resource guide designed to help data analysts understand the healthcare world, focusing on the structure of healthcare data and relevant reference files.

## Table of Contents
- [Understanding Healthcare Data](#understanding-healthcare-data)
  - [Types of Healthcare Data](#types-of-healthcare-data)
  - [Data Formats and Standards](#data-formats-and-standards)
  - [Data Governance and Compliance](#data-governance-and-compliance)
- [Reference Files for Organizing Healthcare Data](#reference-files-for-organizing-healthcare-data)
- [Additional Resources](#additional-resources)


## Understanding Healthcare Data

### Types of Healthcare Data
- **Clinical Data**: Patient health information, treatment records, medical history.
- **Claims Data**: Insurance claim information, billing details.
- **Pharmaceutical Data**: Drug prescriptions, medication adherence data.
- **Patient Demographics**: Age, gender, ethnicity, socio-economic status.

### Data Formats and Standards
- **Electronic Health Records (EHR)**
- **Health Level-7 (HL7)**
- **DICOM (Digital Imaging and Communications in Medicine)**
- **LOINC (Logical Observation Identifiers Names and Codes)**

### Data Governance and Compliance
- **HIPAA (Health Insurance Portability and Accountability Act)**
- **GDPR (General Data Protection Regulation)**

## Reference Files for Organizing Healthcare Data

### ICD Codes (International Classification of Diseases)
- **Description**: A global diagnostic tool for epidemiology, health management, and clinical purposes, standardizing the reporting of diseases and health conditions.
- **Purpose**: Used for standardized diagnosis coding, disease classification, and billing processes.
- **Update Frequency**:
- **Data Format**: Alphanumeric codes.
- **Subtypes**:
  - **ICD-9**: Used historically before being replaced by ICD-10 in October 2015. It used a mix of numeric and alphanumeric codes up to 5 characters in length.
    - **Expected Value Example**: 250.00 (Type 2 diabetes without complication).
  - **ICD-10-CM (Clinical Modification)**: Adopted in the U.S. for diagnosis coding, providing a detailed classification of diseases and health-related problems.
    - **Expected Value Example**: E11.9 (Type 2 diabetes mellitus without complications).
  - **ICD-10-PCS (Procedure Coding System)**: Used for inpatient procedures in U.S. hospitals, describing surgical, medical, and diagnostic services.
    - **Expected Value Example**: 0HDBXZZ (Excision of liver, percutaneous endoscopic approach).
  - **ICD-11**: The latest version, introduced with a more flexible digital health structure and detailed information.
    - **Expected Value Example**: 5A11.2 (Type 2 diabetes mellitus without complications).
- [Learn More About ICD Codes](#icd-codes-link)

### Clinical Classifications Software Refined (CCSR)
- **Description**: An adaptation of ICD-10 codes into clinically meaningful categories, facilitating healthcare analysis and research.
- **Purpose**: Simplifies complex ICD-10 codes for easier analysis in epidemiology, healthcare resource utilization, quality and cost analysis, and more.
- **Update Frequency**: Regularly updated to reflect changes in medical knowledge and coding practices.
- **Data Format**: Grouped categories derived from alphanumeric ICD-10 codes.
- **Application**: Used in various healthcare research domains to understand trends, patterns, and anomalies in healthcare data.
- **Accessibility**: Available to healthcare researchers, analysts, and policymakers for data-driven decision-making.
- [Learn More About CCSR](#ccsr-link)


### CPT Codes (Current Procedural Terminology)
- **Description**: Describes medical, surgical, and diagnostic services and procedures.
- **Purpose**: Essential for billing and coding, providing a standardized system for medical procedures.
- **Update Frequency**:
- **Data Format**: Five-digit numeric codes (e.g., 99213 for a standard office visit).
- [Learn More About CPT Codes](#cpt-codes-link)

### NDC (National Drug Codes)
- **Description**: Unique identifier for human drugs in the United States.
- **Purpose**: Used for pharmacy billing and inventory management, tracking drug prescriptions and utilization.
- **Update Frequency**:
- **Data Format**: 10-digit numeric code in a 4-4-2, 5-4-1, or 5-3-2 format (e.g., 1234-5678-90).
- [Learn More About NDC](#ndc-link)

### SNOMED CT (Systematized Nomenclature of Medicine -- Clinical Terms)
- **Description**: A comprehensive, multilingual clinical healthcare terminology.
- **Purpose**: Used for clear and consistent clinical documentation and data exchange in EHRs.
- **Update Frequency**:
- **Data Format**: Unique identifiers (Concept IDs) with variable lengths, alphanumeric.
- [Learn More About SNOMED CT](#snomed-ct-link)

### HCPCS (Healthcare Common Procedure Coding System)
- **Description**: Codes for procedures, equipment, and supplies not covered by CPT.
- **Purpose**: Used in Medicare and other insurance programs for consistent billing and coding.
- **Update Frequency**:
- **Data Format**: Alphanumeric codes, including a single letter followed by four digits (e.g., G0008 for flu vaccination administration).
- [Learn More About HCPCS](#hcpcs-link)

### RVU (Relative Value Unit)
- **Description**: A system that assigns value to medical services to standardize costs based on time, skill, and resources required.
- **Purpose**: Utilized in calculating physician reimbursement rates, especially in the Medicare Physician Fee Schedule, and widely adopted in other healthcare reimbursement models.
- **Update Frequency**: Quarterly
- **Data Format**: Numerical values, often represented in a table format alongside corresponding medical services. For example, a specific procedure might have a Work RVU of 3.00, a Practice Expense RVU of 1.50, and a Malpractice RVU of 0.30.

- [Learn More About RVU](#rvu-link)

### ASA Classification (American Society of Anesthesiologists Physical Status Classification System)
- **Description**: A classification system used to assess a patient’s pre-anesthesia medical comorbidities.
- **Purpose**: Helps in estimating anesthesia risk and planning patient care by providing a standardized way to communicate patient health status.
- **Update Frequency**: Revised as needed, based on updates in clinical practice guidelines and anesthesiology research.
- **Data Format**: Categorical scale ranging from ASA I to ASA VI. For example, ASA I indicates a healthy patient, ASA II a patient with mild systemic disease, and ASA III a patient with severe systemic disease.
- [Learn More About ASA Classification](#asa-link)

### DRG (Diagnosis-Related Group)
- **Description**: Classifies hospital cases for expected similar hospital resource use.
- **Purpose**: Used for hospital billing and Medicare reimbursement determinations.
- **Update Frequency**: 
- **Data Format**: Numerical codes (e.g., DRG 291 - Heart Failure & Shock with MCC).
- [Learn More About DRG](#drg-link)

### APC (Ambulatory Payment Classification)
- **Description**: A classification for outpatient services.
- **Purpose**: Determines reimbursement for outpatient services under Medicare.
- **Update Frequency**: 
- **Data Format**: Numerical codes (e.g., APC 5072 - Level 2 Excision/Biopsy).
- [Learn More About APC](#apc-link)

### HCC (Hierarchical Condition Categories)
- **Description**: A risk adjustment model predicting future healthcare costs.
- **Purpose**: Used in Medicare Advantage for adjusting payments based on patient risk.
- **Update Frequency**: 
- **Data Format**: Categorical codes (e.g., HCC 19 - Diabetes without Complication).
- [Learn More About HCC](#hcc-link)

### NPI (National Provider Identifier)
- **Description**: A unique identifier for healthcare providers in the U.S.
- **Purpose**: Identifies healthcare providers in standard transactions like healthcare claims.
- **Update Frequency**: N/A (static per provider, updates as provider information changes).
- **Data Format**: 10-digit number (e.g., 1234567890).
- [Learn More About NPI](#npi-link)

### LOINC (Logical Observation Identifiers Names and Codes)
- **Description**: Identifiers for health measurements, observations, and documents.
- **Purpose**: Facilitates the exchange of clinical results and data.
- **Update Frequency**: Regularly (approximately biannually).
- **Data Format**: Alphanumeric codes (e.g., 4548-4 - Hemoglobin A1c/Hemoglobin.total in Blood).
- [Learn More About LOINC](#loinc-link)
  
## Additional Resources

- **Books and Journals**: Publications on healthcare informatics and data management.
- **Online Courses**: Specialized courses in healthcare data analytics.
- **Professional Networks and Conferences**: Join groups like the Health Informatics Society.
- **Healthcare Analytics Software Training**: Learn software like SAS, Tableau, or R.

---

This guide is intended to provide a foundational understanding for those new to healthcare analytics and will be updated as the field evolves. 
