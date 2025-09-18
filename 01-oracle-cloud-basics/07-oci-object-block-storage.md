# 💾 Oracle Cloud Infrastructure (OCI) — Working with Object and Block Storage  

## 🌍 1. Introduction  
In this session, we explore **two core OCI storage services**:  

- **Object Storage** → For unstructured data managed in **buckets**.  
- **Block Storage** → For persistent, high-performance volumes attached to compute instances.  

Both play a key role in ensuring data persistence, accessibility, and scalability for cloud workloads.  

---

## 🗂️ 2. Object Storage  

### 📌 Buckets  
- All objects in OCI are stored inside **buckets**.  
- Bucket setup includes:  
  - **Name**: Unique identifier.  
  - **Storage Tier**:  
    - **Standard** → For frequent access.  
    - **Archive** → For infrequently accessed, long-term data.  
  - **Visibility**:  
    - **Private** (default) → Accessible only to authorized users.  
    - **Public** → Accessible by anyone with the object URL.  

### ⚙️ Advanced Options  
- **Auto-Tiering** → Moves objects between storage tiers based on usage.  
- **Object Versioning** → Maintains multiple versions of objects.  
- **Event Emission** → Triggers notifications on object operations.  
- **Multipart Upload Cleanup** → Removes incomplete uploads.  

### 🔐 Security  
- Objects are encrypted **by default** with Oracle-managed keys.  
- Users may alternatively bring **customer-managed keys**.  

### 📖 Workflow Example  
1. **Create a bucket** → Choose name, tier, and visibility.  
2. **Upload an object** → e.g., an image file.  
3. **Access object via URL**:  
   - If **Private** → Unauthorized error.  
   - If **Public** → Accessible directly from browser.  

---

## 📦 3. Block Storage  

### 📌 Block Volumes  
- Provide persistent **virtual disks** for compute instances.  
- Can be created, attached, detached, or replicated.  

### ⚙️ Key Configuration Options  
- **Volume Name & Compartment** → Logical organization.  
- **Placement** → Choose Availability Domain (AD).  
- **Size & Performance**:  
  - **Default**: 1024 GB, balanced performance.  
  - **Custom**: Manually configure size and performance level.  
- **Backup Policy** → Optional backup scheduling.  
- **Replication**:  
  - Asynchronous replication across regions (e.g., Phoenix → Ashburn).  

### 🔐 Security  
- By default, all block volumes are **encrypted** using Oracle-managed keys.  

### 📖 Workflow Example  
1. **Create Block Volume** → Define size, compartment, and AD.  
2. **Provision Volume** → System allocates storage.  
3. **Attach Volume to Instance** → Provides persistent storage for workloads.  

---

## ✅ 4. Certification-Oriented Key Takeaways  

| Service           | Purpose                     | Visibility / Access | Security |
|-------------------|-----------------------------|---------------------|----------|
| **Object Storage** | Store unstructured data (objects in buckets) | Private (default) / Public | Encrypted (Oracle or customer-managed keys) |
| **Block Storage**  | Persistent virtual disks for compute instances | Tied to AD and instance | Encrypted by default |

---

✍️ Created & Curated by  
Muhammad Naveed Ishaque (Eks2)  
Content Creator | AI Writer | Narrative Simplifier  

🕊️ Siraat AI Academy  
"The Straight Path — Empowering minds with clarity, illuminating paths with purpose."  

---

# 📌 Suggested Filename  
`oci-object-block-storage.md`
