## Learning objectives

After completing this module, you’ll be able to:

- Describe the benefits of high availability and scalability in the cloud.
- Describe the benefits of reliability and predictability in the cloud.
- Describe the benefits of security and governance in the cloud.
- Describe the benefits of manageability in the cloud.

# Benefits of High Availability and Scalability in Cloud
#cloud-benefits

For any application, two biggest considerations are: 
Uptime - Availability
Handling Demand - Scalability
## High Availability

- It is important that resources are available when needed. 
- High Availability focuses on ensuring max availability, regardless of disruptions or events that may occur
- When you’re architecting your solution, you’ll need to account for service availability guarantees. Azure is a highly available cloud environment with uptime guarantees depending on the service. These guarantees are part of the **service-level agreements (SLAs).** #SLA #service-level-agreements

### SLA
- Formal agreement between service provider and customer. that guarantees customer a stated level of services.

## Scalability

- Adjusting resources to meet demand (either by increasing or decreasing the resources previously allocated).
- No need to overpay for services, because of consumption based model of cloud.

### Vertical Scaling

With vertical scaling, if you were developing an app and you needed more processing power, you could vertically scale up to add more CPUs or RAM to the virtual machine. Conversely, if you realized you had over-specified the needs, you could vertically scale down by lowering the CPU or RAM specifications.

### Horizontal Scaling

With horizontal scaling, if you suddenly experienced a steep jump in demand, your deployed resources could be scaled out (either automatically or manually). For example, you could add additional virtual machines or containers, scaling out. In the same manner, if there was a significant drop in demand, deployed resources could be scaled in (either automatically or manually), scaling in.


# Benefits of Reliability and Predictability

## Reliability

- Ability of a system to recover from failures and continue to function.
- Cloud - Decentralized design which naturally supports reliable and resilient infra (Global regions to maintain, quick access, disaster recovery made easy).
- No action needed from user to maintain reliability.

## Predictability
- Cost predictability.
- Both performance and cost predictability highly influenced by Microsoft Azure Well-Architected Framework.
- **Performance predictability** 
	- focuses on predicting the resources needed to deliver a positive experience for your customers. Autoscaling, load balancing, and high availability are just some of the cloud concepts that support performance predictability. If you suddenly need more resources, autoscaling can deploy additional resources to meet the demand, and then scale back when the demand drops. Or if the traffic is heavily focused on one area, load balancing will help redirect some of the overload to less stressed areas
- Cost Predictability
	- focused on forecasting the cost of the cloud sepnd.
	- can track resources in real time, monitor resources to ensure the use in most efficient way.
	- Apply data analytics to find patterns and trends that help to plan future resource allocations and deployments.
	- By operating in the cloud and using cloud analytics and information, you can predict future costs and adjust your resources as needed. You can even use tools like the Total Cost of Ownership (TCO) or Pricing Calculator to get an estimate of potential cloud spend.

# Benefits of security and governance in the cloud

Be it IaaS or SaaS, cloud features support governance and compliance.

Things like set templates help ensure that all your deployed resources meet corporate standards and government regulatory requirements. Additionally, you can update all your deployed resources to new standards as standards change. 

Cloud-based auditing helps flag any resource that’s out of compliance with your corporate standards and provides mitigation strategies. Depending on your operating model, software patches and updates may also automatically be applied, which helps with both governance and security.

On the security side, you can find a cloud solution that matches your security needs. 

> [!info]
> If you want maximum control of security, infrastructure as a service provides you with physical resources but lets you manage the operating systems and installed software, including patches and maintenance. If you want patches and maintenance taken care of automatically, platform as a service or software as a service deployments may be the best cloud strategies for you.

And because the cloud is intended as an over-the-internet delivery of IT resources, cloud providers are typically well suited to handle things like distributed denial of service (DDoS) attacks, making your network more robust and secure.

By establishing a good governance footprint early, you can keep your cloud footprint updated, secure, and well managed.

# Benefits of manageability in the cloud

Two types of manageability - 
1. Management of the Cloud
2. Management in the Cloud

## Management of the Cloud
 (Sales Pitch if you're selling cloud services)
- Automatically scale resource deployment on need.
- Use preconfigured templates to deploy rather than manual configuration.
- Monitor health of the resources and automatically replace if any failures.
- Receive automatic alerts based on configured metrics to be aware of performance in real time.

## Management in the cloud
Management in the cloud speaks to how you’re able to manage your cloud environment and resources. You can manage these:

- Through a web portal.
- Using a command line interface.
- Using APIs.
- Using PowerShell.

# Summary

In this module, you learned about some of the benefits of operating in the cloud. You learned about high availability and reliability, and how those work to keep your applications running. You also learned about how the cloud can provide a more secure environment. Finally, you learned that the cloud provides a highly manageable environment for your resources.

## Additional resources

The following resources provide more information on topics in this module or related to this module.

- [Build great solutions with the Microsoft Azure Well-Architected Framework](https://learn.microsoft.com/en-us/learn/paths/azure-well-architected-framework/) is a Microsoft Learn course that introduces you to the Microsoft Azure Well-Architected Framework.