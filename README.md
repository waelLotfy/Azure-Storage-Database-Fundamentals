# Azure Storage & Database Fundamentals — Hands-on Exploration

## Overview
This repository documents hands-on labs focused on Azure storage and database services completed as part of the AZ-900T00-A course.  
The work explores how Azure stores unstructured data using Blob Storage, hosts static web content, and manages relational data using Azure SQL Database.

---

## Labs Completed
- Create a storage account
- Create Blob containers and upload data
- Deploy a static website using Azure Blob Storage
- Share files securely using Azure Storage
- Monitor storage account usage
- Create an Azure SQL Database
- Query data using SQL

---

## Core Concepts Explored

### Azure Storage Account
- Foundation for Azure storage services
- Provides security, scalability, and redundancy
- Supports multiple storage types (Blob, File, Queue, Table)

### Azure Blob Storage
- Optimized for unstructured data such as documents, images, and backups
- Uses containers to organize blobs
- Supports static website hosting through the special **$web** container

### Static Website Hosting with Blob Storage
- Lightweight, cost-effective hosting for HTML/CSS/JS content
- Public endpoint automatically generated when hosting is enabled
- Ideal for simple sites, documentation, or static front-ends

### Secure File Sharing with Azure Storage
- Enables controlled sharing of files using **Stored Access Policies** and **Shared Access Signatures (SAS)**
- Provides fine-grained access permissions and expiry management
- Supports lifecycle rules for automatic cleanup of shared data
- Demonstrates enterprise-grade governance for external data exchange

### Azure SQL Database
- Fully managed relational database service
- Uses standard SQL for querying data
- Eliminates the need to manage database servers
- Provides built-in high availability, backups, and maintenance

---

## Detailed Lab Summaries

### 1. Create Storage Account and Enable Static Website Hosting
- Created a resource group and deployed a storage account.
- Enabled the **Static website** feature.
- Configured `index.html` and `error.html` document paths.
- Azure generated a public endpoint for hosting.
  
**Outcome:**  
A storage account with static website hosting enabled and a public endpoint ready to serve content.

---

### 2. Upload and Verify Site Content
- Created an `index.html` file and a custom `error.html` page.
- Uploaded both files to the **$web** container.
- Verified the live site and confirmed the error page behavior.

**Outcome:**  
A live public website displaying Version 1 content.

---

### 3. Update the Static Website Content
- Created an updated Version 2 of the HTML file.
- Replaced the existing file in the **$web** container.
- Verified the updated site content.
- Reviewed blob properties such as:
  - Content type
  - Access tier
  - Last modified timestamp

**Outcome:**  
The live website displayed updated Version 2 content after replacing the original file.

---

### 4. Share Files Securely Using Azure Storage
- Created a private container and uploaded a sample report file.
- Configured a **Stored Access Policy** and generated a **SAS URL** for secure partner access.
- Verified that direct anonymous access was blocked while SAS-based access succeeded.
- Revoked partner access by deleting the stored access policy, instantly invalidating all SAS tokens.
- Implemented a **Lifecycle Management Rule** to automatically delete shared files after 30 days.

**Outcome:**  
Secure file sharing implemented with enterprise-grade access control, instant revocation capability, and automated lifecycle management for shared data.

---

### 5. Blob Storage Operations
- Created containers and uploaded sample data.
- Explored blob types and access tiers.
- Monitored storage account usage and metrics.

---

## Key Learnings
- Azure provides different storage services for structured and unstructured data.
- Blob Storage is optimized for scalable file and object storage.
- Static website hosting is a simple, cost-effective way to publish web content.
- Secure file sharing with SAS and access policies enables controlled external collaboration.
- Lifecycle management ensures data hygiene and compliance.
- Azure SQL Database offers a fully managed relational platform.
- Storage and database resources can be monitored for performance and usage.
- Blob properties and access tiers influence performance and cost.

---

## Next Steps
- Explore Azure File Storage and Disk Storage.
- Apply security and access control to storage and databases.
- Integrate storage and databases with compute services.
- Automate deployments using ARM templates or Bicep.
