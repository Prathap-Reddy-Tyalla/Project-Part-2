<h1 align="center">AWS Assignment - 2 </h1>

___

# Project Description: Descriptive Analysis of 311 Contact Center
This assignment is continuation for improvement of the [DAP Design & Implementatio For City of Vancouver](https://prathap-reddy-tyalla.github.io/Project-part-1/) project using the datasets taken from  website [City of Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/dataset/animal-control-inventory-lost-and-found/export/?disjunctive.breed&disjunctive.color&sort=date&refine.date=2023). This project concentrates on details of protection, governance and monitoring of DAP.

## Project Title: Data Protection, Governance, & Monitoring for DAP
This project concentrates on details of protection, governance and monitoring of DAP. As these 3 are vital thing that must be ensured for all the current project. Lack of any of these three aspects would result in the project execution lacking or even failure of the project. We will see how below:
## Project Objective:
* Data Protection design and implementation.
* Data Governance design and implementation.
* Data Monitoring design and implementation.
## Datasets
* The Dataset used is taken from [City of Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/dataset/3-1-1-contact-centre-metrics/information/) for the category of "3-1-1 contact centre metrics"<br>
[cummulative-3-1-1-contact-centre-metrics.xlsx](https://github.com/user-attachments/files/17020770/cummulative-3-1-1-contact-centre-metrics.xlsx)
## Methodology:
* The process involves 3 different steps explained in detail below:
### Step 15: Data Protection
* This **Data Protection** providing protectio to data in many ways like encryption or access granting or other methods.<br>
![step 15-01-kms key creation](https://github.com/user-attachments/assets/9baae4bf-54b8-4de2-91b8-fcdf9f673fef)
* The above image shows how I created a KMS key for encryption and decryption of data.<br>
![step 15-01-kms key information](https://github.com/user-attachments/assets/9ea80654-31a3-4c70-86c5-4a9be409c061)
* The above image shows configuration etails of the KMS key.<br>
![step 15-02-S3 bucket properties for encryption and bucket versioning](https://github.com/user-attachments/assets/43ccdf8c-fe75-46cf-9ad7-59e0b09e414e)
* The above image shows the changes made to enable encryption and bucket versioning for S3 bucket.<br>
![step 15-02-S3 bucket replication rule information](https://github.com/user-attachments/assets/2947229f-1f66-4a8a-b7c2-47464b6b5b46)
* The above image shows the changes made to enable replication rule for S3 bcket.<br>
![step 15-02-S3-Backup bucket properties for encryption and bucket versioning](https://github.com/user-attachments/assets/6639ae34-08a5-4dd7-a6b6-39293e96227d)
* The above image shows the changes made to enable encryption and bucket versioning for S3 backp bucket.<br>
### Step 16: Data Governance
* Data governance refers to the policies, standards, and practices for managing and using data in a way that aligns with organizational goals and regulatory requirements to ensures the quality, integrity, and security of data across its lifecycle.
![step 16-01-trusted folder creation in S3 bucket](https://github.com/user-attachments/assets/bd8281fa-1c11-4176-b18a-6a32f4145a8f)
* The above image shows the trusted folder created in S3 bucket.<br>
![step 16-02-etl design](https://github.com/user-attachments/assets/1c43b6bb-e499-40d1-b86e-beaa3bc8cb96)
* The above image shows the ETL designed to mask sensitive data and store it in trusted folder.<br>
![step 16-02-etl output](https://github.com/user-attachments/assets/c6e30971-5a43-45c4-bd93-57b2a74fb538)
* The above image shows the results of eTL design.<br>
![step 16-03-workflow details](https://github.com/user-attachments/assets/fda485fa-c208-4af7-9ac9-3016fbae148c)
* The above image shows the workflow designed.<br>
### Step 17: Data Monitoring
* Data monitoring involves continuously tracking data usage and access to ensure compliance with governance policies, detect potential breaches, and maintain data integrity.
![step 17-01-alarm creation in cloudwatch](https://github.com/user-attachments/assets/520e08ea-824f-4eb3-a517-4532b2a83481)
* The above image shows alarm information.<br>
![step 17-01-dashboard creation in cloudwatch](https://github.com/user-attachments/assets/dc128e27-c2ff-4374-bb5c-cdcb509d4c17)
* The above image shows the dashboard.<br>
![step 17-02-cloudtrail created to track user activity](https://github.com/user-attachments/assets/5ae5a7ed-8aed-45ee-b45d-26f36bd33e09)
* The above image shows the cloud trail created.<br>
![step 17-02-s3 bucket created automatically for cloudtrail to track user activity](https://github.com/user-attachments/assets/26df573e-70f0-461a-b200-d26483c13238)
* The above image shows the cloud trail outcome stored in S3 buckets.<br>
