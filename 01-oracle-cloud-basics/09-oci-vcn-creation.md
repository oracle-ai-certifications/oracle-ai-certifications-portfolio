# 🌐 Oracle Cloud Infrastructure (OCI) — Creating a Virtual Cloud Network (VCN)

## 📍 1. Introduction  
A **Virtual Cloud Network (VCN)** is the backbone of Oracle Cloud networking. It enables secure communication between compute resources, on-premises systems, and the internet. In this demonstration, we review the process of creating a VCN using the OCI Console.

---

## 🖥️ 2. Steps to Create a VCN

### 🔹 Step 1: Navigate to Networking
- Log into the **OCI Console**.  
- Go to the **Navigation Menu → Networking → Virtual Cloud Networks**.  
- Ensure you are working in the **correct compartment** (e.g., `OCI demo`).  

### 🔹 Step 2: Choose Creation Method
Two options are available:  
1. **Manual Creation** → You define all resources individually.  
2. **VCN Wizard** → Automatically provisions a VCN with key components.  

👉 In this demonstration, the **VCN Wizard** was selected.  

### 🔹 Step 3: Configure VCN
- Provide a **VCN Name** (e.g., `demo VCN`).  
- Confirm the **compartment**.  
- Define the **CIDR block** (range of private IP addresses).  
- Provide CIDR ranges for **public** and **private subnets**.  
- Defaults can be accepted for simplicity.  

### 🔹 Step 4: Review and Create
- Review configuration details.  
- Click **Create** to provision the VCN and associated components.  

---

## ⚙️ 3. Resources Created by the VCN Wizard
When using the wizard, the following components are automatically provisioned:  

- **VCN** with a defined CIDR block.  
- **Public Subnet** → Internet-facing workloads (e.g., web servers).  
- **Private Subnet** → Isolated workloads (e.g., databases).  
- **Internet Gateway** → Enables inbound/outbound internet access for public subnet.  
- **NAT Gateway** → Allows private subnet instances outbound internet access (no inbound).  
- **Service Gateway** → Provides secure private connectivity to Oracle services.  
- **Route Tables** → With preconfigured routing rules for subnets.  

---

## 📖 4. Example Use Case
- **Web Server** → Deployed in the **public subnet** for internet access.  
- **Database Server** → Deployed in the **private subnet**, isolated from the internet, but:  
  - Accesses updates via the **NAT Gateway**.  
  - Connects to Oracle Cloud services privately via the **Service Gateway**.  

---

## ✅ 5. Certification-Oriented Key Takeaways
| Component            | Purpose | Example Use |
|----------------------|---------|-------------|
| **VCN**             | Virtual private network | Core network foundation |
| **Public Subnet**   | Internet-facing | Hosts web servers |
| **Private Subnet**  | Internal-only | Hosts databases |
| **Internet Gateway**| Internet access | Public subnet workloads |
| **NAT Gateway**     | Outbound-only internet | Patch updates from private subnet |
| **Service Gateway** | Secure Oracle service access | Object storage, other services |
| **Route Tables**    | Traffic control | Define routing rules |

---

✍️ Created & Curated by  
Muhammad Naveed Ishaque (Eks2)  
Content Creator | AI Writer | Narrative Simplifier  

🕊️ Siraat AI Academy  
"The Straight Path — Empowering minds with clarity, illuminating paths with purpose."

---

# 📌 Suggested Filename  
`oci-vcn-creation.md`
