# SOC Automation: AI-Driven SOC Workflow
## Introduction
This project demonstrates how to integrate AI into a Security Operations Center (SOC) workflow for automated alert handling and incident response. The lab showcases an end-to-end SOC setup using Splunk as the SIEM, N8N for workflow automation, and OpenAI’s ChatGPT to process alerts and provide actionable insights. It is designed for learning purposes and portfolio enhancement.

## Objective
The main goal of this project is to create a modern, automated SOC workflow that:
1. Collects telemetry from endpoint (Windows 10).
2. Ingests logs into a SIEM (Splunk).
3. Triggers alerts based on security events.
4. Sends alerts to N8N for processing.
5. Leverage ChatGPT to summarize, enrich, assess severity, and recommend next steps for each alert.
6. Outputs actionable results into Slack for analyst review.

## Technologies and Tools Used
1. Hypervisors: VMware Workstation
2. Operating Systems: Windows 10, Ubuntu Server 24.04
3. SIEM: Splunk Enterprise + Splunk Universal Forwarder + Microsoft Windows Add-on
4. Automation & Orchestration: N8N, Docker, Docker Compose
5. AI Integration: OpenAI GPT-4.1 Mini
6. Communication: Slack
7. Additional Tools: Remote Desktop Protocol (RDP)

## Methodology
- Environment setup and VM deployment: I began by deploying multiple virtual machines using VMware Workstation, including Ubuntu Server for Splunk and N8N, Windows 10 for endpoint telemetry, and Kali Linux for optional testing. This created a realistic SOC lab environment to simulate real-world monitoring scenarios.

- Log collection and monitoring: Windows 10 telemetry was collected using the Splunk Universal Forwarder, forwarding Security, System, and Application logs to Splunk Enterprise. Splunk was configured to parse incoming data and generate alerts for events like failed logins or suspicious activity.

- Automation workflow creation: N8N was deployed using Docker Compose on the Ubuntu server. I built workflows to process incoming alerts from Splunk, parse event data, and integrate AI using OpenAI GPT-4.1 Mini. The AI enriched alerts with context, assessed severity, and recommended actionable steps for analysts.

- Alert handling and AI processing: Simulated alerts were generated on the Windows 10 VM, including failed logins and event triggers. These alerts were sent to N8N, processed by ChatGPT, and structured output was sent to Slack for review. This demonstrated automated triage and intelligence enrichment in the SOC workflow.

- Incident response simulation: Recommendations from the AI were used to simulate SOC actions, such as isolating hosts, reviewing event logs, or resetting credentials. This step validated the end-to-end effectiveness of the workflow in improving response efficiency.

- Post-automation analysis: I observed the lab for repeated alert scenarios, monitoring how the AI-assisted workflow handled incidents over time. Metrics included alert processing speed, accuracy of severity assessments, and the usefulness of recommended next steps, providing insight into the practical value of AI integration in SOC operations.

## Conclusion
The SOC Automation Project showcases the practical application of AI and automation in a modern Security Operations Center workflow, bridging the gap between traditional SOC processes and emerging technologies. Through the integration of Splunk for centralized log collection, N8N for orchestrating automated workflows, and GPT-4.1 Mini for intelligent alert analysis, this project demonstrates how alerts from endpoints can be automatically ingested, enriched, and triaged with minimal human intervention. Analysts are empowered with actionable insights delivered in real-time through Slack, improving situational awareness and reducing response times.
