# 🦉 OSssdX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCore-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OSssdX** — Offline SSSD / NSS / realmd Client Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline SSSD / nsswitch / krb5 / realmd identity-client configuration auditor

---

## ✨ Features

- Offline, read-only auditor for the Linux identity *client* stack (SSSD, NSS, Kerberos, realmd)
- sssd.conf parser with conf.d snippet merging, per-domain analysis (ldap / ad / ipa / krb5 / proxy)
- Transport checks — ldap:// without StartTLS, tls_reqcert never/allow, TLS-disable kill switch
- Credential exposure — plaintext / obfuscated bind passwords (always masked), offline password caching
- Access control — permit / missing access_provider, empty simple allow lists, GPO permissive, min_id
- nsswitch.conf — direct ldap/nis sources, ordering, sudoers / automount source hygiene
- krb5.conf — weak crypto, DES/RC4 enctypes, rdns, DNS realm lookup, forwardable, lifetimes, PKINIT
- realmd.conf — residual one-time passwords (masked), automatic join, insecure home / shell defaults
- File permission checks (sssd.conf, keytab, cache)
- CWE + MITRE ATT&CK mapping, score & grade
- Exports TXT / MD / JSON / CSV / SARIF 2.1.0
- Hardened templates, rule catalogue, --explain
- Self-test --demo with weak + hardened fixtures

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OSssdX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
