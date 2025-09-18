# 🔐 Oracle Cloud Infrastructure (OCI) — Security Services & Shared Responsibility Model  

## 📍 1. Introduction  
Security is central to Oracle Cloud Infrastructure (OCI). Oracle employs a **shared security model**, where responsibility is divided between **Oracle** (managing the cloud infrastructure) and the **customer** (managing workloads and configurations).  

This layered approach ensures comprehensive protection across physical infrastructure, network, workloads, data, and applications.  

---

## 🏛️ 2. The Shared Security Model  

### 🔹 On-Premises (Traditional IT)  
- The customer manages **everything**:  
  - Data center facilities  
  - Physical network and servers  
  - Operating systems  
  - Applications and data  

### 🔹 Oracle Cloud (OCI)  
- **Oracle’s Responsibility** → Security of infrastructure:  
  - Data centers, hardware, storage, networking, and virtualization layers.  
- **Customer’s Responsibility** → Security of workloads:  
  - Applications, data, and configuration of compute, storage, networking, and databases.  

✅ Benefit: Oracle reduces infrastructure-level burden while customers retain control over their business-critical assets.  

---

## 🛡️ 3. Layers of Security in OCI  

### 3.1 Infrastructure Protection  
- **Web Application Firewall (WAF)** → Filters malicious inbound traffic to internet-facing apps.  
- **Security Lists & Network Security Groups (NSGs)** → Function as **virtual firewalls** within VCNs.  
- **Network Firewall** → Cloud-native firewall controlling inbound/outbound traffic across applications.  

---

### 3.2 Identity and Access Management (IAM)  
- **Default Deny** → No resource access unless explicitly allowed.  
- **IAM Policies** → Grant **least-privilege access** to users/groups.  
- **Multi-Factor Authentication (MFA)** → Adds a second security layer beyond passwords.  

---

### 3.3 Operating Systems & Workloads  
- **Bastion Service** → Provides secure, time-limited access to resources in private subnets.  
- **OS Management** → Automates monitoring, patching, and updates for operating systems.  

---

### 3.4 Data Protection  
- **Vault Service** → Centralized management of encryption keys and secret credentials.  
- **Data Safe** → Specialized service to secure, audit, and protect sensitive/regulated database data.  

---

### 3.5 Detection & Remediation  
- **Cloud Guard** → Monitors and enforces security posture across OCI resources.  
- **Vulnerability Scanning Service (VSS)** → Detects vulnerabilities in hosts and container images.  

---

## ✅ 4. Certification-Oriented Key Takeaways  
| Security Layer              | Service Example                | Purpose |
|------------------------------|--------------------------------|---------|
| Infrastructure Protection    | WAF, NSGs, Network Firewall    | Defend apps and networks |
| Identity & Access Control    | IAM Policies, MFA              | Restrict and manage access |
| OS & Workloads               | Bastion, OS Management         | Secure private access + patching |
| Data Protection              | Vault, Data Safe               | Key, secret, and data security |
| Detection & Remediation      | Cloud Guard, VSS               | Monitor + mitigate risks |

---

✍️ Created & Curated by  
Muhammad Naveed Ishaque (Eks2)  
Content Creator | AI Writer | Narrative Simplifier  

🕊️ Siraat AI Academy  
"The Straight Path — Empowering minds with clarity, illuminating paths with purpose."  

---

# 📌 Suggested Filename  
`oci-security.md`
