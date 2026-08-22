# Security Policy

At **ZeroState**, security and data confidentiality are our highest priorities. As a zero-knowledge password manager, **Vaulty** is designed around end-to-end local encryption, minimal attack surfaces, and strict security standards.

We take all potential security vulnerabilities seriously and appreciate the responsible disclosure of any discovered flaws.

---

## 🛡️ Supported Versions

We actively maintain and provide security updates for the following versions of Vaulty:

| Version | Supported          | Status |
| :--- | :--- | :--- |
| **v1.x (Latest Release)** | :white_check_mark: | Active Security Patches |
| **< v1.0 / Beta** | :x: | End of Life (EOL) |

*Please always ensure you are running the latest version available in the [Releases](https://github.com) tab.*

---

## 🚨 Reporting a Vulnerability

If you discover a security vulnerability or sensitive flaw within **Vaulty** (including the desktop application, Rust backend, cryptography pipeline, or Chrome Companion Extension), **please DO NOT report it via public GitHub issues, discussions, or pull requests.**

### How to Disclose Privately:
1. **Direct Security Contact**: Send a detailed report to **security@zerostate.dev** *(or open a private [GitHub Security Advisory](https://github.com))*
2. **Include Technical Details**:
   - Detailed description of the issue and potential impact
   - Step-by-step reproduction steps or a minimal Proof of Concept (PoC)
   - Relevant environment details (OS version, Chrome version, Vaulty app version)
   - Any proposed mitigations or suggested fixes (if available)

---

## ⏱️ Response Timelines & SLA

We adhere to standard coordinated vulnerability disclosure practices and commit to the following response timeline:

- **Initial Acknowledgment**: Within **24 to 48 hours** of receiving your report.
- **Triage & Assessment**: Within **3 to 5 business days**, confirming reproduction and assigning a severity rating (CVSS).
- **Patch Development & Release**: High/Critical vulnerabilities will be prioritized for expedited hotfix releases.
- **Public Disclosure**: We follow a standard **90-day responsible disclosure policy**, coordinated with the finder prior to any public release or security advisory notice.

---

## 🔒 Security Architecture Highlights

For reference, reports regarding the core security primitives should consider our design parameters:
- **KDF**: Argon2id (64 MB RAM cost, 3 iterations, 4 parallel lanes)
- **Encryption**: Authenticated AES-256-GCM with unique 96-bit nonces
- **Memory Safety**: Direct zeroization of in-memory sensitive keys via Rust's `zeroize`
- **IPC Isolation**: Local Native Messaging protocol with strict origin validation

---

<div align="center">

Thank you for helping keep **Vaulty** and our users safe!  
Developed with ❤️ by **ZeroState**

</div>
