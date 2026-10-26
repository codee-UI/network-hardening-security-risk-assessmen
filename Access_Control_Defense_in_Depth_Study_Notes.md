# Access Control and Defense in Depth — Cybersecurity Study Notes

## Project Title

**Access Control and Defense-in-Depth: Implementing Administrative, Physical, and Logical Security Controls for Organizational Assets**

## 1. Course Agenda

- Key concepts of access control
- Administrative controls
- Physical controls
- Logical (technical) controls
- Controls overview and review

## 2. Access Control: Core Concept

Access control determines **who can access organizational assets and what actions they may perform**. Assets include buildings, data, systems, networks, applications, and equipment.

Access control both grants appropriate access to authorized people and processes and denies access to unauthorized people, processes, or functions.

The three elements of access control are **subjects, objects, and rules**.

## 3. Subjects, Objects, and Rules

### 3.1 Subjects — Who requests access?

A **subject** is an entity that initiates a request to access a resource or service. It is *active* because it starts the request.

Examples include users, administrators, clients, server processes, applications, programs, workstations, smartphones, endpoints, and removable storage devices.

A subject should have permissions or a clearance level appropriate to the resource and action requested.

### 3.2 Objects — What is being accessed?

An **object** is the resource that a subject attempts to access. It is *passive* in access-control terminology because it responds to requests rather than initiating them.

Examples include files, databases, computers, servers, buildings, server rooms, printers, scanners, communications resources, memory blocks, input/output ports, software tasks, threads, and processes.

Objects may have an owner and a classification. Permissions may be recorded in an access-control list (ACL) or rule base. An object does not necessarily make the authorization decision itself; another system component enforces the access rules.

### 3.3 Rules — How is access decided?

An **access rule** specifies whether a subject may access an object and what level of access is permitted. Rules may compare a validated identity and other attributes against an approved policy or ACL.

A rule can:
- Allow or deny access
- Define permitted actions or the level of access
- Compare multiple attributes
- Apply time-based restrictions

**File example:** A user requests permission to delete a file. The operating system checks the user's permissions. If deletion is authorized, the file is deleted; otherwise, the request is denied.

**Firewall example:** A firewall rule may permit traffic from an approved internal network to an external network while denying traffic that does not meet configured rules.

| Element | Main question | Example |
|---|---|---|
| Subject | Who is requesting access? | An employee |
| Object | What is being accessed? | A confidential file |
| Rule | What is allowed, and under what conditions? | Read-only access for the employee |

## 4. Defense in Depth

**Defense in depth** is a security strategy that combines people, technology, and operational practices to create multiple protective layers around organizational assets. It aims to prevent or deter attacks and reduce the impact of control failures; it cannot guarantee that attacks will never occur.

### Control layers

- **Administrative controls:** Policies, procedures, approvals, and assigned responsibilities.
- **Logical/technical controls:** Passwords, multifactor authentication (MFA), permissions, firewalls, and system access rules.
- **Physical controls:** Locks, badges, guards, cameras, and barriers.

**Data-center example:**
1. A locked door and badge-controlled entry restrict physical access.
2. Network and system permissions restrict access to stored data.
3. Administrative policy defines who is eligible for access and how it must be approved.

Technical examples include using a password plus a second verification factor and separating untrusted networks from sensitive servers with firewalls.

## 5. Privileged Access Management (PAM)

**Privileged Access Management (PAM)** limits and monitors the use of accounts with elevated permissions.

Privileged accounts can perform sensitive actions, such as creating, reading, updating, or deleting records; administering systems; or changing security settings. If these permissions are permanently available, compromised accounts can cause extensive damage.

### Just-in-time privileged access

With **just-in-time (JIT) access**, elevated permissions are enabled only when needed for an approved task and for an appropriate period, rather than being available continuously.

### Ransomware example

An IT employee uses a Domain Admin account for everyday email and opens a malicious attachment. Broad administrative privileges may allow ransomware to affect many servers and workstations.

Safer practices include:
- Use a standard account for routine tasks such as email.
- Use a separate privileged account only for administrative work.
- Grant elevated access only when required.
- Monitor and audit privileged actions.

### Privileged-account users

- Systems administrators
- Help-desk and IT-support staff
- Security analysts
- Approved project or client-service personnel with elevated responsibilities

### Risk-reduction measures

- **Detailed logging:** Record privileged actions for accountability and investigation.
- **Stronger authentication:** Require MFA and appropriate additional verification for privileged access.
- **JIT access:** Restrict elevated permissions to approved tasks and time periods.
- **Trust and policy checks:** Apply appropriate background checks, confidentiality agreements, and acceptable-use requirements according to organizational policy and applicable law.
- **Frequent auditing:** Review privileged activity more closely than ordinary account activity.

## 6. Principle of Least Privilege

The **Principle of Least Privilege (PoLP)** states that users and processes should receive only the minimum permissions necessary to perform their assigned duties.

Benefits include reducing the impact of compromised accounts, limiting accidental or unauthorized changes, reducing unnecessary access to sensitive information, and supporting confidentiality, integrity, and availability.

**Example:** A staff member who only needs to read reports should not automatically receive permission to delete the underlying database.

## 7. Segregation of Duties and Two-Person Controls

### Segregation of duties (SoD)

**Segregation of duties**, also called separation of duties, divides a high-risk process among multiple people so that one person cannot control every step from beginning to end.

Examples:
- One employee submits an invoice; a manager approves it.
- One person proposes a system configuration change; another reviews and approves it before implementation.

These controls can prevent fraud and identify errors. If people deliberately cooperate to bypass controls, this is called **collusion**.

### Dual control

**Dual control** requires two separate people to participate in a sensitive action. For example, two bank employees may each control one part of the combination needed to open a vault.

### Two-person integrity

The **two-person rule** requires at least two people to be present together in a designated high-security area or during a sensitive activity. It can reduce insider risk and provide assistance if one person experiences a medical emergency.

**Distinction:** Segregation of duties divides a process into separately assigned responsibilities; dual control requires multiple people to participate in a sensitive action; the two-person rule requires two people to be present together.

## 8. Authentication and Authorization

- **Authentication:** Confirms the identity of a subject.
- **Authorization:** Determines what an authenticated subject is permitted to do.

**Example:** A worker presents a badge at a server-room door. The system checks the badge and associated identity, then checks whether that identity is authorized to enter. Access is granted or denied according to the configured permissions.

Authentication alone does not authorize a user to access every resource.

## 9. User Provisioning and Account Lifecycle

Access rights should change when a person's employment status or job responsibilities change.

### New employee
- Obtain required approval.
- Create the user's account.
- Assign access based on an approved role or standard profile.
- Obtain additional approval for elevated privileges when required.

### Change of position
- Add access required by the new role.
- Remove access that is no longer needed.
- Review elevated permissions instead of retaining all previous access.

### Separation of employment
- Disable the account according to the approved termination process and time.
- Remove the account from relevant roles and access groups.
- Preserve records as required for audit, legal, and business purposes.
- Delete the account later according to retention and account-management policy.

### Privilege creep

**Privilege creep** occurs when permissions accumulate over time and are not removed when they are no longer required. Creating accounts from **standard role-based profiles**, rather than copying another employee's entire profile, helps reduce the risk of transferring unnecessary permissions.

## 10. Physical Security Controls

**Physical access controls** are tangible mechanisms used to prevent, deter, monitor, or detect unauthorized physical access to people, facilities, and equipment. Personnel safety comes first.

Examples:
- Security guards and guard dogs
- Fences, locked doors, gates, and sealed windows
- Lighting and cable protection
- Laptop locks
- Badges, swipe cards, and other access cards
- Turnstiles and mantraps
- Cameras and motion detectors
- Door, window, fire, and panic alarms

### Badge systems and controlled entry

A physical access system enrolls an authorized person, issues a badge or credential, and associates it with permitted areas. The system checks the credential against an authorized database before allowing entry and may log successful and unsuccessful attempts.

Credential types listed in the course:
- Barcode
- Magnetic stripe
- Proximity
- Smart card
- Hybrid card

High-security enrollment may also include biometric information.

### Crime Prevention Through Environmental Design (CPTED)

**CPTED** uses environmental and architectural design to make spaces safer and reduce opportunities for crime.

- **Organizational:** People and how activities are managed
- **Mechanical:** Technology and hardware
- **Natural design:** Architecture, visibility, and the flow of people

Examples include directing visitor movement, improving visibility in hidden areas, and making boundaries between public and restricted spaces clear.

### Biometrics

Biometrics uses physical or behavioral characteristics to help verify identity.

**Process:**
1. **Enrollment:** Register a biometric characteristic and store a corresponding representation in a system or on a credential.
2. **Verification:** Capture a new sample and compare it with the registered representation.

**Physiological biometrics:** fingerprint, iris scan, retinal scan, palm scan, and vein-pattern scan.

**Behavioral biometrics:** voiceprint, signature dynamics, and keystroke dynamics (such as how long keys are held and timing between keystrokes).

**Limitations and considerations:**
- Equipment and enrollment can be expensive.
- Users may have privacy concerns.
- Biometric data is personally identifiable information and requires protection.
- Collection and use should follow applicable consent, privacy, and organizational requirements.
- Device hygiene and sanitization may be operational concerns.

## 11. Physical Security Monitoring

Monitoring helps organizations record, detect, and investigate physical security events.

### Cameras and sensors
- Cameras can deter misconduct, support monitoring, and provide recorded evidence.
- Infrared, microwave, laser, door, gate, and vibration sensors can help detect perimeter or entry-point activity.
- Integrating sensors with alerting processes can help personnel respond to possible intrusions.

### Physical access logs

A **log** is a record of events, such as a visitor sign-in sheet or electronic badge-entry record.

Good log management includes:
- Recording relevant access events
- Protecting logs against manipulation
- Restricting access to logs containing sensitive information
- Reviewing logs regularly
- Establishing and following retention policies based on legal and business requirements

### Log anomalies

A **log anomaly** is an unusual event or pattern that may need investigation.

Examples include:
- Gaps in date or time records
- Repeated account lockouts
- Attempts to write to a protected directory

Collecting excessive logs without a clear purpose can overwhelm an organization. Logging and retention should be proportionate to operational, legal, and business needs.

> **Compliance note:** The supplied course material states that PCI DSS requires one year of log data. Treat this as a statement from the course notes, not independently verified or universally applicable compliance advice. Check the applicable PCI DSS version and requirements before making a compliance decision.

### Security guards and alarms
- **Security guards** can discourage impersonation, tailgating, theft, and misuse.
- **Door and window alarms** alert personnel when an entry point is opened unexpectedly.
- **Fire alarms** detect conditions such as smoke or heat and help protect people.
- **Panic buttons** alert designated security or emergency personnel.

## 12. Logical (Technical) Access Controls

**Logical access controls** are electronic mechanisms that regulate access to systems, applications, data, and sometimes physical areas.

Examples include passwords, system-based biometric authentication, electronic badge or token readers, user and group permissions, and firewall rules.

A person may have physical access to a device but still be blocked from accessing its data by logical controls.

## 13. Access-Control Models

The course discusses Discretionary Access Control (DAC), Mandatory Access Control (MAC), and Role-Based Access Control (RBAC).

### Discretionary Access Control (DAC)

Under **DAC**, the owner of an object, or another permitted subject, can determine or modify who receives access to that object, within the system's rules.

Depending on the system, a user with access may be able to share information, grant certain permissions to others, or change permissions on owned resources.

**Example:** A file owner grants another user read access to a document.

- **Strength:** Flexible and convenient for sharing.
- **Limitation:** Permissions can become difficult to govern consistently across a large environment.

### Mandatory Access Control (MAC)

Under **MAC**, access rules are centrally and uniformly enforced. Ordinary users and object owners cannot freely change the governing rules; designated security administrators control them.

MAC constrains users from independently passing information to unauthorized subjects, granting their privileges to others, changing security attributes, choosing classifications for new or modified objects, or changing the governing rules.

**Example:** A centrally managed system restricts access according to approved security classifications and permissions.

**Key distinction:** DAC gives object owners some discretion over permissions; MAC places control of the governing rules with designated security administrators.

### Role-Based Access Control (RBAC)

Under **RBAC**, permissions are assigned according to organizational roles, and users receive access through their assigned roles.

**Example:** An HR role may read employee records, while an IT administrator role may manage specified systems.

RBAC can support consistent provisioning and least privilege when roles are carefully designed and reviewed.

### Comparison

| Feature | DAC | MAC | RBAC |
|---|---|---|---|
| Main basis | Owner's discretion over access | Centrally enforced rules | Assigned organizational role |
| Who primarily governs access? | Object owner or permitted subject | Designated security administrators | Role and permission administrators |
| User sharing flexibility | Often more flexible | Restricted by centrally enforced policy | Depends on role permissions |
| Main consideration | Permissions can become inconsistent or hard to scale | Rules are centrally controlled and less flexible for ordinary users | Roles must reflect job responsibilities accurately |

## 14. Access Control and the CIA Triad

Access control and PAM help support the three information-security objectives:

- **Confidentiality:** Restrict information to authorized subjects.
- **Integrity:** Permit changes only to appropriately authorized users and processes.
- **Availability:** Ensure authorized personnel can obtain needed access when required, while limiting misuse that could disrupt systems.

JIT privileged access reduces unnecessary exposure of administrative permissions, helps restrict changes to approved activities, and enables elevated access for authorized maintenance when needed.

## 15. Administrative, Physical, and Logical Controls — Review

| Control category | What it governs | Examples |
|---|---|---|
| Administrative | Policies, approvals, responsibilities, and processes | Access policies, role approvals, segregation of duties, account lifecycle procedures |
| Physical | Entry to facilities and contact with equipment | Guards, fences, locks, badges, cameras, alarms |
| Logical/technical | Electronic access to systems, applications, and data | Passwords, biometrics, tokens, permissions, firewall rules |

Effective protection combines these control categories instead of relying on only one.

## 16. Practical Scenario: Securing a Server Room

Suppose an organization stores sensitive customer records on a server.

1. **Administrative:** Management approves access only for staff who need it.
2. **Physical:** A badge-controlled door restricts entry, and access events are logged.
3. **Logical:** Individual accounts and permissions restrict access to server data.
4. **Authentication:** Users prove their identity before the system evaluates their permissions.
5. **Least privilege:** Staff receive only the access necessary for their duties.
6. **PAM:** Administrators use elevated access only for approved administrative tasks.
7. **Segregation of duties:** High-risk changes require separate review and approval.
8. **Monitoring:** Physical and system logs are reviewed for unusual activity.
9. **Account lifecycle:** Permissions are updated when employees change roles and removed when access is no longer required.
10. **Defense in depth:** The combined layers reduce the chance that a single control failure exposes the asset.

## 17. Key Terms

| Term | Concise definition |
|---|---|
| Access control | Determines who can access an asset and what actions they can perform |
| Subject | Active entity requesting access |
| Object | Resource being accessed |
| Access rule | Condition or instruction used to allow or deny access |
| ACL | Access-control list identifying subjects and their permissions for an object |
| Authentication | Verification of identity |
| Authorization | Determination of permitted actions |
| Defense in depth | Multiple complementary security layers |
| PAM | Management and monitoring of elevated access |
| JIT access | Elevated permissions activated only when needed |
| Least privilege | Only the minimum access necessary for a task |
| Segregation of duties | Dividing a high-risk process among different people |
| Collusion | People cooperating to bypass controls or commit misconduct |
| Dual control | Two people are required to participate in a sensitive action |
| Two-person rule | At least two people must be present together in a designated area or activity |
| Provisioning | Creating accounts and assigning access |
| Privilege creep | Accumulation of unnecessary permissions over time |
| CPTED | Environmental design practices intended to reduce opportunities for crime |
| Biometrics | Identity verification using physical or behavioral characteristics |
| Log anomaly | An unusual event or pattern in recorded activity |
| DAC | Access control that gives object owners some discretion over permissions |
| MAC | Centrally enforced access-control policy |
| RBAC | Access assigned according to roles |

## 18. Revision Questions

Try answering these without looking at the notes.

1. What are the three elements of access control?
2. Why is a subject described as active and an object as passive?
3. What is the difference between authentication and authorization?
4. Explain defense in depth with one physical, one logical, and one administrative control.
5. Why should administrators avoid using privileged accounts for routine email?
6. What is just-in-time privileged access?
7. Explain the difference between segregation of duties, dual control, and the two-person rule.
8. What should happen to access when an employee changes roles or leaves the organization?
9. What is privilege creep, and how can standard role profiles help prevent it?
10. Name five physical access controls and three ways to monitor physical security.
11. What are the enrollment and verification stages of biometric authentication?
12. How do DAC, MAC, and RBAC differ?
13. How do access controls support confidentiality, integrity, and availability?
14. Why must security logs be protected and reviewed?
15. Describe a layered approach to protecting a server room.

## 19. Quick Self-Test

- [ ] I can explain subjects, objects, and rules.
- [ ] I can distinguish administrative, physical, and logical controls.
- [ ] I can explain defense in depth and least privilege.
- [ ] I understand PAM, privileged accounts, and JIT access.
- [ ] I can distinguish authentication from authorization.
- [ ] I can explain segregation of duties, dual control, and the two-person rule.
- [ ] I understand account provisioning, deprovisioning, and privilege creep.
- [ ] I can describe physical controls, biometrics, monitoring, and log anomalies.
- [ ] I can compare DAC, MAC, and RBAC.
- [ ] I can connect access control to the CIA Triad.

---

**Study note:** These notes are based on the supplied course material. Verify current applicable standards before using compliance-specific statements as operational or audit guidance.
