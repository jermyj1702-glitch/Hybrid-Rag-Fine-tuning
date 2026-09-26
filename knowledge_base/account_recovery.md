# Account Recovery

## When To Use
Use this procedure when a customer cannot access their account due to a
lockout, a lost email address, suspected unauthorized access, or a disabled
account — anything beyond a simple forgotten password (see the password reset
procedure for that case).

## Identity Verification
Before any recovery action, verify identity with at least two of: the
registered email, the last order identifier, the billing postal code, or the
last four digits of the payment method on file. Never read back full payment
details or one-time codes to the customer.

## Lockout After Failed Attempts
Accounts lock for 30 minutes after five failed sign-in attempts. If the
customer did not make those attempts, treat it as a possible compromise:
unlock only after identity verification, force a password reset, and
recommend enabling two-factor authentication.

## Lost Or Changed Email
If the customer no longer controls the registered email, collect proof of
identity, update the address through the verified-change workflow, and send a
confirmation to both the old and new addresses where possible.

## Suspected Compromise
1. Verify identity.
2. Lock active sessions and revoke long-lived tokens.
3. Force a password reset and prompt two-factor enrollment.
4. Review recent orders and address changes for fraud.
5. Escalate confirmed account takeover to the security queue.

## Communication
Reassure the customer, explain each protective step, and confirm the account
is secured before closing. Document the recovery reason for audit.
