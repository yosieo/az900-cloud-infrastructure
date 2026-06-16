# Microsoft Azure Infrastructure & Governance Case Study
A structured implementation portfolio demonstrating foundational knowledge of Microsoft Azure architecture, core services, and resource governance, aligned with the **AZ-900T00 (2025)** curriculum.

## 📌 Project Overview
This repository contains a comprehensive architectural breakdown and deployment case study modeled after the hands-on lab exercises in the AZ-900T00 syllabus. Instead of hosting proprietary lab scripts, this public repository serves as a portfolio piece showcasing cloud implementation skills, security best practices, and resource optimization strategies required for an Azure-managed environment.

---

## 🛠️ Tech Stack & Key Concepts
* **Cloud Infrastructure:** Microsoft Azure Portal, Azure Resource Manager (ARM)
* **Compute & Networking:** Azure Virtual Machines, Virtual Networks (VNets), Network Security Groups (NSGs)
* **Storage & Data:** Azure Blob Storage, Storage Accounts
* **Identity & Governance:** Entra ID (formerly Azure AD), Azure Policy, Role-Based Access Control (RBAC), Resource Locks
* **Cost Management:** Azure Pricing Calculator, Total Cost of Ownership (TCO) Calculator

---

## 🏗️ Architectural Framework & Core Implementations

### 1. Compute & High-Availability Networking
* **The Goal:** Build an isolated, secure perimeter to host a virtual cloud instance capable of handling external web traffic.
* **Execution:** 
  * Provisioned a custom **Azure Virtual Network (VNet)** and segmented it into targeted subnets.
  * Deployed a **Windows/Linux Virtual Machine (VM)** within the subnets.
  * Configured **Network Security Group (NSG)** rules, selectively opening inbound traffic (Port 80/443 for HTTP/S and Port 3389/22 for secure administrative access).
* **Key Takeaway:** Understood how Azure Availability Zones shield infrastructure from localized data center outages, reinforcing the principles of high availability and fault tolerance.

### 2. Cloud Data Storage Solutions
* **The Goal:** Implement a scalable, secure object-storage solution for unstructured enterprise data.
* **Execution:** 
  * Deployed an **Azure Storage Account** optimized for hot/cool access tiers.
  * Configured a private **Blob Storage Container** to securely upload, store, and manage unstructured media and diagnostic logs.
* **Key Takeaway:** Learned the distinct trade-offs between Locally Redundant Storage (LRS) for cost-efficiency and Geo-Redundant Storage (GRS) for regional disaster recovery.

### 3. Resource Governance, Compliance, and Security
* **The Goal:** Enforce corporate guardrails on a subscription to avoid resource deletion and accidental over-budget deployments.
* **Execution:** 
  * **Resource Locks:** Applied `CanNotDelete` locks to core production resource groups to eliminate accidental deletions.
  * **Azure Policy:** Created an environment-wide Azure Policy restricting allowed VM SKUs to budget-friendly tiers (e.g., Standard_B series), preventing rogue pricing spikes.
  * **RBAC:** Delegated strict, granular system access to user identities using Azure Role-Based Access Control.
* **Key Takeaway:** Enforcing automated governance at the subscription scale is crucial for compliance and avoiding human error in cloud environments.

---

## 💰 Cloud Economics & Cost Optimization
As part of this case study, a comprehensive financial optimization model was built using official Microsoft pricing tools:
* **Scenario Planning:** Modeled a production workload requiring 3 App Service instances and an Azure SQL database using the [Azure Pricing Calculator](https://microsoft.com).
* **Cost-Control Recommendation:** Identified that shifting traditional on-premises VMs to Azure could achieve structural savings over 3 years by leveraging **Azure Reserved Instances (RIs)** and the **Azure Hybrid Benefit**.

---

## 🧠 Core Competencies Demonstrated

| Domain | Cloud Skillset | Professional Application |
| :--- | :--- | :--- |
| **Infrastructure** | Virtualization & Networking | Deploying scalable, secure infrastructure blocks. |
| **Security** | Zero-Trust & Identity Perimeter | Managing entry vectors via strict NSGs and Entra ID RBAC. |
| **Governance** | Guardrails & Policy Mapping | Automating enterprise compliance using Azure Policy engine. |
| **Finance** | Cost Allocation & Forecasting | Maximizing ROI by preventing cloud waste and identifying idle assets. |

---

## 📈 Training & Portfolio Verification
* **Hands-on Lab Platform:** GoDeploy Training Environment
* **Course Curriculum:** AZ-900: Microsoft Azure Fundamentals (2025)
* **Official Microsoft Learning Curriculum:** [AZ-900 Core Objectives](https://learn.microsoft.com/en-us/training/courses/az-900t00)

---
*Disclaimer: This repository does not redistribute proprietary GoDeploy lab code, setup scripts, or answer keys. It functions strictly as an independent architectural overview and a synthesis of the practical competencies gained while utilizing the GoDeploy training platform.*
