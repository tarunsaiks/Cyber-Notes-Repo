This chapter focuses on the availability part of the CIA triad and the importance of maintaining availability of both human and system resources. These are usually accomplished through the implementation of Incident Response, Business Continuity (BC) and Disaster Recovery (DR) plans. While these three plans may seem to overlap in scope, they are three distinct plans that are vital to the survival of any organization.

Here are the primary things to remember in this chapter: first, the Incident Response plan responds to unexpected changes in operating conditions to keep the business operating; second, the Business Continuity plan enables the business to continue operating throughout the crisis; and finally, if both the Incident Response and Business Continuity plans fail, the Disaster Recovery plan is activated to help the business to return to normal operations as quickly as possible.

#### Health and Human Safety

When it comes to a career in cybersecurity, the day-to-day focus is monitoring information systems and looking out for abnormal network activity, malicious software and threat actors. Security professionals spend their days ensuring the confidentiality, integrity and availability of systems and data, but in addition to safeguarding networks and securing the exchange of data and shared resources, it’s important to realize that cybersecurity goes beyond the technical aspects. Its scope encompasses the protection of people and their personal information. There is nothing more important than the health and safety of our users, coworkers and customers.

# Incident Terminology

#breach #event #exploit #incident #intrusion #threat #vulnerability #zero_day

<dl>
  <dt>Breach</dt>
  <dd>The loss of control, compromise, unauthorized disclosure, unauthorized acquisition, or any similar occurrence where: a person other than an authorized user accesses or potentially accesses personally identifiable information; or an authorized user accesses personally identifiable information for other than an authorized purpose. NIST SP 800-53 Rev. 5</dd>
  <dt>Event</dt>
  <dd>Any observable occurrence in a network or system. NIST SP 800-61 Rev 2</dd>
  <dt>Exploit</dt>
  <dd>A particular attack. It is named this way because these attacks exploit system vulnerabilities.</dd>
  <dt>Incident</dt>
  <dd>An event that actually or potentially jeopardizes the confidentiality, integrity or availability of an information system or the information the system processes, stores or transmits.</dd>
  <dt>Intrusion</dt>
  <dd>A security event, or combination of events, that constitutes a deliberate security incident in which an intruder gains, or attempts to gain, access to a system or system resource without authorization. IETF RFC 4949 Ver 2.</dd>
  <dt>Threat</dt>
  <dd>Any circumstance or event with the potential to adversely impact organizational operations (including mission, functions, image or reputation), organizational assets, individuals, other organizations or the nation through an information system via unauthorized access, destruction, disclosure, modification of information and/or denial of service. NIST SP 800-30 Rev 1</dd>
  <dt>Vulnerability</dt>
  <dd>Weakness in an information system, system security procedures, internal controls or implementation that could be exploited by a threat source. NIST SP 800-30 Rev 1</dd>
  <dt>Zero Day</dt>
  <dd>A previously unknown system vulnerability with the potential of exploitation without risk of detection or prevention because it does not, in general, fit recognized patterns, signatures or methods.</dd> 
</dl>

# The Goal Of Incident Response

Every organization must be prepared for incidents. Despite the best efforts of an organization’s management and security teams to avoid or prevent problems, it is inevitable that  [adverse events](https://learn.isc2.org/content/enforced/9541-CC-SPT-GLOBAL-1ED-1M/build/chapter_02/module_01/ch02-m01-The_Goal_of_Incident_Response.html?d2lSessionVal=30YR1ZhetBhe0BJEGCiGLX1Sq&ou=9541&d2l_body_type=3#) will happen that have the potential to affect the business mission or objectives.

The priority of any incident response is to protect life, health and safety. When any decision related to priorities is to be made, always choose safety first.

The primary goal of incident management is to be prepared. Preparation requires having a policy and a response plan that will lead the organization through the crisis. Some organizations use the term “crisis management” to describe this process, so you might hear this term as well.

An event is any measurable occurrence, and most events are harmless. However, if the event has the potential to disrupt the business’s mission, then it is called an incident. Every organization must have an  [incident response plan](https://learn.isc2.org/content/enforced/9541-CC-SPT-GLOBAL-1ED-1M/build/chapter_02/module_01/ch02-m01-The_Goal_of_Incident_Response.html?d2lSessionVal=30YR1ZhetBhe0BJEGCiGLX1Sq&ou=9541&d2l_body_type=3#) that will help preserve business viability and survival.

The incident response process is aimed at reducing the impact of an incident so the organization can resume the interrupted operations as soon as possible. Note that incident response planning is a subset of the greater discipline of business continuity management (BCM), which we will cover shortly.

# Components of Incident Response Plan

The incident response policy should reference an incident response plan that all employees will follow, depending on their role in the process. The plan may contain several procedures and standards related to incident response. It is a living representation of an organization’s incident response policy.

The organization’s vision, strategy and mission should shape the incident response process. Procedures to implement the plan should define the technical processes, techniques, checklists and other tools that teams will use when responding to an incident.

To prepare for incidents, here are the components commonly found in an incident response plan:

## Preparation

-   Develop a policy approved by management.
-   Identify critical data and systems, single points of failure.
-   Train staff on incident response.
-   Implement an incident response team. (covered in subsequent topic)
-   Practice Incident Identification. (First Response)
-   Identify Roles and Responsibilities.
-   Plan the coordination of communication between stakeholders.
    -   Consider the possibility that a primary method of communication may not be available.

## Detection and Analysis

-   Monitor all possible attack vectors.
-   Analyze incident using known data and threat intelligence.
-   Prioritize incident response.
-   Standardize incident documentation.

## Containment

-   Gather evidence.
-   Choose an appropriate containment strategy.
-   Identify the attacker.
-   Isolate the attack.

## Post-Incident Activity

-   Identify evidence that may need to be retained.
-   Document lessons learned.
Retrospective
-   Preparation
-   Detection and Analysis
-   Containment, Eradication and Recovery
-   Post-incident Activity