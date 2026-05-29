# IBM QRADAR Integration

## Overview

Use this procedure to send strong signals to IBM QRadar using Syslog.

## Steps

### Step 1: Configure QRadar log source

* Open QRadar Admin
* Add Log Source
* Select Syslog

### Step 2: Get QRadar details

* IP address of QRadar
* Port (514 or 6514)

### Step 3: Configure Databahn

* Go to SIEM Integrations
* Select QRadar
* Enter:
  * IP address
  * Port
  * Protocol (UDP/TCP/TLS)

### Step 4: Apply filtering rules

Use this procedure:

* Only HIGH / CRITICAL events
* Only confirmed detections
* Only correlated incidents

### Step 5: Enable export

Activate QRadar forwarding

### Step 6: Validate

* Check QRadar “Offenses”
* Confirm Databahn alerts appear