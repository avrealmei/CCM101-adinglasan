# Cloud Storage Architecture Research

As part of CloudNova Technologies' data engineering assignment, this document provides a comprehensive comparison of the three primary cloud storage architectures and determines the optimal storage solution for the client's upcoming photo-sharing application.

---

## Cloud Storage Comparison Table

| Storage Type | Description (How does it store data?) | Primary Use Case | Cloud Provider Example |
| :--- | :--- | :--- | :--- |
| **Block Storage** | Data is split into raw, equally-sized blocks, each with its own unique address. It functions like a physical hard drive attached directly to a server or virtual machine operating system. | High-performance transactional databases, enterprise resource planning (ERP) systems, and virtual machine boot/root volumes. | AWS EBS (Elastic Block Store) |
| **File Storage** | Data is organized as files and directories within a hierarchical folder structure. It is accessed across a network using file-level sharing protocols. | Shared corporate file servers, department home directories, and collaborative software development workspaces. | AWS EFS (Elastic File System) |
| **Object Storage** | Data is broken down into discrete units called "objects," consisting of the data payload, metadata, and a globally unique identifier (URI). It is accessed over the web via REST APIs. | Unstructured data storage, server backups, media streaming, static web hosting, and user-uploaded media files (photos/videos). | AWS S3 (Simple Storage Service) |

---

## Recommendation for the Client's Photo-Sharing Application

Object Storage is the absolute best choice for the client's photo-sharing application because containers are ephemeral (temporary) and cannot securely or permanently store millions of user-uploaded images locally. By utilizing a scalable object storage architecture, the application achieves infinite scalability, high data durability, and fast web-accessible asset retrieval.
