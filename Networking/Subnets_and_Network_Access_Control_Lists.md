# Subnets and Network Access Control Lists in AWS

## Subnets
A **subnet** is a section of a **Virtual Private Cloud (VPC)** used to group resources based on security or operational needs.  
Subnets can be categorized into:

- **Public Subnets**: Contains resources that need public accessibility, such as web servers.
- **Private Subnets**: Stores sensitive resources like databases, which should only be accessible within the private network.

### Example Analogy:
A coffee shop setup is used to explain subnets:
- **Cashier (Public Subnet)**: Accessible to all customers for placing orders.
- **Barista (Private Subnet)**: Restricted access; can only receive orders through the cashier, preventing direct interaction from customers.

---

## Network Traffic in a VPC
When a client sends a request to an AWS-hosted application, it enters the **VPC** through an **Internet Gateway**.  
Before accessing a subnet, a **Network Access Control List (ACL)** checks the packet for permissions.

---

## Network ACLs (Access Control Lists)
A **Network ACL** is a **virtual firewall** controlling inbound and outbound traffic at the subnet level.

- **Analogy**: Similar to a passport control officer at an airport, checking credentials before allowing entry.
- **Default Behavior**:
  - AWS provides a **default Network ACL** that allows all inbound and outbound traffic.
  - Custom Network ACLs deny all traffic by default until rules are explicitly added.
- **Stateless Filtering**:
  - Network ACLs do not remember previous requests.
  - Every packet is checked individually for **allow/deny** rules.

---

## Security Groups
A **Security Group** is a **stateful** firewall controlling traffic at the **EC2 instance level**.

- **Default Behavior**:
  - Denies all **inbound** traffic.
  - Allows all **outbound** traffic.
  - Custom rules can be added to allow specific inbound/outbound traffic.
- **Analogy**: A **door attendant** at an apartment building:
  - Checks a list before allowing guests inside.
  - Does **not** re-check the list when guests leave.

---

## **Comparison: Network ACLs vs. Security Groups**

| Feature                | Network ACLs                          | Security Groups                     |
|------------------------|--------------------------------------|-------------------------------------|
| **Level of Control**   | Controls traffic at the **subnet** level | Controls traffic at the **instance** level |
| **Statefulness**       | **Stateless** (does not remember previous requests) | **Stateful** (remembers previous requests) |
| **Inbound Rules**      | Evaluated **before** traffic reaches the subnet | Evaluated **when traffic reaches** the instance |
| **Outbound Rules**     | Evaluated **before** traffic leaves the subnet | Evaluated **when traffic leaves** the instance |
| **Default Behavior**   | Allows all traffic unless custom rules deny | Denies all inbound traffic, allows outbound |
| **Rule Processing**    | Rules are processed **sequentially** | Rules are processed as a **set** |
| **Best Use Case**      | Apply broad traffic filtering across subnets | Apply fine-grained security at the instance level |

---

## Stateful vs. Stateless Packet Filtering
- **Security Groups** are **stateful**: They remember previous requests.
- **Network ACLs** are **stateless**: They check every request as new.

---

## AWS VPC Component Flow
1. A **client** sends a request over the internet.
2. The request enters the **Internet Gateway**.
3. It passes through the **Network ACL**.
4. The request reaches the **Public Subnet**, where an **EC2 instance** processes it.
5. The **Security Group** enforces further access controls at the instance level.

By understanding subnets, network ACLs, and security groups, AWS users can **securely control network traffic** within their **VPC** environment.