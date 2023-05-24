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

# Incident Response Team

Along with the organizational need to establish a [Security Operations Center (SOC)](https://learn.isc2.org/content/enforced/9541-CC-SPT-GLOBAL-1ED-1M/build/chapter_02/module_01/ch02-m01-Incident_Response_Team.html?d2lSessionVal=1onfrdPnsJRYGRQpO8FNezDy1&ou=9541&d2l_body_type=3#) is the need to create a suitable incident response team. A properly staffed and trained incident response team can be leveraged, dedicated or a combination of the two, depending on the requirements of the organization. 

Many IT professionals are classified as first responders for incidents. They are the first ones on the scene and know how to differentiate typical IT problems from security incidents. They are similar to medical first responders who have the skills and knowledge to provide medical assistance at accident scenes and help get the patients to medical facilities when necessary. The medical first responders have specific training to help them determine the difference between minor and major injuries. Further, they know what to do when they come across a major injury. 

Similarly, IT professionals need specific training so they can determine the difference between a typical problem that needs troubleshooting and a security incident that they need to report and address at a higher level. 

A typical incident response team is a cross-functional group of individuals who represent the management, technical and functional areas of responsibility most directly impacted by a security incident. Potential team members include the following:

-   Representative(s) of senior management
-   Information security professionals
-   Legal representatives
-   Public affairs/communications representatives
-   Engineering representatives (system and network)


Team members should have training on incident response and the organization’s incident response plan. Typically, team members assist with investigating the incident, assessing the damage, collecting evidence, reporting the incident and initiating recovery procedures. They would also participate in the remediation and lessons learned stages and help with root cause analysis.

Many organizations now have a dedicated team responsible for investigating any computer security incidents that take place. These teams are commonly known as computer incident response teams (CIRTs) or computer security incident response teams (CSIRTs). When an incident occurs, the response team has four primary responsibilities:

-   Determine the amount and scope of damage caused by the incident.
-   Determine whether any confidential information was compromised during the incident.
-   Implement any necessary recovery procedures to restore security and recover from incident-related damage.
-   Supervise the implementation of any additional security measures necessary to improve security and prevent recurrence of the incident.