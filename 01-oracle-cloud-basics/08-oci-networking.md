# 🌐 Oracle Cloud Infrastructure (OCI) — Networking Services

## 📍 1. Introduction to Networking in OCI
Networking is a critical foundation in Oracle Cloud Infrastructure (OCI).  
The **Virtual Cloud Network (VCN)** serves as the core component, enabling secure and flexible communication between resources, the internet, and on-premises systems.  

- **VCN = Virtual Private Network** (isolated, secure by default).  
- Functions like a traditional data center network but delivered virtually.  
- Spans an **entire region** and can serve multiple Availability Domains.  
- Provides **public subnets** (internet-facing) and **private subnets** (internal-only).  

---

## 🖥️ 2. Virtual Cloud Network (VCN)
- **Public Subnet** → Accessible from the internet.  
- **Private Subnet** → Internal-only; cannot be reached directly from the internet.  
- Each subnet receives **IP addresses** from a defined **CIDR block** (e.g., `10.0.0.0/16` → ~65,000 IPs).  
- Ensures communication between compute instances (e.g., web server ↔ database).  

Example Setup:  
- **Web Server** → Public Subnet (reachable via internet).  
- **Database Instance** → Private Subnet (isolated, accessible only by internal resources).  

---

## 🚪 3. Gateways in OCI
Gateways act as routing devices, determining how traffic flows in and out of a VCN.  

### 🔹 Internet Gateway  
- Connects **public subnets** to the internet.  
- Supports **inbound + outbound** traffic.  
- Use Case: Web server accessible to external customers.  

### 🔹 NAT (Network Address Translation) Gateway  
- For **private subnets** only.  
- Supports **outbound internet access** (e.g., installing OS patches).  
- **No inbound connections** allowed.  

### 🔹 Service Gateway  
- Enables **private access** to Oracle services (e.g., Object Storage).  
- Traffic bypasses the internet, increasing **security**.  

---

## 🔗 4. Hybrid Connectivity with On-Premises
Many enterprises require connectivity between OCI and their **on-premises data centers**.  
This is achieved via a **Dynamic Routing Gateway (DRG)** combined with additional services:  

### 🔹 Site-to-Site VPN  
- Creates an **encrypted tunnel** over the internet.  
- Similar to accessing a corporate VPN from home.  
- Cost-effective but internet-dependent (latency may vary).  

### 🔹 FastConnect  
- Provides a **dedicated private line** to OCI.  
- Offers **higher bandwidth** and more consistent reliability compared to VPN.  
- Preferred for mission-critical workloads.  

---

## ✅ 5. Certification-Oriented Key Takeaways
| Component              | Purpose | Accessibility |
|-------------------------|---------|---------------|
| **VCN**                | Virtual private network | Regional, spans ADs |
| **Public Subnet**      | Internet-facing resources | Inbound + Outbound |
| **Private Subnet**     | Internal workloads | Restricted (no direct internet) |
| **Internet Gateway**   | Connects public subnet to internet | Inbound + Outbound |
| **NAT Gateway**        | Private subnet → internet (outbound only) | Outbound only |
| **Service Gateway**    | Secure access to Oracle services | Private |
| **DRG + VPN**          | Cloud ↔ On-premises (encrypted tunnel) | Internet-based |
| **DRG + FastConnect**  | Cloud ↔ On-premises (dedicated line) | Private |

---

✍️ Created & Curated by  
Muhammad Naveed Ishaque (Eks2)  
Content Creator | AI Writer | Narrative Simplifier  

🕊️ Siraat AI Academy  
"The Straight Path — Empowering minds with clarity, illuminating paths with purpose."

---

# 📌 Suggested Filename
`oci-networking.md`
