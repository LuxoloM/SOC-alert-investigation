# Security Incident Investigation Report

## Incident Information

| Field              | Details                                 |
|--------------------|-----------------------------------------|
| Incident ID        | SOC-2026-001                            |
| Incident Type      | Suspicious Authentication Activity      |
| Severity           | Medium                                  |
| Status             | Open - Further Investigation Required   |
| Affected Account   | j.smith                                 |
| Source IP          | 185.XXX.XXX.42                          |
| Destination        | Corporate VPN                           |
| Sensitive Resource | /Finance/Payroll/Employee_Salaries.xlsx |

---

## 1. Executive Summary

A security alert was generated after multiple failed authentication
attempts were detected against the user account `j.smith`.

Five failed authentication attempts occurred from the same source IP
address, followed by a successful authentication.

After authentication, the account established a VPN connection and
accessed a sensitive payroll document. The document was subsequently
downloaded twice.

The available evidence indicates potentially suspicious activity.
However, the evidence currently available is not sufficient to confirm
that the account was compromised.

---

## 2. Incident Timeline

| Time     | Event                         |
|----------|-------------------------------|
| 01:35:12 | Failed authentication         |
| 01:35:18 | Failed authentication         |
| 01:35:25 | Failed authentication         |
| 01:35:31 | Failed authentication         |
| 01:35:42 | Failed authentication         |
| 01:36:03 | Successful authentication     |
| 01:36:17 | VPN connection established    |
| 01:42:08 | Payroll file accessed         |
| 01:43:19 | Payroll file downloaded       |
| 01:44:02 | Payroll file downloaded again |
| 01:47:33 | VPN connection terminated     |

---

## 3. Indicators of Interest

### Source IP

`185.XXX.XXX.42`

This address should be investigated to determine whether it is known
and authorised.

### User Account

`j.smith`

The user's expected activity and historical authentication behaviour
should be reviewed.

### Sensitive File

`/Finance/Payroll/Employee_Salaries.xlsx`

The user's authorisation to access this file should be verified.

---

## 4. Investigation Findings

The investigation identified:

- Five failed authentication attempts.
- A successful authentication following the failed attempts.
- A VPN connection established after successful authentication.
- Access to a sensitive payroll document.
- Two downloads of the payroll document.

The sequence of events warrants further investigation.

---

## 5. Risk Assessment

The activity presents a potential security risk because a sensitive
payroll document was accessed and downloaded following unusual
authentication activity.

The current evidence does not establish whether the activity was
legitimate, accidental, or malicious.

Further evidence is required before confirming account compromise.

---

## 6. Recommended Response

The following actions are recommended:

1. Verify the activity with the affected user.
2. Review historical authentication activity.
3. Investigate the source IP address.
4. Review additional file-access and download logs.
5. Determine whether the user is authorised to access the payroll file.
6. Check whether other sensitive resources were accessed.
7. Escalate the incident if evidence of compromise or unauthorised
   access is identified.

---

## 7. Conclusion

The investigation identified potentially suspicious authentication and
data-access activity involving the `j.smith` account.

The combination of repeated failed authentication attempts, successful
VPN authentication, and subsequent access and downloads of a sensitive
payroll document justifies further investigation.

The incident remains classified as:

**Medium - Open / Further Investigation Required**

No conclusion of confirmed account compromise is made based solely on
the evidence currently available.

---

## Disclaimer

This is a simulated cybersecurity investigation created for educational
and portfolio purposes. No real user accounts, systems, IP addresses,
or confidential information were investigated.
