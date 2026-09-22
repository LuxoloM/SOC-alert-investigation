# Incident Response

## Severity

**Medium**

## Severity Rationale

The incident contains several indicators that require investigation:

- Five consecutive failed authentication attempts.
- A successful authentication from the same source IP.
- A VPN connection was established.
- A sensitive payroll document was accessed.
- The payroll document was downloaded twice.

However, the available evidence does not currently confirm that the
account was compromised or that data was maliciously exfiltrated.

The incident is therefore classified as Medium pending further
investigation.

## Recommended Response

### Immediate Actions

1. Escalate the alert for further investigation.
2. Verify the activity with the affected user.
3. Review the user's authentication history.
4. Investigate the source IP address.
5. Review additional file-access and download activity.
6. Check whether other sensitive resources were accessed.

### If Account Compromise Is Confirmed

The incident-response team should consider:

- Resetting the user's credentials.
- Revoking active sessions.
- Temporarily disabling the affected account.
- Blocking confirmed malicious infrastructure.
- Preserving relevant logs and evidence.
- Investigating potential data exposure.

## Current Status

**Open - Further Investigation Required**

The available evidence indicates potentially suspicious activity but is
not sufficient to confirm account compromise.
