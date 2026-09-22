# Investigation Findings

## Initial Assessment

The investigation identified potentially suspicious authentication
and data-access activity involving the user account `j.smith`.

Five consecutive authentication failures were recorded from the same
source IP address, `185.XXX.XXX.42`, before a successful authentication
occurred.

Following the successful authentication, the account established a VPN
connection and accessed a sensitive payroll file.

The file:

`/Finance/Payroll/Employee_Salaries.xlsx`

was read and subsequently downloaded twice.

## Evidence Requiring Further Investigation

The following evidence should be reviewed:

1. Determine whether `185.XXX.XXX.42` is a known or authorised source
   IP address.

2. Determine whether the user `j.smith` was expected to access the
   corporate VPN at the time of the authentication.

3. Determine whether `j.smith` is authorised to access the payroll file.

4. Review whether the payroll file was transferred, uploaded, emailed,
   or accessed from another location after the downloads.

5. Review historical authentication activity for the account to
   establish whether this behaviour is consistent with the user's
   normal activity.

## Current Assessment

Based on the available evidence, the activity should be treated as
potentially suspicious and investigated further.

The available evidence alone is not sufficient to confirm that the
account was compromised.

## Recommended Next Steps

- Review authentication history for `j.smith`.
- Investigate the source IP address.
- Verify the user's activity and expected working hours.
- Review file-access and download logs.
- Check for additional suspicious activity involving the account.
- Escalate the incident if additional evidence indicates compromise
  or unauthorised data access.
