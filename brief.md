Version: NAFATH-V4
Track: Cybersecurity

## Overview

Securing a national service provider requires visibility and control across the software supply chain. The Twelve-Factor App approach separates configuration and secrets from application code, while AI security practices address attacks that manipulate model inputs or training data. OWASP MASVS provides a structured way to assess mobile application security. In networking, RPKI helps validate whether an autonomous system is authorized to announce an IP prefix, reducing certain BGP hijacking risks. Cybersecurity teams must identify and remediate vulnerabilities such as Log4Shell, while a Software Bill of Materials (SBOM) helps track software components and their dependencies. These measures complement one another: secure configuration reduces exposure, verification and monitoring help detect weaknesses, and component inventories support faster vulnerability response. For my Cybersecurity track, I would next investigate how organizations identify every affected dependency and verify that Log4Shell fixes have been deployed across their systems.

## Software

The Twelve-Factor App methodology suggests that deployment-specific settings should be stored in environment variables instead of being hard-coded into the application code. These settings can include database credentials, service tokens, and other values that might vary between different environments. By separating configuration from the code, applications become more manageable to deploy across various environments and help minimize the risk of exposing sensitive information when code is shared or released. It is still essential to safeguard sensitive information with proper access controls.
Resource: The Twelve-Factor App — Config - https://12factor.net/config
## AI

Adversarial machine learning attacks target the behaviour or reliability of machine-learning systems. Evasion attacks manipulate inputs during model use so that the model produces incorrect predictions, while poisoning attacks interfere with training data or the training process to influence what the model learns. The difference is mainly when and how the attack occurs. Defences include validating data, monitoring model behaviour, and testing systems against realistic threats.
Resource: NIST — Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations - https://csrc.nist.gov/pubs/ai/100/2/e2025/final

## Mobile

The OWASP Mobile Application Security Verification Standard (MASVS) is a security standard used to assess mobile applications against defined security controls. It covers areas such as secure data storage, cryptography, authentication, network communication, platform interaction, code quality, resilience, and privacy. Developers and security testers can use these controls to guide security reviews and testing. MASVS provides a structured baseline for verification, but it does not guarantee that an application is completely secure.
Resource: OWASP — Mobile Application Security Verification Standard (MASVS) - https://mas.owasp.org/MASVS/

## Networking

BGP route hijacking occurs when an autonomous system announces IP address prefixes that it is not authorized to originate, potentially redirecting traffic through an unintended network. Resource Public Key Infrastructure (RPKI) allows prefix holders to publish cryptographically signed Route Origin Authorizations (ROAs). Routers can validate whether a route's originating AS is authorized and apply policies to invalid announcements. However, origin validation does not verify the entire AS path or prevent every routing attack.
Resource: RFC 6811 - BGP Prefix Origin Validation - https://www.rfc-editor.org/rfc/rfc6811

## Cybersecurity

Log4Shell (CVE-2021-44228) was a critical remote code execution vulnerability in Apache Log4j 2, a widely used Java logging library. In affected configurations, an attacker could exploit specially crafted input to trigger lookups and potentially execute code on a vulnerable server. Its widespread use and the possibility of remote exploitation made it especially dangerous. The primary mitigation was to upgrade to a fixed Log4j version, identify affected applications, and apply vendor-recommended mitigations where immediate upgrading was not possible.
Resource: NVD - CVE-2021-44228 Detail - https://nvd.nist.gov/vuln/detail/CVE-2021-44228

## Data

A Software Bill of Materials (SBOM) is a structured inventory of software components and their dependencies. It helps organizations identify affected products when a vulnerability is discovered and understand the software they use or distribute. The NTIA minimum elements include supplier name, component name, version, other unique identifiers, dependency relationships, SBOM author, and timestamp. An SBOM improves visibility, but it does not automatically prove that software is secure or free from vulnerabilities.
Resource: NTIA - The Minimum Elements for a Software Bill of Materials (SBOM) - https://www.ntia.gov/report/2021/minimum-elements-software-bill-materials-sbom

## Misconception in My Track

A common misconception is that updating the logging library in one application automatically secures every system in an organization. In reality, Log4Shell risk depends on which Log4j versions and affected configurations are present across applications and dependencies. Organizations must identify affected systems, apply the appropriate fixed versions or vendor-recommended mitigations, and verify that the changes have been deployed. The Apache Log4j security page documents the vulnerability and its affected versions, showing why software inventory and systematic remediation are necessary.
Evidence source: Apache Log4j Security Vulnerabilities, section “CVE-2021-44228”. https://logging.apache.org/log4j/2.x/security.html

## Open Question

How can organizations reliably identify vulnerable versions of open-source dependencies across applications and transitive dependencies, and verify that security fixes have reached every affected production system?
