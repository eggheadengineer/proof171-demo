# System Security Plan: Severn Ridge Precision LLC

*Generated from synthetic demo data for a fictional company. Not an assessment, not legal advice, and not affiliated with DoD or the Cyber AB.*

Snapshot **2026-10-15** · bundle `714bd43a760a` · score **82** of 110 · Not eligible

## System boundary

- **Organization:** Severn Ridge Precision LLC, Odenton, MD (22 staff)
- **Work:** CNC machining of aluminum and titanium brackets for two defense primes
- **Enclave:** Microsoft 365 GCC High tenant severnridge.us + 14 managed laptops + 2 CAM workstations
- **CUI assets:** laptops, CAM workstations, fw-01, sw-core, Haas VF-4 x2, Zeiss CMM
- **Out of scope:** guest Wi-Fi, break-room TV

## Requirements

Each requirement lists every 800-171A objective, the evidence that decided it, and that evidence's hash.

### Access Control

#### AC.L2-3.1.1: Limit system access to authorized users, processes acting on behalf of authorized users, and devices (including other systems).

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-AC §3.1.1; practice verified as below.

- ✓ `3.1.1[a]` authorized users are identified.  
  *automated · entra-identity:* all 24 enabled people map to active HR records
- ✓ `3.1.1[b]` processes acting on behalf of authorized users are identified.  
  *automated · entra-identity:* 1 service account(s), each with a named owner
- ✓ `3.1.1[c]` devices (including other systems) authorized to connect to the system are identified.  
  *automated · intune-devices:* all 16 managed devices are in the asset inventory
- ✓ `3.1.1[d]` system access is limited to authorized users.  
  *automated · entra-identity:* no enabled accounts for departed staff
- ✓ `3.1.1[e]` system access is limited to processes acting on behalf of authorized users.  
  *automated · entra-identity:* service accounts hold no admin roles and use certificates
- ✓ `3.1.1[f]` system access is limited to authorized devices (including other systems).  
  *automated · intune-devices:* all 16 managed devices are in the asset inventory

#### AC.L2-3.1.2: Limit system access to the types of transactions and functions that authorized users are permitted to execute.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-AC §3.1.2; practice verified as below.

- ✓ `3.1.2[a]` the types of transactions and functions that authorized users are permitted to execute are defined  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.2[b]` system access is limited to the defined types of transactions and functions for authorized users.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock

#### AC.L2-3.1.3: Control the flow of CUI in accordance with approved authorizations.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AC §3.1.3; practice verified as below.

- ✓ `3.1.3[a]` information flow control policies are defined.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.3[b]` methods and enforcement mechanisms for controlling the flow of CUI are defined.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.3[c]` designated sources and destinations (e.g., networks, individuals, and devices) for CUI within systems and between interconnected systems are identified.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.3[d]` authorizations for controlling the flow of CUI are defined.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.3[e]` approved authorizations for controlling the flow of CUI are enforced.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock

#### AC.L2-3.1.4: Separate the duties of individuals to reduce the risk of malevolent activity without collusion.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AC §3.1.4; practice verified as below.

- ✓ `3.1.4[a]` the duties of individuals requiring separation to reduce the risk of malevolent activity are defined.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.4[b]` organization-defined duties of individuals requiring separation are separated.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.4[c]` separate accounts for individuals whose duties and accesses must be separated to reduce the risk of malevolent activity or collusion are established  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock

#### AC.L2-3.1.5: Employ the principle of least privilege, including for specific security functions and privileged accounts.

**Status:** MET · value 3 point(s)

Implementation: governed by policy POL-AC §3.1.5; practice verified as below.

- ✓ `3.1.5[a]` privileged accounts are identified.  
  *automated · entra-identity:* 1 privileged account(s) identified
- ✓ `3.1.5[b]` access to privileged accounts is authorized in accordance with the principle of least privilege.  
  *automated · entra-identity:* 1 privileged account(s), within the approved limit of 2
- ✓ `3.1.5[c]` security functions are identified.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.5[d]` access to security functions is authorized in accordance with the principle of least privilege.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock

#### AC.L2-3.1.6: Use non-privileged accounts or roles when accessing nonsecurity functions

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AC §3.1.6; practice verified as below.

- ✓ `3.1.6[a]` nonsecurity functions are identified.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.6[b]` users are required to use non-privileged accounts or roles when accessing nonsecurity functions.  
  *automated · entra-identity:* admin roles held only by separate adm- accounts

#### AC.L2-3.1.7: Prevent non-privileged users from executing privileged functions and capture the execution of such functions in audit logs.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AC §3.1.7; practice verified as below.

- ✓ `3.1.7[a]` privileged functions are defined.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.7[b]` non-privileged users are defined.  
  *automated · entra-identity:* 23 non-privileged accounts defined
- ✓ `3.1.7[c]` non-privileged users are prevented from executing privileged functions.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.7[d]` the execution of privileged functions is captured in audit logs.  
  *automated · audit:* unified audit log on, 365-day retention

#### AC.L2-3.1.8: Limit unsuccessful logon attempts.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AC §3.1.8; practice verified as below.

- ✓ `3.1.8[a]` the means of limiting unsuccessful logon attempts is defined.  
  *automated · entra-policies:* lockout after 5 failed attempts for 30 min
- ✓ `3.1.8[b]` the defined means of limiting unsuccessful logon attempts is implemented.  
  *automated · entra-policies:* lockout enforced tenant-wide

#### AC.L2-3.1.9: Provide privacy and security notices consistent with applicable CUI rules.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AC §3.1.9; practice verified as below.

- ✓ `3.1.9[a]` privacy and security notices required by CUI-specified rules are identified, consistent, and associated with the specific CUI category  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.9[b]` privacy and security notices are displayed.  
  *automated · entra-policies:* CUI logon banner displayed

#### AC.L2-3.1.10: Use session lock with pattern-hiding displays to prevent access and viewing of data after a period of inactivity

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AC §3.1.10; practice verified as below.

- ✓ `3.1.10[a]` the period of inactivity after which the system initiates a session lock is defined.  
  *automated · entra-policies:* session lock after 15 minutes
- ✓ `3.1.10[b]` access to the system and viewing of data is prevented by initiating a session lock after the defined period of inactivity.  
  *automated · intune-devices:* 15-minute screen lock enforced on every device
- ✓ `3.1.10[c]` previously visible information is concealed via a pattern-hiding display after the defined period of inactivity.  
  *automated · intune-devices:* pattern-hiding lock screen enforced

#### AC.L2-3.1.11: Terminate (automatically) a user session after a defined condition.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AC §3.1.11; practice verified as below.

- ✓ `3.1.11[a]` conditions requiring a user session to terminate are defined.  
  *automated · entra-policies:* sessions end on sign-in frequency and sign-out
- ✓ `3.1.11[b]` a user session is automatically terminated after any of the defined conditions occur.  
  *automated · entra-policies:* sign-in frequency policy enabled

#### AC.L2-3.1.12: Monitor and control remote access sessions.

**Status:** NOT MET · value 5 point(s) · **5 deducted**

Implementation: governed by policy POL-AC §3.1.12; practice verified as below.

- ✓ `3.1.12[a]` remote access sessions are permitted.  
  *automated · firewall:* remote access permitted via ssl-vpn
- ✓ `3.1.12[b]` the types of permitted remote access are identified.  
  *automated · firewall:* remote access permitted via ssl-vpn
- ✗ `3.1.12[c]` remote access sessions are controlled.  
  *automated · firewall:* remote access outside the VPN: rule 9 "TEMP vendor RDP - remove after visit" (RDP from anywhere to 10.20.0.15)
- ✗ `3.1.12[d]` remote access sessions are monitored.  
  *automated · firewall:* accept rules not logged: rule 9

#### AC.L2-3.1.13: Employ cryptographic mechanisms to protect the confidentiality of remote access sessions.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-AC §3.1.13; practice verified as below.

- ✓ `3.1.13[a]` cryptographic mechanisms to protect the confidentiality of remote access sessions are identified.  
  *automated · firewall:* VPN cipher TLS1.3 AES-256-GCM
- ✓ `3.1.13[b]` cryptographic mechanisms to protect the confidentiality of remote access sessions are implemented.  
  *automated · firewall:* FIPS mode enforced

#### AC.L2-3.1.14: Route remote access via managed access control points.

**Status:** NOT MET · value 1 point(s) · **1 deducted**

Implementation: governed by policy POL-AC §3.1.14; practice verified as below.

- ✗ `3.1.14[a]` managed access control points are identified and implemented.  
  *automated · firewall:* remote access outside the VPN: rule 9 "TEMP vendor RDP - remove after visit" (RDP from anywhere to 10.20.0.15)
- ✓ `3.1.14[b]` remote access is routed through managed network access control points.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock

#### AC.L2-3.1.15: Authorize remote execution of privileged commands and remote access to security-relevant information.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AC §3.1.15; practice verified as below.

- ✓ `3.1.15[a]` privileged commands authorized for remote execution are identified.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.15[b]` security-relevant information authorized to be accessed remotely is identified.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.15[c]` the execution of the identified privileged commands via remote access is authorized.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.15[d]` access to the identified security-relevant information via remote access is authorized.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock

#### AC.L2-3.1.16: Authorize wireless access prior to allowing such connections

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-AC §3.1.16; practice verified as below.

- ✓ `3.1.16[a]` wireless access points are identified.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.16[b]` wireless access is authorized prior to allowing such connections.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock

#### AC.L2-3.1.17: Protect wireless access using authentication and encryption

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-AC §3.1.17; practice verified as below.

- ✓ `3.1.17[a]` wireless access to the system is protected using encryption.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.17[b]` wireless access to the system is protected using authentication.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock

#### AC.L2-3.1.18: Control connection of mobile devices.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-AC §3.1.18; practice verified as below.

- ✓ `3.1.18[a]` mobile devices that process, store, or transmit CUI are identified.  
  *automated · intune-devices:* 14 laptops identified as mobile devices handling CUI
- ✓ `3.1.18[b]` the connection of mobile devices is authorized.  
  *automated · intune-devices:* only Intune-enrolled devices may connect (conditional access CA04)
- ✓ `3.1.18[c]` mobile device connections are monitored and logged.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock

#### AC.L2-3.1.19: Encrypt CUI on mobile devices and mobile computing platforms.[23]

**Status:** MET · value 3 point(s)

Implementation: governed by policy POL-AC §3.1.19; practice verified as below.

- ✓ `3.1.19[a]` mobile devices and mobile computing platforms that process, store, or transmit CUI are identified.  
  *automated · intune-devices:* 14 laptops identified
- ✓ `3.1.19[b]` encryption is employed to protect CUI on identified mobile devices and mobile computing platforms.  
  *automated · intune-devices:* BitLocker on every laptop

#### AC.L2-3.1.20: Verify and control/limit connections to and use of external systems.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AC §3.1.20; practice verified as below.

- ✓ `3.1.20[a]` connections to external systems are identified.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.20[b]` use of external systems is identified.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.20[c]` connections to external systems are verified.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.20[d]` use of external systems is verified.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.20[e]` connections to external systems are controlled/limited.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.20[f]` use of external systems is controlled/limited.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock

#### AC.L2-3.1.21: Limit use of portable storage devices on external systems.

**Status:** NOT MET · value 1 point(s) · **1 deducted**

Implementation: governed by policy POL-AC §3.1.21; practice verified as below.

- ✓ `3.1.21[a]` use of organizational portable storage devices containing CUI on external systems is identified and documented.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✗ `3.1.21[b]` limits on the use of organizational portable storage devices containing CUI on external systems are defined.  
  *policy · POL-AC:* known gap: USB write-blocking has an exception for CMM report export; no written limit for use on customer systems
- ✓ `3.1.21[c]` use of organizational portable storage devices containing CUI on external systems is limited as defined.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock

#### AC.L2-3.1.22: Control CUI posted or processed on publicly accessible systems.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AC §3.1.22; practice verified as below.

- ✓ `3.1.22[a]` individuals authorized to post or process information on publicly accessible systems are identified.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.22[b]` procedures to ensure CUI is not posted or processed on publicly accessible systems are identified.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.22[c]` a review process in in place prior to posting of any content to publicly accessible systems.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.22[d]` content on publicly accessible information systems is reviewed to ensure that it does not include CUI.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.1.22[e]` mechanisms are in place to remove and address improper posting of CUI.  
  *policy · POL-AC:* Access Control policy, approved 2026-03-02 by Dana Whitlock

### Awareness and Training

#### AT.L2-3.2.1: Ensure that managers, systems administrators, and users of organizational systems are made aware of the security risks associated with their activities and of the applicable policies, standards, and procedures related to the security of those systems.

**Status:** NOT MET · value 5 point(s) · **5 deducted**

Implementation: governed by policy POL-AT §3.2.1; practice verified as below.

- ✓ `3.2.1[a]` security risks associated with organizational activities involving CUI are identified.  
  *policy · POL-AT:* Awareness and Training policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.2.1[b]` policies, standards, and procedures related to the security of the system are identified.  
  *policy · POL-AT:* Awareness and Training policy, approved 2026-03-02 by Dana Whitlock
- ✗ `3.2.1[c]` managers, systems administrators, and users of the system are made aware of the security risks associated with their activities.  
  *automated · training:* awareness training lapsed: tbrandt (expired 2026-10-06)
- ✗ `3.2.1[d]` managers, systems administrators, and users of the system are made aware of the applicable policies, standards, and procedures related to the security of the system.  
  *automated · training:* awareness training lapsed: tbrandt (expired 2026-10-06)

#### AT.L2-3.2.2: Ensure that personnel are trained to carry out their assigned information security-related duties and responsibilities.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-AT §3.2.2; practice verified as below.

- ✓ `3.2.2[a]` information security-related duties, roles, and responsibilities are defined.  
  *policy · POL-AT:* Awareness and Training policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.2.2[b]` information security-related duties, roles, and responsibilities are assigned to designated personnel.  
  *automated · training:* system administrator holds current role-based training
- ✓ `3.2.2[c]` personnel are adequately trained to carry out their assigned information security-related duties, roles, and responsibilities.  
  *automated · training:* system administrator holds current role-based training

#### AT.L2-3.2.3: Provide security awareness training on recognizing and reporting potential indicators of insider threat.

**Status:** NOT MET · value 1 point(s) · **1 deducted**

Implementation: governed by policy POL-AT §3.2.3; practice verified as below.

- ✓ `3.2.3[a]` potential indicators associated with insider threats are identified.  
  *policy · POL-AT:* Awareness and Training policy, approved 2026-03-02 by Dana Whitlock
- ✗ `3.2.3[b]` security awareness training on recognizing and reporting potential indicators of insider threat is provided to managers and employees.  
  *automated · training:* insider-threat training lapsed: tbrandt (expired 2026-10-06)

### Audit and Accountability

#### AU.L2-3.3.1: Create and retain system audit logs and records to the extent needed to enable the monitoring, analysis, investigation, and reporting of unlawful or unauthorized system activity

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-AU §3.3.1; practice verified as below.

- ✓ `3.3.1[a]` audit logs needed (i.e., event types to be logged) to enable the monitoring, analysis, investigation, and reporting of unlawful or unauthorized system activity are specified.  
  *automated · audit:* unified audit log on, 365-day retention
- ✓ `3.3.1[b]` the content of audit records needed to support monitoring, analysis, investigation, and reporting of unlawful or unauthorized system activity is defined.  
  *automated · audit:* unified audit log on, 365-day retention
- ✓ `3.3.1[c]` audit records are created (generated).  
  *automated · audit:* unified audit log on, 365-day retention
- ✓ `3.3.1[d]` audit records, once created, contain the defined content.  
  *automated · audit:* unified audit log on, 365-day retention
- ✓ `3.3.1[e]` retention requirements for audit records are defined.  
  *automated · audit:* unified audit log on, 365-day retention
- ✓ `3.3.1[f]` audit records are retained as defined.  
  *automated · audit:* unified audit log on, 365-day retention

#### AU.L2-3.3.2: Ensure that the actions of individual system users can be uniquely traced to those users, so they can be held accountable for their actions.

**Status:** MET · value 3 point(s)

Implementation: governed by policy POL-AU §3.3.2; practice verified as below.

- ✓ `3.3.2[a]` the content of the audit records needed to support the ability to uniquely trace users to their actions is defined.  
  *policy · POL-AU:* Audit and Accountability policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.3.2[b]` audit records, once created, contain the defined content.  
  *policy · POL-AU:* Audit and Accountability policy, approved 2026-03-02 by Dana Whitlock

#### AU.L2-3.3.3: Review and update logged events.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AU §3.3.3; practice verified as below.

- ✓ `3.3.3[a]` a process for determining when to review logged events is defined.  
  *policy · POL-AU:* Audit and Accountability policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.3.3[b]` event types being logged are reviewed in accordance with the defined review process.  
  *policy · POL-AU:* Audit and Accountability policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.3.3[c]` event types being logged are updated based on the review.  
  *policy · POL-AU:* Audit and Accountability policy, approved 2026-03-02 by Dana Whitlock

#### AU.L2-3.3.4: Alert in the event of an audit logging process failure.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AU §3.3.4; practice verified as below.

- ✓ `3.3.4[a]` personnel or roles to be alerted in the event of an audit logging process failure are identified.  
  *automated · audit:* alert fires if audit logging stops
- ✓ `3.3.4[b]` types of audit logging process failures for which alert will be generated are defined.  
  *automated · audit:* alert fires if audit logging stops
- ✓ `3.3.4[c]` identified personnel or roles are alerted in the event of an audit logging process failure.  
  *automated · audit:* alert fires if audit logging stops

#### AU.L2-3.3.5: Correlate audit record review, analysis, and reporting processes for investigation and response to indications of unlawful, unauthorized, suspicious, or unusual activity.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-AU §3.3.5; practice verified as below.

- ✓ `3.3.5[a]` audit record review, analysis, and reporting processes for investigation and response to indications of unlawful, unauthorized, suspicious, or unusual activity are defined.  
  *automated · audit:* correlated in Microsoft Sentinel
- ✓ `3.3.5[b]` defined audit record review, analysis, and reporting processes are correlated.  
  *automated · audit:* correlated in Microsoft Sentinel

#### AU.L2-3.3.6: Provide audit record reduction and report generation to support on-demand analysis and reporting.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AU §3.3.6; practice verified as below.

- ✓ `3.3.6[a]` an audit record reduction capability that supports on-demand analysis is provided.  
  *policy · POL-AU:* Audit and Accountability policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.3.6[b]` a report generation capability that supports on-demand reporting is provided.  
  *policy · POL-AU:* Audit and Accountability policy, approved 2026-03-02 by Dana Whitlock

#### AU.L2-3.3.7: Provide a system capability that compares and synchronizes internal system clocks with an authoritative source to generate time stamps for audit records

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AU §3.3.7; practice verified as below.

- ✓ `3.3.7[a]` internal system clocks are used to generate time stamps for audit records.  
  *automated · audit:* time.windows.com (Windows Time, domain hierarchy)
- ✓ `3.3.7[b]` an authoritative source with which to compare and synchronize internal system clocks is specified.  
  *automated · audit:* time.windows.com (Windows Time, domain hierarchy)
- ✓ `3.3.7[c]` internal system clocks used to generate time stamps for audit records are compared to and synchronized with the specified authoritative time source.  
  *automated · audit:* time.windows.com (Windows Time, domain hierarchy)

#### AU.L2-3.3.8: Protect audit information and audit logging tools from unauthorized access, modification, and deletion.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AU §3.3.8; practice verified as below.

- ✓ `3.3.8[a]` audit information is protected from unauthorized access.  
  *automated · audit:* audit records immutable
- ✓ `3.3.8[b]` audit information is protected from unauthorized modification.  
  *automated · audit:* audit records immutable
- ✓ `3.3.8[c]` audit information is protected from unauthorized deletion.  
  *automated · audit:* audit records immutable
- ✓ `3.3.8[d]` audit logging tools are protected from unauthorized access.  
  *automated · audit:* audit records immutable
- ✓ `3.3.8[e]` audit logging tools are protected from unauthorized modification.  
  *automated · audit:* audit records immutable
- ✓ `3.3.8[f]` audit logging tools are protected from unauthorized deletion.  
  *automated · audit:* audit records immutable

#### AU.L2-3.3.9: Limit management of audit logging functionality to a subset of privileged users.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-AU §3.3.9; practice verified as below.

- ✓ `3.3.9[a]` a subset of privileged users granted access to manage audit logging functionality is defined.  
  *automated · audit:* audit management limited to adm-praman
- ✓ `3.3.9[b]` management of audit logging functionality is limited to the defined subset of privileged users.  
  *automated · audit:* audit management limited to adm-praman

### Configuration Management

#### CM.L2-3.4.1: Establish and maintain baseline configurations and inventories of organizational systems (including hardware, software, firmware, and documentation) throughout the respective system development life cycles.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-CM §3.4.1; practice verified as below.

- ✓ `3.4.1[a]` a baseline configuration is established.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.1[b]` the baseline configuration includes hardware, software, firmware, and documentation.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.1[c]` the baseline configuration is maintained (reviewed and updated) throughout the system development life cycle.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.1[d]` a system inventory is established.  
  *automated · intune-devices:* inventory of 21 assets maintained
- ✓ `3.4.1[e]` the system inventory includes hardware, software, firmware, and documentation.  
  *automated · intune-devices:* all 16 managed devices are in the asset inventory
- ✓ `3.4.1[f]` the inventory is maintained (reviewed and updated) throughout the system development life cycle.  
  *automated · intune-devices:* all 16 managed devices are in the asset inventory

#### CM.L2-3.4.2: Establish and enforce security configuration settings for information technology products employed in organizational systems.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-CM §3.4.2; practice verified as below.

- ✓ `3.4.2[a]` security configuration settings for information technology products employed in the system are established and included in the baseline configuration.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.2[b]` security configuration settings for information technology products employed in the system are enforced.  
  *automated · intune-devices:* firewall, BitLocker and 15-minute lock enforced by Intune baseline

#### CM.L2-3.4.3: Track, review, approve or disapprove, and log changes to organizational systems.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-CM §3.4.3; practice verified as below.

- ✓ `3.4.3[a]` changes to the system are tracked.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.3[b]` changes to the system are reviewed.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.3[c]` changes to the system are approved or disapproved.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.3[d]` changes to the system are logged.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock

#### CM.L2-3.4.4: Analyze the security impact of changes prior to implementation.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-CM §3.4.4; practice verified as below.

- ✓ `3.4.4[a]` the security impact of changes to each organizational system is analyzed prior to implementation.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock

#### CM.L2-3.4.5: Define, document, approve, and enforce physical and logical access restrictions associated with changes to organizational systems.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-CM §3.4.5; practice verified as below.

- ✓ `3.4.5[a]` physical access restrictions associated with changes to the system are defined.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.5[b]` physical access restrictions associated with changes to the system are documented.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.5[c]` physical access restrictions associated with changes to the system are approved.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.5[d]` physical access restrictions associated with changes to the system are enforced.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.5[e]` logical access restrictions associated with changes to the system are defined.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.5[f]` logical access restrictions associated with changes to the system are documented.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.5[g]` logical access restrictions associated with changes to the system are approved.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.5[h]` logical access restrictions associated with changes to the system are enforced.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock

#### CM.L2-3.4.6: Employ the principle of least functionality by configuring organizational systems to provide only essential capabilities.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-CM §3.4.6; practice verified as below.

- ✓ `3.4.6[a]` essential system capabilities are defined based on the principle of least functionality.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.6[b]` the system is configured to provide only the defined essential capabilities.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock

#### CM.L2-3.4.7: Restrict, disable, or prevent the use of nonessential programs, functions, ports, protocols, and services.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-CM §3.4.7; practice verified as below.

- ✓ `3.4.7[a]` essential programs are defined.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.7[b]` the use of nonessential programs is defined.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.7[c]` the use of nonessential programs is restricted, disabled, or prevented as defined.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.7[d]` essential functions are defined.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.7[e]` the use of nonessential functions is defined.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.7[f]` the use of nonessential functions is restricted, disabled, or prevented as defined.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.7[g]` essential ports are defined.  
  *automated · firewall:* permitted ports listed per rule
- ✓ `3.4.7[h]` the use of nonessential ports is defined.  
  *automated · firewall:* everything not listed is denied
- ✓ `3.4.7[i]` the use of nonessential ports is restricted, disabled, or prevented as defined.  
  *automated · firewall:* every accept rule names its services
- ✓ `3.4.7[j]` essential protocols are defined.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.7[k]` the use of nonessential protocols is defined.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.7[l]` the use of nonessential protocols is restricted, disabled, or prevented as defined.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.7[m]` essential services are defined.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.7[n]` the use of nonessential services is defined.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.7[o]` the use of nonessential services is restricted, disabled, or prevented as defined.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock

#### CM.L2-3.4.8: Apply deny-by-exception (blacklisting) policy to prevent the use of unauthorized software or deny-all, permit-by-exception (whitelisting) policy to allow the execution of authorized software.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-CM §3.4.8; practice verified as below.

- ✓ `3.4.8[a]` a policy specifying whether whitelisting or blacklisting is to be implemented is specified.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.8[b]` the software allowed to execute under whitelisting or denied use under blacklisting is specified.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.8[c]` whitelisting to allow the execution of authorized software or blacklisting to prevent the use of unauthorized software is implemented as specified.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock

#### CM.L2-3.4.9: Control and monitor user-installed software.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-CM §3.4.9; practice verified as below.

- ✓ `3.4.9[a]` a policy for controlling the installation of software by users is established.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.4.9[b]` installation of software by users is controlled based on the established policy.  
  *automated · entra-policies:* user software installs blocked by Intune
- ✓ `3.4.9[c]` installation of software by users is monitored.  
  *policy · POL-CM:* Configuration Management policy, approved 2026-03-02 by Dana Whitlock

### Identification and Authentication

#### IA.L2-3.5.1: Identify system users, processes acting on behalf of users, and devices.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-IA §3.5.1; practice verified as below.

- ✓ `3.5.1[a]` system users are identified.  
  *automated · entra-identity:* all 24 enabled people map to active HR records
- ✓ `3.5.1[b]` processes acting on behalf of users are identified.  
  *automated · entra-identity:* 1 service account(s), each with a named owner
- ✓ `3.5.1[c]` devices accessing the system are identified.  
  *automated · intune-devices:* all 16 managed devices are in the asset inventory

#### IA.L2-3.5.2: Authenticate (or verify) the identities of users, processes, or devices, as a prerequisite to allowing access to organizational systems.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-IA §3.5.2; practice verified as below.

- ✓ `3.5.2[a]` the identity of each user is authenticated or verified as a prerequisite to system access.  
  *automated · entra-identity:* every enabled account requires authentication
- ✓ `3.5.2[b]` the identity of each process acting on behalf of a user is authenticated or verified as a prerequisite to system access.  
  *automated · entra-identity:* service accounts hold no admin roles and use certificates
- ✓ `3.5.2[c]` the identity of each device accessing or connecting to the system is authenticated or verified as a prerequisite to system access.  
  *policy · POL-IA:* Identification and Authentication policy, approved 2026-03-02 by Dana Whitlock

#### IA.L2-3.5.3: Use multifactor authentication for local and network access to privileged accounts and for network access to non-privileged accounts.[24] [25].

**Status:** NOT MET · value 5 point(s) · **3 deducted**

Implementation: governed by policy POL-IA §3.5.3; practice verified as below.

- ✓ `3.5.3[a]` privileged accounts are identified.  
  *automated · entra-identity:* privileged accounts identified: adm-praman@severnridge.us
- ✓ `3.5.3[b]` multifactor authentication is implemented for local access to privileged accounts.  
  *automated · entra-identity:* privileged accounts use phishing-resistant or app MFA
- ✓ `3.5.3[c]` multifactor authentication is implemented for network access to privileged accounts.  
  *automated · entra-identity:* privileged accounts use phishing-resistant or app MFA
- ✗ `3.5.3[d]` multifactor authentication is implemented for network access to non-privileged accounts.  
  *automated · entra-identity:* no MFA registered: jalvarez@severnridge.us (remote: no)

#### IA.L2-3.5.4: Employ replay-resistant authentication mechanisms for network access to privileged and non-privileged accounts.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-IA §3.5.4; practice verified as below.

- ✓ `3.5.4[a]` replay-resistant authentication mechanisms are implemented for all network account access to privileged and non-privileged accounts.  
  *automated · entra-policies:* legacy (replayable) authentication blocked

#### IA.L2-3.5.5: Prevent reuse of identifiers for a defined period.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-IA §3.5.5; practice verified as below.

- ✓ `3.5.5[a]` a period within which identifiers cannot be reused is defined.  
  *policy · POL-IA:* Identification and Authentication policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.5.5[b]` reuse of identifiers is prevented within the defined period.  
  *policy · POL-IA:* Identification and Authentication policy, approved 2026-03-02 by Dana Whitlock

#### IA.L2-3.5.6: Disable identifiers after a defined period of inactivity.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-IA §3.5.6; practice verified as below.

- ✓ `3.5.6[a]` a period of inactivity after which an identifier is disabled is defined.  
  *policy · POL-IA:* Identification and Authentication policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.5.6[b]` identifiers are disabled after the defined period of inactivity.  
  *automated · entra-identity:* no enabled account idle more than 45 days

#### IA.L2-3.5.7: Enforce a minimum password complexity and change of characters when new passwords are created.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-IA §3.5.7; practice verified as below.

- ✓ `3.5.7[a]` password complexity requirements are defined.  
  *automated · entra-policies:* minimum length 14 with banned-password list
- ✓ `3.5.7[b]` password change of character requirements are defined.  
  *policy · POL-IA:* Identification and Authentication policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.5.7[c]` minimum password complexity requirements as defined are enforced when new passwords are created.  
  *policy · POL-IA:* Identification and Authentication policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.5.7[d]` minimum password change of character requirements as defined are enforced when new passwords are created.  
  *policy · POL-IA:* Identification and Authentication policy, approved 2026-03-02 by Dana Whitlock

#### IA.L2-3.5.8: Prohibit password reuse for a specified number of generations.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-IA §3.5.8; practice verified as below.

- ✓ `3.5.8[a]` the number of generations during which a password cannot be reused is specified.  
  *policy · POL-IA:* Identification and Authentication policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.5.8[b]` reuse of passwords is prohibited during the specified number of generations.  
  *automated · entra-policies:* reuse blocked for 24 generations

#### IA.L2-3.5.9: Allow temporary password use for system logons with an immediate change to a permanent password.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-IA §3.5.9; practice verified as below.

- ✓ `3.5.9[a]` an immediate change to a permanent password is required when a temporary password is used for system logon.  
  *automated · entra-policies:* temporary passwords must be changed at first sign-in

#### IA.L2-3.5.10: Store and transmit only cryptographically-protected passwords.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-IA §3.5.10; practice verified as below.

- ✓ `3.5.10[a]` passwords are cryptographically protected in storage.  
  *policy · POL-IA:* Identification and Authentication policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.5.10[b]` passwords are cryptographically protected in transit.  
  *policy · POL-IA:* Identification and Authentication policy, approved 2026-03-02 by Dana Whitlock

#### IA.L2-3.5.11: Obscure feedback of authentication information

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-IA §3.5.11; practice verified as below.

- ✓ `3.5.11[a]` authentication information is obscured during the authentication process.  
  *policy · POL-IA:* Identification and Authentication policy, approved 2026-03-02 by Dana Whitlock

### Incident Response

#### IR.L2-3.6.1: Establish an operational incident-handling capability for organizational systems that includes preparation, detection, analysis, containment, recovery, and user response activities.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-IR §3.6.1; practice verified as below.

- ✓ `3.6.1[a]` an operational incident-handling capability is established.  
  *policy · POL-IR:* Incident Response policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.6.1[b]` the operational incident-handling capability includes preparation.  
  *policy · POL-IR:* Incident Response policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.6.1[c]` the operational incident-handling capability includes detection.  
  *policy · POL-IR:* Incident Response policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.6.1[d]` the operational incident-handling capability includes analysis.  
  *policy · POL-IR:* Incident Response policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.6.1[e]` the operational incident-handling capability includes containment.  
  *policy · POL-IR:* Incident Response policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.6.1[f]` the operational incident-handling capability includes recovery.  
  *policy · POL-IR:* Incident Response policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.6.1[g]` the operational incident-handling capability includes user response activities.  
  *policy · POL-IR:* Incident Response policy, approved 2026-03-02 by Dana Whitlock

#### IR.L2-3.6.2: Track, document, and report incidents to designated officials and/or authorities both internal and external to the organization.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-IR §3.6.2; practice verified as below.

- ✓ `3.6.2[a]` incidents are tracked.  
  *policy · POL-IR:* Incident Response policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.6.2[b]` incidents are documented.  
  *policy · POL-IR:* Incident Response policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.6.2[c]` authorities to whom incidents are to be reported are identified.  
  *policy · POL-IR:* Incident Response policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.6.2[d]` organizational officials to whom incidents are to be reported are identified.  
  *policy · POL-IR:* Incident Response policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.6.2[e]` identified authorities are notified of incidents.  
  *policy · POL-IR:* Incident Response policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.6.2[f]` identified organizational officials are notified of incidents.  
  *policy · POL-IR:* Incident Response policy, approved 2026-03-02 by Dana Whitlock

#### IR.L2-3.6.3: Test the organizational incident response capability.

**Status:** NOT MET · value 1 point(s) · **1 deducted**

Implementation: governed by policy POL-IR §3.6.3; practice verified as below.

- ✗ `3.6.3[a]` the incident response capability is tested.  
  *record · R-IR-TABLETOP:* Incident response tabletop: ransomware on a CAM workstation: last done 2025-09-30, 380 days ago (limit 365)

### Maintenance

#### MA.L2-3.7.1: Perform maintenance on organizational systems.[26].

**Status:** MET · value 3 point(s)

Implementation: governed by policy POL-MA §3.7.1; practice verified as below.

- ✓ `3.7.1[a]` system maintenance is performed.  
  *policy · POL-MA:* Maintenance policy, approved 2026-03-02 by Dana Whitlock

#### MA.L2-3.7.2: Provide controls on the tools, techniques, mechanisms, and personnel used to conduct system maintenance.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-MA §3.7.2; practice verified as below.

- ✓ `3.7.2[a]` tools used to conduct system maintenance are controlled.  
  *policy · POL-MA:* Maintenance policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.7.2[b]` techniques used to conduct system maintenance are controlled.  
  *policy · POL-MA:* Maintenance policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.7.2[c]` mechanisms used to conduct system maintenance are controlled.  
  *policy · POL-MA:* Maintenance policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.7.2[d]` personnel used to conduct system maintenance are controlled.  
  *policy · POL-MA:* Maintenance policy, approved 2026-03-02 by Dana Whitlock

#### MA.L2-3.7.3: Ensure equipment removed for off-site maintenance is sanitized of any CUI.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-MA §3.7.3; practice verified as below.

- ✓ `3.7.3[a]` equipment to be removed from organizational spaces for off-site maintenance is sanitized of any CUI.  
  *policy · POL-MA:* Maintenance policy, approved 2026-03-02 by Dana Whitlock

#### MA.L2-3.7.4: Check media containing diagnostic and test programs for malicious code before the media are used in organizational systems.

**Status:** MET · value 3 point(s)

Implementation: governed by policy POL-MA §3.7.4; practice verified as below.

- ✓ `3.7.4[a]` media containing diagnostic and test programs are checked for malicious code before being used in organizational systems that process, store, or transmit CUI.  
  *policy · POL-MA:* Maintenance policy, approved 2026-03-02 by Dana Whitlock

#### MA.L2-3.7.5: Require multifactor authentication to establish nonlocal maintenance sessions via external network connections and terminate such connections when nonlocal maintenance is complete.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-MA §3.7.5; practice verified as below.

- ✓ `3.7.5[a]` multifactor authentication is required to establish nonlocal maintenance sessions via external network connections.  
  *policy · POL-MA:* Maintenance policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.7.5[b]` nonlocal maintenance sessions established via external network connections are terminated when nonlocal maintenance is complete.  
  *policy · POL-MA:* Maintenance policy, approved 2026-03-02 by Dana Whitlock

#### MA.L2-3.7.6: Supervise the maintenance activities of maintenance personnel without required access authorization.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-MA §3.7.6; practice verified as below.

- ✓ `3.7.6[a]` maintenance personnel without required access authorization are supervised during maintenance activities.  
  *policy · POL-MA:* Maintenance policy, approved 2026-03-02 by Dana Whitlock

### Media Protection

#### MP.L2-3.8.1: Protect (i.e., physically control and securely store) system media containing CUI, both paper and digital.

**Status:** MET · value 3 point(s)

Implementation: governed by policy POL-MP §3.8.1; practice verified as below.

- ✓ `3.8.1[a]` paper media containing CUI is physically controlled.  
  *policy · POL-MP:* Media Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.8.1[b]` digital media containing CUI is physically controlled.  
  *policy · POL-MP:* Media Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.8.1[c]` paper media containing CUI is securely stored.  
  *policy · POL-MP:* Media Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.8.1[d]` digital media containing CUI is securely stored.  
  *policy · POL-MP:* Media Protection policy, approved 2026-03-02 by Dana Whitlock

#### MP.L2-3.8.2: Limit access to CUI on system media to authorized users

**Status:** MET · value 3 point(s)

Implementation: governed by policy POL-MP §3.8.2; practice verified as below.

- ✓ `3.8.2[a]` access to CUI on system media is limited to authorized users.  
  *policy · POL-MP:* Media Protection policy, approved 2026-03-02 by Dana Whitlock

#### MP.L2-3.8.3: Sanitize or destroy system media containing CUI before disposal or release for reuse.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-MP §3.8.3; practice verified as below.

- ✓ `3.8.3[a]` system media containing CUI is sanitized or destroyed before disposal.  
  *record · R-MP-SANITIZE:* Media sanitization certificates for retired drives (2026-04-22, 176 days old)
- ✓ `3.8.3[b]` system media containing CUI is sanitized before it is released for reuse.  
  *record · R-MP-SANITIZE:* Media sanitization certificates for retired drives (2026-04-22, 176 days old)

#### MP.L2-3.8.4: Mark media with necessary CUI markings and distribution limitations.[27]

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-MP §3.8.4; practice verified as below.

- ✓ `3.8.4[a]` media containing CUI is marked with applicable CUI markings.  
  *policy · POL-MP:* Media Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.8.4[b]` media containing CUI is marked with distribution limitations.  
  *policy · POL-MP:* Media Protection policy, approved 2026-03-02 by Dana Whitlock

#### MP.L2-3.8.5: Control access to media containing CUI and maintain accountability for media during transport outside of controlled areas.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-MP §3.8.5; practice verified as below.

- ✓ `3.8.5[a]` access to media containing CUI is controlled.  
  *policy · POL-MP:* Media Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.8.5[b]` accountability for media containing CUI is maintained during transport outside of controlled areas.  
  *policy · POL-MP:* Media Protection policy, approved 2026-03-02 by Dana Whitlock

#### MP.L2-3.8.6: Implement cryptographic mechanisms to protect the confidentiality of CUI stored on digital media during transport unless otherwise protected by alternative physical safeguards.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-MP §3.8.6; practice verified as below.

- ✓ `3.8.6[a]` the confidentiality of CUI stored on digital media is protected during transport using cryptographic mechanisms or alternative physical safeguards.  
  *policy · POL-MP:* Media Protection policy, approved 2026-03-02 by Dana Whitlock

#### MP.L2-3.8.7: Control the use of removable media on system components.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-MP §3.8.7; practice verified as below.

- ✓ `3.8.7[a]` the use of removable media on system components containing CUI is controlled.  
  *automated · entra-policies:* removable storage write-blocked

#### MP.L2-3.8.8: Prohibit the use of portable storage devices when such devices have no identifiable owner.

**Status:** MET · value 3 point(s)

Implementation: governed by policy POL-MP §3.8.8; practice verified as below.

- ✓ `3.8.8[a]` the use of portable storage devices is prohibited when such devices have no identifiable owner.  
  *policy · POL-MP:* Media Protection policy, approved 2026-03-02 by Dana Whitlock

#### MP.L2-3.8.9: Protect the confidentiality of backup CUI at storage locations.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-MP §3.8.9; practice verified as below.

- ✓ `3.8.9[a]` the confidentiality of backup CUI is protected at storage locations.  
  *policy · POL-MP:* Media Protection policy, approved 2026-03-02 by Dana Whitlock

### Personnel Security

#### PS.L2-3.9.1: Screen individuals prior to authorizing access to organizational systems containing CUI.

**Status:** MET · value 3 point(s)

Implementation: governed by policy POL-PS §3.9.1; practice verified as below.

- ✓ `3.9.1[a]` individuals are screened prior to authorizing access to organizational systems.  
  *record · R-PS-SCREEN:* Pre-access screening register (background checks), reviewed quarterly (2026-07-01, 106 days old)

#### PS.L2-3.9.2: Ensure that organizational systems containing CUI are protected during and after personnel actions such as terminations and transfers

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-PS §3.9.2; practice verified as below.

- ✓ `3.9.2[a]` a policy and/or process for terminating system access authorization and any credentials coincident with personnel actions is established.  
  *policy · POL-PS:* Personnel Security policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.9.2[b]` system access and credentials are terminated consistent with personnel actions such as termination or transfer.  
  *automated · entra-identity:* no enabled accounts for departed staff
- ✓ `3.9.2[c]` the system is protected during and after personnel transfer actions.  
  *policy · POL-PS:* Personnel Security policy, approved 2026-03-02 by Dana Whitlock

### Physical Protection

#### PE.L2-3.10.1: Limit physical access to organizational systems, equipment, and the respective operating environments to authorized individuals.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-PE §3.10.1; practice verified as below.

- ✓ `3.10.1[a]` authorized individuals allowed physical access are identified.  
  *record · R-PE-WALK:* Facility walkthrough: locked server closet, camera coverage, badge readers, alarm panel (2026-07-20, 87 days old)
- ✓ `3.10.1[b]` physical access to organizational systems is limited to authorized individuals.  
  *record · R-PE-WALK:* Facility walkthrough: locked server closet, camera coverage, badge readers, alarm panel (2026-07-20, 87 days old)
- ✓ `3.10.1[c]` physical access to equipment is limited to authorized individuals.  
  *record · R-PE-WALK:* Facility walkthrough: locked server closet, camera coverage, badge readers, alarm panel (2026-07-20, 87 days old)
- ✓ `3.10.1[d]` physical access to operating environments is limited to authorized individuals.  
  *record · R-PE-WALK:* Facility walkthrough: locked server closet, camera coverage, badge readers, alarm panel (2026-07-20, 87 days old)

#### PE.L2-3.10.2: Protect and monitor the physical facility and support infrastructure for organizational systems.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-PE §3.10.2; practice verified as below.

- ✓ `3.10.2[a]` the physical facility where that system resides is protected.  
  *record · R-PE-WALK:* Facility walkthrough: locked server closet, camera coverage, badge readers, alarm panel (2026-07-20, 87 days old)
- ✓ `3.10.2[b]` the support infrastructure for that system is protected.  
  *record · R-PE-WALK:* Facility walkthrough: locked server closet, camera coverage, badge readers, alarm panel (2026-07-20, 87 days old)
- ✓ `3.10.2[c]` the physical facility where that system resides is monitored.  
  *record · R-PE-WALK:* Facility walkthrough: locked server closet, camera coverage, badge readers, alarm panel (2026-07-20, 87 days old)
- ✓ `3.10.2[d]` the support infrastructure for that system is monitored.  
  *record · R-PE-WALK:* Facility walkthrough: locked server closet, camera coverage, badge readers, alarm panel (2026-07-20, 87 days old)

#### PE.L2-3.10.3: Escort visitors and monitor visitor activity.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-PE §3.10.3; practice verified as below.

- ✓ `3.10.3[a]` visitors are escorted.  
  *record · visitor-log:* 6 visits, every one with a named escort
- ✓ `3.10.3[b]` visitor activity is monitored.  
  *record · visitor-log:* visits logged with purpose and badge return

#### PE.L2-3.10.4: Maintain audit logs of physical access.

**Status:** NOT MET · value 1 point(s) · **1 deducted**

Implementation: governed by policy POL-PE §3.10.4; practice verified as below.

- ✗ `3.10.4[a]` audit logs of physical access are maintained.  
  *record · visitor-log:* visitor log last uploaded page ends 2026-09-12 (33 days ago)

#### PE.L2-3.10.5: Control and manage physical access devices.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-PE §3.10.5; practice verified as below.

- ✓ `3.10.5[a]` physical access devices are identified.  
  *record · R-PE-WALK:* Facility walkthrough: locked server closet, camera coverage, badge readers, alarm panel (2026-07-20, 87 days old)
- ✓ `3.10.5[b]` physical access devices are controlled.  
  *record · R-PE-WALK:* Facility walkthrough: locked server closet, camera coverage, badge readers, alarm panel (2026-07-20, 87 days old)
- ✓ `3.10.5[c]` physical access devices are managed.  
  *record · R-PE-WALK:* Facility walkthrough: locked server closet, camera coverage, badge readers, alarm panel (2026-07-20, 87 days old)

#### PE.L2-3.10.6: Enforce safeguarding measures for CUI at alternate work sites.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-PE §3.10.6; practice verified as below.

- ✓ `3.10.6[a]` safeguarding measures for CUI are defined for alternate work sites.  
  *policy · POL-PE:* Physical Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.10.6[b]` safeguarding measures for CUI are enforced for alternate work sites.  
  *policy · POL-PE:* Physical Protection policy, approved 2026-03-02 by Dana Whitlock

### Risk Assessment

#### RA.L2-3.11.1: Periodically assess the risk to organizational operations (including mission, functions, image, or reputation), organizational assets, and individuals, resulting from the operation of organizational systems and the associated processing, storage, or transmission of CUI

**Status:** MET · value 3 point(s)

Implementation: governed by policy POL-RA §3.11.1; practice verified as below.

- ✓ `3.11.1[a]` the frequency to assess risk to organizational operations, organizational assets, and individuals is defined.  
  *record · R-RA-RISK:* Annual risk assessment, signed (2026-05-01, 167 days old)
- ✓ `3.11.1[b]` risk to organizational operations, organizational assets, and individuals resulting from the operation of an organizational system that processes, stores, or transmits CUI is assessed with the defined frequency.  
  *record · R-RA-RISK:* Annual risk assessment, signed (2026-05-01, 167 days old)

#### RA.L2-3.11.2: Scan for vulnerabilities in organizational systems and applications periodically and when new vulnerabilities affecting those systems and applications are identified.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-RA §3.11.2; practice verified as below.

- ✓ `3.11.2[a]` the frequency to scan for vulnerabilities in an organizational system and its applications that process, store, or transmit CUI is defined.  
  *automated · defender-vulns:* scan every 7 days
- ✓ `3.11.2[b]` vulnerability scans are performed in an organizational system that processes, stores, or transmits CUI with the defined frequency.  
  *automated · defender-vulns:* last full scan 3 days ago (every 7 days)
- ✓ `3.11.2[c]` vulnerability scans are performed in an application that contains CUI with the defined frequency.  
  *automated · defender-vulns:* last full scan 3 days ago (every 7 days)
- ✓ `3.11.2[d]` vulnerability scans are performed in an organizational system that processes, stores, or transmits CUI when new vulnerabilities are identified.  
  *automated · defender-vulns:* last full scan 3 days ago (every 7 days)
- ✓ `3.11.2[e]` vulnerability scans are performed in an application that contains CUI when new vulnerabilities are identified.  
  *automated · defender-vulns:* last full scan 3 days ago (every 7 days)

#### RA.L2-3.11.3: Remediate vulnerabilities in accordance with risk assessments.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-RA §3.11.3; practice verified as below.

- ✓ `3.11.3[a]` vulnerabilities are identified.  
  *automated · defender-vulns:* 2 findings tracked
- ✓ `3.11.3[b]` vulnerabilities are remediated in accordance with risk assessments.  
  *automated · defender-vulns:* 2 open finding(s), none past the remediation deadline

### Security Assessment

#### CA.L2-3.12.1: Periodically assess the security controls in organizational systems to determine if the controls are effective in their application.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-CA §3.12.1; practice verified as below.

- ✓ `3.12.1[a]` the frequency of security control assessments is defined.  
  *record · R-CA-SELF:* Annual self-assessment of all 110 requirements, signed (2026-06-15, 122 days old)
- ✓ `3.12.1[b]` security controls are assessed with the defined frequency to determine if the controls are effective in their application.  
  *record · R-CA-SELF:* Annual self-assessment of all 110 requirements, signed (2026-06-15, 122 days old)

#### CA.L2-3.12.2: Develop and implement plans of action designed to correct deficiencies and reduce or eliminate vulnerabilities in organizational systems.

**Status:** MET · value 3 point(s)

Implementation: governed by policy POL-CA §3.12.2; practice verified as below.

- ✓ `3.12.2[a]` deficiencies and vulnerabilities to be addressed by the plan of action are identified.  
  *policy · POL-CA:* Security Assessment policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.12.2[b]` a plan of action is developed to correct identified deficiencies and reduce or eliminate identified vulnerabilities.  
  *policy · POL-CA:* Security Assessment policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.12.2[c]` the plan of action is implemented to correct identified deficiencies and reduce or eliminate identified vulnerabilities.  
  *policy · POL-CA:* Security Assessment policy, approved 2026-03-02 by Dana Whitlock

#### CA.L2-3.12.3: Monitor security controls on an ongoing basis to ensure the continued effectiveness of the controls.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-CA §3.12.3; practice verified as below.

- ✓ `3.12.3[a]` security controls are monitored on an ongoing basis to ensure the continued effectiveness of those controls.  
  *policy · POL-CA:* Security Assessment policy, approved 2026-03-02 by Dana Whitlock

#### CA.L2-3.12.4: Develop, document, and periodically update system security plans that describe system boundaries, system environments of operation, how security requirements are implemented, and the relationships with or connections to other systems.[28]

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-CA §3.12.4; practice verified as below.

- ✓ `3.12.4[a]` a system security plan is developed.  
  *generated · ssp:* SSP generated from this bundle
- ✓ `3.12.4[b]` the system boundary is described and documented in the system security plan.  
  *generated · ssp:* SSP generated from this bundle
- ✓ `3.12.4[c]` the system environment of operation is described and documented in the system security plan.  
  *generated · ssp:* SSP generated from this bundle
- ✓ `3.12.4[d]` the security requirements identified and approved by the designated authority as non-applicable are identified.  
  *generated · ssp:* SSP generated from this bundle
- ✓ `3.12.4[e]` the method of security requirement implementation is described and documented in the system security plan.  
  *generated · ssp:* SSP generated from this bundle
- ✓ `3.12.4[f]` the relationship with or connection to other systems is described and documented in the system security plan.  
  *generated · ssp:* SSP generated from this bundle
- ✓ `3.12.4[g]` the frequency to update the system security plan is defined.  
  *generated · ssp:* SSP generated from this bundle
- ✓ `3.12.4[h]` system security plan is updated with the defined frequency.  
  *generated · ssp:* SSP generated from this bundle

### System and Communications Protection

#### SC.L2-3.13.1: Monitor, control, and protect communications (i.e., information transmitted or received by organizational systems) at the external boundaries and key internal boundaries of organizational systems.

**Status:** NOT MET · value 5 point(s) · **5 deducted**

Implementation: governed by policy POL-SC §3.13.1; practice verified as below.

- ✓ `3.13.1[a]` the external system boundary is defined.  
  *automated · firewall:* external boundary: fw-01
- ✓ `3.13.1[b]` key internal system boundaries are defined.  
  *automated · firewall:* internal zones: enclave, lan, shopfloor, dmz-proxy
- ✗ `3.13.1[c]` communications are monitored at the external system boundary.  
  *automated · firewall:* accept rules not logged: rule 9
- ✗ `3.13.1[d]` communications are monitored at key internal boundaries.  
  *automated · firewall:* accept rules not logged: rule 9
- ✗ `3.13.1[e]` communications are controlled at the external system boundary.  
  *automated · firewall:* internet-exposed internal host: rule 9 "TEMP vendor RDP - remove after visit" (RDP from anywhere to 10.20.0.15)
- ✗ `3.13.1[f]` communications are controlled at key internal boundaries.  
  *automated · firewall:* internet-exposed internal host: rule 9 "TEMP vendor RDP - remove after visit" (RDP from anywhere to 10.20.0.15)
- ✓ `3.13.1[g]` communications are protected at the external system boundary.  
  *automated · firewall:* VPN in FIPS mode (TLS1.3 AES-256-GCM)
- ✓ `3.13.1[h]` communications are protected at key internal boundaries.  
  *automated · firewall:* VPN in FIPS mode (TLS1.3 AES-256-GCM)

#### SC.L2-3.13.2: Employ architectural designs, software development techniques, and systems engineering principles that promote effective information security within organizational systems.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-SC §3.13.2; practice verified as below.

- ✓ `3.13.2[a]` architectural designs that promote effective information security are identified.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.13.2[b]` software development techniques that promote effective information security are identified.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.13.2[c]` systems engineering principles that promote effective information security are identified.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.13.2[d]` identified architectural designs that promote effective information security are employed.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.13.2[e]` identified software development techniques that promote effective information security are employed.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.13.2[f]` identified systems engineering principles that promote effective information security are employed.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock

#### SC.L2-3.13.3: Separate user functionality from system management functionality.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-SC §3.13.3; practice verified as below.

- ✓ `3.13.3[a]` user functionality is identified.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.13.3[b]` system management functionality is identified.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.13.3[c]` user functionality is separated from system management functionality.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock

#### SC.L2-3.13.4: Prevent unauthorized and unintended information transfer via shared system resources.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-SC §3.13.4; practice verified as below.

- ✓ `3.13.4[a]` unauthorized and unintended information transfer via shared system resources is prevented.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock

#### SC.L2-3.13.5: Implement subnetworks for publicly accessible system components that are physically or logically separated from internal networks.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-SC §3.13.5; practice verified as below.

- ✓ `3.13.5[a]` publicly accessible system components are identified.  
  *automated · firewall:* public component: dmz-proxy
- ✓ `3.13.5[b]` subnetworks for publicly accessible system components are physically or logically separated from internal networks.  
  *automated · firewall:* public services only in the DMZ subnet

#### SC.L2-3.13.6: Deny network communications traffic by default and allow network communications traffic by exception (i.e., deny all, permit by exception).

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-SC §3.13.6; practice verified as below.

- ✓ `3.13.6[a]` network communications traffic is denied by default.  
  *automated · firewall:* implicit deny-all
- ✓ `3.13.6[b]` network communications traffic is allowed by exception.  
  *automated · firewall:* every accept rule names its services

#### SC.L2-3.13.7: Prevent remote devices from simultaneously establishing non-remote connections with organizational systems and communicating via some other connection to resources in external networks (i.e., split tunneling).

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-SC §3.13.7; practice verified as below.

- ✓ `3.13.7[a]` remote devices are prevented from simultaneously establishing non-remote connections with the system and communicating via some other connection to resources in external networks (i.e., split tunneling).  
  *automated · firewall:* split tunneling disabled

#### SC.L2-3.13.8: Implement cryptographic mechanisms to prevent unauthorized disclosure of CUI during transmission unless otherwise protected by alternative physical safeguards.

**Status:** MET · value 3 point(s)

Implementation: governed by policy POL-SC §3.13.8; practice verified as below.

- ✓ `3.13.8[a]` cryptographic mechanisms intended to prevent unauthorized disclosure of CUI are identified.  
  *automated · firewall:* TLS 1.3 for CUI in transit
- ✓ `3.13.8[b]` alternative physical safeguards intended to prevent unauthorized disclosure of CUI are identified.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.13.8[c]` either cryptographic mechanisms or alternative physical safeguards are implemented to prevent unauthorized disclosure of CUI during transmission.  
  *automated · firewall:* VPN in FIPS mode (TLS1.3 AES-256-GCM)

#### SC.L2-3.13.9: Terminate network connections associated with communications sessions at the end of the sessions or after a defined period of inactivity.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-SC §3.13.9; practice verified as below.

- ✓ `3.13.9[a]` a period of inactivity to terminate network connections associated with communications sessions is defined.  
  *automated · firewall:* VPN idle timeout 30 min
- ✓ `3.13.9[b]` network connections associated with communications sessions are terminated at the end of the sessions.  
  *automated · firewall:* sessions closed at logoff
- ✓ `3.13.9[c]` network connections associated with communications sessions are terminated after the defined period of inactivity.  
  *automated · firewall:* idle sessions dropped

#### SC.L2-3.13.10: Establish and manage cryptographic keys for cryptography employed in organizational systems.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-SC §3.13.10; practice verified as below.

- ✓ `3.13.10[a]` cryptographic keys are established whenever cryptography is employed.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.13.10[b]` cryptographic keys are managed whenever cryptography is employed.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock

#### SC.L2-3.13.11: Employ FIPS-validated cryptography when used to protect the confidentiality of CUI.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-SC §3.13.11; practice verified as below.

- ✓ `3.13.11[a]` FIPS-validated cryptography is employed to protect the confidentiality of CUI.  
  *automated · intune-devices:* BitLocker with FIPS algorithm policy on every device; VPN in FIPS mode

#### SC.L2-3.13.12: Prohibit remote activation of collaborative computing devices and provide indication of devices in use to users present at the device.[29].

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-SC §3.13.12; practice verified as below.

- ✓ `3.13.12[a]` collaborative computing devices are identified.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.13.12[b]` collaborative computing devices provide indication to users of devices in use.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.13.12[c]` remote activation of collaborative computing devices is prohibited.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock

#### SC.L2-3.13.13: Control and monitor the use of mobile code.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-SC §3.13.13; practice verified as below.

- ✓ `3.13.13[a]` use of mobile code is controlled.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.13.13[b]` use of mobile code is monitored.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock

#### SC.L2-3.13.14: Control and monitor the use of Voice over Internet Protocol (VoIP) technologies.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-SC §3.13.14; practice verified as below.

- ✓ `3.13.14[a]` use of Voice over Internet Protocol (VoIP) technologies is controlled.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.13.14[b]` use of Voice over Internet Protocol (VoIP) technologies is monitored.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock

#### SC.L2-3.13.15: Protect the authenticity of communications sessions.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-SC §3.13.15; practice verified as below.

- ✓ `3.13.15[a]` the authenticity of communications sessions is protected.  
  *policy · POL-SC:* System and Communications Protection policy, approved 2026-03-02 by Dana Whitlock

#### SC.L2-3.13.16: Protect the confidentiality of CUI at rest.

**Status:** MET · value 1 point(s)

Implementation: governed by policy POL-SC §3.13.16; practice verified as below.

- ✓ `3.13.16[a]` the confidentiality of CUI at rest is protected.  
  *automated · intune-devices:* BitLocker on every laptop

### System and Information Integrity

#### SI.L2-3.14.1: Identify, report, and correct system flaws in a timely manner.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-SI §3.14.1; practice verified as below.

- ✓ `3.14.1[a]` the time within which to identify system flaws is specified.  
  *automated · defender-vulns:* 2 open finding(s), none past the remediation deadline
- ✓ `3.14.1[b]` system flaws are identified within the specified time frame.  
  *automated · defender-vulns:* 2 open finding(s), none past the remediation deadline
- ✓ `3.14.1[c]` the time within which to report system flaws is specified.  
  *automated · defender-vulns:* 2 open finding(s), none past the remediation deadline
- ✓ `3.14.1[d]` system flaws are reported within the specified time frame.  
  *automated · defender-vulns:* 2 open finding(s), none past the remediation deadline
- ✓ `3.14.1[e]` the time within which to correct system flaws is specified.  
  *automated · defender-vulns:* 2 open finding(s), none past the remediation deadline
- ✓ `3.14.1[f]` system flaws are corrected within the specified time frame.  
  *automated · defender-vulns:* 2 open finding(s), none past the remediation deadline

#### SI.L2-3.14.2: Provide protection from malicious code at designated locations within organizational systems.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-SI §3.14.2; practice verified as below.

- ✓ `3.14.2[a]` designated locations for malicious code protection are identified.  
  *automated · intune-devices:* Defender real-time protection on all 16 devices
- ✓ `3.14.2[b]` protection from malicious code at designated locations is provided.  
  *automated · intune-devices:* Defender real-time protection on all 16 devices

#### SI.L2-3.14.3: Monitor system security alerts and advisories and take action in response.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-SI §3.14.3; practice verified as below.

- ✓ `3.14.3[a]` response actions to system security alerts and advisories are identified.  
  *policy · POL-SI:* System and Information Integrity policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.14.3[b]` system security alerts and advisories are monitored.  
  *policy · POL-SI:* System and Information Integrity policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.14.3[c]` actions in response to system security alerts and advisories are taken.  
  *policy · POL-SI:* System and Information Integrity policy, approved 2026-03-02 by Dana Whitlock

#### SI.L2-3.14.4: Update malicious code protection mechanisms when new releases are available.

**Status:** NOT MET · value 5 point(s) · **5 deducted**

Implementation: governed by policy POL-SI §3.14.4; practice verified as below.

- ✗ `3.14.4[a]` malicious code protection mechanisms are updated when new releases are available.  
  *automated · intune-devices:* signatures out of date on SRP-LT06 (13 days), SRP-LT07 (13 days)

#### SI.L2-3.14.5: Perform periodic scans of organizational systems and real-time scans of files from external sources as files are downloaded, opened, or executed.

**Status:** MET · value 3 point(s)

Implementation: governed by policy POL-SI §3.14.5; practice verified as below.

- ✓ `3.14.5[a]` the frequency for malicious code scans is defined.  
  *automated · defender-vulns:* last full scan 3 days ago (every 7 days)
- ✓ `3.14.5[b]` malicious code scans are performed with the defined frequency.  
  *automated · defender-vulns:* last full scan 3 days ago (every 7 days)
- ✓ `3.14.5[c]` real-time malicious code scans of files from external sources as files are downloaded, opened, or executed are performed.  
  *automated · defender-vulns:* last full scan 3 days ago (every 7 days)

#### SI.L2-3.14.6: Monitor organizational systems, including inbound and outbound communications traffic, to detect attacks and indicators of potential attacks.

**Status:** MET · value 5 point(s)

Implementation: governed by policy POL-SI §3.14.6; practice verified as below.

- ✓ `3.14.6[a]` the system is monitored to detect attacks and indicators of potential attacks.  
  *policy · POL-SI:* System and Information Integrity policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.14.6[b]` inbound communications traffic is monitored to detect attacks and indicators of potential attacks.  
  *policy · POL-SI:* System and Information Integrity policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.14.6[c]` outbound communications traffic is monitored to detect attacks and indicators of potential attacks.  
  *policy · POL-SI:* System and Information Integrity policy, approved 2026-03-02 by Dana Whitlock

#### SI.L2-3.14.7: Identify unauthorized use of organizational systems.

**Status:** MET · value 3 point(s)

Implementation: governed by policy POL-SI §3.14.7; practice verified as below.

- ✓ `3.14.7[a]` authorized use of the system is defined.  
  *policy · POL-SI:* System and Information Integrity policy, approved 2026-03-02 by Dana Whitlock
- ✓ `3.14.7[b]` unauthorized use of the system is identified.  
  *policy · POL-SI:* System and Information Integrity policy, approved 2026-03-02 by Dana Whitlock

## Evidence manifest

| File | Kind | Dated | sha256 |
|---|---|---|---|
| gaps.yaml | plan | 2026-10-15 | `e1e4cc75be0b` |
| policies/AC.md | policy | 2026-03-02 | `6f4a3ef4b3b0` |
| policies/AT.md | policy | 2026-03-02 | `a7d727856531` |
| policies/AU.md | policy | 2026-03-02 | `550b07ec7fdf` |
| policies/CA.md | policy | 2026-03-02 | `f4b6a50bb71a` |
| policies/CM.md | policy | 2026-03-02 | `368c4daf34b7` |
| policies/IA.md | policy | 2026-03-02 | `4c624f4e23c9` |
| policies/IR.md | policy | 2026-03-02 | `a4fdf84ccf2d` |
| policies/MA.md | policy | 2026-03-02 | `814471a85569` |
| policies/MP.md | policy | 2026-03-02 | `fd37de33ad6d` |
| policies/PE.md | policy | 2026-03-02 | `b0eb4e4b7772` |
| policies/PS.md | policy | 2026-03-02 | `5505ff201d65` |
| policies/RA.md | policy | 2026-03-02 | `0220be839567` |
| policies/SC.md | policy | 2026-03-02 | `1c8bf81054f0` |
| policies/SI.md | policy | 2026-03-02 | `dd61876ae06f` |
| records/R-CA-SELF.md | record | 2026-06-15 | `f0c8a719fb39` |
| records/R-IR-TABLETOP.md | record | 2025-09-30 | `3850d72dff02` |
| records/R-MP-SANITIZE.md | record | 2026-04-22 | `fc57dc118d39` |
| records/R-PE-WALK.md | record | 2026-07-20 | `65bae76961b7` |
| records/R-PS-SCREEN.md | record | 2026-07-01 | `f685b32a4dad` |
| records/R-RA-RISK.md | record | 2026-05-01 | `8abab8636a94` |
| snapshots/2026-10-15/asset_inventory.csv | automated | 2026-10-15 | `6a96749ddd5c` |
| snapshots/2026-10-15/audit_config.json | automated | 2026-10-15 | `0fba50ea6028` |
| snapshots/2026-10-15/badge_access.csv | record | 2026-10-15 | `9d7ac51c682a` |
| snapshots/2026-10-15/defender_vulns.json | automated | 2026-10-15 | `4fa74a685cfd` |
| snapshots/2026-10-15/entra_policies.json | automated | 2026-10-15 | `88139bb4a9b7` |
| snapshots/2026-10-15/entra_users.json | automated | 2026-10-15 | `5330a6cb3bf3` |
| snapshots/2026-10-15/firewall.json | automated | 2026-10-15 | `6c29c26a336b` |
| snapshots/2026-10-15/hr_roster.csv | automated | 2026-10-15 | `bc516a97316b` |
| snapshots/2026-10-15/intune_devices.json | automated | 2026-10-15 | `69b110bd9013` |
| snapshots/2026-10-15/training.csv | automated | 2026-10-15 | `c0833ebc2787` |
| snapshots/2026-10-15/visitor_log.csv | record | 2026-10-15 | `83a43dd952ad` |
