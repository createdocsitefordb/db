# :material-shield-bug: Ingest CrowdStrike Logs via AWS SQS / S3

Logs from CrowdStrike are exported into AWS and ingested into Databahn.

Two ingestion options are supported:

Option A: S3 polling (simple)
Option B: S3 + SQS (recommended, real-time)

## :material-bucket-outline: S3 Polling Method

### Step 1: Enable CrowdStrike export

* Enable FDR or event streaming
* Configure S3 delivery

### Step 2: Create S3 bucket

Example: crowdstrike-telemetry-bucket

### Step 3: Configure Databahn S3 connector

In Databahn:

* Select S3 source
* Provide bucket name
* Set polling interval (which can range from 5–15 minutes)

### Step 4: Validate

* Wait for logs
* Confirm ingestion in dashboard

## :material-message-arrow-right: S3 + SQS Event-Driven Method (Recommended)

### Step 1: Enable CrowdStrike export

* Enable FDR or streaming export
* Deliver logs to S3 bucket

### Step 2: Create S3 bucket

Example: crowdstrike-telemetry-bucket

### Step 3: Create SQS queue

Create queue (e.g., crowdstrike-ingestion-queue)

### Step 4: Configure S3 event notification

* Open S3 bucket
* Go to Event Notifications
* Set:
   * Event type: ObjectCreated
   * Destination: SQS queue

### Step 5: Configure Databahn connector

In Databahn:

* Choose S3 + SQS ingestion
* Enter:
   * Bucket name
   * SQS queue URL
   * AWS region
   * IAM credentials or role

Step 6: Validate ingestion

Check Databahn for:

* Process execution logs
* Network activity
* File modifications
* Detection events