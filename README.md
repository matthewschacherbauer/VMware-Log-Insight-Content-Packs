# VMware Log Insight Content Packs
This repository contains VMware Log Insight content packs containing sanitized dashboards used in test and production environments to monitor and troubleshoot real-world environments.

## Content Packs

### Microsoft AD Certificate Services

This Content Pack monitors the activity and issued certificates from Enterprise Certificate Authorities running Microsoft Active Directory Certificate Services.

![Certificate Services](MS%20AD%20Certificate%20Services/resources/ws-msadcs-01.png?raw=true)

### Microsoft AD Domain Services

This Content Pack provides supplemental dashboards for the official Active Directory content pack. LDAP Signing and NTLM Auditing require additional configuration on Domain Controllers, as these events do not generate under default configurations.

These dashboards allow an administrator to specifically target activities like:
* LDAP Signing and Channel Binding Compliance
* NTLM Auditing
* Password Activity Monitoring - Changes, Resets, and Lockout Events
* Authentication Events for Netlogon, NTLM, and Kerberos

|     |     |
| --- | --- |
| ![Password Activity](MS%20AD%20Domain%20Services/resources/ws-msadds-02.png?raw=true) | ![Kerberos Authentication](MS%20AD%20Domain%20Services/resources/ws-msadds-04.png?raw=true) |

### Microsoft RD Licensing Manager

This Content Pack monitors the activity and issued licenses from the Microsoft Remote Desktop Licensing Manager service.

* Activity for issuing and renewing licenses
* Track the quantity of version and type of licenses issued
* Monitor for faults and license exhaustion events

![License Monitor](MS%20RD%20Licensing%20Manager/resources/ws-msrdlicensing-01.png?raw=true)

### VMware App Volumes

This Content Pack monitors the activity and load on VMware App Volumes Manager servers.

* Total operations over time
* App Stack populatity and attach counts
* Monitor for database faults

|     |     |
| --- | --- |
| ![Manager Activity](VMware%20App%20Volumes/resources/ws-vmwavm-01.png?raw=true) | ![Attach Operations](VMware%20App%20Volumes/resources/ws-vmwavm-02.png?raw=true) |

### VMware Horizon

This Content Pack provides supplemental dashboards for the official VMware Horizon content pack. Additional agent groups are provided within the content pack to capture events from desktops. For full functionality, Log Insight must be deployed within the desktop image.

* Connection Server event monitoring
* Desktop Agent event monitoring
* Horizon Logon Monitor event capture
* Pool counts by size and status
* Popular catalog items and utilization
* Disconnect event monitoring
* Session start failure troubleshooting

|     |     |
| --- | --- |
| ![Broker Events](VMware%20Horizon/resources/ws-vmwhzn-01.png?raw=true) | ![Logon Time](VMware%20Horizon/resources/ws-vmwhzn-07.png?raw=true) |


### VMware Unified Access Gateway

This Content Pack monitors the activity of your VMware Unified Access Gateway appliances and is geared toward the use of Unified Access Gateways in the Horizon use case.

* Monitor the status, activity, and workload of each UAG
* Monitor the start and end of Horizon sessions
* Monitor authentication activity and track failure events

![Session Start Events](VMware%20Unified%20Access%20Gateway/resources/ws-vmwuag-02.png?raw=true)

### VMware WorkspaceOne Access

This Content Pack provides supplemental dashboards for the official VMware Identity Manager content pack.

These dashboards allow an administrator to specifically target activities like:
* Services performing SAML token validation against WorkspaceOne Access appliances
* Kerberos, LDAP, and Radius authentication events performed by the Connectors
* Monitor Horizon Sync status

|     |     |
| --- | --- |
| ![SAML Validations](VMware%20WorkspaceOne%20Access/resources/ws-vmwwsoa-03.png?raw=true) | ![Connector LDAP Activity](VMware%20WorkspaceOne%20Access/resources/ws-vmwwsoa-04.png?raw=true) |
