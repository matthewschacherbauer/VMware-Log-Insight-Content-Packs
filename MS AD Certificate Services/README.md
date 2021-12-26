# WS Content Pack for Microsoft Active Directory Certificate Services

This Content Pack monitors the activity and issued certificates from Enterprise Certificate Authorities running Microsoft Active Directory Certificate Services.

## Dashboards

### Certificate Services

This dashboard contains the following widgets.

* Certificate Services Activity
* Requests by Username
* Certificates Issued
* Certificates Issued by CA
* Certificates Issued by Subject
* Activity by EventID

![Certificate Services](resources/ws-msadcs-01.png?raw=true)

## Resources

### net.wolfspirit.loginsight.microsoft.ad.certificateservices.vlcp

This is the VMware vRealize Log Insight Content Pack bundle. This file contains the dashboards, queries, agent groups, and alarms and should be added to your VMware vRealize Log Insight installation.

## Installation Instructions

After installing this Content Pack, you must configure the required Agent Groups.

### Agent Groups

#### WS - Microsoft - AD Certificate Services

This is the Agent Group that collects the required EventIDs from the Certificate Authority event logs.

