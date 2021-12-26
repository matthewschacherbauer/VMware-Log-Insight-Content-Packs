# WS Content Pack for Microsoft Remote Desktop Licensing Manager

This Content Pack monitors the activity and issued licenses from the Microsoft Remote Desktop Licensing Manager service.

## Dashboards

### License Manager Service

This dashboard contains the following widgets.

* Remote Desktop CALs Issued
* Issued License Type
* Remote Desktop CALs Issued or Renewed
* Licensing Server Faults
* RDS Low CALs Events
* RDS CALs Exhaused Events
* License Server Faults - Detail

![License Manager Services](resources/ws-msrdlicensing-01.png?raw=true)

### License Upgrades

This dashboard contains the following widgets.

* License Upgrade Events
* Requested License Type
* Remote Desktop CALs Issued or Renewed

## Resources

### net.wolfspirit.loginsight.microsoft.rdp.licensemanager.vlcp

This is the VMware vRealize Log Insight Content Pack bundle. This file contains the dashboards, queries, agent groups, and alarms and should be added to your VMware vRealize Log Insight installation.

## Installation Instructions

After installing this Content Pack, you must configure the required Agent Groups.

### Agent Groups

#### WS - Microsoft - Remote Desktop License Manager

This is the Agent Group that collects the required events from the RD License Manager event logs.

