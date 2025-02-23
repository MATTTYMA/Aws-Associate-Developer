# Relational Databases and Amazon RDS

## Relational Databases
A **relational database** stores data in tables that relate to each other. This approach ensures data consistency, easy querying, and scalability.

### Example Use Case
A relational database can be used in a coffee shop's inventory system where each product record includes:
- **Product Name**
- **Size**
- **Price**

**Structured Query Language (SQL)** is commonly used to manage and query relational databases.

## Amazon Relational Database Service (RDS)
**Amazon RDS** is a managed service that simplifies the setup, operation, and scaling of relational databases in AWS. It automates:
- **Hardware provisioning**
- **Database setup**
- **Patching**
- **Backups**

### Key Features:
- Security features like **encryption at rest** and **encryption in transit**.
- Integration with AWS services such as **AWS Lambda**.

## Amazon RDS Database Engines
Amazon RDS supports six major relational database engines:
- **Amazon Aurora**
- **PostgreSQL**
- **MySQL**
- **MariaDB**
- **Oracle Database**
- **Microsoft SQL Server**

## Amazon Aurora
**Amazon Aurora** is an enterprise-class relational database that is compatible with MySQL and PostgreSQL. It offers:
- **Performance improvements** (up to 5x faster than MySQL, 3x faster than PostgreSQL)
- **High availability** through automatic replication (six copies of data across three Availability Zones)
- **Automated backups** to Amazon S3

Aurora helps in reducing **input/output (I/O) operations**, ensuring cost-efficiency while maintaining reliability.

---
This summary provides an overview of relational databases, Amazon RDS, and the key features of Amazon Aurora.