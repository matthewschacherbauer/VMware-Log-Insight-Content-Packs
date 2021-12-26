# WS Content Pack for Microsoft Active Directory Domain Services

This Content Pack provides supplemental dashboards for the official Active Directory content pack.

## Dashboards

### LDAP Channel Binding

This dashboard will help you identify clients that are impacted, or may be impacted, by changes to the LDAP Channel Binding and Channel Signing requirements.

This dashboard may require changes to your Domain Controller Security Policy to generate the required audit events. See the Installation Instructions below for more details. This is an optional configuration that will only affect the widgets on this dashboard.

This dashboard contains the following widgets.

* Channel Binding Failure Events
* Clients Failing Channel Binding
* Channel Binding Failures over Time

### LDAP Signing

This dashboard will help you identify clients that are impacted, or may be impacted, by changes to the LDAP Channel Binding and Channel Signing requirements.

This dashboard may require changes to your Domain Controller Security Policy to generate the required audit events. See the Installation Instructions below for more details. This is an optional configuration that will only affect the widgets on this dashboard.

This dashboard contains the following widgets.

* Binding Type
* Requests by Domain Controller
* Unsigned Bind Requests
* Simple Bind Requests without Encryption
* Unsigned Bind Clients
* Unsigned Bind Identities
* Simple Bind Clients
* Simple Bind Identities

### NTLM Audit Events

This dashboard may require changes to your Domain Controller Security Policy to generate the required audit events. See the Installation Instructions below for more details. This is an optional configuration that will only affect the widgets on this dashboard.

This dashboard contains the following widgets.

* NTLM Audit Events by EventID
* By Username
* By Workstation Name
* By Secure Channel Name
* By Secure Channel Type
* By Domain Name

![NTLM Audit Events](resources/ws-msadds-01.png?raw=true)

### Password Activity

This dashboard monitors for password related events, inclduing password changes, resets, and lockouts.

This dashboard contains the following widgets.

* Password Change by DC (4723)
* Password Reset by DC (4724)
* Account Lockout by DC (4740)
* Recent Account Lockouts and Source
* Recently Changed Passwords (4723)
* Recently Changed Passwords by Source (4723)
* Recently Changed Passwords by Target (4723)
* Recently Reset Passwords (4724)
* Recently Reset Passwords by Source (4724)
* Recently Reset Passwords by Target (4724)

![Password Activity](resources/ws-msadds-02.png?raw=true)

### Logon Authentication

This dashboard contains the following widgets.

* All Authentication Over Time by DC
* Authentication by Type
* By Process
* Success by DC (4624)
* Success by Process (4624)
* Success by Source (4624)
* Failure by DC (4625)
* Failure by Reason (4625)
* Failure by Source (4625)
* Failure by UserID (4525)

![Logon Authentication](resources/ws-msadds-03.png?raw=true)

### Kerberos Authentication

This dashboard contains the following widgets.

* All Authentication Over Time by DC
* Authentication by Type
* Kerberos Authentication Type
* Success Over Time by DC (4768)
* Success by UserID (4768)
* Success by ClientIP (4768)
* Failures Over Time by DC (4771)
* Failures by Reason (4771)
* Failures by Source (4771)
* Failures by UserID (4771)

![Kerberos Authentication](resources/ws-msadds-04.png?raw=true)

### NTLM Authentication

This dashboard contains the following widgets.

* All Authentication Over Time by DC
* Authentication by Type
* Success Over Time by DC (4776)
* Success by Source Workstation (4776)
* Success by UserID (4776)
* Failures Over Time by DC (4776)
* Failures by Reason (4776)
* Failures by Source Workstation (4776)
* Failures by UserID (4776)

![NTLM Authentication](resources/ws-msadds-05.png?raw=true)

### Operations

This dashboard contains the following widgets.

* Activity by Task
* User Account Operations
* Computer Account Operations

## Resources

### net.wolfspirit.loginsight.microsoft.ad.domainservices.vlcp

This is the VMware vRealize Log Insight Content Pack bundle. This file contains the dashboards, queries, agent groups, and alarms and should be added to your VMware vRealize Log Insight installation.

## Installation Instructions

After installing this Content Pack, you must configure the required Agent Groups.

Additional configuration is required to enable collection of NTLM Audit Events and LDAP Interface diagnostic events.

### Agent Groups

#### WS - Microsoft - Active Directory 2012+

This is the Agent Group that collects the required EventIDs from the Domain Controller event logs. This agent group is based on the official Active Directory Content Pack with additional log gathering. The additional log collectors are required to retrieve NTLM Audit Events.

### LDAP Interface Diagnostic Events

LDAP Channel Binding diagnostic events must be enabled to generate the required events. This is not a default configuration and will significantly increase the logging activity on Domain Controllers. This should be enabled during troubleshooting activities only.

Diagnostic event logging can be enabled with the following registry key:
Reg Add HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\NTDS\Diagnostics /v "16 LDAP Interface Events" /t REG_DWORD /d 2

For more information, see the following Microsoft help article.

https://support.microsoft.com/en-us/topic/2020-ldap-channel-binding-and-ldap-signing-requirements-for-windows-ef185fb8-00f7-167d-744c-f299a66fc00a

### NTLM Audit Security Policy

System Security Policy on the Domain Controllers must be configured to generate NTLM Auditing Events. This is not a default configuration.

Caution: Only the auditing policies should be enabled. Enabling the restriction policies may significantly impact authentication operations in the domain.

Refer to the following Microsoft Documentation to enable the required policies.

https://docs.microsoft.com/en-us/windows/security/threat-protection/security-policy-settings/network-security-restrict-ntlm-audit-incoming-ntlm-traffic

https://docs.microsoft.com/en-us/windows/security/threat-protection/security-policy-settings/network-security-restrict-ntlm-audit-ntlm-authentication-in-this-domain
