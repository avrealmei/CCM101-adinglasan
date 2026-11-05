# 🔍 Security Audit Report: Chapter 8 Concepts

<div align="center">


## 📌 Security Theory Definitions

### 1. The Principle of Least Privilege (PoLP)
The Principle of Least Privilege (PoLP) dictates that a user account, process, or service should only be given the bare minimum permissions necessary to perform its intended function. In cloud user accounts, this is crucial because it limits the "blast radius" if an account or credential is compromised, preventing attackers from gaining root control or accessing sensitive data across the entire infrastructure.

### 2. Attack Surface
An attack surface refers to the sum total of all vulnerable entry points, exposed ports, services, and interfaces through which an unauthorized user can try to enter or extract data from a virtual machine or cloud environment. When applied to a virtual machine, every open network port or unpatched software package expands this surface, increasing the likelihood of a security breach.

### 3. Default Deny Policy
A Default Deny policy is a security posture where all network traffic is blocked by default, and only explicitly approved traffic channels are permitted to pass through. It is significantly safer than trying to block specific hackers individually because malicious actors constantly change IP addresses and attack vectors, whereas a strict deny-all baseline ensures unknown threats are automatically intercepted.
