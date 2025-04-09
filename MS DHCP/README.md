# WS Content Pack for Microsoft DHCP Server

This Content Pack provides dashboards for the Microsoft DHCP Server.

Installing this content pack requires configuration of an Agent Group to collect logging information from your DHCP Server. The DHCP Server must be configured to log events.

## Dashboards

### DHCP Server

This dashboard will help you identify events related to the lifecycle of client DHCP requests.

This dashboard contains the following widgets.

* DHCP Server Events
* Leases by Client Vendor Class
* Leases by Operation
* Recent Requests
* Leases Expired
* Leases Deleted

![DHCP Server](resources/ws-msdhcp-01.png?raw=true)

### Alerts

This dashboard will help you identify service events that may impact the issuance of addresses to DHCP clients.

This dashboard contains the following widgets.

* Scope Exhausted Events
* DNS Record Failed to be Deleted
