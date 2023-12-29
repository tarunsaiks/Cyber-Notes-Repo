# Azure??

Cloud Computing platform - provides a lot of services, making it easier to build solutions, deploy applications, manage infra, platform and software services.

Azure has simple web services for hosting your business presence in the cloud. Azure also supports running fully virtualized computers managing your custom software solutions. Azure provides a wealth of cloud-based services like remote storage, database hosting, and centralized account management. Azure also offers new capabilities like artificial intelligence (AI) and Internet of Things (IoT) focused services.

| **AZ-900 Domain Area** | **Weight** |
| ---- | ---- |
| Describe cloud concepts | 25-30% |
| Describe Azure architecture and services | 35-40% |
| Describe Azure management and governance | 30-35% |
# Introduction to Cloud Computing

### Learning Objectives

- Define cloud computing.
- Describe the shared responsibility model.
- Define cloud models, including public, private, and hybrid.
- Identify appropriate use cases for each cloud model.
- Describe the consumption-based model.
- Compare cloud pricing models.

## What is Cloud Computing

- Delivery of computing services (vm's, storage, databases, network, services) over internet.
- Scalable with Pay as you use model
- Can be managed either by end user or cloud service provider.

## Shared Responsibility Model

Traditional data center - Single organization - Owner - Totally responsible for physical space, security, managing servers.

Shared responsibility Model - responsibility shared between cloud provider and the consumer. Physical security, power, cooling and network connectivity taken care by provider, applications, data and other things can be either managed by consumer or provider based on model (IaaS, PaaS, SaaS).

> [!info]
> Then, for some things, the responsibility depends on the situation. If you’re using a cloud SQL database, the cloud provider would be responsible for maintaining the actual database. However, you’re still responsible for the data that gets ingested into the database. If you deployed a virtual machine and installed an SQL database on it, you’d be responsible for database patches and updates, as well as maintaining the data and information stored in the database.

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
## Cloud Models








