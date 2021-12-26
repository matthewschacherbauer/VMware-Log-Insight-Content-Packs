# WS Content Pack for VMware Unified Access Gateway

This Content Pack monitors the activity of your VMware Unified Access Gateway appliances and is geared toward the use of Unified Access Gateways in the Horizon use case.

## Dashboards

### Status

This dashboard contains the following widgets.

* Events by Activity over Time
* UAG Event Levels
* Request Activity by Unique Session
* Problem Events

![Status](resources/ws-vmwuag-01.png?raw=true)

### Session Start

This dashboard contains the following widgets.

* Authenticated Session Count
* Login Attempts by UAG
* Client Protocol
* Successful Authentications
* Failed Authentications
* Authentication Failure by Cause
* Authentication Failures by Cause over Time

![Session Start](resources/ws-vmwuag-02.png?raw=true)

### Session End

This dashboard contains the following widgets.

* Authenticated Session Count
* Session Close by UAG
* Session Close Cause

![Session End](resources/ws-vmwuag-03.png?raw=true)

## Resources

### net.wolfspirit.loginsight.vmware.uag.vlcp

This is the VMware vRealize Log Insight Content Pack bundle. This file contains the dashboards, queries, agent groups, and alarms and should be added to your VMware vRealize Log Insight installation.

## Installation Instructions

After installing this Content Pack, you must configure Unified Access Gateway appliances to forward logs via syslog to Log Insight.

