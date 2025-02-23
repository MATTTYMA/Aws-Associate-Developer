# AWS Storage: Instance Stores and Amazon EBS

## Instance Stores
- **Instance stores** provide block-level storage for Amazon EC2 instances.
- This storage is physically attached to the host computer and has the same lifespan as the instance.
- **If the instance stops or is terminated, all data on the instance store is lost.**
- Best for **temporary** storage use cases.

### Instance Store Lifecycle
1. **Running Instance:** The EC2 instance is running with an attached instance store containing data.
2. **Stopped/Terminated:** When the instance stops or terminates, the instance store still contains data.
3. **Data Loss:** Once the instance is terminated, all data in the instance store is **deleted permanently**.

---

## Amazon Elastic Block Store (EBS)
- **EBS provides persistent block-level storage** that can be attached to EC2 instances.
- **Unlike instance stores, EBS volumes persist even if the instance stops or terminates.**
- You can configure the volume size and type during creation.
- **Supports backups through EBS snapshots.**

### EBS Snapshots
- EBS snapshots are **incremental backups**.
- The first snapshot copies all data, while subsequent snapshots store **only the changed data**.
- This method reduces storage costs compared to full backups.

#### Example of Incremental Backup:
- **Day 1:** Full backup of volume.
- **Day 2:** Only changed data is backed up.
- **Day 3:** Newly added volumes are backed up, previous unchanged data is skipped.

---

## Comparison Table: Instance Store vs. EBS

| Feature            | Instance Store                  | Amazon EBS                          |
|-------------------|--------------------------------|------------------------------------|
| **Persistence**   | Temporary (data lost on termination) | Persistent (data remains available) |
| **Storage Type**  | Attached to host machine       | Separate block storage              |
| **Use Cases**     | Temporary cache, buffer, ephemeral storage | Long-term storage, databases       |
| **Backup**       | Not supported                  | Supports EBS snapshots             |
| **Flexibility**  | Cannot be detached from instance | Can be detached and reattached to other instances |

---

## Key Takeaways
- **Use Instance Store for temporary, high-speed storage** where data loss is acceptable.
- **Use Amazon EBS for persistent storage** where data needs to survive instance terminations.
- **EBS snapshots enable cost-efficient backups** by storing only changed data over time.