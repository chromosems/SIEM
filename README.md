# SIEM Using Elastic web Portal

## Objective
The aim of this SIEM project is to capture nmap scan log activity from the agent endpoint, followed by the creation of a tailored dashboard, and concluding with the implementation of alerting mechanisms
<img width="745" alt="image" src="https://github.com/chromosems/SIEM/assets/44053943/f9d28e47-6d69-4e07-93a9-7e7f9e73b443">

### Skills Learned
- Visualization of security Events
- Generating security events.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Querying security events.
  

### Tools Used
- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Network analysis tools (nmap) for capturing and examining network traffic.
- Elastic-agent to capture activity from Endpoint( kali machine).

## Steps
- Generating Security Events on kali. Using Nmap with command  nmap -Pn (IP address) to discover hosts and services on a network to check for open ports and in this case, open ports are visible on one machine and the other are closed. 
- <img width="679" alt="image" src="https://github.com/chromosems/SIEM/assets/44053943/548a153a-0dd3-4fb7-983f-5d671bcd0003">
-*Ref 1: The image demonstartes the captured nmap scanning*
- Generate the security events in the elastic SIEM, this is done through logs panel to evaluate if events logs were captured
-  <img width="706" alt="image" src="https://github.com/chromosems/SIEM/assets/44053943/7bd8a703-b31b-43eb-990c-c51374a78541">
-*Ref 2: Events captured after running nmap scans from endpoint device*
- Visualization is crucial in SIEM for various factors including detection of anomalies,faste incident response enhanced understanding among others simplifying complex data therefore, the visualization type of choice used here was Area(can always be changed on preference), vertical axis set count method and Horizontal axis  with date histograph and timestamp field
- <img width="856" alt="image" src="https://github.com/chromosems/SIEM/assets/44053943/de43cf1f-eced-4df9-bbdb-a941a0f3ffba">
- <img width="793" alt="image" src="https://github.com/chromosems/SIEM/assets/44053943/bbf7cd39-8f9f-4a01-97a5-5a91e18cb1ae">
- Alerts are crucial features in detecting security incidents and response therefore created an alert rule hence the alert is triggered when defined conditions are met ,creating an alert to detect Nmap scans
- <img width="848" alt="image" src="https://github.com/chromosems/SIEM/assets/44053943/5729a2fd-9d10-4edb-a808-a936e328bf09">
-*Ref 3: The alert will perform test every after 5 mins*
- <img width="841" alt="image" src="https://github.com/chromosems/SIEM/assets/44053943/89b4ae3f-5bfd-47c5-a6e3-eafceb02064f">
- In conclusion, I was able to forward the nmap scan data from agent / kali vm  using Elastic agent, queried the logs, created a dashboard and lastly created alerts to detect security events




