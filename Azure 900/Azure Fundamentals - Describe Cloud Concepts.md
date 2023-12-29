# Azure??

Cloud Computing platform - provides a lot of services, making it easier to build solutions, deploy applications, manage infra, platform and software services.

Azure has simple web services for hosting your business presence in the cloud. Azure also supports running fully virtualized computers managing your custom software solutions. Azure provides a wealth of cloud-based services like remote storage, database hosting, and centralized account management. Azure also offers new capabilities like artificial intelligence (AI) and Internet of Things (IoT) focused services.

| **AZ-900 Domain Area** | **Weight** |
| ---- | ---- |
| Describe cloud concepts | 25-30% |
| Describe Azure architecture and services | 35-40% |
| Describe Azure management and governance | 30-35% |
# Introduction to Cloud Computing
#CloudComputing
### Learning Objectives

- Define cloud computing.
- Describe the shared responsibility model.
- Define cloud models, including public, private, and hybrid.
- Identify appropriate use cases for each cloud model.
- Describe the consumption-based model.
- Compare cloud pricing models.

## What is Cloud Computing
#CloudComputing 
- Delivery of computing services (vm's, storage, databases, network, services) over internet.
- Scalable with Pay as you use model
- Can be managed either by end user or cloud service provider.

## Shared Responsibility Model

Traditional data center - Single organization - Owner - Totally responsible for physical space, security, managing servers.

**Shared responsibility Model** - responsibility shared between cloud provider and the consumer. Physical security, power, cooling and network connectivity taken care by provider, applications, data and other things can be either managed by consumer or provider based on model (IaaS, PaaS, SaaS).

> [!info]
> Then, for some things, the responsibility depends on the situation. If you’re using a cloud SQL database, the cloud provider would be responsible for maintaining the actual database. However, you’re still responsible for the data that gets ingested into the database. If you deployed a virtual machine and installed an SQL database on it, you’d be responsible for database patches and updates, as well as maintaining the data and information stored in the database.

#IaaS #PaaS #SaaS #On-Premise
![Responsibility Comparison Char](https://learn.microsoft.com/en-us/training/wwl-azure/describe-cloud-compute/media/shared-responsibility-b3829bfe.svg)


You’ll (consumer) always be responsible for:

- The information and data stored in the cloud
- Devices that are allowed to connect to your cloud (cell phones, computers, and so on)
- The accounts and identities of the people, services, and devices within your organization

The cloud provider is always responsible for:

- The **physical datacenter**
- The **physical network**
- The **physical hosts**

Your service model will determine responsibility for things like:

- Operating systems
- Network controls
- Applications
- Identity and infrastructure
## Cloud Models - Private, Public and Hybrid

### Private cloud
#private-cloud
- almost similar to normal datacenter
- delivers IT Solutions over internet - used only by single entity or organization
- costly and offers less benefits than a public cloud

### Public Cloud
#public-cloud
- Built, controlled and maintained by a third party cloud provider
- Anyone that wants to purchase cloud services can use and access resources
- The general public availability is a key difference between public and private clouds.

### Hybrid cloud
#hybrid-cloud
- Uses both Private and Public features
- A hybrid cloud environment can be used to allow a private cloud to surge for increased, temporary demand by deploying public cloud resources. 
- Hybrid cloud can be used to provide an extra layer of security. 
- For example, users can flexibly choose which services to keep in public cloud and which to deploy to their private cloud infrastructure.

### Comparison between Cloud Models
|**Public cloud**|**Private cloud**|**Hybrid cloud**|
|---|---|---|
|No capital expenditures to scale up|Organizations have complete control over resources and security|Provides the most flexibility|
|Applications can be quickly provisioned and deprovisioned|Data is not collocated with other organizations’ data|Organizations determine where to run their applications|
|Organizations pay only for what they use|Hardware must be purchased for startup and maintenance|Organizations control security, compliance, or legal requirements|
|Organizations don’t have complete control over resources and security|Organizations are responsible for hardware maintenance and updates||
## Multi-Cloud 
#multi-cloud
A fourth, and increasingly likely scenario is a multi-cloud scenario. In a multi-cloud scenario, you use multiple public cloud providers. Maybe you use different features from different cloud providers. Or maybe you started your cloud journey with one provider and are in the process of migrating to a different provider. Regardless, in a multi-cloud environment you deal with two (or more) public cloud providers and manage resources and security in both environments.

## Azure Arc
#AzureArc #Azure
Azure Arc is a set of technologies that helps manage your cloud environment. Azure Arc can help manage your cloud environment, whether it's a public cloud solely on Azure, a private cloud in your datacenter, a hybrid configuration, or even a multi-cloud environment running on multiple cloud providers at once.

## Azure VMware Solution
#Azure #AzureVMWare
What if you’re already established with VMware in a private cloud environment but want to migrate to a public or hybrid cloud? Azure VMware Solution lets you run your VMware workloads in Azure with seamless integration and scalability.


## Consumption Based Model

IT Infra models has generally two types of expenses - CapEx and OpEx

**CapEx** -  a one-time, up-front expenditure to purchase or secure tangible resources. A new building, repaving the parking lot, building a datacenter, or buying a company vehicle are examples of CapEx.

**OpEx** - spending money on services or products over time. Renting a convention center, leasing a company vehicle, or signing up for cloud services are all examples of OpEx.