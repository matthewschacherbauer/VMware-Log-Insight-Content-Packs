# WS Content Pack for VMware Horizon

This Content Pack provides supplemental dashboards for the official VMware Horizon content pack. Additional agent groups are provided within the content pack to capture events from desktops. For full functionality, Log Insight must be deployed within the desktop image.

## Dashboards

### Broker Event Overview

This dashboard contains the following widgets.

* All Broker Events
* Broker Authentication Events
* Daily Peak Concurrent Sessions
* Broker Error Events by Type
* Broker Error Events
* Broker Warning Events by Type
* Broker Warning Events
* Broker Informational Events by Type
* Broker Informational Events
* Broker Audit Failures by Type
* Broker Audit Failure Events
* Broker Audit Success by Type
* Broker Audit Success Events
* Machines Not Ready
* Machine Not Ready Cause
* Agent Pending Expired
* Authentication Error Event Trends

![Broker Event Overview](resources/ws-vmwhzn-01.png?raw=true)

### Broker Pool Health

This dashboard contains the following widgets.

* Available Desktops by Pool
* Pool Dynamic Size
* Error VMs by Pool
* Agent Unreachable VMs by Pool
* Dirty VMs by Pool
* Guests Customizing by Pool

![Broker Pool Health](resources/ws-vmwhzn-02.png?raw=true)

### Catalog Popularity

This dashboard contains the following widgets.

* Horizon Resource Requests
* Session Type
* Request by Application Pool
* Request by Desktop Pool

![Catalog Popularity](resources/ws-vmwhzn-03.png?raw=true)

### Broker Launch Failures

This dashboard contains the following widgets.

* All Session Start Failures
* Unique Count of Sessions with Start Failures
* Desktop Start Failures by Pool Name
* App Start Failures by Application Name
* Desktop Start Failures by Username
* App Start Failures by Username
* Desktop Start Failures by Cause
* App Start Failures by Cause

![Broker Launch Failures](resources/ws-vmwhzn-04.png?raw=true)

### Disconnect Auditing

This dashboard contains the following widgets.

* Agent Connection State Change Events
* Disconnect Events by Pool
* Disconnect Events by Hostname
* Disconnections by Session Length
* Disconnected Session Average Length

![Disconnect Auditing](resources/ws-vmwhzn-05.png?raw=true)

### Desktop Agent Status

This dashboard contains the following widgets.

* Agent Status Messages
* Agent Session State
* Agent Ready Status Messages
* Agent Accepting Connections Status
* Agent Error States over Time
* Agent in Warning States over Time
* Agent in Error States over Time
* Agents with Pending Sessions
* Sessions per Farm Member
* Client Version
* Client Type
* Client Protocol
* Security Gateway Location
* Security Gateway
* View Agent Version
* DEM Agent Version
* OS Version
* AVM Endpoints
* Terminal Services Enabled

![Desktop Agent Status](resources/ws-vmwhzn-06.png?raw=true)

### Desktop Logon Time

This dashboard displays information reported by the Horizon Logon Monitor. The Horizon Logon Monitor must be installed and the Log Insight agent must be configured to collect logging information from the Logon Monitor within the end user desktops. This is not a default configuration.

This dashboard contains the following widgets.

* Count of Logon Monitor Events
* Average Total Logon Time
* Free Space at Logon
* Average Logon Script Time
* Average Machine Policy Time
* Average User Policy Time
* Average Shell Load Time

![Desktop Logon Time](resources/ws-vmwhzn-07.png?raw=true)

### Broker Admin Events

This dashboard contains the following widgets.

* Administrative Operations
* Administrative Event Categories
* Top Administrative Logon Users
* Desktop Image Push Operations
* Farm Image Push Operations

### Broker Replication

This dashboard compares the configuration replication version states between Horizon Connection Servers to help identify servers that may be behind or out of date compared to the cluster.

This dashboard contains the following widgets.

* Broker Sync: SamlAuthHealth Version
* Broker Sync: CertificateSsoHealth Version
* Broker Sync: BrokerHealth Version
* Broker Sync: GwHealth Version

### Cloud Connector

This dashboard monitors updates from the Horizon Subscription Licensing service. The Cloud Connector intermittently writes subscription licensing updates to the Connection Servers.

This dashboard contains the following widgets.

* Last Subscription Licensing Update

## Resources

### net.wolfspirit.loginsight.vmware.horizon.common.vlcp

This is the VMware vRealize Log Insight Content Pack bundle. This file contains the dashboards, queries, agent groups, and alarms and should be added to your VMware vRealize Log Insight installation.

## Installation Instructions

After installing this Content Pack, you must configure the required Agent Groups.

### Agent Groups

#### WS - Horizon - Agent (Windows)

This is the Agent Group that collects the required events from the VMware Horizon Agent logs. The Horizon Agent is the desktop agent component installed in the VDI images. Configuration of this agent group is required to collect system logs, App Volumes client logs, and Horizon Logon Monitor logs.

#### WS - Horizon - Broker (Windows)

This is the Agent Group that collects the required events from the VMware Horizon Connection Server logs. There are no differences between this Agent Group configuration and the one provided by the official Content Pack.
