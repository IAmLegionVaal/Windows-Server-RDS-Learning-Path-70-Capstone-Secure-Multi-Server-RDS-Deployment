# Windows Server RDS Learning Path 70 — Capstone: Secure Multi-Server RDS Deployment

**Level:** Expert · **Module:** 70/70

## Goal
Design, build, secure, validate and document a production-style multi-server RDS deployment.

## Required architecture
- `DC01` and `DC02` for AD DS/DNS
- Highly available Connection Brokers with supported SQL backend
- RD Web Access and RD Gateway
- RD Licensing with legitimate CAL configuration
- At least two RD Session Hosts
- Profile/file services
- Internal and simulated external clients

## Delivery phases
1. Produce topology, addressing, DNS, OU, group, certificate, licensing, profile, monitoring and recovery designs.
2. Build and validate AD DS, DNS, sites, servers and clients.
3. Deploy Broker, Web, Gateway, Licensing and Session Hosts.
4. Create collections, full desktops and RemoteApps.
5. Apply least privilege, NLA, TLS, Gateway authorization, MFA architecture, Firewall, LAPS, auditing and service-account controls.
6. Validate profiles, load balancing, drain mode, sequential patching and component outages.
7. Perform health, capacity, backup and recovery assessments.
8. Close findings and publish sanitized evidence plus executive acceptance.

```powershell
Get-RDServer
Get-RDSessionCollection
Get-RDSessionHost -CollectionName 'RDS-Lab-Desktop' -ConnectionBroker '<broker-fqdn>'
Get-RDUserSession -ConnectionBroker '<broker-fqdn>'
Get-RDCertificate -ConnectionBroker '<broker-fqdn>'
Get-RDLicenseConfiguration -ConnectionBroker '<broker-fqdn>'
```

## Acceptance evidence
Create `evidence/` sections for architecture, build records, identity/access, policy/services, certificates/licensing, Gateway, sessions/apps, profiles, monitoring, performance, backup/recovery, outage tests, findings and final acceptance.

Every result must be observed in the lab. Include timestamps, commands, screenshots, events, expected versus actual results, deviations, root causes, corrective actions and retests. Redact credentials, keys, tokens, licence details and real organizational data.

## Acceptance criteria
- Required roles are healthy and correctly distributed.
- DNS, certificates, licensing and Gateway checks pass.
- Access is group-based and direct external RDP is unavailable.
- Session reconnection/load balancing/profile consistency work.
- Audit events are retained.
- Backup and recovery tests succeed.
- Findings have severity, owner, due date and validation.
- The environment can be rebuilt from the documentation.

## References
- https://learn.microsoft.com/en-us/windows-server/remote/remote-desktop-services/overview
- https://learn.microsoft.com/en-us/windows-server/remote/remote-desktop-services/rds-deploy-infrastructure

## Completion
This capstone completes the 70-module Windows Server RDS learning path.
