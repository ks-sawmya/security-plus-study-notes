# CompTIA Security+ SY0-701 — Domain 1: General Security Concepts

These are my personal study notes while preparing for the CompTIA Security+ SY0-701 certification.

---

## 1.1 Security Concepts

### CIA Triad

The CIA Triad represents the three fundamental goals of information security:

* **Confidentiality**
* **Integrity**
* **Availability**

### Confidentiality

Confidentiality protects information from unauthorized access or disclosure.

**Think:**

> Who is allowed to see this information?

Examples:

* Encryption
* Access controls
* File permissions
* Authentication
* Data classification

A confidentiality breach occurs when unauthorized people can access sensitive information.

**Example:**
An employee without permission views a confidential customer database.

---

### Integrity

Integrity ensures that information remains accurate, complete, and has not been modified without authorization.

**Think:**

> Has the information been changed?

Examples:

* Hashing
* Digital signatures
* File integrity monitoring
* Checksums

**Example:**
A malware infection modifies an important system file.

---

### Availability

Availability ensures that systems and information are accessible when needed by authorized users.

**Think:**

> Can I access it when I need it?

Examples:

* Backups
* Redundant systems
* Failover systems
* Load balancing
* UPS
* Disaster recovery

**Example:**
A server becomes unavailable because of a denial-of-service attack.

---

### Easy CIA Memory Trick

**Confidentiality → Who can see it?**

**Integrity → Was it changed?**

**Availability → Can I access it?**

---

# 1.2 Non-Repudiation

Non-repudiation provides evidence that a person or entity performed an action.

It makes it difficult for someone to later deny performing that action.

### Example

An employee digitally signs an important transaction.

Later, the employee claims:

> "I never approved that transaction."

A digital signature can provide evidence associated with the employee's private key.

### Common technology

* Digital signatures
* Digital certificates
* Audit logs

### Important distinction

**Authentication:** Who are you?

**Authorization:** What are you allowed to do?

**Non-repudiation:** Can you deny performing the action?

---

# Authentication vs Authorization vs Accounting

### Authentication

Authentication verifies a user's identity.

**Question:**

> Who are you?

Examples:

* Username and password
* Fingerprint
* Smart card
* Security token
* MFA

---

### Authorization

Authorization determines what an authenticated user is allowed to access or perform.

**Question:**

> What are you allowed to do?

Examples:

* Read-only access
* Administrator privileges
* File permissions
* Application permissions

---

### Accounting / Auditing

Accounting records what a user or system did.

**Question:**

> What did you do?

Examples:

* Login logs
* Audit logs
* File access logs
* System activity logs

### AAA

**Authentication → Who are you?**

**Authorization → What can you do?**

**Accounting → What did you do?**

---

# Security Controls

Security controls are safeguards used to reduce security risks.

Security controls can be classified by:

1. Control function
2. Control category

---

## Control Functions

### Preventive

Preventive controls are designed to stop an incident from occurring.

Examples:

* Firewall
* Access control
* Security awareness training
* MFA
* Network segmentation

**Think:** Stop it before it happens.

---

### Detective

Detective controls identify or detect security incidents.

Examples:

* Intrusion Detection System (IDS)
* CCTV
* Log monitoring
* Security Information and Event Management (SIEM)
* File integrity monitoring

**Think:** Find out what happened.

---

### Corrective

Corrective controls are used to correct problems and restore normal operation after an incident.

Examples:

* Restoring from backup
* Rebuilding an infected system
* Removing malware
* Applying a fix after an incident

**Think:** Fix it.

---

### Deterrent

Deterrent controls discourage people from attempting malicious activity.

Examples:

* Security guards
* Warning signs
* Visible cameras
* Fences
* Security banners

**Think:** Discourage the attacker.

---

### Compensating

A compensating control is an alternative control used when the preferred control cannot be implemented.

**Example:**

A legacy application cannot support MFA.

An organization adds an additional authentication gateway in front of the application.

The additional gateway acts as a compensating control.

**Think:** Alternative protection.

---

### Directive

Directive controls provide instructions or guidance about expected behavior.

Examples:

* Security policies
* Procedures
* Standards
* Acceptable use policies
* Security awareness instructions

**Think:** Tell people what they should do.

---

# Security Control Categories

## Technical Controls

Technical controls use technology to protect systems and information.

Examples:

* Firewalls
* IDS/IPS
* Encryption
* Antivirus
* Access control systems
* MFA

---

## Physical Controls

Physical controls protect physical locations, equipment, and people.

Examples:

* Locks
* Fences
* Security guards
* CCTV
* Mantraps
* Bollards
* Lighting

---

## Administrative Controls

Administrative controls are policies, procedures, guidelines, and management activities.

Examples:

* Security policies
* Risk assessments
* Security awareness training
* Incident response policies
* Acceptable use policies

---

## Operational Controls

Operational controls are security activities and processes performed by people.

Examples:

* Security guards
* Incident response procedures
* User training
* Monitoring activities
* Change management processes

---

# Security Control Examples

| Control                     | Function   | Category              |
| --------------------------- | ---------- | --------------------- |
| Firewall                    | Preventive | Technical             |
| IDS                         | Detective  | Technical             |
| CCTV                        | Detective  | Physical              |
| Security guard              | Deterrent  | Operational           |
| Security awareness training | Preventive | Administrative        |
| Backup restoration          | Corrective | Technical/Operational |
| Fence                       | Deterrent  | Physical              |
| MFA                         | Preventive | Technical             |
| Security policy             | Directive  | Administrative        |
| Log monitoring              | Detective  | Technical             |

---

# Defense in Depth

Defense in depth uses multiple layers of security controls.

The goal is to avoid relying on a single security control.

### Example

A company may use:

1. Firewall
2. Network segmentation
3. IDS/IPS
4. MFA
5. Endpoint protection
6. Logging
7. Security awareness training

If one control fails, other controls can still provide protection.

**Key idea:**

> Multiple layers of security reduce reliance on a single control.

---

# Zero Trust

Zero Trust is a security approach based on the principle of:

> Never trust, always verify.

Users and devices should not automatically be trusted simply because they are inside the organization's network.

Important concepts include:

* Verify explicitly
* Use least privilege
* Assume breach
* Continuously evaluate access
* Authenticate users and devices

### Example

An employee working from inside the company network still needs to authenticate before accessing a sensitive application.

---

# Gap Analysis

A gap analysis compares the organization's current security state with the desired or required state.

It identifies what is missing.

### Example

Current state:

* Password authentication only

Required state:

* MFA required

**Gap:**

The organization needs to implement MFA.

---

# Zero-Day Vulnerability

A zero-day vulnerability is a previously unknown vulnerability or a vulnerability for which no effective patch is available at the time it is exploited or publicly disclosed.

A zero-day attack can be difficult to defend against because organizations may not yet have a patch.

---

# Vulnerability vs Threat vs Risk

These concepts are commonly confused.

### Vulnerability

A weakness that could be exploited.

**Example:**

An unpatched web server.

---

### Threat

Something capable of exploiting a vulnerability.

Examples:

* Hacker
* Malware
* Insider
* Natural disaster

---

### Risk

The potential for loss or damage when a threat exploits a vulnerability.

**Simple relationship:**

> Threat + Vulnerability → Potential Risk

---

# Exploit

An exploit is a technique, code, or method used to take advantage of a vulnerability.

### Example

A server has a known software vulnerability.

An attacker uses exploit code to gain unauthorized access.

---

# Threat Actors

A threat actor is an individual or group that performs malicious activity.

Common categories include:

### Nation-State

Government-sponsored groups.

Possible goals:

* Espionage
* Intelligence gathering
* Political objectives
* Military objectives

---

### Organized Crime

Criminal groups motivated primarily by financial gain.

Examples:

* Ransomware operations
* Credential theft
* Financial fraud

---

### Hacktivists

Attackers motivated by political or social causes.

Possible activities:

* Website defacement
* Data leaks
* Denial-of-service attacks

---

### Insider Threat

A person with legitimate access who misuses that access.

Insider threats can be:

* Malicious
* Negligent
* Accidental

---

### Script Kiddie

An inexperienced attacker who uses existing tools or scripts without necessarily understanding how they work.

---

### Shadow IT

Technology or services used by employees without official approval from the organization's IT or security teams.

Examples:

* Unapproved cloud storage
* Personal applications
* Unauthorized software

Shadow IT can create security and compliance risks.

---

# Risk Concepts

## Risk Appetite

The amount of risk an organization is willing to accept while achieving its objectives.

---

## Risk Tolerance

The acceptable level of variation from the organization's desired risk level.

---

## Risk Acceptance

The organization knowingly accepts a risk rather than implementing additional controls.

---

## Risk Avoidance

The organization eliminates the activity that creates the risk.

### Example

A company stops using a vulnerable application entirely.

---

## Risk Transfer

The organization transfers some financial or operational consequences of a risk to another party.

Example:

* Cybersecurity insurance
* Outsourcing certain services

---

## Risk Mitigation

The organization reduces the likelihood or impact of a risk by implementing controls.

Example:

* Installing a firewall
* Implementing MFA
* Applying security patches

---

# Business Impact Analysis (BIA)

A Business Impact Analysis identifies the potential effects of a disruption to business operations.

A BIA helps determine:

* Which systems are most important
* Which services are critical
* How long systems can be unavailable
* What the business impact would be

---

# Recovery Terms

## Recovery Time Objective (RTO)

RTO defines the maximum acceptable amount of time a system can remain unavailable after a disruption.

**Think:**

> How quickly must we restore it?

Example:

RTO = 4 hours

The organization wants the system restored within four hours.

---

## Recovery Point Objective (RPO)

RPO defines the maximum acceptable amount of data loss measured in time.

**Think:**

> How much data can we afford to lose?

Example:

RPO = 1 hour

The organization can tolerate losing up to approximately one hour of data.

---

### RTO vs RPO

**RTO → Time to restore**

**RPO → Amount of data/time that can be lost**

---

# Mean Time to Repair (MTTR)

MTTR represents the average time required to repair or restore a system after a failure.

**Think:**

> How long does it take us to fix it?

---

# Mean Time Between Failures (MTBF)

MTBF represents the average amount of operating time between failures.

**Think:**

> How long does the system operate before failing?

---

# Business Continuity

Business continuity focuses on maintaining critical business operations during and after a disruption.

Examples:

* Alternate work locations
* Backup communication methods
* Redundant systems
* Business continuity plans

---

# Disaster Recovery

Disaster recovery focuses on restoring IT systems and services after a major disruption.

Examples:

* Backup restoration
* Alternate data centers
* Cloud recovery
* System restoration procedures

---

# Incident Response

Incident response is the process used to detect, respond to, contain, and recover from security incidents.

Common phases include:

1. Preparation
2. Detection/Analysis
3. Containment
4. Eradication
5. Recovery
6. Lessons Learned

---

# Data Classification

Data classification organizes information according to its sensitivity and importance.

Common classifications include:

### Public

Information that can be freely shared.

Example:

* Public website content

### Internal

Information intended for use within an organization.

Example:

* Internal procedures

### Confidential

Sensitive information requiring protection.

Example:

* Business information
* Customer information

### Restricted

Highly sensitive information requiring strict access controls.

Example:

* Highly sensitive financial or personal information

Organizations may use different classification names depending on their policies.

---

# Data States

Data commonly exists in three states.

## Data at Rest

Data stored on a device or storage system.

Examples:

* Hard drive
* SSD
* Database
* USB drive

Security controls:

* Encryption
* Access controls

---

## Data in Transit

Data moving between systems.

Examples:

* Web traffic
* Email
* Network communication

Security controls:

* TLS
* VPN
* Encryption

---

## Data in Use

Data actively being processed or accessed.

Examples:

* Data loaded into memory
* Information being processed by an application

Security controls may include:

* Access controls
* Application security
* Secure processing environments

---

# Encryption

Encryption transforms readable data (plaintext) into unreadable data (ciphertext).

A key is used as part of the encryption/decryption process.

### Encryption primarily supports:

**Confidentiality**

It can also contribute to other security objectives depending on the implementation.

---

# Hashing

Hashing converts data into a fixed-length value called a hash.

Hashing is commonly used to help verify integrity.

### Important distinction

**Encryption → Can be decrypted with the appropriate key.**

**Hashing → Designed as a one-way function.**

Common uses:

* File integrity
* Password storage
* Digital signatures

---

# Digital Signatures

Digital signatures use asymmetric cryptography to provide evidence of authenticity and integrity.

They can help provide:

* Integrity
* Authentication/identity evidence
* Non-repudiation

Digital signatures do **not** primarily provide confidentiality.

---

# Digital Certificates

Digital certificates bind an identity to a public key.

Certificates are commonly issued by a:

**Certificate Authority (CA)**

Certificates are commonly used with:

* HTTPS
* TLS
* Public Key Infrastructure (PKI)

---

# Public Key Infrastructure (PKI)

PKI is a framework used to manage digital certificates and public-key cryptography.

Important components include:

* Certificate Authority (CA)
* Registration Authority (RA)
* Digital certificates
* Public/private key pairs
* Certificate revocation mechanisms

---

# Symmetric Cryptography

Symmetric encryption uses the same key for encryption and decryption.

Advantages:

* Fast
* Efficient for large amounts of data

Challenge:

* Securely sharing the key

Examples:

* AES

---

# Asymmetric Cryptography

Asymmetric cryptography uses a pair of keys:

* Public key
* Private key

The keys are mathematically related.

Uses include:

* Digital signatures
* Key exchange
* Encryption
* Digital certificates

Asymmetric cryptography is generally slower than symmetric cryptography.

---

# Symmetric vs Asymmetric

| Feature      | Symmetric      | Asymmetric                         |
| ------------ | -------------- | ---------------------------------- |
| Keys         | One shared key | Public + private key               |
| Speed        | Faster         | Slower                             |
| Large data   | Well suited    | Less efficient                     |
| Key exchange | More difficult | Easier for public-key distribution |
| Example      | AES            | RSA/ECC                            |

---

# Security Baselines

A security baseline is a minimum set of security requirements or configurations that systems should meet.

Examples:

* Minimum password requirements
* Required encryption
* Approved software
* Required logging
* Endpoint security configuration

Baselines help create consistent security across systems.

---

# Hardening

Hardening reduces the attack surface of a system.

Examples:

* Disable unnecessary services
* Remove unused software
* Change default passwords
* Apply security patches
* Restrict unnecessary ports
* Configure secure settings
* Enable logging

**Goal:**

> Reduce unnecessary exposure and attack opportunities.

---

# Attack Surface

The attack surface represents the collection of possible entry points that an attacker could use to compromise a system or organization.

Examples:

* Open network ports
* Web applications
* APIs
* User accounts
* Remote access services
* Unpatched software

Reducing unnecessary services and access can reduce the attack surface.

---

# Least Privilege

Least privilege means users and systems should receive only the permissions necessary to perform their required tasks.

### Example

A help-desk employee does not need domain administrator privileges.

Giving unnecessary privileges increases risk.

---

# Separation of Duties

Separation of duties divides sensitive responsibilities between multiple people.

### Example

One employee creates a financial transaction and another employee approves it.

This reduces the possibility of fraud or abuse by a single person.

---

# Job Rotation

Job rotation periodically moves employees between different roles or responsibilities.

Benefits can include:

* Detecting suspicious activity
* Reducing dependence on one individual
* Improving knowledge sharing

---

# Mandatory Vacation

Mandatory vacation requires employees to take time away from their normal duties.

This can help expose fraudulent activities that depend on continuous control by one person.

---

# Defense in Depth vs Least Privilege

### Defense in Depth

Uses multiple layers of security controls.

### Least Privilege

Limits users and systems to only the access they need.

These are different security principles but can be used together.

---

# Authentication Factors

Authentication factors are categories of evidence used to verify identity.

## Something You Know

Examples:

* Password
* PIN
* Security question

---

## Something You Have

Examples:

* Smart card
* Security token
* Mobile device

---

## Something You Are

Biometric characteristics.

Examples:

* Fingerprint
* Face
* Retina
* Iris

---

## Somewhere You Are

Location-based authentication.

Examples:

* GPS location
* Network location
* Geographic restrictions

---

## Something You Do

Behavioral characteristics.

Examples:

* Typing pattern
* Signature dynamics
* Mouse movement patterns

---

# Multifactor Authentication (MFA)

MFA requires authentication using multiple **different factors**.

Example:

* Password = Something you know
* Security token = Something you have

That is MFA.

### Important

Two passwords do **not** normally count as MFA because both are the same factor category:

**Something you know.**

---

# Biometrics

Biometrics use physical or behavioral characteristics to identify users.

Examples:

* Fingerprint
* Facial recognition
* Iris recognition
* Voice recognition

### Important concepts

**False Acceptance Rate (FAR)**

A system incorrectly accepts an unauthorized person.

**False Rejection Rate (FRR)**

A system incorrectly rejects an authorized person.

---

# Security Policies

Security policies provide organizational requirements and expectations for protecting information and systems.

Examples:

* Acceptable Use Policy
* Password Policy
* Access Control Policy
* Data Retention Policy
* Incident Response Policy
* Remote Access Policy

Policies help establish consistent security practices.

---

# Procedures

Procedures provide detailed instructions for performing a task.

### Policy

Defines what is required.

### Procedure

Explains how to perform the task.

---

# Standards

Standards provide specific requirements that must be followed.

Example:

An organization requires all laptops to use full-disk encryption.

---

# Guidelines

Guidelines provide recommendations or suggested practices.

Unlike mandatory standards, guidelines are generally more flexible.

---

# Security Awareness Training

Security awareness training teaches employees how to recognize and respond to security threats.

Topics may include:

* Phishing
* Password security
* Social engineering
* Data handling
* Incident reporting
* Physical security

Security awareness training can act as an:

**Administrative + Preventive control**

---

# Social Engineering

Social engineering manipulates people into performing actions or revealing information.

Examples:

* Phishing
* Spear phishing
* Vishing
* Smishing
* Impersonation
* Tailgating
* Pretexting

The attacker targets people rather than relying only on technical vulnerabilities.

---

# Phishing

Phishing uses fraudulent messages to trick victims into revealing information or performing an action.

Example:

An attacker sends an email pretending to be a bank.

---

# Spear Phishing

Spear phishing is targeted phishing directed at a specific person or organization.

Example:

An attacker researches an employee and creates a personalized email.

---

# Whaling

Whaling is phishing specifically targeting high-profile individuals such as executives.

---

# Vishing

Voice phishing.

Uses phone calls or voice communication.

---

# Smishing

SMS phishing.

Uses text messages.

---

# Tailgating

Tailgating occurs when an unauthorized person follows an authorized person into a restricted physical area.

---

# Pretexting

Pretexting involves creating a believable story or scenario to manipulate a victim into providing information or performing an action.

---

# Honeypot

A honeypot is a system designed to attract and monitor attackers.

It appears to be a legitimate target but is primarily used for:

* Detection
* Research
* Attack analysis

---

# Honeynet

A honeynet is a network containing multiple honeypots or deliberately vulnerable systems.

It can provide a broader environment for observing attacker behavior.

---

# Honeypot vs Honeynet

**Honeypot → One deceptive system**

**Honeynet → Network of deceptive systems**

---

# Deception Technology

Deception technology uses fake systems, accounts, data, or services to detect or misdirect attackers.

Examples:

* Honeypots
* Honeynets
* Decoy accounts
* Fake credentials

---

# Secure Configuration

Secure configuration involves configuring systems according to security requirements.

Examples:

* Disable unused services
* Remove unnecessary applications
* Use strong authentication
* Apply patches
* Enable logging
* Restrict permissions
* Configure firewalls

---

# Change Management

Change management controls modifications to systems and infrastructure.

A typical change process may include:

1. Request the change
2. Analyze impact
3. Obtain approval
4. Test the change
5. Implement the change
6. Document the change
7. Verify results

The goal is to reduce unexpected outages and security problems.

---

# Configuration Management

Configuration management maintains consistent and controlled system configurations.

It can help organizations:

* Track changes
* Maintain baselines
* Identify unauthorized changes
* Keep systems consistent

---

# Vulnerability Management

Vulnerability management is the ongoing process of identifying, evaluating, prioritizing, and addressing vulnerabilities.

Typical activities include:

1. Identify assets
2. Scan for vulnerabilities
3. Analyze results
4. Prioritize vulnerabilities
5. Remediate
6. Verify remediation
7. Continuously monitor

---

# Patch Management

Patch management involves identifying, testing, approving, and deploying software updates.

Patches may address:

* Security vulnerabilities
* Bugs
* Stability problems
* Compatibility issues

---

# Security Monitoring

Security monitoring involves observing systems and network activity for suspicious or malicious behavior.

Examples:

* Log monitoring
* SIEM
* IDS/IPS
* Endpoint monitoring
* Network monitoring

---

# Key Domain 1 Exam Reminders

### CIA

**Confidentiality → Prevent unauthorized disclosure**

**Integrity → Prevent unauthorized modification**

**Availability → Keep systems accessible**

---

### AAA

**Authentication → Who are you?**

**Authorization → What can you do?**

**Accounting → What did you do?**

---

### Non-Repudiation

**Provides evidence that an action was performed by a particular entity.**

---

### Security Control Functions

**Preventive → Prevent**

**Detective → Detect**

**Corrective → Fix**

**Deterrent → Discourage**

**Compensating → Alternative**

**Directive → Tell/guide**

---

### Security Control Categories

**Technical → Technology**

**Physical → Physical protection**

**Administrative → Policies/training**

**Operational → People/processes**

---

### RTO vs RPO

**RTO → How quickly must we recover?**

**RPO → How much data can we lose?**

---

### Encryption vs Hashing

**Encryption → Confidentiality**

**Hashing → Integrity**

---

### Symmetric vs Asymmetric

**Symmetric → Same key**

**Asymmetric → Public + private keys**

---

### Authentication Factors

**Something you know**

**Something you have**

**Something you are**

**Somewhere you are**

**Something you do**

---

### Least Privilege

Give users and systems only the access they need.

---

### Defense in Depth

Use multiple layers of security controls.

---

## Domain 1 Progress

**Domain 1: General Security Concepts — Completed**

Topics covered:

* Security concepts
* CIA Triad
* Non-repudiation
* Authentication
* Authorization
* Accounting
* Security controls
* Control functions
* Control categories
* Defense in depth
* Zero Trust
* Risk concepts
* Threats and vulnerabilities
* Business impact analysis
* RTO and RPO
* Business continuity
* Disaster recovery
* Data classification
* Data states
* Encryption
* Hashing
* Digital signatures
* Digital certificates
* PKI
* Symmetric and asymmetric cryptography
* Security baselines
* Hardening
* Attack surface
* Least privilege
* Separation of duties
* Authentication factors
* MFA
* Biometrics
* Security policies
* Security awareness
* Social engineering
* Honeypots and honeynets
* Change management
* Configuration management
* Vulnerability management
* Patch management
* Security monitoring

---

*These are personal study notes created while preparing for CompTIA Security+ SY0-701. I will continue updating this repository as I progress through the remaining Security+ domains.*
