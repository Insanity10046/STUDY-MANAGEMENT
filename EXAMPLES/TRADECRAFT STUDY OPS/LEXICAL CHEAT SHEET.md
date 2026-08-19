
---

## 1. INFORMATION RECONNAISSANCE PILLAR

| TERM | MEANING | FUNCTION: WHY | PRIMARY CONSTRAINT: HOW |
|---|---|---|---|
| **Pivoting** | Using one identifier to find another, e.g. username → email → breach data → phone number. | Expands target footprint and correlates identities. | Work from a known seed; do not mix collection with personal accounts. |
| **Username pivoting** | Checking a known username across multiple platforms to find other accounts. | Maps the target’s account presence. | Use non-attributable sessions; avoid logging into target services. |
| **Email-based pivoting** | Using a known email to find personal emails, usernames, or breach data. | Identifies associated accounts and exposure. | Verify breach data; treat as unverified until corroborated. |
| **Reverse image search** | Searching a photo to find where else it appears. | Reveals stolen, synthetic, or reused images. | Use multiple engines; images may be altered or cropped. |
| **Directory mapping** | Using workplace listings to identify colleagues, reporting chains, and structure. | Builds organizational picture and access paths. | Keep collection passive; do not access non-public systems. |
| **Search dorking** | Using advanced operators like `site:`, `filetype:`, `intitle:`. | Surfaces hidden or indexed data. | Stay within legal search access; document queries. |
| **Metadata extraction** | Pulling hidden data from files/images, e.g. GPS, device, timestamps. | Attributes location, device, and time. | Validate authenticity; avoid opening untrusted files outside a sandbox. |
| **Link charting** | Visually mapping relationships between people, accounts, emails, and organizations. | Identifies central nodes and indirect connections. | Distinguish confirmed vs. inferred links; update continuously. |
| **OSINT** | Collection from publicly available information. | Creates baseline target understanding without direct contact. | Cite sources; avoid tipping the target. |
| **Passive reconnaissance** | Observing without interacting with the target. | Reduces risk of detection. | Do not trigger logs or alerts. |
| **Active reconnaissance** | Interacting with target systems or people. | Obtains deeper data than passive recon. | Use cover or disposable infrastructure; risk of burning. |
| **Social network analysis** | Mapping relationships, roles, and influence. | Identifies access paths and gatekeepers. | Protect the source of the graph; inferential links must be marked. |
| **Pattern-of-life analysis** | Observing routines over time. | Predicts windows, habits, and vulnerabilities. | Avoid alerting target; store data securely. |
| **Breach data aggregation** | Combining leaked datasets to build identity maps. | Recovers credentials, emails, and associations. | Handle exposed PII lawfully; do not re-victimise. |
| **Digital exhaust analysis** | Analyzing cookies, analytics, metadata, and account traces. | Infers habits, devices, and affiliations. | Collect only what is necessary; minimize retention. |
| **GEOINT / geospatial intelligence** | Using imagery and location data. | Locates physical footprint and movements. | Use commercial or open imagery legally. |
| **Dark web monitoring** | Observing forums, markets, or leaks on hidden services. | Detects exposure, breached data, or threat activity. | Use isolated environment and Tor; do not transact illegally. |

---

## 2. INFORMATION PROTECTION PILLAR

| TERM | MEANING | FUNCTION: WHY | PRIMARY CONSTRAINT: HOW |
|---|---|---|---|
| **OPSEC five-step** | Identify critical info, threat, vulnerabilities, risk, countermeasures. | Protects the operation from adversary collection. | Run continuously; not a one-time checklist. |
| **Threat modeling** | Determining adversary capability, intent, and opportunity. | Focuses defenses on likely attack paths. | Update as environment or mission changes. |
| **Attack surface reduction** | Minimizing exposed digital and physical information. | Reduces available points of compromise. | Regular audits; remove unnecessary accounts and data. |
| **Digital fingerprinting** | Unique browser/device characteristics used for tracking. | Avoids linking operational activity to real identity. | Use clean devices, separate profiles, and hardened browsers. |
| **Metadata discipline** | Stripping EXIF, timestamps, author data before upload. | Prevents accidental location or device disclosure. | Automate stripping; never upload raw operational files. |
| **Compartmentalization** | Separating identities, devices, and information by need-to-know. | Contains damage if one component is compromised. | No cross-linking between real and operational identities. |
| **Secure communications** | Use of E2E encryption, Signal, PGP, verified keys. | Protects message content and metadata. | Verify fingerprints out-of-band; avoid cleartext. |
| **SIM-swap defense** | Using non-SMS 2FA, carrier lock, and hardware tokens. | Prevents account takeover via phone number theft. | Never rely on SMS for critical accounts. |
| **Countersurveillance** | Detecting hostile observation or following. | Identifies surveillance before an operation. | Use route variation, choke points, and observation stops. |
| **IMSI catcher detection** | Detecting fake cell towers or unusual baseband activity. | Avoids location interception. | Monitor network anomalies; use RF detection tools. |
| **Faraday bag** | RF-blocking enclosure for devices. | Prevents tracking or remote access. | Test effectiveness; devices may still log locally. |
| **Canary tokens / honeypots** | Bait files or accounts that alert when opened. | Detects intrusion or unauthorized access. | Deploy in plausible locations; monitor alerts. |
| **Burner phone discipline** | Using prepaid phones paid with cash and used only in non-associated areas. | Maintains non-attributable communications. | Never link to real identity, accounts, or locations. |
| **Tails / amnesic OS** | Live operating system that leaves no local trace. | Reduces forensic residue. | Use on untrusted hardware; do not persist data. |
| **Data minimization** | Collecting and retaining only necessary information. | Limits damage if compromised. | Delete or compartmentalize data after use. |
| **Domain registration age / WHOIS** | Checking how long a domain has existed and who registered it. | Flags newly registered or suspicious domains. | Passive lookup; do not rely on this alone. |
| **Website content / cached pages** | Reviewing whether a site is shallow, templated, or broken. | Detects phishing or synthetic legitimacy. | Use cache/archive services; do not enter credentials. |
| **Reverse image search** | Checking whether a profile photo is stolen, reused, or AI-generated. | Detects fake personas. | Cross-check multiple engines. |
| **Connection** | Examining whether an account has a realistic network. | Validates social graph authenticity. | Mutual connections can be fabricated; treat as clue, not proof. |
| **Posting history** | Checking whether posts are original, recycled, or low-effort. | Detects sock puppets and synthetic accounts. | Analyze cadence, language, and content depth. |
| **Email header analysis** | Inspecting SPF, DKIM, DMARC, and routing headers. | Detects spoofed or forged email. | Read raw headers, not just display name. |
| **Carrier lookup** | Determining whether a phone number matches claimed location or is VoIP/burner. | Validates contact authenticity. | Numbers can be ported; use as one signal. |
| **Metadata consistency** | Comparing persona photos, timestamps, and devices against claimed identity. | Detects legend discrepancies. | Check timezone, device, editing artifacts. |
| **Out-of-band verification** | Confirming a request through a separate known channel. | Defeats impersonation. | Use pre-established contact info, not info in the message. |
| **Challenge-response authentication** | Asking a pre-agreed code word or question. | Authenticates a live correspondent. | Avoid predictable answers; rotate codes. |
| **Deepfake / voice-clone detection** | Analyzing audio or video for synthetic artifacts. | Detects AI-generated impersonation. | Use multimodal cues; do not rely on one tool. |
| **Caller ID spoofing** | Faking the displayed phone number. | Enables vishing or impersonation. | Defenders should never trust caller ID alone; call back known number. |

---

## 3. INFORMATION CONSTRUCTION PILLAR

| TERM | MEANING | FUNCTION: WHY | PRIMARY CONSTRAINT: HOW |
|---|---|---|---|
| **Cover for status** | Long-term stable identity explaining who you are and why you are present. | Establishes legitimacy over time. | Maintain consistent backstory, documentation, and behavior. |
| **Cover for action** | Specific operational cover for a particular mission or action. | Explains current activity under the status cover. | Align with status cover; minimize deviation. |
| **Legend** | A detailed false biography. | Supports cover and withstands scrutiny. | Make it plausible, verifiable, and not over-documented. |
| **Backstopping** | Creating supporting artifacts such as documents, social media, references. | Makes the legend survive background checks. | Ensure consistency across all channels. |
| **Persona** | A constructed digital identity. | Presents a false identity online. | Use separate device/network; build realistic history. |
| **Sock puppet** | A fake online account controlled by an operator. | Engages without attribution. | Age accounts; avoid cross-linking with real identity. |
| **Natural cover** | Using a real existing identity or profession as cover. | Reduces fabrication burden. | Limits operational freedom; real identity may be exposed. |
| **Artificial cover** | Fabricated identity or employment. | Gives full control of backstory. | High maintenance; high risk if probed. |
| **Official cover** | Government or diplomatic status used as cover. | Provides legal or consular protection. | Subject to host-country surveillance; not deniable. |
| **Non-official cover (NOC)** | No visible government tie. | Provides deniability. | No diplomatic immunity; high consequence if burned. |
| **Digital consistency** | Timezone, language, browser fingerprint, and device alignment with persona. | Avoids pattern mismatch and OSINT discovery. | Never log real and persona identities on same device. |
| **Account aging** | Creating accounts and letting them sit before operational use. | Makes accounts appear established. | Occasional benign activity; avoid sudden operational use. |
| **Content seeding** | Populating a persona with original posts and photos over time. | Gives the identity substance. | Avoid reverse-image ties; use original or cleared media. |
| **Pretext development** | Crafting a false reason or role for approach. | Justifies contact or request. | Fit the target’s expectations; rehearse. |
| **Red-team legend test** | Stress-testing an identity against investigation. | Finds weak points before adversary does. | Use independent assessor; update legend. |
| **Plausible deniability** | Designing an operation so involvement can be denied. | Protects identity and mission. | Avoid direct evidence linking real person to action. |

---

## 4. INFORMATION MANIPULATION PILLAR

| TERM | MEANING | FUNCTION: WHY | PRIMARY CONSTRAINT: HOW |
|---|---|---|---|
| **Elicitation** | Covertly drawing out information in normal conversation. | Collects without direct questioning. | Use open-ended, non-suspicious framing. |
| **Flattery** | Praise to lower defenses and encourage disclosure. | Makes target feel valued and talkative. | Keep credible; do not overdo. |
| **Feigned ignorance** | Pretending not to know something so the target explains it. | Reveals details the target assumes are known. | Avoid appearing totally incompetent. |
| **Bracketing** | Asking for exact data using estimates, e.g. “salary around 80?” | Elicits confirmation or correction. | Use plausible ranges; do not guess too precisely. |
| **Active listening** | Restating, clarifying, and validating to encourage disclosure. | Builds rapport and deeper sharing. | Do not over-mirror or sound mechanical. |
| **Mirroring** | Imitating body language, pace, tone, or phrasing. | Increases liking and unconscious rapport. | Keep subtle; avoid obvious mimicry. |
| **Rapport building** | Creating trust and mutual identification. | Lowers resistance and increases cooperation. | Gradual and context-appropriate. |
| **Pretexting** | Using a fabricated story or role to obtain information or access. | Gains trust and justifies requests. | Keep coherent with persona and cover. |
| **Phishing** | Mass deceptive emails. | Harvests credentials or delivers malware. | Use plausible domains; avoid obvious red flags. |
| **Spear phishing** | Targeted phishing against a specific individual or organization. | Increases success through personalization. | Research target; personalize; use clean infrastructure. |
| **Vishing** | Voice phishing by phone. | Manipulates via real-time vocal interaction. | Use controlled caller ID; know the script. |
| **SMiShing** | SMS phishing. | Delivers malicious links or requests via text. | Short, urgent, plausible message. |
| **Baiting** | Offering something enticing such as USB drives, downloads, or prizes. | Exploits curiosity or greed. | Drop infected media in target area; use plausible lure. |
| **Tailgating** | Following an authorized person into a secure area. | Gains physical access. | Use confidence and appropriate props. |
| **Quid pro quo** | Offering help or benefit in exchange for information or access. | Creates a reciprocal exchange. | Offer should be plausible and low-suspicion. |
| **Cialdini principles** | Reciprocity, commitment/consistency, social proof, authority, liking, scarcity. | Leverages predictable influence triggers. | Choose the principle fitting the target and context. |
| **Authority misrepresentation** | Pretending to be authority, IT, executive, or official. | Induces compliance. | Backstop with badge, email signature, or uniform. |
| **Urgency / scarcity** | Pressuring the target to act quickly or risk loss. | Bypasses rational verification. | Avoid excessive pressure; keep threat credible. |
| **Fear appeal** | Threat of loss, legal action, or security breach. | Triggers immediate action. | Credible threat; do not overstate. |
| **Foot-in-the-door** | Small request followed by larger one. | Uses commitment/consistency to gain compliance. | Sequence gradually. |
| **Door-in-the-face** | Large request refused, then smaller request accepted. | Exploits reciprocal concession. | Large request must be plausible enough to be refused. |

---
