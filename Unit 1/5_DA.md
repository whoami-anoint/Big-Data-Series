# Unit 1 : 
## Chapter 5: Designing Data Architecture, Data Sources, Quality, Pre-Processing, and Storing

[![Share on Twitter](https://img.shields.io/badge/-Share%20on%20Twitter-blue?logo=twitter&style=flat-square)](https://twitter.com/intent/tweet?text=https%3A%2F%2Fgithub.com%2Fwhoami-anoint%2FBig-Data-Series)
[![GitHub discussions](https://img.shields.io/github/discussions/whoami-anoint/DevOps)](https://github.com/whoami-anoint/Big-Data-Series/discussions)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/whoami-anoint/DevOps)](https://github.com/whoami-anoint/Big-Data-Series/pulls)

## Designing Data Architecture

- **Definition:** Data architecture refers to the structure, organization, and integration of data systems within an organization.
- **Purpose:** It ensures data is collected, stored, and processed effectively to meet business needs.

## Key Components of Data Architecture

1. **Data Collection:** 
   - **Sources:** Identify data sources, both internal and external.
   - **Methods:** Define how data will be collected, e.g., batch processing, real-time streaming.

2. **Data Storage:**
   - **Databases:** Choose suitable database systems (SQL, NoSQL) based on data type and access patterns.
   - **Data Warehouses:** Consider centralized storage for structured data.
   - **Data Lakes:** Store both structured and unstructured data in a scalable repository.

3. **Data Processing:**
   - **ETL (Extract, Transform, Load):** Implement processes to clean, transform, and load data into storage systems.
   - **Streaming Processing:** Enable real-time data processing and analysis.

4. **Data Governance:**
   - **Policies:** Establish data governance policies to ensure data quality, security, and compliance.
   - **Data Catalog:** Maintain a catalog of available data assets.

## Data Sources

- **Internal Sources:** Data generated within the organization, such as transaction systems, CRM, and employee databases.
- **External Sources:** Data from third-party providers, public datasets, social media, and IoT devices.

## Data Quality

- **Definition:** Data quality refers to the accuracy, completeness, consistency, and reliability of data.
- **Importance:** High-quality data is essential for making informed decisions and avoiding errors.

## Methods for Ensuring Data Quality

1. **Data Cleansing:**
   - **Remove Errors:** Identify and eliminate duplicate, incomplete, or inaccurate data.
   - **Standardization:** Ensure data conforms to predefined formats and standards.

2. **Data Validation:**
   - **Validation Rules:** Implement rules to validate data against predefined criteria.
   - **Cross-Field Validation:** Ensure consistency between related data fields.

3. **Data Profiling:**
   - **Analysis:** Profile data to identify anomalies, patterns, and outliers.
   - **Data Quality Score:** Assign scores to assess data quality.

## Data Pre-Processing

- **Definition:** Data pre-processing involves cleaning, transforming, and structuring data to make it suitable for analysis.
- **Tasks:** Data cleaning, normalization, encoding, and feature selection.

## Data Storage

1. **Relational Databases:**
   - **Structure:** Organized in tables with predefined schemas.
   - **Use Cases:** Suitable for structured data and transactional systems.

2. **NoSQL Databases:**
   - **Structure:** Schema-less, accommodating diverse data types.
   - **Use Cases:** Ideal for handling unstructured and semi-structured data.

3. **Data Warehouses:**
   - **Structure:** Optimized for analytical queries with star or snowflake schemas.
   - **Use Cases:** Centralized storage for structured historical data.

4. **Data Lakes:**
   - **Structure:** Store raw and unstructured data in their native formats.
   - **Use Cases:** Suitable for storing and processing large volumes of diverse data types.
