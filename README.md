<h1 align="center">City of Vancouver Project Part 2 Assignemnt</h1>

___

# Project Description: Exploratory Analysis of Lost and Found Animal Records
In this assignment I will be describing the details of the City of Vancouver project mainly about the Data concerns of the Data Analytic Platform (DAP) implemented previously. For this assignment I used the processed and published dataset information from website [City of Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/dataset/animal-control-inventory-lost-and-found/export/?disjunctive.breed&disjunctive.color&sort=date&refine.date=2023).

## Project Title: Understanding the process of ensuring Data Protection, Governance, & Monitoring for DAP
The primary need of this project is to conduct a exploratory analsis of the process of providing and ensuring the Data Protection, Governance, & Monitoring for DAP model i developed in the previous assignment. This project mainly deals with the process after the basic model fo DAP is developed and implemented. This project mainly discusses on the various tools and technologies used in providing Data Protection, Governance, & Monitoring for DAP model developed.
## Project Objective:
* Designing and implementing the Data Protection options for DAP model.
* Designing and implementing the Data Governance options for DAP model.
* Designing and implementing the Data Monitoring options for DAP model.
## Datasets
* There are two datasets wi=hich i will be using here.
* The first dataset is **"Found Inventory Dataset"**, it contains information on animals found, with columns such as:
  * SNO: Serial Number
  * Breed: Animal breed
  * Color: Color description
  * Date: Date when the animal was found
  * Name: Name of the animal
  * Sex: Animal's sex
  * State: Status (Yes indicating matched or found)
  * [2024_animal_control_Found_inventory.xlsx](https://github.com/user-attachments/files/16974871/2024_animal_control_Found_inventory.xlsx) contains the information of this match found dataset.
* The second datset is **"Lost and Found Inventory Dataset"**, it Contains details on lost animals, with similar columns, including:
  * SNO: Serial Number
  * Breed: Animal breed
  * Color: Color description
  * Date: Date of the record
  * Name: Name of the animal
  * Sex: Animal's sex
  * State: Lost or Found status
  * [2024_animal_control_inventory_lost_and_found.xlsx](https://github.com/user-attachments/files/16974850/2024_animal_control_inventory_lost_and_found.xlsx) contains the information of this lost and found inventory dataset.
* Using both these datasets I will be planning my DAP for City of Vancouver.
## Methodology:
* The process of Designing and implementing the Data Protection, Governance, & Monitoring for DAP model is complex.
* This involves 4 different steps. I will be explaining on these steps in detail below:
### Step 14: Data Enriching
* This is the step where we are going to define the whole architecture of the DAP.
* This step includes enhancing my dataset by adding additional information from external or related sources.<br>
![step014](https://github.com/user-attachments/assets/b9c3405c-0a19-475c-990f-2a1fd4a0fa66)
* The Above Image contains information of the DAP "**Data Enriching**" step.<br>
![step014-2](https://github.com/user-attachments/assets/4032d5e0-9a5e-40ce-92e6-c362a7df1378)
* The Above Image contains information of the DAP "**Data Enriching**" step.<br>
![step014-3](https://github.com/user-attachments/assets/130e6f76-7fb2-4eb2-8360-448176b7ec69)
* The Above Image contains information of the DAP "**Data Enriching**" step.
### Step 15: Data Protection
* This **Data Protection** involves safeguarding sensitive information from unauthorized access, misuse, or breaches.
* It is critical when handling datasets that may include personal information about pet owners or internal records.
* For this we are creating KMS keys for encryption and decryption of data inthe S3 buckets.<br>
![fig14](https://github.com/user-attachments/assets/7f0f3811-d1ff-4e36-8d5c-77517dc8971e)
* The above image shows my newly created KMS key information.
* I am also enabling the Bucket Versioning and encrypting using the KMS key i created for both my S3 bucket and S3 backup bucket I created.<br>
![fig15](https://github.com/user-attachments/assets/15d46b70-9a5b-48eb-81a9-34b3e7e38d4d)
* The above images shows my S3 bucket properties information.<br>
![fig16](https://github.com/user-attachments/assets/c58cb083-03e4-4d23-a4d2-05264aeafdb9)
* The above images shows my S3 backup bucket properties information.<br>
* I am also configuring the backup option by doing a mirroring replication of my S3 bucket with another bucket.<br>
![fig17](https://github.com/user-attachments/assets/d11c43b3-91ca-44f2-a4fe-6167c39f1bf3)
* The above image shows my replication information.
### Step 16: Data Governance
* Data governance refers to the policies, standards, and practices for managing and using data in a way that aligns with organizational goals and regulatory requirements.
* It ensures the quality, integrity, and security of data across its lifecycle.
* For this first I am creating Trusted folder where i can store data which has been masked to protect sensitive data information.<br>
![fig27](https://github.com/user-attachments/assets/42a7f45d-2a77-4427-b4a0-6502f05af6a7)
* The above image shows the Trusted folder created.
* I them create an ETL to convert the raw data available using ETL to identify and mask the sensitive information.<br>
![fig28](https://github.com/user-attachments/assets/e0fb6123-ac94-41f1-b9d8-1c8003ee55a6)
* The above image shows the ETL pipeline for saving the trusted information from raw data.
* I then move on to storing the information retrieved from ETL into the trusted folder.<br>
![fig29](https://github.com/user-attachments/assets/ca5e6f77-1ac7-4b88-8389-86f9df496390)
* The above image shows the resultant information stored as csv file in trusted folder.
### Step 17: Data Monitoring
* Data monitoring involves continuously tracking data usage and access to ensure compliance with governance policies, detect potential breaches, and maintain data integrity.
* Here we will be using "**AWS CloudWatch**" service to create a dashboard based on our needs.<br>
![fig39](https://github.com/user-attachments/assets/c2b37041-9b1f-4b57-bb10-98a26f017e8c)
* The above image displays the dashboard of AWS CloudWatch
* I then move on to create a user activity trail using the "**AWS CloudTrail**" service, so that i can track user activities for any anomalies.<br>
![fig40](https://github.com/user-attachments/assets/8b022324-8eb3-4b4e-b7bc-854ad8d49b3c)
* The above image shows the cloud trail created for tracking user activity.<br>
![fig41](https://github.com/user-attachments/assets/0af61951-03a0-44ae-8a78-a303ea702d14)
* The above image displays the information of cloud trail saved in S3.
