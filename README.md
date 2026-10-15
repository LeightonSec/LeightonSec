# LeightonSec

Security tooling and research: detection engineering, AI security, OT/ICS and GRC.
I don't trust a security claim, including my own, until I've seen the raw evidence behind it.

## Focus Areas

**Detection & Threat Intelligence**: network analysis, threat intelligence pipelines and detection tooling, with adversarial test coverage and regression locks.

**AI Security**: detecting prompt injection, jailbreaks and adversarial inputs against LLMs. Weighted scoring, evasion-resistant signatures and false-positive tuning.

**OT/ICS**: Modbus TCP anomaly detection and Purdue-model IT/OT boundary analysis.

**GRC & Compliance**: NIS2 vendor risk frameworks, MFA audit tooling and policy assessment aligned to EU and NCSC standards.

**Post-Quantum Cryptography**: sovereign communication protocols resistant to quantum attack.

## Projects

| Repository | Description |
|---|---|
| [ai-firewall](https://github.com/LeightonSec/ai-firewall) | LLM prompt injection and jailbreak detection. Tiered weighted scoring, evasion-resistant signatures, adversarial test suite. 82 tests, CI green. |
| [security-gate](https://github.com/LeightonSec/security-gate) | Self-enforcing static analysis gate. 20 scanners, 201 tests, CI with real teeth. Caught and patched a live CVE (GHSA-6v7p-g79w-8964) in its own dependency graph. Scanners cover .py and .ts; SCA covers Python dependencies only.
| [modbus-sentinel](https://github.com/LeightonSec/modbus-sentinel) | Modbus TCP anomaly detector with a fail-closed MBAP parser. 62 tests, 98% coverage. |
| [cascade-map](https://github.com/LeightonSec/cascade-map) | Models how NIS2 vendor risk cascades into failure, with a Purdue/IT-OT boundary overlay. v0.3.0, 115 tests. |
| [security-toolkit](https://github.com/LeightonSec/security-toolkit) | Modular web log analyser. SQLi detection hardened against string-boolean and comment-terminator evasion. 31-test adversarial suite with locked regression cases. |
| [llm-honeypot](https://github.com/LeightonSec/llm-honeypot) | Fake AI assistant that silently logs and classifies attack attempts. Detects prompt injection, jailbreaks, data extraction, and reconnaissance. |
| [password-policy-checker](https://github.com/LeightonSec/password-policy-checker) | Password policy evaluator against NIST SP 800-63B and NCSC guidance, with HaveIBeenPwned k-anonymity breach checking. |
| [port-scanner](https://github.com/LeightonSec/port-scanner) | TCP connect port scanner with banner grabbing, CIDR support, and JSON/Markdown output. |
| [nis2-vendor-risk-framework](https://github.com/LeightonSec/nis2-vendor-risk-framework) | NIS2-aligned third-party risk assessment framework with scoring rubric and worked example. |
| [mfa-coverage-tracker](https://github.com/LeightonSec/mfa-coverage-tracker) | M365 MFA audit tool that identifies weak or missing MFA, generates HTML risk reports. |
| [intel-pipeline](https://github.com/LeightonSec/intel-pipeline) | Automated threat intelligence collection and processing pipeline. |
| [pcap-analyser](https://github.com/LeightonSec/pcap-analyser) | Network packet capture analysis and anomaly detection. |
| [incident-tracker](https://github.com/LeightonSec/incident-tracker) | SOC incident ticketing and case management system. |
| [unified-dashboard](https://github.com/LeightonSec/unified-dashboard) | Single pane of glass across the security toolkit. |

## About

Security engineer with a background in IT infrastructure and NHS
deployment. CompTIA Security+ and Network+ certified, eAIS in progress.

Every project ships with a quality gate, adversarial test coverage, and
documented design decisions. The gate enforces itself. Automated gate coverage is Python and TypeScript.

Targeting OT/ICS threat detection and AI security engineering roles.

→ [bastionprotocol.org](https://bastionprotocol.org)
