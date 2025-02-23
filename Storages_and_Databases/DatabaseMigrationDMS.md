# AWS Database Migration Service (AWS DMS)

## Overview
AWS Database Migration Service (AWS DMS) enables the migration of relational databases, nonrelational databases, and other data stores to AWS. It ensures minimal downtime for applications relying on the source database during migration.

## Types of Migrations
AWS DMS supports:
1. **Homogeneous Migrations**: Source and target databases are of the same type (e.g., MySQL to MySQL, SQL Server to SQL Server).
2. **Heterogeneous Migrations**: Source and target databases are of different types (e.g., Oracle to Amazon Aurora). This involves using the AWS Schema Conversion Tool to convert the schema before migration.

## Other Use Cases for AWS DMS
- **Development & Test Database Migration**: Enables developers to test applications with real production data without affecting live users.
- **Database Consolidation**: Combines multiple databases into a single central database.
- **Continuous Data Replication**: Allows ongoing replication of data from source to target systems, useful for disaster recovery or geographical redundancy.

## Key Features
- **Minimal Downtime**: The source database remains operational throughout the migration.
- **Flexible Source and Target Compatibility**: Works with both on-premises and cloud-hosted databases.
- **One-Time or Continuous Migration**: Supports both single-time migrations and ongoing replication.

AWS DMS is a powerful tool to migrate databases securely, efficiently, and with minimal disruption.