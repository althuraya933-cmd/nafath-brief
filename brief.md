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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
