#cloud #azure #az-305 #professional

## Exam Overview

- The AZ-305 exam is designed to test your knowledge and skills in designing and implementing solutions that run on Microsoft Azure.
- The exam covers topics such as identity, business continuity, security, data platforms, disaster recovery, networking, virtualization, and governance.

## Identity

- Understand the different types of identity solutions available in Azure, including Azure Active Directory (AAD), AAD B2C, and AAD B2B.
- Know how to configure authentication and authorization for applications using AAD.
- Understand how to use AAD to manage access to resources.

### Azure Active Directory (AAD)

Azure Active Directory (AAD) is a cloud-based identity and access management service that helps you manage user identities and access to your resources. With AAD, you can manage users, groups, and devices, and provide secure access to your applications and resources.

### AAD B2C

Azure Active Directory B2C (AAD B2C) is a customer identity and access management service that helps you manage customer identities and provide secure access to your applications. With AAD B2C, you can enable customers to sign in to your applications using their existing social or enterprise identities, or by creating new accounts in your application.

### AAD B2B

Azure Active Directory B2B (AAD B2B) is a feature of AAD that allows you to collaborate with external users by inviting them to access your resources using their own credentials. With AAD B2B, you can share resources with external users while maintaining control over who has access to your resources

### Configuring Authentication

To configure authentication for your application using AAD, you need to register your application in the Azure portal and configure it to use AAD as an identity provider. Here are the steps to do this:

1. Sign in to the [Azure portal] and navigate to the **Azure Active Directory** blade.
2. In the left-hand menu, select **App registrations** and then click **New registration**.
3. Enter a name for your application and select the supported account types.
4. Provide a **Redirect URI** where AAD will redirect users after they have signed in.
5. Click **Register** to create the application.

Once your application is registered, you can configure it to use OpenID Connect or OAuth 2.0 for authentication. You can do this by updating the application’s code to use one of these protocols and providing the necessary configuration information, such as the application’s client ID and tenant ID.

### Configuring Authorization

To configure authorization for your application using AAD, you need to define the permissions that your application requires and request consent from users to access these permissions. Here are the steps to do this:

1. In the Azure portal, navigate to your application’s registration page.
2. In the left-hand menu, select **API permissions**.
3. Click **Add a permission** and select the API that your application needs to access.
4. Select the permissions that your application requires and click **Add permissions**.

Once you have defined the permissions that your application requires, you can request consent from users when they sign in to your application. You can do this by including a `prompt=consent` parameter in the authentication request, which will prompt users to grant consent to your application.

### Role-Based Access Control (RBAC)

Role-based access control (RBAC) is a method of managing access to resources based on the roles assigned to users. With RBAC, you can define roles with specific permissions and assign these roles to users or groups. This allows you to control who has access to your resources and what actions they can perform.

To use RBAC in Azure, you need to define roles and assign them to users or groups. Here are the steps to do this:

1. Sign in to the [Azure portal] and navigate to the **Azure Active Directory** blade.
2. In the left-hand menu, select **Roles and administrators**.
3. Select the role you want to assign and click **Add assignments**.
4. Search for the user or group you want to assign the role to and click **Select**.

Once you have assigned roles to users or groups, they will have access to the resources specified in the role definition.

### Conditional Access

Conditional access is a feature of AAD that allows you to enforce policies based on conditions such as user location, device state, and sign-in risk. With conditional access, you can control access to your resources based on these conditions.

To use conditional access in Azure, you need to create a conditional access policy. Here are the steps to do this:

1. Sign in to the [Azure portal] and navigate to the **Azure Active Directory** blade.
2. In the left-hand menu, select **Security** and then **Conditional Access**.
3. Click **New policy** and provide a name for your policy.
4. Select the conditions you want to apply and configure the actions that will be taken when these conditions are met.
5. Click **Create** to create the policy.

Once you have created a conditional access policy, it will be enforced when users attempt to access your resources.

### Privileged Identity Management (PIM)

Privileged identity management (PIM) is a feature of AAD that allows you to manage and monitor access to privileged roles in your organization. With PIM, you can control who has access to these roles and when they can use them.

To use PIM in Azure, you need to enable it for your organization. Here are the steps to do this:

1. Sign in to the [Azure portal] and navigate to the **Azure Active Directory** blade.
2. In the left-hand menu, select **Identity Governance**.
3. Click **Get started** under **Privileged Identity Management**.
4. Follow the prompts to enable PIM for your organization.

Once PIM is enabled, you can manage access to privileged roles using features such as just-in-time (JIT) access and approval workflows.

## Business Continuity

- Understand the different options for ensuring business continuity in Azure, including backup and restore, site recovery, and geo-redundancy.
- Know how to design and implement a disaster recovery plan using Azure Site Recovery.
- Understand how to use Azure Backup to protect data.

### Backup and Restore

Backup and restore is a method of protecting your data by creating copies of it and storing them in a separate location. In the event of a disaster, you can use these backups to restore your data and resume operations.

Azure provides several options for backing up your data, including Azure Backup and Azure Site Recovery. With Azure Backup, you can back up your data to the cloud and restore it when needed. With Azure Site Recovery, you can replicate your virtual machines to another location and failover to them in the event of a disaster.

### Site Recovery

Site recovery is a method of protecting your applications by replicating them to another location. In the event of a disaster, you can failover to the replicated applications and resume operations.

Azure Site Recovery provides a solution for replicating your virtual machines to another location. With Site Recovery, you can configure replication, failover, and failback for your virtual machines. This allows you to protect your applications and ensure their availability during a disaster.

### Geo-Redundancy

Geo-redundancy is a method of protecting your data by storing copies of it in multiple geographic locations. In the event of a disaster that affects one location, you can use the data stored in another location to resume operations.

Azure provides several options for achieving geo-redundancy, including using geo-redundant storage (GRS) and read-access geo-redundant storage (RA-GRS). With GRS, your data is replicated to another region for durability. With RA-GRS, your data is replicated to another region and is also available for read access.

### Designing a Disaster Recovery Plan

To design a disaster recovery plan using Azure Site Recovery, you need to consider several factors, including your recovery objectives, the applications you want to protect, and the resources you have available.

Here are some steps to follow when designing a disaster recovery plan with Azure Site Recovery:

1. **Identify your recovery objectives**: Determine your recovery time objective (RTO) and recovery point objective (RPO). These objectives define how quickly you need to recover your applications and how much data loss is acceptable.
2. **Assess your applications**: Identify the applications you want to protect and assess their dependencies and requirements. This will help you determine the best way to replicate and failover these applications.
3. **Choose a replication target**: Select a target location for replicating your applications. This could be another region within the same cloud provider or a different cloud provider altogether.
4. **Define your failover and failback processes**: Determine how you will failover to the replicated applications in the event of a disaster and how you will failback to the primary location once it is restored.

### Implementing a Disaster Recovery Plan

Once you have designed your disaster recovery plan, you can implement it using Azure Site Recovery. Here are some steps to follow when implementing a disaster recovery plan with Azure Site Recovery:

1. **Set up replication**: Configure replication for your virtual machines using Azure Site Recovery. This involves installing the Site Recovery agent on your virtual machines, creating a replication policy, and setting up replication.
2. **Test failover**: Perform a test failover to ensure that your disaster recovery plan is working as expected. This involves failing over to the replicated virtual machines and verifying that they are functioning correctly.
3. **Monitor replication**: Monitor the replication status of your virtual machines to ensure that they are being replicated correctly. You can do this using the Azure portal or by setting up alerts.
4. **Perform failover and failback**: In the event of a disaster, perform a failover to the replicated virtual machines. Once the primary location is restored, perform a failback to return to normal operations.

### Configuring Azure Backup

To use Azure Backup to protect your data, you need to configure it by creating a backup vault, defining a backup policy, and selecting the data you want to back up. Here are the steps to do this:

1. Sign in to the [Azure portal] and navigate to the **Backup** blade.
2. Click **Add** and select **Backup vault**.
3. Provide a name and location for your backup vault and click **Create**.
4. Once your backup vault is created, navigate to it and click **Backup**.
5. Select the type of data you want to back up and follow the prompts to configure your backup policy.

Once you have configured Azure Backup, it will automatically create backups of your data according to the schedule you defined in your backup policy.

### Restoring Data with Azure Backup

In the event that you need to restore data from a backup, you can do so using Azure Backup. Here are the steps to restore data with Azure Backup:

1. Sign in to the [Azure portal] and navigate to your backup vault.
2. Click **Restore** and select the type of data you want to restore.
3. Select the backup from which you want to restore data and click **OK**.
4. Follow the prompts to configure your restore settings and click **Restore**.

Once you have initiated a restore operation, Azure Backup will restore your data from the selected backup.

## Security

- Understand the different security features available in Azure, including network security groups (NSGs), application security groups (ASGs), and Azure Firewall.
- Know how to configure security for virtual networks and subnets using NSGs and ASGs.
- Understand how to use Azure Security Center to monitor the security of your resources.



## Data Platforms

- Understand the different data platform options available in Azure, including Azure SQL Database, Cosmos DB, and Azure Data Lake Storage.
- Know how to design and implement a data platform solution using these services.
- Understand how to use Azure Data Factory to move and transform data.



## Disaster Recovery

- Understand the different options for disaster recovery in Azure, including backup and restore, site recovery, and geo-redundancy.
- Know how to design and implement a disaster recovery plan using Azure Site Recovery.
- Understand how to use Azure Backup to protect data.



## Networking

- Understand the different networking options available in Azure, including virtual networks (vNets), ExpressRoute, and VPN Gateway.
- Know how to design and implement a virtual network using vNets.
- Understand how to use ExpressRoute or VPN Gateway to connect on-premises networks to Azure.



## Virtualization

- Understand the different virtualization options available in Azure, including virtual machines (VMs) and containers.
- Know how to design and implement a virtualization solution using VMs or containers.
- Understand how to use Azure Kubernetes Service (AKS) to manage containerized applications.



## Governance

- Understand the different governance features available in Azure, including resource locks, tags, and policies.
- Know how to use these features to manage resources at scale.
- Understand how to use Azure Blueprints to enforce governance across multiple subscriptions.

