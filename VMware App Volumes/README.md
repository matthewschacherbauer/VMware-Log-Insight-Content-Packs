# WS Content Pack for VMware App Volumes

This Content Pack monitors the activity and load on VMware App Volumes Manager servers.

## Dashboards

### Manager Activity

This dashboard contains the following widgets.

* Activity by Manager
* Manager Balance
* Total Unique Users
* User Events
* Total Unique Computers
* Computer Events
* Agent Version

![Manager Activity](resources/ws-vmwavm-01.png?raw=true)

### Volume Operations

This dashboard contains the following widgets.

* Volume Attach Operations over Time
* Volume Attach Operations
* Volume Attach Count
* Volume Popularity

![Volume Operations](resources/ws-vmwavm-02.png?raw=true)

### Diagnostic

This dashboard contains the following widgets.

* ODBC Errors
* Missing Volumes

![Diagnostic](resources/ws-vmwavm-03.png?raw=true)

## Resources

### net.wolfspirit.loginsight.vmware.appvolumes.manager.vlcp

This is the VMware vRealize Log Insight Content Pack bundle. This file contains the dashboards, queries, agent groups, and alarms and should be added to your VMware vRealize Log Insight installation.

## Installation Instructions

After installing this Content Pack, you must configure the required Agent Groups.

### Agent Groups

#### WS - App Volumes Managers

This is the Agent Group that collects the required events from the VMware App Volumes Manager logs.

