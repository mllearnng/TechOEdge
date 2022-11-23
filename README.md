# Business Overview

Many problems exist when deploying or transferring analytics to the cloud. Differences in features between on-premises and cloud data platforms, security, and governance
are all technical concerns. The danger of moving on-premises data into the cloud has prompted organizations to limit cloud analytics initiatives, especially in regulated industries where data protection is crucial. Cloud-based safe Data Lake solutions aid in
the development of rich analytics on data while classifying it into several storage phases, such as raw, cleansed, and analytical. This project aims to securely manage,streamline, and perform analysis on the structured and semi-structured YouTube videos
data based on the video categories and the trending metrics.

# Why Glue :

 - Remove infrastructure management with automatic provisioning and worker management, and consolidate all your data integration needs into a single service.
 - Quickly identify data across multiple AWS datasets, and then make it instantly available for querying and transforming.
 - Using AWS Glue interactive sessions, data engineers can interactively explore and prepare data using the integrated development environment (IDE) or notebook of their choice.
 - More easily support various data processing frameworks, such as ETL and ELT, and various workloads, including batch, micro-batch, and streaming.
 
# When we should not use Glue : 
  - Amount of Work Involved in the Customization - AWS Glue is a managed ETL service for Apache Spark. And it is not a full-fledged ETL service like Talend, Xplexty, etc.
  - AWS Glue is specifically made for the AWS console and its products. And hence it isn’t easy to use for other technologies.Also, it supports limited data sources like S3 and JDBC. Hence, you need to move your data to these cloud applications (if it is not there already) for the AWS Glue functioning.
This is one of the biggest limitations of the AWS Glue. To overcome this limitation, you need to have the above-mentioned data sources.
 - Limitations of Real-time data - As AWS Glue only supports a handful of data sources like S3, there is no room to include an incremental synchronization with the data source.

# Architecture

<img width="808" alt="Screen Shot 2022-11-19 at 10 25 20 PM" src="https://user-images.githubusercontent.com/50221802/202885639-367970bd-c4a6-4e67-90c4-2019cbf0d2db.png">

# Pricing 

AWS Glue ETL jobs are billed at an hourly rate based on data processing units (DPU), which map to performance of the serverless infrastructure on which Glue runs. For the AWS Glue Data Catalog, users pay a monthly fee for storing and accessing Data Catalog the metadata. The first million objects stored are free, and the first million accesses are free. A development endpoint provisioned to interactively develop ETL code is billed per second. [pricing](https://aws.amazon.com/glue/pricing)

# Comparision with Azure 

Azure Data Factory and AWS Glue are two serverless offerings from competing products from the two biggest cloud service providers and both use Spark as an underlying tech stack. They are PaaS based products focused on ETL and ELT.

Similarities between AWS Glue and Azure Data Factory are given below:

- Both are fully managed and have server-less ETL engines.
- Both services support structured and unstructured data ingestion.
- Both services can generate codes automatically.
- Spark’s foundational technology stacks in both services.
- Both services support the trigger type schedule is manual as well as automatic.
- Both services allow you to concentrate on developing business logic and data transformation.
- Both services can perform data cleaning, transformation, and aggregation.
- AWS Glue can connect to data warehouses and move data to and from Amazon Redshift, whereas ADF can connect to data warehouses and move data into and out of SQL DW.
- Both services have transparent pricing and support SLAs.
- Both have the ability for customers to add new data sources, where developers can write custom code in Scala or Python and import custom libraries and Jar files into Glue ETL jobs to access data sources not natively supported by AWS Glue.

With AWS Glue, you are limited to using other AWS services as data sources, though one could argue that you could use JDBC to connect with other databases. In contrast, ADF can connect to a lot more data sources, including SaaS platforms, Web services, AWS services, and many more.

# Differences between AWS Glue and Azure Data Factory are given below:
- AWS Glue primarily focuses on service ETL and data cataloging, while ADF primarily focuses on service ETL.
- AWS Glue supports database replication at both levels: full table and incremental via change data capture through AWS Database Migration Service (DMS). On the other hand, ADF also supports database replication at both levels: full table and incremental via a custom SELECT query.
- AWS Glue does not have any SaaS sources, while ADF has about 20 SaaS sources, with several more in preview.
- AWS Glue has HIPAA and GDPR certifications for compliance, governance, and security. On the other hand, ADF has HIPAA, GDPR, and ISO 27001 certifications for compliance, governance, and security.
- AWS Glue supports data sharing inside AWS, while ADF doesn’t.
- AWS Glue has Python and Scala as developer tools. As developer tools, ADF includes a REST API, .Net and Python SDKs, and a PowerShell CLI.

Finally, With AWS Glue, developers will need to do a lot more scripting with Python or Scala and will need to know Spark. Azure Data Factory provides a more intuitive visual drag/drop low-code alternative.
