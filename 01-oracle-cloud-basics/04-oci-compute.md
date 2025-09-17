# ⚙️ Oracle Cloud Infrastructure (OCI) Compute Service — Notes for Certification Prep  

## 🌍 1. Introduction  
The **OCI Compute Service** is the foundation of many Oracle Cloud solutions. It provides compute instances—servers where applications and workloads are deployed. These instances can be securely accessed, configured, and scaled to match business needs.  

---

## 🖥️ 2. Compute Instances  
A compute instance is essentially a server running on OCI.  

### 🔹 Key Characteristics  
- Hosted in the cloud, accessible remotely.  
- Built on **shapes** (templates defining CPU, memory, and storage).  
- Can be scaled vertically (resizing resources) or horizontally (adding/removing instances).  

---

## 🏷️ 3. Types of Compute Instances  

### 3.1 Virtual Machine (VM)  
- Logical server running on top of a shared physical server (bare metal).  
- Multiple VMs may exist on one physical machine.  
- Strong logical isolation ensures security between tenants.  
- Best suited for:  
  - General applications that don’t require full physical server capacity.  

### 3.2 Bare Metal Instance  
- A **dedicated physical server** provided to a single customer.  
- Offers maximum performance with full hardware access.  
- Suitable for:  
  - CPU-intensive workloads.  
  - Applications requiring complete hardware control.  
  - Third-party apps needing dedicated servers.  

### 3.3 Dedicated VM Host  
- A bare metal server configured to host only your virtual machines.  
- Combines the benefits of bare metal (dedicated hardware) with VM flexibility.  

---

## 🔲 4. Compute Shapes  
Shapes define the configuration of compute resources.  

### Types of Shapes  
- **Fixed Shapes** → Predefined CPU + memory combinations.  
  - Used in bare metal instances (non-customizable).  
  - Also available for VMs.  
- **Flexible Shapes** → Customizable CPU and memory values.  
  - Only available for VMs.  

### Processor Options  
- OCI supports AMD, Intel, and ARM-based processors.  

---

## 📈 5. Scaling Options  

### 5.1 Vertical Scaling  
- Adjust the **shape** of a VM (e.g., from Standard 2.1 → Standard 2.2).  
- Requires stopping and restarting the VM → causes temporary downtime.  

### 5.2 Horizontal Scaling (Auto Scaling)  
- Automatically adjusts the number of VMs.  
- Two modes:  
  1. **Metric-Based Auto Scaling**  
     - Triggered when monitored performance metrics cross thresholds.  
     - Example: Add instances if CPU usage exceeds 80%.  
  2. **Scheduled Auto Scaling**  
     - Predefined schedule for scaling up/down.  
     - Example: Scale out during business promotions, then scale in afterward.  

---

## ✅ 6. Key Exam Insights  
- **Compute Instances** = Core infrastructure for deploying apps/workloads.  
- **Instance Types** = VM (shared physical), Bare Metal (dedicated), Dedicated VM Host (dedicated for your VMs).  
- **Shapes** = Resource templates (fixed vs flexible).  
- **Scaling** = Vertical (resize) and Horizontal (auto scaling via metrics or schedule).  
- **Auto Scaling** is essential for cost optimization and handling fluctuating demand.  

---

✍️ Created & Curated by  
Muhammad Naveed Ishaque (Eks2)  
Content Creator | AI Writer | Narrative Simplifier  

🕊️ Siraat AI Academy  
"The Straight Path — Empowering minds with clarity, illuminating paths with purpose."
