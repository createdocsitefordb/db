# :material-firewall: Ingest Palo Alto Networks Firewall Data via Syslog into Databahn
Use this procedure to ingest logs via Syslog

## :material-clipboard-check-outline: Access Prerequisites

* Admin access to a Palo Alto Networks firewall
* Permission to configure:
* Syslog server profiles
* Log forwarding profiles
* Security policy rules

## :material-server-network: Step 1: Configure Syslog Server Profile

On Palo Alto Networks firewall:

Navigate:

Device → Server Profiles → Syslog → Add

Configure:

- Name: Databahn-Syslog
- Server IP: Databahn Syslog Receiver IP
- Port: 514 (UDP/TCP) or 6514 (TLS recommended)
- Protocol: UDP / TCP / TLS
- Facility: LOG_LOCAL0–LOG_LOCAL7

## :material-forward: Step 2: Configure Log Forwarding Profile

Navigate to Objects → Log Forwarding → Add

Select logs:

- Traffic logs
- Threat logs
- URL filtering logs
- System logs
- VPN logs

Attach Syslog profile created above.

## :material-shield-lock: Step 3: Apply to Security Policy

Navigate Policies → Security → (select rule)

Under Actions tab, select Log Forwarding Profile

## :material-check-circle: Step 4: Commit Configuration

Click Commit and then click Apply Changes

