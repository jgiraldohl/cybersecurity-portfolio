# Splunk Log Ingestion and Search Lab

## Project Overview

This hands-on lab focused on deploying a distributed Splunk environment in AWS, configuring log forwarding from a Linux host, troubleshooting data ingestion, and exploring log analysis using Splunk Search Processing Language (SPL).

The lab was part of a cybersecurity workshop and provided practical experience with log collection, centralized monitoring, and data analysis.

## Environment and Architecture

The lab consisted of two AWS EC2 instances:

- **splunk-server:** Splunk Enterprise instance responsible for receiving, indexing, and searching log data.
- **linux-os:** Linux instance running Splunk Universal Forwarder to collect and forward system logs.

The Universal Forwarder monitored Linux system logs, including `/var/log/syslog`, and transmitted events to the Splunk Enterprise server over TCP port 9997.

## Technical Implementation

### 1. Splunk Universal Forwarder Configuration

Configured Splunk Universal Forwarder on the Linux host to collect system logs and forward them to the Splunk Enterprise instance.

Configured the forwarding destination through `outputs.conf` and verified the forwarding connection.

### 2. Troubleshooting Log Forwarding

Initially, the forwarder was configured to send data to the Splunk server's public IP address. Although the receiving port was listening, the forwarder showed the connection as configured but inactive.

**Root cause:** The forwarding destination was incorrectly configured for communication between instances within the same AWS VPC.

**Resolution:**
- Reconfigured the forwarding destination to use the Splunk server's private IP address.
- Verified that TCP port 9997 was listening on the receiving instance.
- Confirmed that the forwarder connection became active.
- Verified successful log ingestion into Splunk.

### 3. Log Ingestion and Validation

Validated incoming events in Splunk using the "os-log" index.

Explored event metadata, including:

- Host
- Source
- Sourcetype
- Event count
- Time range

Confirmed that Linux system logs were successfully indexed and searchable.



### 4. Splunk Search and Data Analysis

Practiced Splunk Search Processing Language (SPL) to retrieve, aggregate, and visualize log data.

Examples included:

- Retrieving events from a specific index.
- Counting events by host and source.
- Identifying distinct log sources.
- Analyzing event distribution over time.
- Exploring internal Splunk indexes and audit-related data.

## Skills Demonstrated

- Splunk Enterprise fundamentals
- Splunk Universal Forwarder configuration
- Linux system log collection
- AWS EC2 networking fundamentals
- Log ingestion troubleshooting
- TCP-based log forwarding
- SPL search and data aggregation
- Centralized log monitoring
- Technical troubleshooting and root cause analysis

## Project Outcome

Successfully established log forwarding between two AWS EC2 instances, resolved a connectivity issue, and validated the ingestion of Linux system logs into Splunk.

The lab provided foundational experience in centralized logging and SIEM-related workflows, supporting further development in cybersecurity operations and security monitoring.

## Environment Disclaimer

This project was conducted in a controlled educational lab environment using AWS EC2 and Linux system logs.

