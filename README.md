# SOC / SIEM Lab – SOC Level 1 Workflow Environment

This repository documents a modular SOC Level 1 lab environment built using
Wazuh SIEM and free, open-source tools.

The objective is to simulate realistic enterprise SOC workflows —
from log ingestion to alert triage and escalation —
without focusing on tool installation tutorials or beginner walkthroughs.

This is a growing SOC system, not a single lab exercise.


## Overview

The lab is designed to mirror how a real SOC operates:

- Centralized log ingestion
- Endpoint visibility
- Alert generation and triage
- Investigation-driven analysis
- Escalation-ready documentation

Each mini project in this repository represents a distinct SOC capability.
Together, they form a complete SOC Level 1 practice environment suitable for
portfolio review and interview discussion.


## High-Level Architecture

The lab simulates a small enterprise environment consisting of:

- Centralized SIEM platform (Wazuh)
- Windows Server endpoint as a monitored enterprise asset
- Attacker simulation system (Kali Linux)
- SOC analyst workstation for monitoring and investigation

All security telemetry flows into the SIEM, where alerts are generated
and investigated using standard SOC workflows.


## Environment & Systems

| System              | Role                          | Purpose |
|---------------------|-------------------------------|---------|
| Ubuntu Server 22    | SIEM Platform                 | Log ingestion, correlation, alerting |
| Windows Server 2022 | Monitored Endpoint            | Primary log source |
| Windows 11          | SOC Analyst Workstation       | Alert triage & investigation |
| Kali Linux          | Attacker Simulation           | Malicious activity generation |


## Tools Used & Rationale

### Wazuh SIEM
- Centralized log collection and alerting
- Rule-based detections and decoders
- SOC-style dashboards and investigations

### Sysmon
- Enhanced endpoint telemetry
- Process, network, and persistence visibility
- Commonly used in SOC investigations

### OpenSearch (Wazuh Indexer)
- Log indexing and historical search
- Enables query-based investigations

The tooling is open-source, but the workflows intentionally reflect
enterprise SOC logic.

## Scope & Limitations

### Included
- SIEM deployment and configuration
- Agent-based log ingestion
- Endpoint visibility validation
- Alert generation from baseline telemetry

### Not Included (Yet)
- Custom detection engineering
- Advanced correlation rules
- Full-scale incident response automation

Each limitation is addressed in later mini projects.


## Skills Demonstrated

- SIEM architecture understanding
- Endpoint telemetry collection
- Alert interpretation and triage
- SOC investigation mindset
- Documentation and reporting discipline
- Detection-focused thinking (not dashboard-driven)


## Repository Structure

Each mini project contains:
- Clearly defined scope
- Focused documentation
- Supporting screenshots or diagrams
- Outputs aligned with SOC workflows

Refer to individual mini project READMEs for detailed context.


## Roadmap

- Mini Project 1: SIEM Setup & Log Ingestion (Completed)
- Mini Project 2: Log Visibility Baseline
- Mini Project 3: Detection Rules & Decoders
- Mini Project 4: Attack Simulation & Detection
- Mini Project 5: Alert Triage & Incident Response


## Project Philosophy

- Tools are secondary to workflow
- Alerts without investigation are noise
- Documentation is part of security work
- SOC maturity comes from decision-making, not dashboards
