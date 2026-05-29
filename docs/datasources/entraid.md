# Ingest Identity Logs from Microsoft Entra ID using Microsoft Graph API

Use this procedure to send identity and authentication logs from Microsoft Entra ID into Databahn using Microsoft Graph API.

This includes:

* Sign-in logs
* Audit logs
* User activity logs

## Prerequisites

* Azure/Entra admin access
* Tenant ID
* App registration permissions

Required API permissions:

* AuditLog.Read.All
* Directory.Read.All
* SecurityEvents.Read.All (optional)


## Step-by-step setup

### Step 1: Register application

* Go to Microsoft Entra Admin Center
* Navigate to App registrations
* Click New registration
* Save:
   * Tenant ID
   * Client ID

### Step 2: Configure API permissions

* Open your app
* Go to API Permissions
* Add Microsoft Graph permissions:
  * AuditLog.Read.All
  * Directory.Read.All
* Click Grant admin consent

### Step 3: Create authentication secret

* Go to Certificates & Secrets
* Create Client Secret
* Copy and store securely

### Step 4: Configure Databahn connector

In Databahn:

* Add new source → Microsoft Entra ID
* Enter:
  * Tenant ID
  * Client ID
  * Client Secret
* Set polling interval (recommended: 5–15 minutes)

### Step 5: Validate ingestion

* Perform a test login
* Check Databahn dashboard
* Confirm sign-in logs appear