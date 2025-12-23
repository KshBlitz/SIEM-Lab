# Mini Project 1 – SIEM Setup & Log Ingestion

## Objective
Establish a functional SOC SIEM foundation with verified log ingestion
and endpoint visibility.

## Scope
- SIEM installation and configuration
- Agent deployment
- Sysmon telemetry ingestion
- Communication and data flow verification

No attack simulation or custom detections are included in this phase.


## Why This Phase Exists

In an enterprise SOC, detection and response capabilities are only as
reliable as the underlying telemetry pipeline.

Before building detections or simulating attacks, the following must be true:
- Endpoints reliably generate logs
- Logs are forwarded without loss
- The SIEM can index, query, and visualize events
- Analysts can confirm visibility and agent health

This phase validates those prerequisites.


## Environment Alignment

This mini project uses a small enterprise-style environment:

- Ubuntu Server 22 acts as the centralized SIEM platform
- Windows Server 2022 represents a monitored enterprise asset
- Windows 11 is used as the SOC analyst workstation
- Kali Linux is reserved for future attacker simulation phases

Each system has a defined role and is intentionally scoped.


## SIEM Architecture Alignment

The architecture follows a standard agent-based SIEM model:

1. Endpoint activity is generated on Windows Server 2022
2. Sysmon enhances native Windows telemetry
3. Wazuh Agent collects and forwards logs securely
4. Wazuh Manager processes events using decoders and rules
5. Events are indexed in OpenSearch
6. The Wazuh Dashboard provides analyst visibility

This separation mirrors common enterprise SOC deployments.


## What Is Verified in This Phase

- Wazuh agent is connected and reporting
- Sysmon events are ingested and searchable
- Endpoint telemetry is visible in dashboards
- SIEM components are communicating as expected


## Scope Control

This mini project intentionally does NOT include:
- Attack simulation
- Custom detection rules
- Alert tuning
- Incident investigation workflows

Those capabilities depend on a stable telemetry foundation
and are addressed in later mini projects.


## What This Enables

With the SIEM foundation in place, subsequent mini projects can focus on:
- Baseline behavior analysis
- Detection rule development
- Attack simulation and validation
- Alert triage and investigation workflows
