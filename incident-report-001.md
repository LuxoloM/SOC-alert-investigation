# Incident Report 001 — Suspicious VPN and Confidential File Download

## 1. Incident Summary

A user account showed multiple failed authentication attempts followed by a successful VPN connection. The account then accessed the Finance folder and downloaded a confidential employee salary file.

## 2. Evidence

- Source IP: 10.20.14.27
- User Account: j.smith
- File Accessed: /Finance/Payroll/Employee_Salaries.xlsx
- Activity: Multiple failed authentication attempts followed by confidential file download

## 3. Indicators of Suspicious Activity

- Multiple failed authentication attempts
- Successful VPN authentication afterward
- Access to a sensitive Finance/Payroll directory
- Download of a confidential employee salary spreadsheet

## 4. Initial Assessment

The sequence of authentication failures followed by successful VPN access and downloading a confidential payroll file requires investigation.

At this stage, there is insufficient evidence to confirm whether the activity was malicious or authorized.

## 5. Recommended Investigation

1. Verify whether the user account owner initiated the VPN connection.
2. Review VPN authentication logs.
3. Review endpoint/device information associated with the source IP.
4. Check whether the account accessed other sensitive files.
5. Review the timing and frequency of the failed authentication attempts.
6. Check for additional suspicious activity associated with the account or IP address.

## 6. Recommended Response

If unauthorized activity is confirmed:

- Disable or temporarily lock the affected account.
- Revoke active VPN sessions.
- Reset the user's credentials.
- Investigate the endpoint associated with the source IP.
- Preserve relevant authentication, VPN and file-access logs.
- Escalate the incident according to the organization's incident-response procedure.

## 7. MITRE ATT&CK Mapping

Potential techniques to investigate:

- T1078 — Valid Accounts
- T1110 — Brute Force
- T1213 — Data from Information Repositories

These mappings are preliminary and should be confirmed after further investigation.

## 8. Analyst Conclusion

The available evidence indicates potentially suspicious account activity involving VPN authentication and access to confidential payroll data. Further log and endpoint investigation is required before determining whether the activity represents a security incident.
