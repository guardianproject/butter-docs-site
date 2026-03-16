---
description: How to Make a Butter Box Tamper Resistant
---

# Security

This guide was designed for deployments in hostile, semi-hostile, or low-trust environments, where devices may be inspected, confiscated, modified, or misused. It aims to provide practical recommendations to make the RCBox more physically and digitally tamper-resistant.&#x20;

Following the recommendations in this guide will help reduce risk, not guarantee absolute security. RCBox is assumed to be a field-deployable, low-cost, offline system, so these recommendations prioritize realistic, maintainable protections.

**Threat Model Assumptions**

Before applying controls, clearly define your deployment context. This guide assumes one or more of the following risks:

* Physical access by unauthorized users
* Device confiscation or inspection by authorities
* Curious or malicious local users
* Content manipulation or replacement
* Network misuse or impersonation
* Credential reuse or default configuration abuse

Remember that controls should adapt to the local risk level, over-hardening can reduce usability and trust.

### Section 1: Physical Tamper Resistance

#### Enclosure and  Hardware Protection

Physical access to the Butter Box allows SD card cloning, firmware replacement, malware injection and broadcasting of malicious information. PCB are also delicate and should have additional protection to keep them safe from everyday handling and weather exposure.

Recommendations:

1. Use a sealed or semi-sealed enclosure (screws instead of snap-fit)
2. Prefer tamper-evident screws (Torx, security hex)
3. Apply tamper-evident stickers over enclosure seams and SD card slots

<figure><img src=".gitbook/assets/media-type-placeholder.png" alt=""><figcaption></figcaption></figure>

#### SD Card & Storage Protection

Recommendations:

1. Use high-quality SD cards to reduce corruption
2. Encrypt sensitive partitions (where feasible)
3. Keep content and OS separated (firmware vs content packs)
4. Avoid labeling SD cards with sensitive identifiers

Optional (higher risk contexts):

1. Epoxy Resin. Electronico potting solutions ​​protect Printed Circuit Boards from extreme temperatures, moisture, vibration, and other environmental threats.
2. Physically block SD card removal



<table data-header-hidden><thead><tr><th>Epoxy Resin</th><th>Epoxy Resin</th><th data-type="image">Lock Box</th></tr></thead><tbody><tr><td><img src=".gitbook/assets/unknown (3).jpeg" alt=""></td><td><img src=".gitbook/assets/unknown (4).jpeg" alt=""></td><td><a href=".gitbook/assets/unknown (5).jpeg">unknown (5).jpeg</a></td></tr></tbody></table>

#### Power & Port Management

Recommendations:

1. Disable or physically block unused ports (USB, HDMI). Inexpensive physical port blockers can be used to reduce the risk of tampering with the Butter Box by preventing unauthorized access to exposed interfaces. These blockers limit the ability of bad actors to inject malicious code, connect unauthorized peripherals, or broadcast unwanted content. Ports are sealed with plastic blockers that can only be removed using a dedicated key included in the deployment kit.
2. Avoid exposing Ethernet ports unless required. Ethernet ports should remain disabled or physically blocked unless they are explicitly required for the deployment. When Ethernet access is necessary, its use should be clearly documented and limited to trusted operators.
3. Use short internal cables to reduce easy probing
4. Label power banks generically (avoid project names)

<table data-header-hidden><thead><tr><th>USB &#x26; HDMI</th><th>Ethernet Ports</th><th data-type="image"></th></tr></thead><tbody><tr><td><img src=".gitbook/assets/unknown (6).jpeg" alt=""></td><td><img src=".gitbook/assets/unknown (7).jpeg" alt=""></td><td></td></tr></tbody></table>

#### Environmental & Operational Practices

Recommendations:

* Store boxes in controlled locations when not in use
* Rotate devices periodically in long deployments
* Assume devices may be copied or lost
* Treat Butter Boxes as semi-disposable infrastructure, not personal devices.<br>

### Section 2: Digital Tamper Resistance

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

* The local chat was created by an administrative user called butterbox-admin. The password for this user is also butterbox-admin.
* Change this password by logging into the Butter Box, going to the public chatroom, then visiting your user profile and updating the password. At your discretion, you may also wish to change the name from butterbox-admin so that other users will recognize you.

Best practices:

* Use unique passwords per deployment
* Store credentials offline in secure documentation
* Never reuse credentials across regions

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



### Section 3: Misuse & Abuse Mitigation

#### Local Chat & Content Abuse

Risks:

* Harassment or hate speech
* Impersonation
* Disinformation spread

Mitigations:

* Clear usage guidelines displayed locally
* Community moderation roles (if appropriate)
* Ability to reset or wipe chat data quickly
* Limit who can upload or replace content
* Keep a read-only mode for most users



### Section 4: Incident Response & Recovery

Prepare for compromise:

* Assume some devices will be tampered with
* Maintain a simple wipe and re-flash procedure
* Track deployments

<br>
