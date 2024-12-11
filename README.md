# Class-participation-10-weeks
This repository has all the details of my work that has been done in 10 weeks.

I worked on a 10-week project analyzing employee training and duties data from my university. The project leveraged a variety of AWS services, including CloudWatch and SageMaker, to implement an end-to-end data analytics and machine learning workflow. My primary goal was to provide actionable insights that optimize training strategies, balance duty allocation, and improve employee performance.

The project involved cleaning, transforming, and analyzing the dataset using descriptive and exploratory analysis techniques. It culminated in the development of machine learning models to predict performance outcomes based on training hours and duties assigned.

The Employee Training and Duties Data Analysis project aims to provide a comprehensive understanding of training patterns and duty performance within a university context. Over 10 weeks, extensive data processing and analysis were performed using AWS cloud services to uncover trends, address data quality issues, and generate actionable insights for improving training programs and optimizing resource allocation.

By leveraging Descriptive Analysis and elements of Exploratory Data Analysis (EDA), the project identifies critical patterns, such as training hours across departments and their impact on duty completion rates. The analysis not only highlights existing inefficiencies but also lays the groundwork for data-driven decision-making to enhance employee effectiveness.

Descriptive Analysis: This type of analysis summarizes and describes the main features of a dataset in a structured and straightforward way.

Exploratory Data Analysis (EDA): EDA investigates datasets to find underlying patterns, relationships, and anomalies. It’s more interactive and focuses on uncovering deeper insights.

Breakdown of the components of Descriptive and Exploratory Analysis based on my classwork:

**1. Data Ingestion**

I began by uploading the raw employee data to AWS S3. This ensured centralized storage and easy access for further processing. I organized the data into two distinct buckets:

**Raw Data Bucket:** Contained the unprocessed employee data.

**Transformed Data Bucket:** Used for storing the cleaned and processed data.

This step set the foundation for efficient data handling throughout the project.
![image](https://github.com/user-attachments/assets/45fea0f6-947f-43a8-8e78-ad74c4df2189)

![image](https://github.com/user-attachments/assets/bf7f473d-d39e-427f-b26d-e0bbe8c53e55)


**2. Data Profiling**

Using AWS Glue DataBrew, I performed data profiling to understand the structure and quality of the dataset.
Here’s what I focused on:

Identifying missing values, duplicate records, and outliers in columns like Training Hours, Department, and Duties.

Generating summary statistics such as:

a)Average training hours per department.

b)Frequency of specific duties assigned across departments.

Checking correlations between training hours and employee performance indicators.

The profiling step gave me a clear view of data quality issues and provided insights into key features for analysis.
![image](https://github.com/user-attachments/assets/99689680-256b-40d1-80ea-e69c0f042854)

![image](https://github.com/user-attachments/assets/72377bd9-f5ea-400d-b260-0a4362255898)

![image](https://github.com/user-attachments/assets/b37a252b-6e3b-4917-8c59-e55e40077319)

![image](https://github.com/user-attachments/assets/fcac7d01-ffc8-49b2-ad8f-aca4e8e97a37)

**3. Data Cleaning**

After profiling, I cleaned the data to address the issues identified. This included:

i) Handling Missing Values:

*Imputed missing values in the Training Hours column using the average hours for the respective departments.

*For categorical columns like Department, missing values were filled with "Unknown."

ii) Removing Duplicates:

*Ensured no duplicate employee records remained in the dataset.

iii) Standardizing Data:

*Normalized department names and job duty descriptions to maintain consistency.

The cleaned dataset was stored in the transformed bucket for subsequent steps.

![image](https://github.com/user-attachments/assets/375cc0bf-5789-4a11-923d-e08e579d93b0)

![image](https://github.com/user-attachments/assets/c94b557c-1fbf-4ff6-92c2-700ffe8855d7)

![image](https://github.com/user-attachments/assets/2ae6fd3a-334e-4d45-8cda-03ab77738c6a)

**4. Data Transformation**

In this step, I prepared the data for deeper analysis. I used AWS Glue to create an ETL (Extract, Transform, Load) pipeline to automate data transformations.
Here’s what I accomplished:

i) Grouped employees by department and calculated:

*Total training hours.

*Average training hours per employee.

ii) Aggregated duties to identify the most common responsibilities in each department.

iii) Derived new metrics, such as a training efficiency score, by combining training hours and performance ratings.

The transformed dataset provided a structured view of the data, ready for visualization and reporting.

![image](https://github.com/user-attachments/assets/a1a9040c-b506-4512-9ca9-9ad44affe8f9)

**5. Data Visualization**

Objective:

The goal of data visualization was to translate insights from the data into clear, actionable visual representations. These visualizations made it easier to understand trends, patterns, and relationships in employee training and duties data. 


**6. Final Deliverables**

1. Cleaned Dataset

Formats: Provided in both CSV and Parquet for flexibility.

Content: Imputed missing values, removed duplicates, and standardized categorical fields.

Storage:

AWS S3 for centralized access.

CSV for easy sharing.

Parquet for efficient processing in future analyses.

2. Automated ETL Pipeline

Process:
Extracted raw data from the S3 raw bucket.

Performed transformations like grouping, aggregations, and imputations.

Loaded the cleaned data into a transformed bucket.

Features:

Scalable: Can process new datasets automatically.

Configurable: Allows easy updates to transformation logic.

3. Visualizations

A collection of interactive and static visualizations:

Bar charts, pie charts, heatmaps, and dashboards.

Formats: PNGs for sharing; Tableau dashboards for interactivity.

4. Insights Report

A detailed PDF summarizing:

Trends and patterns in employee training and duties.

Department-wise and role-specific insights.

Correlations between training and performance.

Includes recommendations for:

Investing in targeted training programs.

Balancing duty distribution among roles.

By delivering these outputs, I ensured the project not only provided actionable insights but also a robust framework for future data analyses and decision-making processes.

In the later weeks, we worked on Amazon CloudWatch

Key Features of Amazon CloudWatch

Metrics Monitoring:

Tracks key metrics from AWS services like EC2, S3, RDS, and Lambda.
Allows you to set custom metrics for application-specific monitoring.

Example: Monitor CPU utilization, disk usage, or request counts.
Log Management:

Collects and stores log data from services like EC2, Lambda, and ECS.

Allows searching, filtering, and analyzing log data in near real-time.

Example: Debugging application errors by reviewing application logs.

Alarms:

Enables you to set thresholds for metrics and trigger actions if thresholds are breached.

Example: Create an alarm to notify if CPU usage exceeds 80% for 5 minutes.
Dashboards:

Provides customizable dashboards to visualize metrics and logs.

Example: Combine CPU, memory, and disk utilization into a single view for an EC2 instance.

Event Management:

Tracks AWS resource changes and notifies you about operational events.

Example: Automatically trigger an action if an EC2 instance state changes to "stopped."

Insights:

Includes CloudWatch Logs Insights for advanced log analysis.

Provides anomaly detection for unusual behavior in metrics.

![image](https://github.com/user-attachments/assets/895eed2c-6a61-4d83-a3e1-c918d90941af)

In the last week, we have used SageMaker

Amazon SageMaker is a fully managed service that provides tools for building, training, deploying, and managing machine learning (ML) models at scale. It eliminates the complexity of ML workflows, enabling users to focus on data science and experimentation.
![Week 10](https://github.com/user-attachments/assets/97d84065-abd7-44c9-ad1a-9aa25d95cde7)

This project demonstrated the power of leveraging AWS tools for data analytics and machine learning. The descriptive and exploratory analyses provided deep insights into training and duty allocation patterns, while the machine learning model offered predictive capabilities to enhance decision-making.

The integration of tools like CloudWatch for monitoring and SageMaker for ML workflows ensured efficiency, scalability, and accuracy throughout the project. The insights derived from the analysis can help my university optimize training programs, balance workloads, and ultimately improve employee performance.

Through this project, I gained hands-on experience with end-to-end data workflows, AWS services, and machine learning, which are critical skills for any data analyst or machine learning engineer.
