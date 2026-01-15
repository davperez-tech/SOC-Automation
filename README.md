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

