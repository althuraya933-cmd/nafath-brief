Version: NAFATH-V4
Track: Cybersecurity

## Overview

A secure software supply chain necessitates a coordinated strategy to safeguard software development, artificial intelligence, mobile applications, networks, cybersecurity, and data management. Proper handling of software configurations and secrets is crucial to minimize the risk of disclosing sensitive data. AI systems must be secured against attacks that can alter inputs or compromise training data. Mobile applications ought to be evaluated according to established security criteria, while network operators may implement routing security measures to mitigate the chances of BGP route hijacking. Well-known vulnerabilities, like Log4Shell, highlight the importance of prompt patching and effective dependency management. A Software Bill of Materials (SBOM) enables organizations to pinpoint the components within their software and evaluate potential vulnerability exposures. Together, these practices improve visibility, reduce security risks, and help organisations make informed decisions about the technologies and suppliers they trust.

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

## Open Question
