# **Joey’s Microsoft Azure Fundamentals (AZ-900) Cheatsheet**

**Benefits of cloud services:**  
The big three: Azure, AWS and GCP

* Security and Compliance  
* Flexibility and Scalability  
* Reduced downtime

Azure Specifically

* Integration with other Microsoft products  
* Enterprise agreement for large companies using other Microsoft Products

**Storage Options:**  
Locally-redundant Storage (LRS): Replicates data three times in a single data center from the primary region, providing efficiency cost but less data protection. The primary region is where the storage account was created.

Zone-redundant Storage (ZRS): The zone-redundant option replicates your storage data across three availability zones in the primary region.

Geo-redundant Storage (GRS): It replicates your data to a secondary region. It is like using locally redundant storage in two regions, with data having three copies in one data centre for each region

Geo-zone-redundant Storage (GZRS): It offers high availability from redundancy across zones and protection from regional outages. Data is copied across three availability zones in the primary region and also replicated to the secondary region. It is the optimal choice for achieving the best availability, excellent performance and resilience for disaster recovery.

**Different types of Services:**  
Software as a Service (Saas): Microsoft office 365  
Platform as a Service (Paas): Examples Include Azure App services and Azure Cosmos dB  
Infrastructure as a Service (Iaas): Examples include Virtual Machines  
![image](https://github.com/user-attachments/assets/861116b0-0bea-45b4-8ab5-9c9538d2438f)

Azure Hierarchical Structure  
![image](https://github.com/user-attachments/assets/8710a7c6-cb17-4d62-b183-a2063fcd3ce7)
**Azure Storage Services** (except for disks the rest require a storage account set up to be used)  
Blobs (Binary Large Objects): Storing large amounts of unstructured data such as video, images, documents. Used for storing files for widespread access, streaming video and audio content, storing backup disaster recovery and archives and lastly direct delivery of images or documents to the web.

Access tiers for blobs

* Hot Access tier: Frequently accessed data  
* Cool Access tier: Data accessed infrequently  
* Cold Access tier: Rarely accessed data  
* Archive Access tier: Archiving purposes

Files: Allowing files in the cloud to be easily accessed from different devices, including both cloud and on-premises systems. Files can be accessed from most operating systems, including Windows, Linux and macOS. This can be used when a shared storage solution is required for multiple users or applications and when cross-platform access is needed. Accessible via Server Message Block (SMB) or Network File System (NFS) protocols

Queues: Digital message service in the cloud, enables communication between various components, programs or applications. They are usually implemented in workflows that contain multiple other services.

Tables: NoSQL data in storage account. Store and retrieve data flexible and schema-less (flexible data structure). Suitable for fast and scalable access to large amounts of unstructured data, it is also cost effective and simple to manage.

Disks/ Azure Managed Disks: Provide storage space for operating systems, applications and data.Are used in virtual machines functionality.

**Data Migration options**  
Azure Migrate (real-time): A service to move from on-premises to the cloud and offers a variety of tools for assessing and migrating data. Helpful for companies looking to move their data to azure cloud.

Azure Data Box (conventional): A physical migration service, where the data box is a hardware device with numerous storage drives. Azure sends the box to your location, you copy data onto it, and send back. Once the process is complete, Azure ensures your data is restored in their data center and ready for future use.

**File Operations Tools**  
AzCopy: Command-line tool that facilitates file manipulation such as upload, download and copying between storage accounts and local sources. Can be used too to work with other cloud providers, being helpful for file movement between clouds.

Azure Storage Explorer: Application with a graphical interface that has the same functionality as AzCopy. It is used to handle files and blobs in Azure storage accounts.

Azure File Sync: It is a service that can synchronize files across different computers and Azure cloud. It ensures that the most recent files are accessible from any location. 

**Azure Compute Services**  
Iaas: Provides virtualized computing resources over the internet, it is an alternative to traditional on-premises infrastructure. These include virtual machines and networking. Using a virtual machine in the cloud eliminates the need for hardware maintenance and provides the freedom to select your operating system and install a variety of applications, like you would do with an on-premises server. Azure manages the hardware failures and potential disasters, ensuring your virtual machine remains unaffected.

Paas: This takes the advantages to a higher level and allows cloud users to forget about the OS and software components. It simplifies the process of building and running applications by providing a ready-made platform to use.

Serverless: An example is Azure SQL which allows users to control certain infrastructure-related configurations, such as database performance and network security. Serverless shifts more responsibility to the cloud provider, with users focusing mainly on writing code. Applications are broken down into smaller, standalone components that get executed in response to events.

Serverless Choices:

* Azure Functions: Allowing developers to run code in response to events without the need to manage infrastructure. Being characterized by low complexity, functions are primarily used to address specific requirements.  
* Containers Services: A container is a lightweight, standalone, and executable software package that includes everything required to run a piece of software. WIth containers, you can ignore all software prerequisites necessary to test or run applications including the operating system. An example is that a website can be divided into several containers: one for the front end, one for the back end, and Azure SQL for the database. This ensures independent maintenance, scaling and updating of different application components.  
  * Azure Container Services  
    * Azure Container Instances: Quickly run containers, test or run applications.  
    * Azure Kubernetes: A container orchestrator for deployment, management and scaling of containerized applications.

![image](https://github.com/user-attachments/assets/1f7a786e-8bc3-46ee-bbf7-a18f768971d3)

Public IP addresses are accessible from the internet while Private IP addresses/ Private endpoints can only connect devices within the same IP address space.

**Azure Networking Services** (To connect computers and devices to share data and resources, and it enables communication and collaboration)  
Azure Virtual Network (VNET): Enables communication between cloud resources. They are conceptual connections, not physical. VNETs use private IP addresses (endpoints) and resources within a VNET can communicate with each other and are not reachable from the internet. The VNET has a private IP space and can be divided into subnets if needed, if internet access is needed, resources can use a public endpoint. Network peering enables communications between VNETs which bypasses the public internet by using Microsoft’s network ensuring that the traffic is still private.

Azure VPN Gateway: Connectivity can be done between on-premises environments and the cloud using Azure VPN Gateway. It allows access to Azure networks and resources. The data is encrypted and kept secured from unauthorized access even though the communication is made over the Internet.

Azure ExpressRoute: A network connection service that has better security and privacy. It extends the on-premises network into azure cloud through a dedicated private connection that bypasses the public internet. The connection offers improved reliability, speed and security compared to the regular internet.

Azure DNS: Azure offers its own DNS service for hosting and resolving DNS domains. It uses Azure cloud infrastructure for domain name resolution. It enables great management of DNS records, offering scalability, security and integration with other Azure resources.

**Azure Virtual Machines**  
It is a computer within a computer and allows running different operating systems and applications without the need for a separate physical device. VMs can be used to host applications, conduct analytics, handle data-related tasks and to run legacy applications.

VM properties include processors, memory and OS. While VM components include disks, Network Interface card and Public IP  
![image](https://github.com/user-attachments/assets/56459144-1ad9-4531-ad97-481cde2b5b42)

Scale sets: It is a feature that enables you to deploy and manage a set of identical virtual machines. The number of virtual machines can be automatically adjusted based on a workload or a defined schedule. This flexibility guarantees top performance and efficient resource utilisation. One possible use case is scaling up to have multiple VMs to handle more users during black friday sales and decreasing it back when it is a normal period. Another example is using multiple VMs to loading the data and a single VM when viewing

Available sets: This allows virtual machines to be dispersed in data centers across various physical hardware racks, network switches and storage units. This distribution protects your VMs from possible hardware or maintenance failures. One example is that if a rack or section of the data center encounters an issue, VMs in other racks continue to run, ensuring availability.

**Migration from on-premises**  
VMs can serve as the initial phase for companies looking to migrate to Azure cloud. The eventual end goal is to use Paas as they provide a more streamlined approach to application development and deployment compared to traditional VMs. This too eliminates the need for managing underlying infrastructure and enables developers to focus on coding and application functionality accelerating development cycles and improving overall efficiency.

![image](https://github.com/user-attachments/assets/a3a345f7-b113-4bbd-8e28-021c7b5be752)

**Migrating to modern services**  
The first step to move a website and legacy applications from on-premises to cloud would be the use of virtual machines. This enables the company to have all their critical software components in a secure and highly available cloud environment. The next level would be to migrate or refactor existing applications to use native azure services. This includes container services if the application can be easily split in multiple smaller components or using app service, a highly capable and flexible Azure platform specialized in application hosting.

Azure App Service: It is a fully managed platform for building, deploying and scaling web apps. It supports multiple programming languages, provides automatic scaling and offers various services like web apps, API apps, web jobs and mobile apps.

* Web Apps: A type of service that allows you to build, host and scale web applications in the cloud. They provide a fully managed platform with features such as automatic scaling, continuous integration and deployment. It includes support for multiple programming languages, including .NET, Java, Node.js, Python and more. Azure Migrate service, provides capability to migrate traditional websites to web apps. The tool automatically accesses the existing website and presents a checklist to ensure a seamless migration process.  
* API: Also known as Application Programming Interface allows different software applications to communicate with each other with ease. It defines the rules and methods for how software components should interact, without delving into the underlying code. It’s like a menu in a restaurant where you simply choose your meal and it gets served to you, without knowing the necessary ingredients and the steps to cook it.  
* Web Jobs: These serve as background tasks or scripts running alongside a web app which can perform a variety of automated functions, including scheduled jobs, continuous process, or on-demand tasks. Offering a flexible and scalable solution, web jobs execute code in the background  
* Mobile Apps: This helps to build scalable back-end services for mobile applications. This feature provides options such as authentication, offline data sync, push notification and the ability to connect to on-premises systems.

Azure app service is a complete solution for modern applications, covering various aspects. Use web apps for both the UI and back-end functionality. Integrate API apps for seamless information exchange with other systems. Web jobs manage background processes and schedule activities and mobile apps support back-end structure for mobile apps. In complex setups, Azure services like storage and database can be used to handle data and communications with other components can be done through VNETs.

**Azure Directory Services**  
Active Directory: This is a conventional tool for managing identity and permissions in on-premises windows based environments. AD acts as an address book for an organization;s digital assets, organizing and storing information about users, computers and resources. It operates as a centralized identification service for users and computers while managing access to company resources. In AD, only authorized users and computers can access the org’s resources and files. Permissions are granted based on roles, mirroring how employees have access in specific building areas are limited to their roles. The permission structure ensures that users can only access resources they are allowed to. Users, Groups and Computers are the components of Active Directory.

Azure Directory Services: These are cloud based tools for managing user identities and access. They support secure access to applications and resources, playing a key role in authentication, authorization and identity management in both Azure and hybrid envs. Microsoft Extra ID is the main feature of Azure directory services. 

Microsoft Entra ID: This is its cloud counterpart, a more straightforward, simplified, and user-friendly online version. This serves as a master key for the Azure cloud env, simplifying online experience with a  single set of login credentials for services like email, file storage and other cloud resources. It prioritizes convenience, eliminating the need to remember multiple usernames and passwords for various Microsoft cloud platforms. Microsoft Entra ID offers key services like Authentication using multi-factor authentication, Single Sign-On (SSO), application management and device management and access policies. This helps too in efficiently revoking access and adjusting permissions to prevent unauthorized access and data breaches. Microsoft Entra ID uses **conditional access**, a tool that determines resources based on the user identity, location and decide used.

Hybrid environment: This refers to an infrastructure that combines elements of both on-premises and cloud based services. This approach provides the ability to leverage the benefits of both on-premises and cloud solutions based on specific needs and requirements, allowing business to transition gradually to the cloud while maintaining certain aspects of their infrastructure on-premises. In such a setup, Active Directory and Microsoft Entra ID can work together to share info about users, computers, groups and their properties. This sync enables access to resources in both cloud and local networks.

**Azure Authentication Methods**  
Multi-factor Authentication (MFA): Requires an additional form of identification during sign-in. This safeguards against unauthorized access, even when a password has been compromised. MFA provides additional security by requiring two or more elements to fully authenticate such as a Code sent to a user’s phone, biometric property or asking the user a challenge question.

Passwordless Authentication: This eliminates the need for passwords and makes the process more user-friendly. To enable this, devices like computers need to be registered, associating them with the user. Once registered, authentication can occur using something the user has, knows, or is, without relying on a password. Passwordless Authentication methods include Windows Hello for Business (Using biometric such as fingerprint or face recognition, or a pin code), Microsoft Authenticator app (a mobile app that offers multi-factor authentication options and works on any iOS or android phone, users can sign in by receiving a notification on their phone, confirming with a fingerprint or face or a pin code) and FIDO2 security keys (Available in different form like USB devices instead of entering a password).

Azure Permission model, this refers to the structure and system in place for managing and controlling access to Azure resources. Microsoft Entra ID offers two primary models for managing access: directory roles and Role-Based Access Control (RBAC). In Entra ID, a role is a collection of permissions that define the actions a user, group or system can perform on Azure resources. The **Reader Role** allows the ability to view any resource in the Azure portal but does not allow making changes. **Contributor Role**, the highest access level, allows for changes to the underlying resources. 

**Directory roles** are a type of role focused on identity and access management within the organization and are not directly related to managing access to Azure resources.

**Role Based Access Control (RBAC)** is a framework that enables you to manage access to Azure resources by controlling who can do what within a subscription, resource group or individual resource. RBAC inheritance refers to the way permissions are propagated through different levels of the resource hierarchy. Roles can be assigned at various scopes, such as subscription, resource group or resource level. When the rights has been adjusted out of the inheritance logic flow we can say that inheritance has been broken.

Azure Cloud Security: This refers to the protection of data, applications and infrastructure in cloud computing. It involves practices like data encryption, identity management, network security, compliance adherence and measures to detect and respond to security incidents. 

Zero trust is a security model that starts with the assumption of a potential breach and safeguards resources accordingly. This model verifies each request as if it originated from an unsecured network. Below are some key principles of it:

* Explicit verification: Always authenticate and authorize based on all available channels. Using modern features such as MFA to simplify the implementation of this process, ensuring validation of a user’s identity.  
* Least privilege access: Restricting user access by using risk-based adaptive policies and data protection measures. Users should only be granted access to the resources and permissions essential for their specific job roles, avoiding unnecessary privileges.  
* Assume breach: Acknowledges that determined attackers may find a way in, therefore security measures are designed to minimize the impact of a breach, limit access and implement additional protection within the network. Simply put, if a malicious actor gains access to specific components within an org, they should be prevented from expanding their access to other areas.

Defense-in-depth: The goal of this is to safeguard resources and prevent unauthorized access and information theft. This strategy employs multiple layers of mechanisms to block the progress of an attack attempting to gain unauthorized access to data.

* Physical Security: protects computing hardware in the data center  
* Identity and Access: manages access to infrastructure and access control  
* Perimeter: uses firewalls and other tools to protect against large-scale attacks, involving multiple attempts to gain access.  
* Network: controls resource communication through segmentation and access controls like VNETs  
* Compute: Secures VMs access and ensures they are protected by anti-virus and anti-malware software.  
* Application: Ensures applications are secure and free of vulnerabilities.  
* Data: Controls access to critical business and customer data.

Microsoft Defender for cloud is a monitoring tool for security posture management and threat protection. It provides guidance and notifications to enhance security. 

* Asses (continuous assessment): Identify and Tracking vulnerabilities  
* Secure (security hardening): helps strengthen resources and services  
* Defend (threat defense): detects and resolves threats targeting resources, workloads and services.

**Azure Service vs Azure Resources:**  
Service: It refers to a set of features of functionality and integrated components. Some examples include Azure Monitor, Azure Resource Manager and Microsoft Cost Management.  
Resource: This refers to a specific product or object of a service and is a manageable item. Some examples include databases, web apps and VM.

**Management and governance in Azure**  
Cost Management  
Resource Management  
Policy and standards implementation  
Monitoring

**Management and governance in Azure use cases:**   
Manage resources supporting business applications  
Proactively manage costs to avoid going over budget  
Ensuring data protection standards are implemented and enforced  
Monitor the performance and availability of applications and resources

**Overview**  
Costs in Azure

* Renting resources and services instead of having your own  
* Typical Azure cost structure: pay-as-you-go  
* Azure Marketplace for third-party vendors  
* Typically Cost Management tasks in Azure  
  * Follow-up of resource and application costs  
  * Setting up budgets, limits and alerts  
  * Cost analysis

Governance and Compliance

* Guiding principles for operating responsibility  
* Governance’s Principles: accountability transparency and security  
* Typical use case: compliance  
  * Adherence to applicable industry, laws and regulations  
  * Supervised internally and externally  
* Typically Governance tasks in Azure  
  * Set up specific governance policies  
  * Log user actions to provide an audit trail  
  * Document and report fulfillment of regulatory obligations with the help of Azure  
  * Azure takes into account different requirements according to region

**Resource management and monitoring:** The creation, organization and control of resources in Azure.  
Resource Management Features:

* Infrastructure as a code (IaC): Refers to how resource infrastructure is managed in Azure  
  * Managing resources using structured code and automation tools rather than manual processes.  
    * Benefits:  
      * Consistency and reproducibility  
      * Easier to document and share  
      * Less error-prone  
* Resource tags: Used as metadata to organize and control resources. Tags are used specifically to label resources and track them more efficiently.  
* Resource locks: Used to prevent modification to resources or to prevent deletion, either accidental or on purpose. The locks can be set permanently or temporarily.

Monitoring:

* It is important to maintain an overview of all process in Azure  
  * Typical monitoring tasks in Azure:  
    * Identify potential issues with resources or applications  
    * Follow-up on usage and costs  
    * Analyze log history to plan for future needs

    

**Factors that affect costs**

* Consumption: Using resource leads to costs  
* Subscription type: Depending on the type, there might be allowances or free products  
* Resource type and settings: There are higher tiers that can increase costs  
* Azure region:  Regional pricing differs, and data transfer to other regions are more expensive


**Ways to manage costs**

* Maintenance and monitoring: finding underused or over-expensive resources  
* Other pricing models: short-term flexibility vs long-term engagement  
* Geography: minimize inter-regional data transfers  
* Cost management tools: cost estimation, budgets and alerts

**Cost management tasks**

* Compare costs for running on-premises infrastructure vs Azure cloud  
* Estimate cost for provisioning resources in Azure  
* Analyze costs  
* Set up budgets and automatic alerts


  
**Cost Management Tools**

* Pricing Calculator: Estimates the cost of specific resource configuration in Azure. It is freely available and accessible without logging in to Azure. It estimates costs of individual resources or services or a specific combination. There are also templates of different scenarios such as a big data analytics set-up.  
* Total Cost of Ownership (TCO) Calculator: Compare the total cost of on-premises infrastructure with the same configuration in Azure Cloud. It is typically used to support and prepare migration to Azure, and also freely available. The TCO also includes hidden costs like operating costs.  
* Cost Management: Provide users with insights and controls to monitor, analyze, and optimize costs. Central hub in Azure for all things cost-related. This tool can help set up budgets and cost alerts, manage billing options and invoices and an API for exporting cost details to external systems.  
  * Cost Analysis Tool: A tool that can be found within the cost management platform is used primarily for ad-host cost exploration. It is able to create custom visualization and filters, create forecasts and even be able to connect to power BI for more advanced analysis.


**Governance and Compliance Implementation**

* Service Trust Portal: It is a repository where Microsoft details its security, privacy and compliance practices. The portal provides resources and documentation for us to manage compliance and data security which includes documentation on specific certifications like ISO (International Organization for Standardization) and GDPR (General Data Protection Regulation).  
* Microsoft Purview: This is a comprehend data management service for Azure and other Microsoft products. It is a combination of previous Azure Purview with Microsoft 365 Compliance. Its specific focus on managing data assets such as Data security, Data governance and Data risk and compliance.  
  * Use cases of Microsoft Purview  
    * Data Catalog: centralized overview of all data assets and their metadata  
    * Data Map: visual representation of data flows through systems and applications to track data origins and destination  
    * Data labelling: Assisting with classification, and metadata enrichment  
    * Secure data transfer and sharing  
  * Compliance Manager: A tool for assessing compliance of data assets with specific regulations and standards.  
    * It shows a dashboard to access current compliance status with a specific set of regulations  
      * Current compliance status summarized with a scoring system  
      * Recommendation to improve compliance and reduce risks

**Governance and Compliance Tool**

* Azure Policy: Enforce standards and best practices by defining and applying rules and policies to resources. Used to set rules and standards for resources.  
  * Enforces compliances to applicable standards and regulations  
  * Can be set at any level and automatically be inherited by sublevels  
  * Automatic remediation such as applying missing tags  
  * Azure Policies can be grouped into Initiatives: This refers to groups of related policies for a larger goal  
    * This can be user-defined or built-in for common scenarios or regulations  
    * Example: HIPAA/HITRUST built-in initiative  
      * MFA should be enabled  
      * There should be more than one owner assigned to a subscription  
      * Automatic check for missing members in the Administrators group   
* Azure Blueprints: Standardize deployments, replicate configurations from existing environments. It helps to standardize new cloud subscriptions or deployments.   
  * This links between blueprint (what should be deployed) and resources (what was deployed)  
  * Supports versioning: Keep track of updates or revert to a previous working version to ensure transparency and support recovery in case of problems.  
  * Azure Blueprints components also known as artifacts:  
    * Contains parameters that can be specified  
    * Configuration either in blueprint or at deployment  
    * Examples:  
      * Role assignments  
      * Policy assignments  
      * Resource group configuration  
      * Predefined resource templates

![image](https://github.com/user-attachments/assets/45e87888-1d10-4254-8b7d-133c63880f13)

**Main tools for interacting with Azure**

* Azure Portal: Graphical UI and dashboard to view and manage Azure services  
  * Can be used to build, develop and monitor cloud developments and web apps  
  * Creating custom dashboards to organize and view resources  
  * Configure accessibility options  
  * Used by everyone  
* PowerShell: Execute scripts and functions for (automatic) management of Azure resources  
  * Commands can be used one-off or in a script for automation  
  * Uses PowerShell syntax  
  * Used by IT Team  
* Azure Command Line Interface (CLI): Execute scripts and functions for (automatic) management of Azure resources  
  * Equivalent function to the powershell tool  
  * Uses bash syntax to input commands  
  * Used by IT Team  
* Azure Arc: Used to connect to external resources  
  * Examples  
    * SQL servers (relational DB)  
    * Kubernetes servers (deploy apps)  
    * VMs (run in isolation)  
    * On-premise servers (sensitive data)  
  * Azure acts as a single portal for hybrid cloud implementations  
  * Used by IT Team  
* Azure Mobile: Used to manage and monitor resources on the go  
  * App for both Android and iOS  
  * Used to manage and monitor resources on the go  
  * Used by everyone

**Azure Resource Management**

* Resource Groups  
  * Grouping of related resources  
  * Can be managed collectively  
  * Resource tags and properties like access roles can be assigned at the group level  
* Comparable with different teams at a company

**Azure Resource Manager (ARM) :** Resource management layer in Azure portal. 

* Used for resting, updating or deleting resources  
* Handle access control and resource properties  
* Important features  
  * Resource Providers: Supplies and manages specific types of resources  
    * Example: Microsoft.Computer for virtual machines  
    * ARM relies on the providers to execute resource tasks  
    * Compared with architect/ general contractor (Azure Resource Manager) overseeing specialized professionals like the electrician (resource provider)  
  * Templates:  Define and configure resource for repeated use  
    * Modular: separate templates can be combined for more complex deployments  
    * Integrate with Azure DevOps for automation with pipelines  
    * Uses Infrastructure as Code (IaC) supports versioning  
    *  Uses built-in templates or create your own using Bicep syntax (Azure specific programming language)

**Azure Monitor:** All-in platform for monitoring in Azure

* Workflow:  
  * Data collection: there are two types of data Azure Monitor can provide  
    * Metrics: Numerical data related to the performance of resources, applications and services. An example is memory usage  
    * Logs: event data related to actions by users or Azure. An example is changes made by a particular user  
  * Analysis and visualisation: Evaluate how resources and applications are performing and to identify possible issues   
    * Metrics: Calculate statistics or plot charts over time  
    * Logs: User queries to apply specific filters or create tables or lists  
    * Analysis tools  
      * Azure Monitor built-in tools  
      * External tools like PowerBI  
  * Proactive monitoring and alerts:  
    * Set up tests and alerts (testing resource’ responsiveness)  
    * Set up business rules to automatically handle specific issues (sending out an email or running a script)  
    * Automation and machine learning functionality

    

**Azure Monitoring Tools**

* Azure Monitor  
  * Application Insights: used for application performance management  
    * Detect, diagnose and address issues  
    * Provide insights into performance availability and usage  
    * Typical tasks:  
      * View and visualize performance metrics  
      * Find errors and bugs using smart detection feature  
      * Setup live and automatic monitoring  
  * Log Analytics: Used for system performance management  
    * Monitoring resource, services and infrastructure  
    * In conjunction with Application Insights for application  
    * Use cases:  
      * Tracking the performance of resources  
      * Troubleshooting and diagnostics  
      * Capacity planning  
      * Ensuring security and compliance  
  * Alerts: Used for setting up automatic alerts for specific conditions:  
    * Alerts based on specific metrics like CPU usage or a logical combination of several conditions  
    * Notification via various channels like emails and text messages  
    * Escalation of alerts if the problem persists  
    * Automatic remediation  
* Service Health: Used to check the current status of the Azure CLoud Service in general:  
  * Planned maintenance  
  * Outages and incidents  
  * Upcoming updates and changes  
* Advisor: Used for personalized recommendations to optimize Azure resources:  
  * Cost: reduce overall Azure spending  
  * Security: Identify possible security issues  
  * Performance: Improve speed and responsiveness  
  * Reliability: Ensure availability and resilience  
  * Operational Excellence: Apply best practices for efficient resource management and deployment

**Cloud Models**

* Private cloud: Provides greater control for the company and its IT department but comes with greater costs. A private cloud however may be hosted from your on site datacenter or hosted in a dedicated datacenter offsite by a third party.  
* Public cloud: A built, controlled and maintained by a third-party cloud provider. Anyone that wants to purchase cloud services can access and use resources  
* Hybrid coud: Uses both public and private cloud in an interconnected environment.
