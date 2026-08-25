# 🔵 Cloud Provider Comparison Report 🔴

<p align="center">

### 🔵 CCM101 – Cloud Computing 🔴

**CloudNova Technologies | Cloud Migration Planning**

</p>

<p align="center">

<img src="https://img.shields.io/badge/CCM101-CLOUD_COMPUTING-1976D2?style=for-the-badge" />
<img src="https://img.shields.io/badge/MISSION-2-D32F2F?style=for-the-badge" />
<img src="https://img.shields.io/badge/CLOUD_MIGRATION-PLANNING-1976D2?style=for-the-badge" />

</p>

---

<!-- ===================================================== -->
<!-- 🔵🔴 HORIZONTAL NAVIGATION BAR -->
<!-- ===================================================== -->

<table align="center">
<tr>

<td align="center">
<a href="#infrastructure-service-comparison-table">
<img src="https://img.shields.io/badge/☁️_COMPARISON-1976D2?style=for-the-badge" />
</a>
</td>

<td>&nbsp;&nbsp;&nbsp;</td>

<td align="center">
<a href="#guide-questions">
<img src="https://img.shields.io/badge/📋_GUIDE_QUESTIONS-D32F2F?style=for-the-badge" />
</a>
</td>

<td>&nbsp;&nbsp;&nbsp;</td>

<td align="center">
<a href="#cloud-migration-summary">
<img src="https://img.shields.io/badge/📊_SUMMARY-1976D2?style=for-the-badge" />
</a>
</td>

</tr>
</table>

---

<a id="infrastructure-service-comparison-table"></a>

## 🔵 Infrastructure Service Comparison Table 🔴

**Project:** CloudNova Technologies - Cloud Migration Planning  
**Date:** August 25, 2026

This comparison identifies equivalent infrastructure services provided by the three major public cloud platforms. Understanding these services helps cloud engineers determine how existing infrastructure can be mapped to cloud-based resources. The comparison also provides a foundation for evaluating which provider may best match an organization's technical and business requirements.

| Infrastructure Component | Amazon Web Services (AWS) | Microsoft Azure | Google Cloud Platform (GCP) |
| :--- | :--- | :--- | :--- |
| **Compute** | EC2 (Elastic Compute Cloud) | Virtual Machines | Compute Engine |
| **Storage** | S3 (Object) / EBS (Block) | Blob Storage / Disk Storage | Cloud Storage / Persistent Disk |
| **Networking** | VPC (Virtual Private Cloud) | VNet (Virtual Network) | VPC Network |
| **Identity & Access Management** | AWS IAM | Microsoft Entra ID (formerly Azure AD) | Cloud IAM |

---

## 💡 Infrastructure Comparison Explanation

The table shows that AWS, Azure, and GCP provide equivalent services for the major infrastructure categories.

| Infrastructure Component | Purpose |
|---|---|
| ⚙️ **Compute** | Provides processing resources for applications and workloads |
| 💾 **Storage** | Provides persistent storage for operating systems, applications, and data |
| 🌐 **Networking** | Connects cloud resources and manages network communication |
| 🔐 **Identity & Access Management** | Controls user access and permissions |
| ☁️ **Cloud Infrastructure** | Provides scalable resources without requiring physical hardware |

### 🔵 Compute Services

AWS **EC2**, Azure **Virtual Machines**, and GCP **Compute Engine** provide virtual computing resources. These services allow organizations to run applications without purchasing and maintaining their own physical servers. Compute resources can also be scaled according to workload requirements.

### 🔴 Storage Services

AWS provides **S3 and EBS**, Azure provides **Blob Storage and Disk Storage**, and GCP provides **Cloud Storage and Persistent Disk**. These services support different storage requirements such as object storage and block storage. Selecting the correct storage service is important for performance, availability, backup, and cost management.

### 🔵 Networking Services

AWS **VPC**, Azure **VNet**, and GCP **VPC Network** provide virtual networking environments. They allow organizations to configure subnets, routes, network access, and security controls for cloud resources. Networking is an important part of cloud architecture because it determines how resources communicate with one another.

### 🔴 Identity and Access Management

AWS IAM, Microsoft Entra ID, and Cloud IAM provide identity and access management capabilities. These systems allow administrators to control which users, applications, and services can access cloud resources. Proper access control helps reduce unauthorized access and supports cloud security.

---

<a id="guide-questions"></a>

# 🔴 Guide Questions

---

## 1. Which cloud provider offers the broadest range of services?

AWS offers the broadest range of services because it was the first major player in the public cloud market (launching in 2006). Its extensive service catalog covers everything from basic compute to specialized satellite communications and quantum computing, giving it the most mature ecosystem available. **This wide range of services gives organizations many options when building, expanding, and integrating different types of cloud workloads.**

### 💡 Additional Understanding

AWS provides services across many categories, including compute, storage, networking, databases, security, analytics, artificial intelligence, machine learning, Internet of Things, and application development. This extensive service ecosystem can be useful for organizations that want to use multiple cloud capabilities from a single provider. However, the best provider still depends on the organization's specific requirements, budget, existing technology, and technical expertise.

---

## 2. Which cloud platform would you recommend for an organization that primarily uses Microsoft products?

I would recommend Microsoft Azure because it offers seamless integration with existing Microsoft technologies like Windows Server, Active Directory, and Office 365. Organizations can often use their existing software licenses in the cloud through the Azure Hybrid Benefit, making the migration more cost-effective. **This makes Azure a practical option for organizations that already depend heavily on Microsoft's products, identity services, and enterprise technologies.**

### 💡 Additional Understanding

Azure is designed to work closely with Microsoft's existing enterprise ecosystem. This can make it easier for organizations to manage users, applications, servers, and other resources when their existing infrastructure already uses Microsoft technologies. Azure can therefore reduce some of the complexity involved in migrating Microsoft-based workloads to the cloud.

---

## 3. Which platform is widely recognized for Artificial Intelligence (AI), Machine Learning (ML), and Kubernetes services?

Google Cloud Platform (GCP) is the leader in this area because Google originally developed Kubernetes and has a long history of processing massive amounts of data. Their specialized AI tools (like Vertex AI) and deep learning hardware (TPUs) make them the preferred choice for data-heavy and AI-driven projects. **These capabilities make GCP particularly attractive for organizations developing AI, machine learning, data analytics, and containerized applications.**

### 💡 Additional Understanding

GCP has strong technologies for managing large-scale data and machine learning workloads. Google Kubernetes Engine (GKE) also provides managed Kubernetes capabilities for deploying and managing containerized applications. These technologies can be useful for organizations that need scalable infrastructure for modern cloud-native applications.

---

## 4. What similarities did you observe among the three cloud providers?

All three providers follow a similar "pay-as-you-go" pricing model and offer high availability through global data centers (Regions and Zones). They also share a common infrastructure foundation where they provide virtualized compute, storage, and networking resources managed through a central Identity (IAM) system. **These similarities mean that the fundamental cloud infrastructure concepts can be transferred between providers even when the service names and interfaces are different.**

### 💡 Additional Understanding

The three providers use similar fundamental cloud computing concepts. For example, a virtual machine on AWS has a comparable role to a virtual machine on Azure or Compute Engine on GCP. This makes it possible for cloud engineers to compare equivalent services and plan migrations between cloud platforms.

---

<a id="cloud-migration-summary"></a>

# 🔵 Cloud Migration Summary 🔴

The comparison demonstrates that AWS, Microsoft Azure, and Google Cloud Platform all provide the major infrastructure services required for modern cloud environments. Although the providers use different product names and interfaces, their fundamental concepts of compute, storage, networking, and identity management are similar. This allows cloud engineers to map existing infrastructure resources to equivalent services when planning a cloud migration.

## 📊 Provider Strengths

| Provider | Primary Strength | Example Use |
|---|---|---|
| 🔵 **AWS** | Broad service ecosystem | Large and diverse cloud environments |
| 🔴 **Microsoft Azure** | Microsoft ecosystem integration | Microsoft-based enterprise workloads |
| 🔵 **Google Cloud Platform** | AI, ML, data, and Kubernetes | AI and cloud-native applications |

---

## 🔄 Example Cloud Service Mapping

| Existing Infrastructure | 🔵 AWS | 🔴 Azure | 🔵 GCP |
|---|---|---|---|
| 🖥️ **Compute** | EC2 | Virtual Machines | Compute Engine |
| 💾 **Object Storage** | S3 | Blob Storage | Cloud Storage |
| 💿 **Block Storage** | EBS | Disk Storage | Persistent Disk |
| 🌐 **Networking** | VPC | VNet | VPC Network |
| 🔐 **IAM** | AWS IAM | Microsoft Entra ID | Cloud IAM |

This mapping demonstrates how similar infrastructure requirements can be implemented across different cloud providers. It is useful during migration planning because engineers can identify the closest equivalent service before moving workloads. The final selection should consider performance, cost, security, compatibility, availability, and organizational requirements.

---

## 🧠 Key Learning

This activity helped me understand that AWS, Azure, and GCP provide similar fundamental cloud infrastructure capabilities while using different service names and technologies. Comparing equivalent services makes it easier to understand cloud architecture and plan possible migrations between providers. It also demonstrates the importance of selecting a cloud platform based on the organization's workload requirements rather than simply choosing a provider based on popularity.

---

## ☁️ Cloud Migration Planning Considerations

| Consideration | Why It Matters |
|---|---|
| 💰 **Cost** | Helps determine whether the cloud solution is financially practical |
| ⚙️ **Performance** | Ensures applications receive sufficient computing and storage resources |
| 🔐 **Security** | Protects applications, data, identities, and infrastructure |
| 🌐 **Networking** | Ensures reliable communication between cloud resources |
| 📈 **Scalability** | Allows resources to increase or decrease according to demand |
| 🔄 **Compatibility** | Determines whether existing applications can operate in the selected cloud |
| 🛠️ **Management** | Determines how easily administrators can monitor and maintain resources |
| 📍 **Availability** | Helps ensure services remain accessible when required |

---

<p align="center">

🔵 **CLOUD COMPUTING** &nbsp; • &nbsp;
🔴 **CLOUD MIGRATION** &nbsp; • &nbsp;
🔵 **INFRASTRUCTURE** &nbsp; • &nbsp;
🔴 **CLOUD PROVIDERS**

</p>

<p align="center">

### 🔵 CCM101 – Cloud Computing 🔴

**CloudNova Technologies**  
**Mission 2 | Cloud Migration Planning**

</p>

<p align="center">

<a href="#-cloud-provider-comparison-report">
<img src="https://img.shields.io/badge/⬆️_BACK_TO_TOP-1976D2?style=for-the-badge" />
</a>

</p>
