# :material-sitemap: SIEM Integrations Overview

In this setup, Databahn is the central security data platform.

Databahn:

* Collects logs from multiple security tools (firewalls, identity, endpoint, cloud)
* Normalizes and enriches all incoming logs
* Detects threats and correlates events across sources
* Identifies high-confidence security signals
* Forwards only those strong signals to external SIEM platforms

### :material-export: Supported SIEM Destinations

Databahn can send filtered security events to:

* Microsoft Sentinel
* Splunk
* IBM QRadar

### :material-clipboard-list: Prerequisites

#### :material-cog: Databahn Prerequisites

Before configuring SIEM export:

* Databahn must be receiving logs from all sources
* Detection engine must be enabled
* SIEM export module must be active
* Admin access to SIEM integration settings

#### :material-server-security: SIEM Prerequisites

##### :material-shield-search: Microsoft Sentinel

* Log Analytics Workspace created
* Workspace ID available
* Primary Key OR DCR/DCE endpoint available

##### :material-chart-line: Splunk

* HTTP Event Collector (HEC) enabled
* HEC token generated
* Index created (e.g., security)

##### :material-radar: IBM QRadar

* Syslog receiver enabled
* QRadar IP address available
* Port configured (usually 514 or 6514)

### :material-lan: Network Requirements

Databahn must be able to reach SIEM endpoints:

* HTTPS (Sentinel, Splunk)
* Syslog TCP/UDP (QRadar)