# Introduction

Defender XDR is integrated threat protection suite with solutions that detect malicious activity across email, endpoints, applications and identity. 

This makes one of the crucial job responsibilities of a SOC Analyst.

![](../../../Pasted%20image%2020240729223221.png)

---
# Explore XDR use cases

## Detection of Threat

The victim receives a malicious email on a personal email account not protected by Microsoft Defender for Office 365 (MDO) or a USB drive and opens the attachment. Once the attachment opens, the malware infects the computer. The user is unaware that an attack occurred. But Microsoft Defender for Endpoints (MDE) detects this attack, raises an alert to security operations, and provides details about the threat to the Security team. Disable user access from device while infected - MDE communicates to Intune that the risk level on this endpoint has changed. An Intune Compliance Policy configured with an MDE risk level severity is triggered and marks the account as noncompliant with organizations policy. The Conditional Access created in Microsoft Entra ID blocks user access to apps.

![](../../../Pasted%20image%2020240729223826.png)

## Remediation

MDE (Microsoft Defender for Endpoints) remediates either automatically or via approval from security analyst or manual investigation of threat.

It also remediated threat across enterprise by adding info on this attack to Microsoft Threat Intelligence system.

Restore Access - Once the infected devices are remediated,  MDE signals Intune to change the risk status and Entra ID Conditional Access to allow access to enterprise resources. Threat intelligence feeds are used by Microsoft tools, securing other assets in attack surface.

MDO and Microsoft Defender for Cloud use the signals to detect and remediate threats in email, office collaboration, Azure, and more.

![](../../../Pasted%20image%2020240729224713.png)

#### Access Restricted
Restricts access based on Conditional Access knowing about device risk using MDE notified Intune, which then updated the compliance status of the device in Entra ID.

During this time, the user is restricted from accessing corporate resources. This applies to all new resource requests and blocks any current access to resources that support continuous access evaluation (CAE). 

People are able to do general internet productivity tasks, like research YouTube, Wikipedia, and anything else that doesn’t require corporate authentication, but won’t have access to corporate resources.

#### Access Restored
Once the threat has been remediated and cleaned up, MDE triggers Intune to update Microsoft Entra ID, and Conditional Access restores the user’s access to corporate resources.

This mitigates risk to the organization by ensuring attackers who might be in control of these devices can't access corporate resources, while minimizing the impact on user productivity to minimize disruption of business processes.

---
# Understand XDR in SOC

![](../../../Pasted%20image%2020240729225306.png)