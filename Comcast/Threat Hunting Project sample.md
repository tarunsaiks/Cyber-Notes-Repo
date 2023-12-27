1. Create a Home Lab Environment either in localhost or cloud provider - Azure - AD, Sentinel SIEM (AWS - CloudTrail and )
2. Install Intrusion Detection System (IDS) like Snort to work with basic detection system.
3. Learn and Install Splunk (Enterprise version, Widely used and huge marketplace supports add-ons) or Wazuh (Free, open-source, supports AtomicRedTeam (built-in)) any SIEM based tool to monitor and search within logs to gain insights.
4. Using either PowerAutomate or custom python script deployed in a server to create IoC's from twitter (looking for other options to gain IoC's)
5. Using these IoC's build a 


1. Classify and Arrange data into normal and malicious data and build a naive bayes classifier like spam filter to predict and give accuracy.

2. Integrate OpenCTI or MISP with SIEM tool, (Generate feeds from open-source tools or sites like twitter using python or PowerAutomate, get data dumps in excel CSV) perform adversarial testing using scripts hosted in a server to manage and 