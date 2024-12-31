# Azure Role-Based Access Control (RBAC) & User Permissions Configuration

## Project Overview
In this project, I configured and tested different **Role-Based Access Control (RBAC)** roles in **Azure Active Directory (AAD)**. The goal was to explore how different roles impact user permissions at various levels in Azure, such as **tenant-level**, **subscription-level**, and **resource group-level**. This exercise helped me better understand Azure's permission model and how to enforce the **principle of least privilege** in cloud environments.

## Roles Configured and Observed
### 1. **Tenant-Level Global Reader**
   - **User**: `globalreaderjohn`
   - **Role Assigned**: Tenant-Level **Global Reader** (read-only permissions across the entire Azure tenant)
   - **Outcome**: Logged in as `globalreaderjohn` and verified the result of being a **Global Reader** at the tenant level (access to view resources, but no ability to modify them).

### 2. **Subscription-Level Reader**
   - **User**: `subreaderjane`
   - **Role Assigned**: Subscription-Level **Reader** (read-only permissions at the subscription level)
   - **Outcome**: Logged in as `subreaderjane` and confirmed that the **Subscription Reader** role allowed them to view subscription-level resources but not modify them.

### 3. **Resource Group-Level Contributor**
   - **User**: `rgcontributordave`
   - **Role Assigned**: **Contributor** at the Resource Group level for a newly created resource group called `Permissions-Tester`
   - **Outcome**: 
     - Assigned **Contributor** permissions on the resource group `RG-Cyber-Lab` to `rgcontributordave` and observed their ability to manage resources within the group.
     - Logged in as `rgcontributordave` to confirm that the **Contributor** role allowed them to create, modify, and delete resources in the specified group, while restricting access to other resources outside of that group.

## Key Learnings
- **Understanding Azure RBAC**: This project reinforced my understanding of how Azure uses **role-based access control** to manage permissions at different scopes (tenant, subscription, and resource group levels).
- **Security Best Practices**: I learned how important it is to assign users the **least privileged access** based on their roles to minimize security risks in cloud environments.
- **Practical Experience**: This hands-on task helped me practice assigning roles and testing user access, ensuring that users only have the permissions they need.

## Technologies Used
- **Azure Active Directory (AAD)**
- **Azure Role-Based Access Control (RBAC)**
- **Azure Resource Manager (ARM)**

## Conclusion
This exercise helped me gain practical experience in managing **role assignments** and **permissions** in Azure. By configuring these different roles, I learned how to carefully manage access at various levels, ensuring secure and efficient use of resources in an Azure environment. These skills are critical for roles involving **cloud governance**, **security**, and **resource management**.

