# Batch-Based-ETL-Pipeline-Visualization

## Overview
This project demonstrates a **batch-based ETL (Extract, Transform, Load) pipeline** using **AWS services**. The pipeline reads data from an **S3 bucket**, performs **data integrity checks and transformations** using **AWS Glue**, and loads the transformed data into an **Amazon RDS** instance.

## Architecture
The architecture consists of the following AWS services:

- **AWS Lambda**: Triggers the ETL process and performs initial data processing.
- **AWS Glue**: Handles data transformations and prepares it for loading.
- **Amazon S3**: Stores raw and processed data.
- **Amazon RDS**: Stores the final transformed data.
- **Amazon DynamoDB**: Logs job executions and audits.

##  Project Structure
##  Setup Instructions

### 1.IAM Roles
- Create necessary **IAM roles** with appropriate **S3, Glue, Lambda, and RDS permissions**.

### 2.S3 Buckets
- Create **source and processed data buckets** in Amazon **S3**.

### 3.RDS Instance
- Set up an **Amazon RDS** instance and ensure it is **publicly accessible or within VPC**.

### 4.DynamoDB Table
- Create a **DynamoDB table** for logging and auditing.

### 5.AWS Glue Job
- Set up an **AWS Glue job** using the provided `ETL_Job_to_RDS.py` script.

### 6.Lambda Function
- Deploy the **Lambda function** using the `lambda_function.py` script.

##  Running the Pipeline

1. **Upload Data**  
   - Upload the raw data to the **source S3 bucket**.

2. **Trigger Lambda**  
   - Manually trigger the **Lambda function** or use a **CloudWatch event**.

3. **Monitor Glue Job**  
   - Check the **AWS Glue job** logs to ensure successful execution.

4. **Query RDS**  
   - Validate the **transformed data** in the **RDS database**.

## 🏁 Conclusion
This project provides a **comprehensive example** of setting up a **batch-based ETL pipeline** using AWS services. It demonstrates the **integration of multiple AWS components** for seamless data processing and analytics.

---

### 🛠 Technologies Used:
- **AWS Lambda**
- **AWS Glue**
- **Amazon S3**
- **Amazon RDS**
- **Amazon DynamoDB**
- **Python**
- **Boto3**
