# Introduction

Defender XDR is integrated threat protection suite with solutions that detect malicious activity across email, endpoints, applications and identity. 

This makes one of the crucial job responsibilities of a SOC Analyst.

![](../../Pasted%20image%2020240729223221.png)

## Detection of Threat

The victim receives a malicious email on a personal email account not protected by Microsoft Defender for Office 365 (MDO) or a USB drive and opens the attachment. Once the attachment opens, the malware infects the computer. The user is unaware that an attack occurred. But Microsoft Defender for Endpoints (MDE) detects this attack, raises an alert to security operations, and provides details about the threat to the Security team. Disable user access from device while infected - MDE communicates to Intune that the risk level on this endpoint has changed. An Intune Compliance Policy configured with an MDE risk level severity is triggered and marks the account as noncompliant with organizations policy. The Conditional Access created in Microsoft Entra ID blocks user access to apps.

![](../../Pasted%20image%2020240729223826.png)
