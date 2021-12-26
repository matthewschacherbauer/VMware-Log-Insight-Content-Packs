# WS Content Pack for VMware WorkspaceONE Access

This Content Pack provides supplemental dashboards for the official VMware Identity Manager content pack.

## Dashboards

The dashboards in this Content Pack collect logs and metrics from the WorkspaceONE Access appliances and the WorkspaceONE Connectors. The metrics are divided into dashboard names that begin with either Workspace or Connector.

### Workspace Sessions

This dashboard contains the following widgets.

* Sessions Over Time
* Number of Unique Successful User Logins
* API Handling Time in ms
* Resource Launches - Success
* Resource Launches - Failure

![Workspace Sessions](resources/ws-vmwwsoa-01.png?raw=true)

### Workspace Launch Failures

This dashboard contains the following widgets.

* Authenticated Launch Failures Over Time by Cause
* Authenticated Launch Failures by Cause
* Unique Users Experiencing Launch Failures
* All Launch Failures Over Time
* All Launch Failures by Cause

![Workspace Launch Failures](resources/ws-vmwwsoa-02.png?raw=true)

### Workspace SAML Client

This dashboard contains the following widgets.

* SAML Token Validation Activity
* SAML Validation by Client
* SAML Validation by Client over Time

![Workspace SAML Client](resources/ws-vmwwsoa-03.png?raw=true)

### Workspace Diagnostic

The widgets on the diagnostic dashboard are root cause of prior service disruptions. These are expected to be empty of results.

This dashboard contains the following widgets.

* Failed Resource Launch - Expired SAML SP Metadata
* SAML SP Metadata Refresh Failed Events
* Horizon Sync Failed Events
* ElasticSearch Warning Status
* System User Events

### Connector Authentication

This dashboard contains the following widgets.

* Password Authentication Events by Connector
* Password Auth by Connector
* Password Auth Results

### Connector Kerberos

This dashboard contains the following widgets.

* Kerberos Authentication Events by Connector
* Total Unique Users
* Kerberos Authentication Results

### Connector LDAP

This dashboard contains the following widgets.

* LDAP Authentication Events by Connector
* Total Unique Users
* LDAP Queries by Destination Server over Time
* LDAP Authentication Results
* Authentication Result over Time

![Connector LDAP](resources/ws-vmwwsoa-04.png?raw=true)

### Connector Radius

This dashboard contains the following widgets.

* Radius Challenge Events by Connector
* Radius Challenge Result
* Radius Challenge Result over Time
* Challenge Failure by User

![Connector Radius](resources/ws-vmwwsoa-05.png?raw=true)

### Connector Sync

This dashboard contains the following widgets.

* Horizon Connection Server Configuration
* Horizon Sync Status
* Horizon Sync Status by Connector

### Connector Misc

This dashboard contains the following widgets.

* Connectors by Tenant
* Domain Discovery Events

## Resources

### net.wolfspirit.loginsight.vmware.workspaceone.access.vlcp

This is the VMware vRealize Log Insight Content Pack bundle. This file contains the dashboards, queries, agent groups, and alarms and should be added to your VMware vRealize Log Insight installation.

## Installation Instructions

After installing this Content Pack, you must configure the required Agent Groups.

### Agent Groups

#### WS - Identity Manager

This is the Agent Group for collecting events from the On-Premise WorkspaceONE Access appliance. This is a direct copy of the official Identity Manager Agent Group.

#### WS - Identity Manager Windows Connector

This is the Agent Group for collecting events from the On-Premise WorkspaceONE Connector. This is a direct copy of the official Identity Manager Windows Collector Agent Group.
