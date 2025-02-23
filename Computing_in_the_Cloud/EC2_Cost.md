# Amazon EC2 Pricing Options Summary

## 1. On-Demand Instances

- Best for short-term, unpredictable workloads.
- No upfront payment, pay only for what you use.
- Ideal for development, testing, and applications with fluctuating demand.

## 2. Reserved Instances (RIs)

- Commit to **1 or 3 years** for significant savings compared to On-Demand pricing.
- **Standard RIs**: More savings, but less flexibility.
- **Convertible RIs**: Allows changing instance attributes but with lower discounts.

### Standard RIs vs. Convertible RIs

### **Which One Should You Choose?**

| Feature                    | **Standard RIs**                  | **Convertible RIs**                        |
| -------------------------- | --------------------------------- | ------------------------------------------ |
| **Maximum Savings**        | Up to **72%**                     | Up to **66%**                              |
| **Instance Type Change**   | ❌ Not allowed                    | ✅ Allowed                                 |
| **Instance Family Change** | ❌ Not allowed                    | ✅ Allowed                                 |
| **Region Change**          | ❌ Not allowed                    | ✅ Allowed                                 |
| **Can be Sold?**           | ✅ Yes, on RI Marketplace         | ❌ No resale                               |
| **Best For**               | **Stable, predictable workloads** | **Changing workloads with evolving needs** |

## 3. EC2 Instance Savings Plans

- Provide **up to 72% savings** for consistent compute usage over **1 or 3 years**.
- More flexible than Reserved Instances (can apply to different instance types within a family).

## 4. Spot Instances

- **Up to 90% cheaper** than On-Demand instances.
- Uses **unused AWS capacity**, so instances can be interrupted at any time.
- Best for **batch processing, big data workloads, and fault-tolerant applications**.

## 5. Dedicated Hosts

- Entire **physical server reserved** for your exclusive use.
- Helps with **licensing and compliance** requirements.
- Most **expensive option** but provides full control over hardware.

---

## Recommendation

✅ **Use On-Demand** for unpredictable or short-term workloads.  
💰 **Choose Reserved Instances** or **Savings Plans** for steady workloads to maximize cost savings.  
📌 **Consider Spot Instances** for fault-tolerant, batch, or background jobs.  
🏢 **Opt for Dedicated Hosts** only if compliance or licensing demands it.

# Amazon EC2 Cost Comparison

| **Pricing Model**        | **Upfront Cost** | **Hourly Cost**       | **Commitment**       | **Flexibility** | **Best For** |
|-------------------------|----------------|----------------------|----------------------|----------------|-------------|
| **On-Demand**           | ❌ No           | 💰 High               | ⏳ None               | ✅ Full         | Short-term, unpredictable workloads |
| **Standard Reserved**   | ✅ Yes          | 💰 Low (Up to 72% off) | ⏳ 1 or 3 years       | ❌ Fixed       | Long-term, stable workloads |
| **Convertible Reserved**| ✅ Yes          | 💰 Medium (Up to 66% off) | ⏳ 1 or 3 years  | 🔄 Moderate (Instance changes allowed) | Long-term workloads with potential instance type changes |
| **Savings Plans**       | ✅ Yes          | 💰 Medium to Low (Up to 72% off) | ⏳ 1 or 3 years  | 🔄 High       | Consistent compute usage with flexibility |
| **Spot Instances**      | ❌ No           | 💰 Very Low (Up to 90% off) | ⏳ None           | ❌ Can be interrupted | Batch jobs, background processing, fault-tolerant workloads |
| **Dedicated Hosts**     | ✅ High         | 💰 High                | ⏳ 1 or 3 years      | ❌ None        | Compliance, regulatory needs, specialized workloads |

---

## **Key Takeaways:**
- **On-Demand**: Expensive but flexible—ideal for unpredictable workloads.
- **Reserved Instances**: Lower cost but requires long-term commitment.
- **Savings Plans**: Similar to Reserved Instances but offer more flexibility.
- **Spot Instances**: Cheapest option but **can be interrupted** at any time.
- **Dedicated Hosts**: Most expensive, but necessary for compliance-heavy workloads.

---