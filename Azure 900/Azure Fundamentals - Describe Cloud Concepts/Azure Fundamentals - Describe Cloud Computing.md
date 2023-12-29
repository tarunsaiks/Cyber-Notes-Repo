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
### Multi-Cloud 
#multi-cloud
A fourth, and increasingly likely scenario is a multi-cloud scenario. In a multi-cloud scenario, you use multiple public cloud providers. Maybe you use different features from different cloud providers. Or maybe you started your cloud journey with one provider and are in the process of migrating to a different provider. Regardless, in a multi-cloud environment you deal with two (or more) public cloud providers and manage resources and security in both environments.

### Azure Arc
#AzureArc #Azure
Azure Arc is a set of technologies that helps manage your cloud environment. Azure Arc can help manage your cloud environment, whether it's a public cloud solely on Azure, a private cloud in your datacenter, a hybrid configuration, or even a multi-cloud environment running on multiple cloud providers at once.

### Azure VMware Solution
#Azure #AzureVMWare
What if you’re already established with VMware in a private cloud environment but want to migrate to a public or hybrid cloud? Azure VMware Solution lets you run your VMware workloads in Azure with seamless integration and scalability.


## Consumption Based Model

IT Infra models has generally two types of expenses - CapEx and OpEx

#capex
**CapEx** -  a one-time, up-front expenditure to purchase or secure tangible resources. A new building, repaving the parking lot, building a datacenter, or buying a company vehicle are examples of CapEx.

#opex
**OpEx** - spending money on services or products over time. Renting a convention center, leasing a company vehicle, or signing up for cloud services are all examples of OpEx.

Cloud computing falls under OpEx because cloud computing operates on a consumption-based model. With cloud computing, you don’t pay for the physical infrastructure, the electricity, the security, or anything else associated with maintaining a datacenter. Instead, you pay for the IT resources you use. If you don’t use any IT resources this month, you don’t pay for any IT resources.

This consumption-based model has many benefits, including:

- No upfront costs.
- No need to purchase and manage costly infrastructure that users might not use to its fullest potential.
- The ability to pay for more resources when they're needed.
- The ability to stop paying for resources that are no longer needed.

## Compare cloud pricing models

Cloud computing is the delivery of computing services over the internet by using a pay-as-you-go pricing model. You typically pay only for the cloud services you use, which helps you:

- Plan and manage your operating costs.
- Run your infrastructure more efficiently.
- Scale as your business needs change.

To put it another way, cloud computing is **a way to rent compute power and storage from someone else’s datacenter.** You can treat cloud resources like you would resources in your own datacenter. However, ==unlike in your own datacenter, when you're done using cloud resources, you give them back. You’re billed only for what you use==.

Instead of maintaining CPUs and storage in your datacenter, you rent them for the time that you need them. The cloud provider takes care of maintaining the underlying infrastructure for you. The cloud enables you to quickly solve your toughest business challenges and bring cutting-edge solutions to your users.

# Summary

Completed100 XP

- 2 minutes

In this module, you learned about general cloud concepts. You started with things like just understanding what cloud computing is. You also learned about the shared responsibility model and how you and your cloud provider share the responsibility of keeping your information in the cloud secure. You briefly covered the differences between the cloud models (public, private, hybrid, and multi-cloud). Then, you wrapped up with a unit on how the cloud shifts IT spend from a capital expense to an operational expense.

## Learning objectives

You should now be able to:

- Define cloud computing.
- Describe the shared responsibility model.
- Define cloud models, including public, private, and hybrid.
- Identify appropriate use cases for each cloud model.
- Describe the consumption-based model.
- Compare cloud pricing models.

## Additional resources

The following resources provide more information on topics in this module or related to this module.

- [Shared responsibility model](https://learn.microsoft.com/en-us/azure/security/fundamentals/shared-responsibility) - The shared responsibility model is the sharing of responsibilities for the cloud between you and your cloud provider.
- [Introduction to Azure VMware Solution](https://learn.microsoft.com/en-us/learn/modules/intro-azure-vmware-solution/) is a Microsoft Learn course that dives deeper into Azure VMware Solution.
- [Introduction to Azure hybrid cloud services](https://learn.microsoft.com/en-us/learn/modules/intro-to-azure-hybrid-services/) is a Microsoft Learn course that explains hybrid cloud in greater detail.