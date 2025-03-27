# Portfolio-Assignment

# Project Description
This research analyzes CUPE 1004 employee salary data and gender distribution using AWS-based processing systems. Data collection from the City of Vancouver website, under the Open Government Licence - Vancouver, underwent thorough ETL (Extract, Transform, Load) procedures to ensure data accuracy and accessibility. AWS Glue, S3, and EC2 were utilized to optimize data profiling, transformation, and storage. The study follows APA guidelines for reporting its methodologies and results, contributing to improved workforce analytics and decision-making. The research provides a descriptive evaluation of CUPE 1004's pay rates and gender distribution, revealing trends that inform employee compensation practices, gender equality, and workforce management.

# Project Title
The analysis utilizes AWS cloud services to interpret workforce pay scales together with gender composition data.

# Objective
The minimum and maximum pay rates for different positions should be studied to understand the salary patterns of CUPE 1004 members.
As part of the investigation analyze the gender representation within the workforce while tracking differences between male and female staff across job categories.
The organization should determine the existence of gender-based income differences while focusing on higher-paying roles and document all discovered discrepancies.
The study should produce analysis-based findings to assist with organizational workforce oversight as well as salary revision and gender equality improvement tactics.
Present workforce enhancement proposals which focus on pay equity enhancement and the development of female employment in advanced positions.

# Dataset
The open data portal maintained by the City of Vancouver supplied the information set for this investigation. The data collection includes employee details from CUPE 1004 which includes all information about its members.
Position title means the specific names assigned to work roles belonging to employees.
Exempt/Union Classification: Employee classification type (CUPE 1004).
Pay ranges exist for different positions with their minimum and maximum hourly rate levels.
Gender Breakdown: Distribution of employees by gender (Female, Male, Total).

# Methodology

# 1. Data Collection and Preparation
# Data Ingestion Draw.io diagram
![image](https://github.com/user-attachments/assets/61de913a-250b-496b-839b-f96ca358b9b1)
![image](https://github.com/user-attachments/assets/a1a2a434-4e67-4107-9ba8-b6ddbb04c914)

# Power Shell by using Remote Desktop Connection
The web-based installation of Windows on Amazon EC2 operated through PowerShell to send a CSV file into an Amazon S3 storage bucket. The chosen approach provided protected scalable affordable storage solutions which allowed continuous data conversion processes. After the upload process the instance received termination due to optimization needs and reduced costs. A system of permissions was developed to protect the data and maintain AWS best practices standards.
![image](https://github.com/user-attachments/assets/ff06d302-edac-4923-9179-200f94bba74c)

# CSV dataset file in S3 location
![image](https://github.com/user-attachments/assets/7d7052c5-0533-464d-b4f8-1781a5d74932)

# Data Profiling (AWS Glue DataBrew)
 Data processing started only after identifying and resolving all discrepancies, such as missing values alongside formatting errors. Schema enforcement with duplicate removal methods enabled the maintenance of data integrity through applied validation techniques. Keeping the dataset clean through preprocessing steps made it possible to perform analysis and transformation without obstructions.
AWS Glue DataBrew acted as the tool for performing complete data profiling and cleaning operations which improved data quality and maintained its integrity. The data profiling analysis included investigations of missing values and anomaly detections as well as distribution analysis of the data. The data became more readable through field renaming while removing excess fields containing redundant location identifiers. The process replaced gaps in essential data groups including Minimum Hourly Rate and Maximum Hourly Rate alongside demographic data categories (Female, Male, and Total). The analysis received refined datasets after specific data categorization was applied to separate food categories along with position types and data elements.
![image](https://github.com/user-attachments/assets/7eb673c5-08e6-46a7-9649-43a85c87e6f8)

# Created and run the job
![image](https://github.com/user-attachments/assets/c1c88f66-106e-444e-becf-75830fd4d391)

# After Cleaning job, csv and parquet stored in S3 User and System folders
![image](https://github.com/user-attachments/assets/cfa92655-37a7-43d1-a86e-ee861a332a07)
![image](https://github.com/user-attachments/assets/2de7c687-dd48-4772-af43-70ff6f11c3ed)

# 2. Descriptive Statistics
# Data Cataloging (AWS Glue Data Catalog, Glue Crawler)
A new "workforce-cur-gau" AWS Glue database combined with a customized S3 bucket functioned for storing cleaned and filtered data. A database within the "workforce-cur-gau" AWS Glue platform used meaningful transformed data to remove redundant fields and conduct reporting-oriented and analytical changes. AWS Glue features a custom crawler that acts as a data detection and cataloging system to simplify the process of organizing S3 bucket contents. The custom crawler served as an important data structure identification tool to maintain accurate and current incoming data that supported future analysis requirements. The solution proved to be a good option for simple connections to Amazon Athena analytics services within AWS to access transformed data quickly for reporting purposes.
![image](https://github.com/user-attachments/assets/1c2de38f-dc04-417d-823e-d76adf2b361e)

# Query Execution Using AWS Athena  
# Data Analysis Using AWS Athena  
Once the transformed dataset was stored in Amazon S3, AWS Athena was utilized to execute SQL queries directly on the data. AWS Athena processed the stored Amazon S3 data through the execution of SQL queries to analyze the information. Floating above traditional server management, Athena served organizations with analysis capabilities that needed no extra ETL pipelines or infrastructure platforms to operate. 
Analysis required the execution of one critical SQL statement to determine the average minimum hourly wage in downtown Vancouver for workforce pay trend assessment. 
Athena enabled effortless extraction of insights from large-scale S3 data because it integrated smoothly with S3 for cost-effective and scalable queries. 
Athena allowed project users to perform quick and real-time data analysis thus generating essential workforce metrics in an effective manner.

![image](https://github.com/user-attachments/assets/72847084-1fb9-4f24-900c-43e52183d135)

# 3. Data Visualization
Visual ETL Pipeline Implementation
The automation of ETL processing happened through AWS Glue to achieve efficient data management practices. The pipeline obtained workforce pay rate and demographic data before it used data categories and classification filters for transformation steps and added timestamps for processing time tracking. The processed data underwent systematic storage both as CSV and Parquet formats to serve the analytical needs and operational requirements throughout the organization.
![image](https://github.com/user-attachments/assets/f1ab4698-bf34-4840-aef2-88b1f2196c60)
![image](https://github.com/user-attachments/assets/895baad3-2e1c-412c-b707-f571ecbc2e94)

# 4. Customer Segmentation
The workforce pay rates and gender data from Vancouver enables a comprehensive customer segmentation analysis through multiple data aspects. Gender statistics in different job sections including Construction, Trades and Equipment Operators show inconsistencies between worker numbers and wage levels. The examination of minimum and maximum hourly earnings creates occupational segments which demonstrate possible differences in wages according to salary categories between genders. The time frame across five consecutive years (2019–2023) allows researchers to track workforce trends that reflect gender representation evolution during that period. Public organizations maintain separate categories for positions which reveal differences between 'Exempt' and 'Union' classification systems. This segmentation system delivers essential workforce understanding about Vancouver's workforce structure which lets stakeholders detect gender balance improvement areas and guide workplace diversity policy development.
Loading the Dataset:
A Visual ETL pipeline was created in AWS Glue.
The raw dataset from the S3 bucket (workforce-raw-gau) was loaded into the pipeline.
The name of the ETL pipeline is workforce-payrates-QC-gau.
![image](https://github.com/user-attachments/assets/d7bb27e5-9d2f-4f27-922f-617e57028e8e)
# Jobs run successfully
![image](https://github.com/user-attachments/assets/f3169025-c8cf-416d-b08f-736a0dd4550e)
Data quality rules were applied to the dataset to ensure its integrity:
Completeness: We ensured that the "Status" column had at least 50% non-null values.
Uniqueness: We validated that the "Location" column had at least 13% unique values. This step checks for duplicates or inconsistencies, improving the accuracy of the dataset.
A Conditional Router transformation was employed to segment the data based on validation outcomes:
Pass Folder: Data that met all the quality criteria was routed here for further processing.
Fail Folder: Data that failed to meet the necessary criteria was routed here for further review or exclusion.
We modified the schemas for both the pass and fail datasets to ensure compatibility with their respective destination folders. This is crucial for maintaining a structured and organized data flow.
The processed data was then uploaded to the S3 bucket, ensuring a clear distinction between validated and unvalidated data.
# Dataset created in passed and failed folders
![image](https://github.com/user-attachments/assets/1699c612-2d70-4dc3-82eb-e8ef7f6e0608)
![image](https://github.com/user-attachments/assets/6219122f-ec9a-47b5-a24d-3577e87d9257)

# 5. Insights and Findings
# Insights
# Gender Pay Gaps:
The obtained analysis data shows significant differences in payment levels between male and female staff members which require comprehensive examination to address possible pay equity problems.
# Data Quality Improvement:
Maintaining high data quality through preprocessing steps that combined data cleaning and validation resulted in an important dataset improvement for effective analysis.
# Efficiency of AWS Services:
AWS Glue and S3 storage combined to simplify data handling operations while providing improved scalability that supports the analysis of ongoing workforce trends.
# Findings
# Imbalance in Workforce Composition:
The database shows particular positions which suffer from significant gender inequality thus opening doors for specific recruitment strategies and inclusion programs.
# Salary Distribution Trends:
The assessment of salary data reveals clear patterns between pay values and both job titles and gender distribution so organizations need complete compensation structure overviews to guarantee fair pay.
# Cost-Effectiveness of Cloud Solutions:
The expense data demonstrates that AWS enables data processing and storage at low rates which bolsters cloud infrastructure development prospects through its affordable nature.

# 6. Recommendations
1. Enhance Data Quality and Integrity
Consistent data quality inspections by conducting planned audits will help maintain the accuracy and finish of all datasets.
AWS Glue with automated validation rules should conduct systematic checks for irregularities and absent values both when ingesting and processing data.
2. Optimize Data Processing Pipelines
The usage of AWS Glue for automated ETL processes should remain the same to maximize efficiency and minimize user interaction.
An elastic infrastructure can be achieved through AWS Lambda since sporadic processes require serverless computing without keeping EC2 instances operating at all times.
3. Implement Advanced Analytics
The AWS platform should be used to implement predictive analytics capabilities so organizations can work with machine learning to track workforce pay structures alongside gender distribution analytics. The analysis would create forecasts about future staffing requirements along with salary patterns.
The solution includes integrating AWS QuickSight and similar visualization tools to build dashboards that present real-time workforce demographic and pay rate information for monitoring purposes.
4. Enhance Security and Compliance
The organization should use encryption systems to protect information when it stays in storage and when it moves between systems. The organization should use AWS KMS in order to manage its encryption keys.
Organizations should build an IAM policy framework for sensitive data access control to let authorized users only process this information.
5. Focus on User Accessibility
Create simple interfaces which let non-expert staff members conduct data analysis using methods that bypass complex technical requirements.
The organization should hold training programs for stakeholders about proper utilization of data for their decision-making procedures.
6. Continuous Monitoring and Improvement
The cloud monitoring system CloudWatch Dashboards tracks data metrics while it uses alerts to report deviations in storage and processing activities.
A feedback mechanism should allow users to provide insights about data accessibility quality through continuous improvement based on actual user experiences.
7. Cost Management
AWS Cost Explorer helps organizations analyze spending patterns to optimize costs mainly in data storage and processing operations.
Set budget alerts throughout AWS to block unnecessary spending and meet expected budgeted costs.
The recommended measures help organizations both improve their data processing capacity and maintain data quality which enables them to extract valuable insights from workforce pay rate and gender distribution assessments.

# Tools and Technologies
AWS Cloud Services.

AWS S3 (Simple Storage Service): For raw data ingestion, storage of processed files (CSV, Parquet), and DataBrew/Glue job outputs.

Initial data file staging together with PowerShell script execution takes place on the AWS EC2 (Elastic Compute Cloud) platform.

AWS Glue DataBrew serves as a tool for data profiling and interactive data cleanup in addition to its transformation job execution capabilities.

AWS Glue Data Catalog serves as the central storage facility for metadata organization.

The AWS Glue Crawler function serves as a data catalog population system running automatically.

SQL commands in AWS Athena enable users to extract descriptive statistics from the S3 data that was cataloged through the system.

# Conclusion
This research effectively demonstrates how AWS cloud services—specifically AWS Glue, S3, and EC2—can be utilized to process and analyze workforce pay rates and gender distribution for CUPE 1004 employees. By employing robust ETL procedures, the study ensured data accuracy, consistency, and accessibility, enabling informed, evidence-based decision-making. The automated data profiling and transformation processes established a reliable framework for managing workforce information, supporting strategic planning and policy initiatives aimed at promoting gender equality and fair compensation. Overall, this approach delivers a scalable and efficient data analytics solution that strengthens organizational insights and contributes to a more equitable workplace.


