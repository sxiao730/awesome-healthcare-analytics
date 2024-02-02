# awesome-healthcare-analytics

This repository is a curated resource guide designed to help data analysts understand the healthcare (mainly for U.S.), focusing on the structure of healthcare data and relevant reference files.

## Table of Contents
- [Understanding Healthcare Data](#understanding-healthcare-data)
  - [Types of Healthcare Data](#types-of-healthcare-data)
  - [Data Governance and Compliance](#data-governance-and-compliance)
  - [Reference Files for Organizing Healthcare Data](#reference-files-for-organizing-healthcare-data)
- [Data Formats and Standards](#data-formats-and-standards)
- [Additional Resources](#additional-resources)


## Understanding Healthcare Data

### Types of Healthcare Data
- **Clinical Data**: Patient health information, treatment records, medical history.
- **Claims Data**: Insurance claim information, billing details.
- **Pharmaceutical Data**: Drug prescriptions, medication adherence data.
- **Patient Demographics**: Age, gender, ethnicity, socio-economic status.


### Data Governance and Compliance
- [**HIPAA (Health Insurance Portability and Accountability Act)**](#https://www.hhs.gov/hipaa/for-professionals/index.html): a U.S. law that sets national standards to protect sensitive patient health information from being disclosed without the patient's consent or knowledge.
- [**GDPR (General Data Protection Regulation)**](#https://gdpr.eu/recital-53-processing-of-sensitive-data-in-health-and-social-sector/): a comprehensive data protection law in the EU that mandates strict privacy and security measures for personal data, significantly impacting healthcare by requiring robust protection and responsible handling of patient information.

### Reference Files for Organizing Healthcare Data

#### ICD Codes (International Classification of Diseases)
- **Description**: A global diagnostic tool developed by the World Health Organization (WHO) for epidemiology, health management, and clinical purposes, standardizing the reporting of diseases and health conditions.
- **Purpose**: Used for standardized diagnosis coding, disease classification, and billing processes.
- **Update Frequency**: annually.
- **Data Format**: Alphanumeric codes.
- **Subtypes**:
  - **ICD-9-CM(Clinical Modification)**: Used historically in U.S. since 1979 and being replaced by ICD-10(below) in October 2015. The codes are mostly numeric between 3-5 digits long with a few exceptions with leading alphabets. 
    - **Expected Value Example**: 250.00 (Type 2 diabetes without complication).
  - **ICD-10-CM (Clinical Modification)**: Adopted in the U.S. in October 2015 systematically for diagnosis coding, providing a detailed classification of diseases and health-related problems. It consists of alphanumeric codes that are typically 3 to 7 characters in length.
    - **Expected Value Example**: E11.9 (Type 2 diabetes mellitus without complications).
  - **ICD-10-PCS (Procedure Coding System)**: Used for **inpatient** procedures in U.S. hospitals, describing surgical, medical, and diagnostic services.Outpatient procedures are coded under CPT.
    - **Expected Value Example**: 0HDBXZZ (Excision of liver, percutaneous endoscopic approach).
  - **ICD-11**: The latest version, introduced with a more flexible digital health structure and detailed information. U.S. has not adopted it as of 2024.
    - **Expected Value Example**: 5A11.2 (Type 2 diabetes mellitus without complications).
- [Learn More About ICD Codes](#https://www.cms.gov/medicare/coding-billing/icd-10-codes/icd-10-resources)
- [ICD-10-CM files download](#https://www.cdc.gov/nchs/icd/comprehensive-listing-of-icd-10-cm-files.htm)
- [Latest News about ICD-10 codes](#https://www.cms.gov/medicare/coding-billing/icd-10-codes/latest-news)

#### General Equivalence Mappings (GEMs)
- **Description**: A set of mappings developed to assist with the transition from ICD-9-CM to ICD-10-CM and ICD-10-PCS coding systems. The GEMs between ICD-10 (WHO version) and ICD-10-CM(U.S. diagnoses) is in development as of 2024.
- **Purpose**: Helps coders, health care providers, and researchers convert data from ICD-9-CM to the more detailed ICD-10 system, supporting data continuity and comparability.
- **Update Frequency**: annually. 
- **Data Format**: GEMs files contain tables mapping ICD-9-CM codes to their most appropriate ICD-10 equivalents (and vice versa), with each mapping typically represented as a pair of ICD-9 and ICD-10 codes.
- [2018 ICD-10-CM and GEMs Download](#https://www.cms.gov/medicare/coding-billing/icd-10-codes/2018-icd-10-cm-gem) 

#### Clinical Classifications Software Refined (CCSR)
- **Description**: An adaptation of ICD-10 codes into clinically meaningful categories, facilitating healthcare analysis and research.
- **Purpose**: Simplifies complex ICD-10 diagnoses or procedure codes for easier analysis in epidemiology, healthcare resource utilization, quality and cost analysis, and more. It aggregates more than 70,000 ICD-10-CM diagnosis codes into over 530 clinically meaningful categories and more than 80,000 ICD-10-PCS procedure codes into over 320 clinically meaningful categories. 
- **Update Frequency**: Regularly updated to reflect changes in medical knowledge and coding practices.
- **Data Format**: Grouped categories derived from alphanumeric ICD-10 codes.
- **Application**: Used in various healthcare research domains to understand trends, patterns, and anomalies in healthcare data.
- **Accessibility**: Available to healthcare researchers, analysts, and policymakers for data-driven decision-making.
- [Learn More About CCSR](#https://hcup-us.ahrq.gov/toolssoftware/ccsr/ccs_refined.jsp)
- For ICD-9-CM classifications, go to [Clinical Classifications Software (CCS)](#https://hcup-us.ahrq.gov/toolssoftware/ccs/ccs.jsp)

#### DRG (Diagnosis-Related Group)
- **Description**: Originally developed in 1980s to classify hospital cases for expected similar hospital resource use.
- **Purpose**: Used for hospital billing and Medicare reimbursement determinations. They are based on diagnoses, procedures, age, sex, discharge status, and the presence of complications or comorbidities.
- **Update Frequency**: 
- **Subtypes**:
  - **Medicare Severity DRG (MS-DRG)**: used by Medicare for inpatient payment system. Cases are classified into MS-DRGs for payments based on the principal diagnosis, up to 24 additional diagnoses, and up to 25 procedures performed during the stay. A small portion of MS-DRGs are also based on the patient's age, sex, and discharge status.
  - **All Patient DRG(AP-DRG)**:
  - **All Patient, Severity-Adjusted DRGs (APS-DRG)**:
  
- **Data Format**: Numerical codes (e.g., DRG 291 - Heart Failure & Shock with MCC).
- [Learn More About DRG](#drg-link)



#### CPT Codes (Current Procedural Terminology)
- **Description**: Describes medical, surgical, and diagnostic services and procedures.
- **Purpose**: Essential for billing and coding, providing a standardized system for medical procedures.
- **Update Frequency**:
- **Data Format**: Five-digit numeric codes (e.g., 99213 for a standard office visit).
- [Learn More About CPT Codes](#cpt-codes-link)

#### NDC (National Drug Codes)
- **Description**: Unique identifier for human drugs in the United States.
- **Purpose**: Used for pharmacy billing and inventory management, tracking drug prescriptions and utilization.
- **Update Frequency**:
- **Data Format**: 10-digit numeric code in a 4-4-2, 5-4-1, or 5-3-2 format (e.g., 1234-5678-90).
- [Learn More About NDC](#ndc-link)

#### SNOMED CT (Systematized Nomenclature of Medicine -- Clinical Terms)
- **Description**: A comprehensive, multilingual clinical healthcare terminology.
- **Purpose**: Used for clear and consistent clinical documentation and data exchange in EHRs.
- **Update Frequency**:
- **Data Format**: Unique identifiers (Concept IDs) with variable lengths, alphanumeric.
- [Learn More About SNOMED CT](#snomed-ct-link)

#### HCPCS (Healthcare Common Procedure Coding System)
- **Description**: Codes for procedures, equipment, and supplies not covered by CPT.
- **Purpose**: Used in Medicare and other insurance programs for consistent billing and coding.
- **Update Frequency**:
- **Data Format**: Alphanumeric codes, including a single letter followed by four digits (e.g., G0008 for flu vaccination administration).
- [Learn More About HCPCS](#hcpcs-link)

#### RVU (Relative Value Unit)
- **Description**: A system that assigns value to medical services to standardize costs based on time, skill, and resources required.
- **Purpose**: Utilized in calculating physician reimbursement rates, especially in the Medicare Physician Fee Schedule, and widely adopted in other healthcare reimbursement models.
- **Update Frequency**: Quarterly
- **Data Format**: Numerical values, often represented in a table format alongside corresponding medical services. For example, a specific procedure might have a Work RVU of 3.00, a Practice Expense RVU of 1.50, and a Malpractice RVU of 0.30.

- [Learn More About RVU](#rvu-link)

#### ASA Classification (American Society of Anesthesiologists Physical Status Classification System)
- **Description**: A classification system used to assess a patient’s pre-anesthesia medical comorbidities.
- **Purpose**: Helps in estimating anesthesia risk and planning patient care by providing a standardized way to communicate patient health status.
- **Update Frequency**: Revised as needed, based on updates in clinical practice guidelines and anesthesiology research.
- **Data Format**: Categorical scale ranging from ASA I to ASA VI. For example, ASA I indicates a healthy patient, ASA II a patient with mild systemic disease, and ASA III a patient with severe systemic disease.
- [Learn More About ASA Classification](#asa-link)


#### APC (Ambulatory Payment Classification)
- **Description**: A classification for outpatient services.
- **Purpose**: Determines reimbursement for outpatient services under Medicare.
- **Update Frequency**: 
- **Data Format**: Numerical codes (e.g., APC 5072 - Level 2 Excision/Biopsy).
- [Learn More About APC](#apc-link)

#### HCC (Hierarchical Condition Categories)
- **Description**: A risk adjustment model predicting future healthcare costs.
- **Purpose**: Used in Medicare Advantage for adjusting payments based on patient risk.
- **Update Frequency**: 
- **Data Format**: Categorical codes (e.g., HCC 19 - Diabetes without Complication).
- [Learn More About HCC](#hcc-link)

#### NPI (National Provider Identifier)
- **Description**: A unique identifier for healthcare providers in the U.S.
- **Purpose**: Identifies healthcare providers in standard transactions like healthcare claims.
- **Update Frequency**: N/A (static per provider, updates as provider information changes).
- **Data Format**: 10-digit number (e.g., 1234567890).
- [Learn More About NPI](#npi-link)

#### LOINC (Logical Observation Identifiers Names and Codes)
- **Description**: Identifiers for health measurements, observations, and documents.
- **Purpose**: Facilitates the exchange of clinical results and data.
- **Update Frequency**: Regularly (approximately biannually).
- **Data Format**: Alphanumeric codes (e.g., 4548-4 - Hemoglobin A1c/Hemoglobin.total in Blood).
- [Learn More About LOINC](#loinc-link)
 
## Data Formats and Standards
- **Electronic Health Records (EHR)**
- **Health Level-7 (HL7)**
- **DICOM (Digital Imaging and Communications in Medicine)**

## Additional Resources

- **Books and Journals**: Publications on healthcare informatics and data management.
- **Online Courses**: Specialized courses in healthcare data analytics.
- **Professional Networks and Conferences**: Join groups like the Health Informatics Society.
- **Healthcare Analytics Software Training**: Learn software like SAS, Tableau, or R.
- **Helpful Links to public datasets**: 
-[National Center for Health Statistics(NCHS)](#https://www.cdc.gov/nchs/index.htm): provides timely and accurate health statistics for the U.S.
-[Healthcare Cost and Utilization Project(HCUP)](#https://hcup-us.ahrq.gov/overview.jsp): a family of healthcare databases and related software tools and products developed to provide a comprehensive overview of U.S. hospital care, including data on utilization, access, charges, quality, and outcomes. It has the largest collection of longitudinal hospital care data in the U.S. beginning in 1988.

---

This guide is intended to provide a foundational understanding for those new to healthcare analytics and will be updated as the field evolves. 
