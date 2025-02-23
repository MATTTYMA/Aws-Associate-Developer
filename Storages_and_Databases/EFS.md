# Summary of Amazon Elastic File System (Amazon EFS)

## Overview of File Storage

- **File storage** allows multiple clients (users, applications, servers) to access shared data stored in file folders.
- Uses **block storage** with a local file system to organize files.
- Ideal for **multi-user** and **multi-resource** environments needing access to the same data.

## Amazon Elastic File System (Amazon EFS)

- **Scalable file system** for AWS Cloud services and on-premises resources.
- Automatically **grows and shrinks** as files are added or removed.
- Can scale **to petabytes** without disrupting applications.
- Supports **simultaneous access** from multiple instances across Availability Zones.
- On-premises servers can access **EFS using AWS Direct Connect**.

## Amazon EFS vs. Amazon EBS

| Feature          | Amazon EBS                                                                     | Amazon EFS                                                       |
| ---------------- | ------------------------------------------------------------------------------ | ---------------------------------------------------------------- |
| **Storage Type** | Block storage                                                                  | File storage                                                     |
| **Availability** | Stores data in a **single** Availability Zone                                  | Stores data in **multiple** Availability Zones                   |
| **Scalability**  | Fixed size; requires resizing manually                                         | Automatically scales up and down                                 |
| **Access**       | Attached to a **single EC2 instance**                                          | Accessed **concurrently** across multiple instances              |
| **Use Case**     | Best for **single instance** applications with low-latency block storage needs | Best for **multi-instance** applications requiring shared access |

## Key Takeaways

- **Amazon EFS** is ideal for workloads requiring **shared storage** across multiple EC2 instances.
- **Unlike EBS**, EFS provides a **regional** file storage solution across multiple Availability Zones.
- Supports **AWS Direct Connect**, making it suitable for both **cloud and on-premises** applications.
