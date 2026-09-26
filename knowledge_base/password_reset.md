# Password Reset

## Scope
This covers the routine case of a customer who knows their account email but
has forgotten or wants to change their password. Lockouts, lost email access,
or suspected compromise follow the account recovery procedure instead.

## Self-Service Flow
Direct the customer to the "Forgot password" link on the sign-in page. A reset
email is sent to the registered address and the link is valid for 60 minutes
and single use. Advise checking spam folders and allowing a few minutes for
delivery.

## Common Failure Points
- **No email received:** confirm the spelling of the registered address,
  resend once, and check the address is not an unverified alias.
- **Link expired or already used:** generate a fresh reset; old links
  intentionally stop working for security.
- **Reset succeeds but sign-in still fails:** confirm the customer is using
  the updated password and not a saved browser autofill of the old one.

## Password Requirements
Minimum 10 characters with a mix of letter case and at least one number or
symbol. Reused or breached passwords are rejected. Encourage a password
manager and two-factor authentication.

## Agent Steps
1. Confirm the registered email.
2. Trigger or guide the self-service reset; do not set a password on the
   customer's behalf.
3. If delivery fails repeatedly, verify the address health and escalate to
   account recovery.
4. Confirm the customer can sign in before closing.

## Communication
Keep it brief and reassuring. Never ask the customer to send their password,
and never share a one-time link through an unverified channel.
