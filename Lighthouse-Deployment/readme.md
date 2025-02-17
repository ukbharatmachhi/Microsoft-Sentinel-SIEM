# Azure Lighthouse: Overview & Deployment
Azure Lighthouse is a multi-tenant management solution that enables Managed Service Providers (MSPs) and enterprises to manage multiple Azure tenants securely and efficiently. It allows cross-tenant access to subscriptions, resource groups, and services without requiring direct logins to each customer’s environment.

## Key Features of Azure Lighthouse
**1. Centralized Management** – Manage multiple Azure tenants from a single pane of glass.
**2. Granular Access Control** – Uses Azure RBAC to control permissions per tenant.
**3. Scalability** – Ideal for MSPs and enterprises managing multiple clients.
**4. Security & Compliance **– Provides just-in-time access and least privilege access control.
**5. Automation & Monitoring** – Uses Azure Monitor, Log Analytics, and Security Center across tenants.

## Benefits
1.  Manage multiple Azure tenants from a **single interface**.
2.  Enforce **role-based access control (RBAC)** for security.
3.  Improve **efficiency** by automating onboarding using **ARM Templates**.

## Azure Lighthouse Deployment Process to Client Tenant
### Step 1: Log Into the Clients tenant 
Goto Azure Portal and Login as Global Administrator and search for Azure Lighthouse and Click on Deploy to Azure for Azure Lighthouse – Subscription Deployment 

![Reference Image](light1.jpg)
