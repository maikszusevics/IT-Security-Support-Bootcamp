# Fundamental Cybersecurity Concepts
> This is a work in progress based on the [Pluralsight General Security Concepts for CompTIA Security+](/Learning/Pluralsight/INCOMPLETE-General-Security-Concepts-for-CompTIA-Security+.md) course.

### CIA Triad (Confidentiality, Integrity, and Availability)
Three elements that help ensure that data is kept secure, accurate, and accessible to authorised users.
#### Confidentiality 
- Privacy
- Encryption or 2FA
- Airgaps
#### Integrity
- Consistency and accuracy
- File permissions/access control
- Version control
#### Availability
- Consistent Availability
- Patches, updates
- Backups, DR/HA
### Non-repudiation
The assurance that someone cannot deny the validity of something.
A service that is maintained so that a sender and recipient cannot deny having participated in the communication.

PKI (public key infrastructure) can provide non-repudiation through the use of public/private keys. Assuming that a user keeps his private key secure, data encrypted via that private key could only originate from that user.
### Authentication, Authorisation, and Accounting (AAA)

Authentication identifies the user and allows (or denies) access based on available and necessary credentials.

Authorisation provides things like length of time allowed on the network, controls who has access to certain folders, files, or storage locations, and to what extent do their permissions allow them to make change.

Accounting tracks the start and stop time of each session - can be used for billing or general tracking.

##### Identification vs Authentication vs Authorisation
Identification is who you are. This can be labelled via username, securityID, smart card. Authentication is proving who you are, this can be done via username-password combo, OTP, or biometric data like fingerprint or retina scan. Authorisation is what permissions you have, it's what you're allowed to access and do once you've been authenticated.

#### Authentication Factors

- Something you know
	- Password or "secret"
- Something you are
	- Fingerprint, retina scan, etc.
- Something you have
	- Smart card, token, two-factor code, etc.
- Somewhere you are
	- Location based
- Something you do
	- Signature, patterns of behaviour or language, etc.
- Someone you know
	- Social proof, having a friend or colleague "vouch" for you

#### Authenticating Systems
##### Multifactor Authentication
- Two or more pieces of information used to authenticate
	- Pin
	- Password
	- Fingerprint
- Must be from different categories
	- **Password and PIN would only be 1-factor because they both fall under "something you know"**

### Gap Analysis
Process of identifying and evaluating the discrepancies or "gaps" between an organisation's current security measures and its desired or required security posture.

### Zero Trust
#### Control Plane
##### Adaptive Identity
##### Threat Scope Reduction
##### Policy-Driven Access Control
##### Policy Administrator
##### Policy Engine

### Data Plane

#### Implicit Trust Zones
#### Subject/System

#### Policy Enforcement Point

### Physical Security

#### Bollards
#### Access Control Vestibule (Mantrap)

#### Fencing

#### Video Surveillance
#### Security Guard
#### Access Badge
#### Lighting
#### Sensors
##### Infrared Pressure
##### Microwave
##### Ultrasonic
### Deception and Disruption technology
#### Honeypot
#### Honeynet
#### Honeylife
#### Honeytoken
