# Microsoft Sentinel Integration

## Overview

Use this procedure to send Databahn strong security signals into Microsoft Sentinel.

## Steps

### Step 1: Collect Sentinel details

From Microsoft:

* Workspace ID
* Primary Key OR DCR endpoint

### Step 2: Configure Databahn connector

* Go to Databahn → SIEM Integrations
* Select Microsoft Sentinel
* Enter credentials

### Step 3: Map event fields

Use this procedure:

Map Databahn output to Sentinel schema:

* user → Account
* ip → IPAddress
* event type → Activity
* severity → Level

### Step 4: Enable export
Turn ON Sentinel forwarding

### Step 5: Validate

* Trigger a high-severity event
* Confirm ingestion in Sentinel logs