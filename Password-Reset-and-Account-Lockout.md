# Password Reset and Account Lockout

## Common User Issues

- Forgot password
- Account locked
- Unable to log in
- Password expired

## Password Reset Process

1. Verify user identity.
2. Open Active Directory Users and Computers.
3. Locate the user account.
4. Reset the password.
5. Require password change at next login if needed.
6. Inform the user and test login.

## Account Lockout Troubleshooting

### Possible Causes

- Multiple incorrect password attempts
- Saved old credentials
- Mobile device using outdated password
- Mapped drives or services using old credentials

### Steps

1. Verify account is locked.
2. Unlock the account in Active Directory.
3. Ask user if password was recently changed.
4. Check for devices using old credentials.
5. Monitor for repeated lockouts.

## Interview Answer

If a user cannot log in, I would first determine whether the issue is a forgotten password, expired password, or account lockout. After verifying the user's identity, I would reset the password or unlock the account in Active Directory and then help the user test access.
