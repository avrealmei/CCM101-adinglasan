# 🔵 CLOUD PROVIDER COMPARISON REPORT 🔴

<p align="center">

### ☁️ CCM101 – Cloud Computing

**CloudNova Technologies | Cloud Migration Planning**



<!-- ===================================================== -->
<!-- 🔵🔴 HORIZONTAL NAVIGATION -->
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

# 🔵 Infrastructure Service Comparison Table 🔴

**Project:** CloudNova Technologies - Cloud Migration Planning  
**Date:** August 25, 2026

## 📋 Report Overview

This report compares the major infrastructure services offered by **Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP)**.

The purpose of this comparison is to understand how the three major cloud providers deliver equivalent cloud infrastructure services using different product names and technologies.

This comparison supports the **Cloud Infrastructure Blueprint** by helping identify suitable cloud services for future deployment and migration planning.

---

## 🎯 Comparison Objectives

| Objective | Description |
|---|---|
| 🔵 **Identify Services** | Identify equivalent infrastructure services from AWS, Azure, and GCP |
| 🔴 **Compare Providers** | Compare the major capabilities of each cloud platform |
| 🔵 **Understand Cloud Services** | Understand the purpose of compute, storage, networking, and IAM |
| 🔴 **Support Migration** | Identify possible cloud services for infrastructure migration |
| 🔵 **Evaluate Strengths** | Understand the major strengths of each cloud provider |
| 🔴 **Support Decision-Making** | Provide information for selecting an appropriate cloud platform |

---

## ☁️ Infrastructure Service Comparison

| Infrastructure Component | 🔵 Amazon Web Services (AWS) | 🔴 Microsoft Azure | 🔵 Google Cloud Platform (GCP) |
| :--- | :--- | :--- | :--- |
| **Compute** | EC2 (Elastic Compute Cloud) | Virtual Machines | Compute Engine |
| **Storage** | S3 (Object) / EBS (Block) | Blob Storage / Disk Storage | Cloud Storage / Persistent Disk |
| **Networking** | VPC (Virtual Private Cloud) | VNet (Virtual Network) | VPC Network |
| **Identity & Access Management** | AWS IAM | Microsoft Entra ID (formerly Azure AD) | Cloud IAM |

---

## 💡 Understanding the Infrastructure Components

The services listed in the table perform similar fundamental infrastructure functions, even though their names and implementations differ.

### ⚙️ Compute

Compute services provide the processing resources required to run applications, operating systems, APIs, websites, databases, and other workloads.

| Provider | Compute Service | Main Purpose |
|---|---|---|
| 🔵 AWS | EC2 | Runs virtual servers in the cloud |
| 🔴 Azure | Virtual Machines | Runs Windows or Linux virtual machines |
| 🔵 GCP | Compute Engine | Runs configurable virtual machine instances |

**Cloud Concept:** Compute represents the processing layer of a cloud infrastructure.

---

### 💾 Storage

Cloud storage provides persistent locations for applications, operating systems, backups, files, and other data.

| Provider | Object Storage | Block Storage |
|---|---|---|
| 🔵 AWS | S3 | EBS |
| 🔴 Azure | Blob Storage | Disk Storage |
| 🔵 GCP | Cloud Storage | Persistent Disk |

**Cloud Concept:** Storage provides persistent data capacity that can be used independently or together with compute resources.

---

### 🌐 Networking

Cloud networking allows virtual machines, applications, databases, users, and other services to communicate.

| Provider | Virtual Network | Main Purpose |
|---|---|---|
| 🔵 AWS | VPC | Creates an isolated virtual network |
| 🔴 Azure | VNet | Provides private cloud networking |
| 🔵 GCP | VPC Network | Connects cloud resources securely |

**Cloud Concept:** Networking provides connectivity and helps define how cloud resources communicate with one another.

---

### 🔐 Identity & Access Management

Identity and Access Management controls users, roles, permissions, and access to cloud resources.

| Provider | IAM Service | Main Purpose |
|---|---|---|
| 🔵 AWS | AWS IAM | Controls access to AWS resources |
| 🔴 Azure | Microsoft Entra ID | Manages identities and access |
| 🔵 GCP | Cloud IAM | Controls access to GCP resources |

**Cloud Concept:** IAM provides an important security layer by ensuring that users and services receive only the permissions they require.

---

# 🔴 Guide Questions

<a id="guide-questions"></a>

---

## 1. Which cloud provider offers the broadest range of services?

AWS offers the broadest range of services because it was the first major player in the public cloud market (launching in 2006). Its extensive service catalog covers everything from basic compute to specialized satellite communications and quantum computing, giving it the most mature ecosystem available. **This wide range of services gives organizations many options when building, expanding, and integrating different types of cloud workloads.**

### 💡 Additional Understanding

AWS provides services across numerous categories, including compute, storage, networking, databases, security, analytics, artificial intelligence, machine learning, and application development.

A broad service catalog can be useful for organizations that want to build multiple parts of their infrastructure within a single cloud ecosystem.

However, service breadth alone does not determine which provider is best because organizations must also consider cost, performance, security, compatibility, and existing infrastructure.

---

## 2. Which cloud platform would you recommend for an organization that primarily uses Microsoft products?

I would recommend Microsoft Azure because it offers seamless integration with existing Microsoft technologies like Windows Server, Active Directory, and Office 365. Organizations can often use their existing software licenses in the cloud through the Azure Hybrid Benefit, making the migration more cost-effective. **This makes Azure a practical option for organizations that already depend heavily on Microsoft's products, identity services, and enterprise technologies.**

### 💡 Additional Understanding

Azure is particularly relevant for organizations that already use Microsoft-based infrastructure and services.

Its integration with Microsoft identity, server, productivity, and enterprise technologies can simplify administration and migration planning.

Organizations should still evaluate workload requirements, licensing, pricing, security, and performance before making a final provider decision.

---

## 3. Which platform is widely recognized for Artificial Intelligence (AI), Machine Learning (ML), and Kubernetes services?

Google Cloud Platform (GCP) is the leader in this area because Google originally developed Kubernetes and has a long history of processing massive amounts of data. Their specialized AI tools (like Vertex AI) and deep learning hardware (TPUs) make them the preferred choice for data-heavy and AI-driven projects. **These capabilities make GCP particularly attractive for organizations developing AI, machine learning, data analytics, and containerized applications.**

### 💡 Additional Understanding

GCP has strong capabilities for large-scale data processing, machine learning, artificial intelligence, and cloud-native development.

Google Kubernetes Engine (GKE) also provides managed Kubernetes capabilities for deploying and managing containerized workloads.

These technologies make GCP a strong option for projects that require advanced data processing, machine learning, AI development, or Kubernetes-based infrastructure.

---

## 4. What similarities did you observe among the three cloud providers?

All three providers follow a similar "pay-as-you-go" pricing model and offer high availability through global data centers (Regions and Zones). They also share a common infrastructure foundation where they provide virtualized compute, storage, and networking resources managed through a central Identity (IAM) system. **These similarities mean that the fundamental cloud infrastructure concepts can be transferred between providers even when the service names and interfaces are different.**

### 💡 Additional Understanding

The three providers follow similar fundamental cloud computing concepts.

For example, AWS EC2, Azure Virtual Machines, and GCP Compute Engine all provide virtual computing resources even though they are different products.

This similarity makes it possible for cloud engineers to compare equivalent services and plan infrastructure migrations between cloud providers.

---

<a id="cloud-migration-summary"></a>

# 🔵 Cloud Migration Summary 🔴

The comparison demonstrates that AWS, Microsoft Azure, and Google Cloud Platform provide the major infrastructure services required for modern cloud environments.

Although the providers use different product names and interfaces, their fundamental infrastructure concepts remain similar.

This allows cloud engineers to map existing infrastructure components to equivalent cloud services during migration planning.

---

## 🔄 Cloud Service Mapping

The following table demonstrates how common infrastructure resources can be mapped between the three major cloud providers.

| Existing Infrastructure | 🔵 AWS | 🔴 Microsoft Azure | 🔵 GCP |
|---|---|---|---|
| 🖥️ **Virtual Server** | EC2 | Virtual Machines | Compute Engine |
| 💾 **Object Storage** | S3 | Blob Storage | Cloud Storage |
| 💿 **Block Storage** | EBS | Disk Storage | Persistent Disk |
| 🌐 **Virtual Network** | VPC | VNet | VPC Network |
| 🔐 **Identity Management** | AWS IAM | Microsoft Entra ID | Cloud IAM |

### 📌 Migration Concept

A cloud migration does not necessarily require an organization to completely redesign its infrastructure.

Instead, existing workloads can be analyzed and mapped to equivalent cloud services.

For example:

```text
Existing Server
      │
      ▼
┌───────────────────────┐
│ Compute Requirement   │
└───────────┬───────────┘
            │
      ┌─────┼─────┐
      ▼     ▼     ▼
     AWS   Azure  GCP
     EC2    VM    Compute
