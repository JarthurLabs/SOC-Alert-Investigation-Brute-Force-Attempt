# SIEM Query Examples

These are generic SIEM-style examples for defensive log review.

## Repeated Failed Logins

```text
event_id=4625
| stats count by user, source_ip
| where count >= 5
```

## Failed Logins Followed by Success

```text
(event_id=4625 OR event_id=4624)
| transaction user, source_ip maxspan=15m
| search event_id=4625 event_id=4624
```

## Tuning Notes

- Exclude known password reset windows.
- Review VPN and remote access context.
- Correlate with MFA logs when available.
- Alert on success after repeated failures.
