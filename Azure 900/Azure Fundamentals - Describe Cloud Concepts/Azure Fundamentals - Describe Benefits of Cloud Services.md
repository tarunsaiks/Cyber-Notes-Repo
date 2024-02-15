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
- 