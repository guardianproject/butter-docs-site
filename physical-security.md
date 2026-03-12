---
description: How to Make a Butter Box Tamper Resistant
---

# Physical Security

This guide was designed for deployments in hostile, semi-hostile, or low-trust environments, where devices may be inspected, confiscated, modified, or misused. It aims to provide practical recommendations to make the RCBox more physically and digitally tamper-resistant.&#x20;

Following the recommendations in this guide will help reduce risk, not guarantee absolute security. RCBox is assumed to be a field-deployable, low-cost, offline system, so these recommendations prioritize realistic, maintainable protections.

### 1. Threat Model Assumptions

Before applying controls, clearly define your deployment context. This guide assumes one or more of the following risks:

* Physical access by unauthorized users
* Device confiscation or inspection by authorities
* Curious or malicious local users
* Content manipulation or replacement
* Network misuse or impersonation
* Credential reuse or default configuration abuse

Remember that controls should adapt to the local risk level, over-hardening can reduce usability and trust.



### 2. Physical Tamper Resistance

#### Enclosure and  Hardware Protection

Physical access to the RCBox allows SD card cloning, firmware replacement, malware injection and broadcasting of malicious information. PCB are also delicate and should have additional protection to keep them safe from everyday handling and weather exposure.



Recommendations:

* Use a sealed or semi-sealed enclosure (screws instead of snap-fit)

![](.gitbook/assets/unknown.jpeg)

* Prefer tamper-evident screws (Torx, security hex)

![](<.gitbook/assets/unknown (1).jpeg>)

* Apply tamper-evident stickers over enclosure seams and SD card slots

![](<.gitbook/assets/unknown (2).jpeg>)

<br>

#### SD Card & Storage Protection

Recommendations:

* Use high-quality SD cards to reduce corruption
* Encrypt sensitive partitions (where feasible)
* Keep content and OS separated (firmware vs content packs)
* Avoid labeling SD cards with sensitive identifiers

Optional (higher risk contexts):

* Epoxy Resin. Electronico potting solutions ​​protect Printed Circuit Boards from extreme temperatures, moisture, vibration, and other environmental threats.



| ![](<.gitbook/assets/unknown (3).jpeg>) | ![](<.gitbook/assets/unknown (4).jpeg>) |
| --------------------------------------- | --------------------------------------- |

<br>

* Physically block SD card removal

![](<.gitbook/assets/unknown (5).jpeg>)

#### Power & Port Management

Recommendations:

* Disable or physically block unused ports (USB, HDMI). Inexpensive physical port blockers can be used to reduce the risk of tampering with the RCBox by preventing unauthorized access to exposed interfaces. These blockers limit the ability of bad actors to inject malicious code, connect unauthorized peripherals, or broadcast unwanted content. Ports are sealed with plastic blockers that can only be removed using a dedicated key included in the deployment kit.

![](<.gitbook/assets/unknown (6).jpeg>)

* Avoid exposing Ethernet ports unless required. Ethernet ports should remain disabled or physically blocked unless they are explicitly required for the deployment. When Ethernet access is necessary, its use should be clearly documented and limited to trusted operators.

![](<.gitbook/assets/unknown (7).jpeg>)

* Use short internal cables to reduce easy probing
* Label power banks generically (avoid project names)

<br>

#### Environmental & Operational Practices

Recommendations:

* Store boxes in controlled locations when not in use
* Rotate devices periodically in long deployments
* Assume devices may be copied or lost

Treat RCBoxes as semi-disposable infrastructure, not personal devices.

<br>

### Digital Tamper Resistance

#### Credential Hygiene (Critical)

Mandatory actions:

SSH

* By default, the pi user has the password butterbox-admin.
* Change this password by sshing into the pi and running passwd.
* If you'd prefer to use an SSH key, be sure to disable password access once you enable key-based access.

RaspAP

* The access point has an administrative interface that can be used to change its settings.
* Defaults: user: admin, password: secret (ironically, this is not secret).
* Change this by logging in at[ http://butterbox.lan/admin](http://butterbox.lan/admin) (or[ http://comolamantequilla.lan/admin](http://comolamantequilla.lan/admin) for a Spanish language box) and using the Web UI.

Chat

* The public room was created by an administrative user called butterbox-admin. The password for this user is also butterbox-admin.
* Change this password by logging into the Butter Box, going to the public chatroom, then visiting your user profile and updating the password. At your discretion, you may also wish to change the name from butterbox-admin so that other users will recognize you.

Best practices:

* Use unique passwords per deployment
* Store credentials offline in secure documentation
* Never reuse credentials across regions<br>

#### Service Hardening

Recommendations:

* Disable services not strictly required:
* SSH (or restrict to key-based auth)
* Bluetooth
* USB ports



#### Content Integrity & Authenticity

Recommendations:

* Keep firmware immutable during normal operation
* Maintain a known-good baseline image
* Re-flash devices periodically in long deployments

Operational control:

* Only trusted operators should install or update content
* Document update sources and dates



### Misuse & Abuse Mitigation

#### Offline Chat & Messaging Risks

Risks:

* Harassment or hate speech
* Impersonation
* Disinformation spread

Mitigations:

* Clear usage guidelines displayed locally
* Community moderation roles (if appropriate)
* Ability to reset or wipe chat data quickly



#### Content Abuse

Mitigations:

* Limit who can upload or replace content
* Keep a read-only mode for most users



### Incident Response & Recovery

Prepare for compromise:

* Assume some devices will be tampered with
* Maintain a simple wipe and re-flash procedure
* Track deployments

<br>
