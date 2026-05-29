# Log Ingestion into Databahn

Databahn ingests logs from three primary categories:

* Network logs via Palo Alto Networks (Syslog)
* Identity logs via Microsoft Entra ID (API)
* Endpoint logs via CrowdStrike (AWS SQS / S3)

Each category has specific access, configuration, and network requirements.