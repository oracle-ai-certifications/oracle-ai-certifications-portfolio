# ⚙️ Oracle Cloud Infrastructure (OCI) — Creating a Compute Instance  

## 🌍 1. Introduction  
In Oracle Cloud Infrastructure (OCI), a compute instance represents a virtual or physical server where workloads and applications are deployed. Understanding the **creation workflow** in the OCI Console is essential for managing resources effectively and for success in Oracle AI and Cloud certification exams.  

---

## 🖥️ 2. Steps to Create a Compute Instance  

### 🔹 Step 1: Access Compute Services  
- Open the **Navigation Menu** → Select **Compute** → Choose **Instances**.  
- Confirm you are in the **correct compartment** before creating the instance.  

### 🔹 Step 2: Name & Compartment  
- Assign a **meaningful instance name** (e.g., *demo-instance*).  
- Select the appropriate **compartment** to organize resources logically.  

### 🔹 Step 3: Placement & Capacity  
- Choose an **Availability Domain (AD)** within the selected region.  
- Configure **Capacity Options**:  
  - **On-Demand** (default, pay as you go).  
  - **Preemptible** (low-cost, but can be reclaimed by OCI).  
  - **Dedicated VM Host** (runs only your VMs).  
  - **Capacity Reservation** (reserve in advance for guaranteed availability).  
- Optionally, define a **Fault Domain**, or allow Oracle to assign it automatically.  

### 🔹 Step 4: Image & Shape  
- **Image (Software Layer)** → Defines the operating system.  
  - Examples: Oracle Linux (default), CentOS, Autonomous Linux, etc.  
- **Shape (Hardware Layer)** → Defines CPUs, memory, and compute resources.  
  - Options: Virtual Machine (VM) or Bare Metal.  
  - Supported processors: AMD, Intel, Ampere ARM.  
  - Example: *VM.Standard.E4.Flex* (1 OCPU, 8 GB memory).  

### 🔹 Step 5: Networking  
- Select an existing **Virtual Cloud Network (VCN)** or create a new one.  
- Choose a **Subnet**:  
  - Public Subnet → Routable from the internet.  
  - Private Subnet → Internal-only communication.  
- Optionally assign a **public IPv4 address** for internet access.  

### 🔹 Step 6: Secure Access (SSH Keys)  
- Add an **SSH key pair** to connect securely to the instance.  
- Without SSH keys, remote login is not possible.  

### 🔹 Step 7: Provisioning & Verification  
- Click **Create Compute Instance**.  
- Instance status transitions to *Provisioning* and then *Running*.  
- Verify:  
  - Public and private IP addresses.  
  - Region, availability domain, and fault domain allocation.  

---

## ✅ 3. Key Exam Insights  
- **Compartment Selection** is critical for organizing and accessing resources.  
- **Placement Options** (on-demand, preemptible, dedicated, reserved) determine performance and cost trade-offs.  
- **Images** = Operating system / software layer; **Shapes** = hardware configuration.  
- **Networking Setup** (VCN, subnet, public/private IP) defines connectivity.  
- **SSH Keys** ensure secure administrative access.  
- An instance is deployed into a **specific region, AD, and FD**, which impacts availability and resilience.  

---

✍️ Created & Curated by  
Muhammad Naveed Ishaque (Eks2)  
Content Creator | AI Writer | Narrative Simplifier  

🕊️ Siraat AI Academy  
"The Straight Path — Empowering minds with clarity, illuminating paths with purpose."
