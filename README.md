# Uber Business Intelligence Engineering Project via GCP
### The project is integrated and learned from many sources. This is a way of working with a Business Intelligence role for end-to-end projects in the data industry.
## [Final Dashboard](https://lookerstudio.google.com/reporting/fe1cef1c-cb6e-4434-aeb8-828900b8f1a5)

## Project Scope: 

* Design and implement an end-to-end **ETL data pipeline** integrating Uber ride-sharing data into **Google Big Query data warehouse** by utilizing Python, Google Cloud Storage, Google compute engine.
* Construct a **comprehensive STAR data model** in Google Big Query with QuickDBD and SQL, optimizing data analytics processes.
* Develop an **interactive dashboard** using Google Looker Analytics to visualize key Uber KPIs such as driver productivity, rider retention, and revenue while enabling dynamic filtering capabilities for business users.

### Technologies: 
**Technology used:** SQL, Python, QuickDBD, Google Cloud Storage, Google compute engine, Google Big Query, Google Looker Analytics

### Services:
* Cloud Storage: Provides online file storage and allows users to retrieve data from the cloud, making it accessible from anywhere.
* Compute Engine: Offers a cloud computing service that provides virtual machines for running applications.
* Big Query: A cloud-based data warehouse designed for storing, analyzing, and querying large datasets.
* Looker: A web-based tool specializing in data visualization and reporting.

## Key Learning

- Leveraging Python and GCP for a comprehensive end-to-end ETL pipeline.
- Implementing a robust STAR data model in Google Big Query for optimized data analysis.
- Designing an interactive dashboard with Google Looker Analytics for dynamic data visualization and filtering capabilities.
- Incorporating effective data preprocessing techniques for efficient and accurate data analysis.

## Key Struggles

- Addressing potential challenges in data integration and management throughout the ETL process.
- Balancing the complexities of data transformation with the need for maintaining data integrity and accuracy.
- Ensuring seamless communication and compatibility between various components within the GCP ecosystem.
- Managing and optimizing computational resources to meet the demands of large-scale data processing.

## Key Insight

- Unveiling critical insights into key Uber KPIs, including driver productivity, rider retention, and revenue generation, through dynamic and interactive data visualization.
- Empowering business users with the ability to make data-driven decisions through user-friendly and customizable dashboards.
- Highlighting the significance of leveraging comprehensive data analytics tools for deriving actionable business intelligence and strategic insights.

## Architecture
![image](https://github.com/user-attachments/assets/a6cd4ad7-67ff-4fc3-9cf1-bcee990371d6)



## Dataset Used
* [Dataset](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)
* [Data Dictionary](https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_yellow.pdf)

## Step 1: Data Modelling 
**Fact vs. Dimension tables**
* **Fact Table: (changing)**
  * Contains quantitative measures or metrics that are used for analysis
  * Typically contains foreign keys that link to dimension tables
  * Contains columns that have high cardinality and change frequently
  * Contains columns that are not useful for analysis by themselves, but are necessary for calculating metrics

* **Dimension Table: (static)**
  * Contains columns that describe attributes of the data being analyzed
  * Typically contains primary keys that link to fact tables
  * Contains columns that have low cardinality and don't change frequently
  * Contains columns that can be used for grouping or filtering data for analysis

### The Star-Schema data model:
![image](https://github.com/user-attachments/assets/ad91c7a7-c433-49de-9667-fdc14f2c1e02)


## Step 2: Store Data in Google Cloud Storage and set up Google Cloud Service
* **Google Cloud Storage**
  * Create a new Google Project → Create a Google Cloud Bucket → Load data into Google Cloud Storage → Edit Access to Public
   
* **Google Cloud Compute Engine**
  * Create a new Instance → Chose region, configuration → Run SSH
  * Edit Firewall:
    * Create new Firewall rules
    * Sources IPV4 address 0.0.0.0/0
    * Port: Result from the Compute Engine
* Run External IP address: port
## Step 3: Write Transformation Code and ETL Script
* Python Transformation Code (Jupiter Notebook) can be found [here](https://github.com/Namdataa/Uber-Analytics/blob/main/Notebook%20(About%20ETL)/Uber%20Data%20Transform.ipynb)
* Python ETL Code can be found [here](https://github.com/Namdataa/Uber-Analytics/blob/main/Notebook%20(About%20ETL)/ETL%20to%20BigQuery.ipynb)
* Get API File connect to BigQuery
  * Go to GCP API → Create new credential → Service Account → Create new keys → Download keys
  * Code connect to BigQuery in [here](https://github.com/Namdataa/Uber-Analytics/blob/main/Notebook%20(About%20ETL)/ETL%20to%20BigQuery.ipynb)
 
## Step 4: Write SQL Queries on Google Big Query
* SQL Queries can be found [here](https://github.com/Namdataa/Uber-Analytics/blob/main/Create%20table%20Analystics.sql)

## Step 5: Load data into Google Looker Studio and create a Dashboard 
* The last step is to Develop an interactive dashboard using Google Looker Analytics to visualize key Uber KPIs such as driver productivity, rider retention, and revenue while enabling dynamic filtering capabilities for business users
* [**Result Dashboard**](https://lookerstudio.google.com/reporting/fe1cef1c-cb6e-4434-aeb8-828900b8f1a5)
