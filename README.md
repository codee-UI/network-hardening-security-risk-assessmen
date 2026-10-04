# Security Risk Assessment — Network Hardening

## Repository Description

Security risk assessment for a social media organization following a major data breach, with recommended network hardening measures including multi-factor authentication, strong password policies, and regular firewall maintenance.

---

## Overview

This repository documents a simulated security risk assessment for a social media organization that experienced a major data breach affecting customers' personal information, including names and addresses.

Four major vulnerabilities were identified:

1. Employees share passwords.
2. The database administrator password is still set to a default value.
3. Firewall rules are not configured to filter incoming and outgoing traffic.
4. Multi-factor authentication (MFA) is not enabled.

The recommended hardening measures are:

- Implement multi-factor authentication (MFA)
- Set and enforce strong password policies
- Perform regular firewall maintenance

---

# Part 1 — Select Network Hardening Tools and Methods

## 1. Implement Multi-Factor Authentication (MFA)

MFA requires users to verify their identity using more than one authentication factor before gaining access to an account or system.

Possible factors include:

- Passwords
- PINs
- One-time passcodes
- Security tokens
- ID cards
- Fingerprint scans

### Vulnerabilities Addressed

MFA helps reduce the risks associated with:

- Password sharing
- Stolen passwords
- Weak passwords
- Brute-force attacks
- Unauthorized account access

```text
Password
   +
Second Authentication Factor
   |
   v
Successful Authentication
```

Even if a malicious actor obtains or guesses a password, they would still need the additional authentication factor.

---

## 2. Set and Enforce Strong Password Policies

The organization should establish and enforce a formal password policy for all users, especially privileged and administrative accounts.

A strong password policy can include:

- Minimum password length
- Password complexity requirements
- Restrictions on password reuse
- Removal of default passwords
- Rules against password sharing
- Limits on unsuccessful login attempts
- Account lockout or additional verification after repeated failures

### Vulnerabilities Addressed

This hardening method directly addresses:

- Employees sharing passwords
- The database administrator using a default password
- Brute-force password attacks
- Unauthorized account access

---

## 3. Perform Regular Firewall Maintenance

The organization's firewall currently lacks rules for properly filtering network traffic.

Firewall maintenance should include:

- Reviewing existing rules
- Adding appropriate allow and deny rules
- Removing obsolete rules
- Blocking suspicious traffic sources
- Reviewing inbound and outbound traffic policies
- Updating configurations after security incidents
- Ensuring rules reflect current security requirements

### Vulnerability Addressed

This directly addresses the absence of firewall filtering rules.

A properly configured firewall helps control which traffic is permitted to enter or leave the organization's network.

---

# Part 2 — Explain the Recommendations

## Multi-Factor Authentication

MFA adds an additional layer of protection beyond a password.

This is effective because a malicious actor who obtains or guesses a password still needs another authentication factor before access is granted.

MFA may also reduce the usefulness of password sharing. Even if a password is shared, the other person may not possess the additional authentication factor.

### Implementation Frequency

MFA should be:

- Enabled as a continuous security control
- Required for privileged and administrative accounts
- Used whenever users authenticate to sensitive systems
- Reviewed periodically to ensure enrolled factors remain valid

---

## Strong Password Policies

A password policy makes unauthorized access more difficult by creating consistent authentication requirements.

The organization should immediately remove default passwords and prevent weak or reused credentials.

Policies can also limit unsuccessful login attempts. For example, an account can be temporarily suspended after several failed attempts.

This helps reduce the effectiveness of brute-force attacks.

### Implementation Frequency

Password policies should be:

- Enforced continuously
- Applied when accounts are created
- Applied whenever passwords are changed
- Reviewed periodically
- Updated when security requirements change

---

## Firewall Maintenance

Regular firewall maintenance ensures filtering rules remain appropriate as the network changes.

Administrators should confirm that:

- Allowed traffic is necessary
- Unwanted traffic is blocked
- Suspicious sources are denied when appropriate
- Obsolete rules are removed
- Rules are reviewed after security incidents

Proper firewall filtering can help protect the organization against unauthorized access and some forms of DoS and DDoS traffic.

### Implementation Frequency

Firewall maintenance should occur:

- Regularly on a defined schedule
- Whenever a major network change occurs
- After a security incident
- When new threats or security requirements are identified

---

# Vulnerability-to-Control Mapping

| Identified Vulnerability | Recommended Hardening Control | Why It Helps |
|---|---|---|
| Employees share passwords | MFA + password policy | Reduces usefulness of shared credentials and prohibits password sharing |
| Database admin uses default password | Strong password policy | Requires replacement of default credentials and stronger passwords |
| Firewall lacks traffic-filtering rules | Firewall maintenance | Establishes and maintains allowed/denied traffic rules |
| MFA is not used | Implement MFA | Adds another authentication factor beyond passwords |

---

# Risk Reduction Summary

```text
Identified Vulnerabilities
        |
        v
+-----------------------------+
| Shared passwords            |
| Default admin password      |
| Missing firewall rules      |
| No MFA                      |
+-----------------------------+
        |
        v
Network Hardening
        |
        +---------------------------+
        |             |             |
        v             v             v
      MFA       Password Policy   Firewall
                                  Maintenance
        |             |             |
        +-------------+-------------+
                      |
                      v
           Reduced Attack Surface
                      |
                      v
        Lower Risk of Future Breach
```

---

# Recommended Priority

1. Immediately replace all default administrative passwords.
2. Enable MFA for privileged and sensitive accounts.
3. Enforce organization-wide password policies.
4. Create and review firewall filtering rules.
5. Establish recurring firewall and access-control reviews.

---

# Key Findings

- Password sharing increases the risk of unauthorized access.
- A default database administrator password creates a major authentication weakness.
- Missing firewall rules leave network traffic insufficiently controlled.
- The absence of MFA means passwords are the only authentication barrier.
- MFA, strong password policies, and firewall maintenance provide complementary protection.
- These controls should be maintained continuously or reviewed regularly rather than treated as one-time fixes.

---

# Skills Demonstrated

- Security risk assessment
- Network hardening
- Multi-factor authentication
- Password security
- Firewall configuration
- Access control
- Brute-force mitigation
- Network traffic filtering
- Defense in depth
- Vulnerability remediation

---

# Repository Purpose

This repository is maintained as part of a cybersecurity learning and professional portfolio.

It demonstrates the ability to:

- Identify network and authentication vulnerabilities
- Select appropriate hardening controls
- Explain why each control is effective
- Recommend implementation and maintenance practices
- Connect vulnerabilities to practical security improvements

---

# Disclaimer

This repository documents a simulated cybersecurity training scenario and is intended for educational and portfolio purposes.

---

## Suggested GitHub Topics

`cybersecurity` `network-security` `network-hardening` `mfa` `password-security` `firewall` `risk-assessment` `access-control` `defense-in-depth`

## Keywords

`Cybersecurity` `Security Risk Assessment` `Network Hardening` `MFA` `Password Policy` `Firewall Maintenance` `Access Control` `Brute Force Mitigation` `Network Security` `Defense in Depth`
