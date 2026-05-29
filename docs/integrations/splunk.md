# :material-chart-line: Splunk Integration

## :material-information-outline: Overview

Use this procedure to send strong signals to Splunk via HTTP Event Collector (HEC).

## :material-stairs: Steps

### Step 1: Enable HEC in Splunk

* Go to Settings → Data Inputs → HTTP Event Collector
* Enable HEC
* Create token

### Step 2: Configure Databahn

* Go to Databahn → SIEM Integrations
* Select Splunk
* Enter:
  * HEC URL
  * Token
  * Index name

### Step 3: Apply filtering

Use this procedure:

* Forward only:
  * HIGH severity
  * CRITICAL severity
  * Correlated events only

### Step 4: Enable export

Turn ON Splunk forwarding

### Step 5: Validate

Search Splunk index
Confirm events arriving