![License: CISCO](https://img.shields.io/badge/License-CISCO-blue.svg)
[![published](https://static.production.devnetcloud.com/codeexchange/assets/images/devnet-published.svg)](https://developer.cisco.com/codeexchange/github/repo/CiscoDevNet/MISP-SecureX-Orchestration-Workflows)

# MISP Events to Cisco XDR Incident and Ticketing System

## Features
*	Import events from [MISP](https://www.circl.lu/doc/misp/automation/) into Cisco XDR (also works for SecureX).
*	Automatically enrich observables and search for potential compromised assets with an automated Cisco XDR Investigation.
*	Send observables judgements to Private intel database within Cisco XDR and connect this feed to your security solutions (e.g. Cisco Sure Firewall). 
*	Auto create a prioritized and correlated incident within Cisco XDR Incident Manager, combing all sightings per MISP event in 1 single Incident.
*	Post Incident to a ticketing system or notification of choice (this can Webex, Email, MS teams, ServiceNow etc.).

> **Note:** Please test this properly before implementing in a production environment. This is a sample workflow!

## Required Targets
- MISP API ([SecureX Orchestration Remote Connector](https://ciscosecurity.github.io/sxo-05-security-workflows/remote/) may be needed)

## Required Account Keys
- [MISP API Keys](https://www.circl.lu/doc/misp/automation/)

## Setup instructions

### Configure Global Variables

1. Browse to your SecureX orchestration instance. This wille be a different URL depending on the region your account is in: 

* US: https://xdr.us.security.cisco.com/automate/workflows
* EU: https://xdr.eu.security.cisco.com/automate/workflows
* APJC: https://xdr.apjc.security.cisco.com/automate/workflows

2. Click on **IMPORT** to import the workflow:

![](screenshots/import-workflow.png)

3. Click on **Browse** and copy paste the content of the [misp-event-to-incident-workflow.json](https://raw.githubusercontent.com/CiscoDevNet/MISP-SecureX-Orchestration-Workflows/main/misp-event-to-incident-workflow.json) file inside of the text window. Select **IMPORT AS A NEW WORKFLOW (DUPLICATE)** and click on **IMPORT**.

![](screenshots/copy-paste.png)

4. Make sure you have filled in the MISP HTTP Target and API Credentials in the `MISP-GET-EVENTS` activity. 

5. At the bottom of the Workflow you can optionally add any ticketing system or notification of choice.

## Notes

* Please test this properly before implementing in a production environment. This is a sample workflow!

## Author(s)

* Pieter van Schaik (Cisco)
* Maarten Lutterman (Cisco)
* Christopher van der Made (Cisco)
