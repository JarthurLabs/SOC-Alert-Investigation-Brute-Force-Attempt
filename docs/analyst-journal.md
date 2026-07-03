# Analyst Journal

This investigation started with a common beginner trap: failed logins look exciting, but failed logins alone are not always a good alert.

## First pass

My first detection idea was simple:

> Alert when one user has three failed logins in ten minutes.

That technically works, but it catches normal behavior too easily. People mistype passwords, password managers break, VPN sessions expire, and Monday mornings exist.

## Correction

I changed the logic to care more about the full pattern:

- repeated failures
- same source
- same user
- successful login after the failures
- privileged or unusual activity after login

That made the case more useful because the alert was no longer just “someone failed login.” It became “someone failed several times, then got in, then something more sensitive happened.”

## Threshold I reconsidered

I originally treated the successful login as enough to call the account compromised. That was too strong. It could still be the real user after a password issue.

The better disposition was suspicious activity pending validation. That is more honest and closer to how a junior analyst should write it.

## Small lesson

A good alert is not just loud. It helps the analyst make the next decision. Noise with a badge is still noise.