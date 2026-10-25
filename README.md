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


OSssdX is an offline, read-only auditor for the Linux identity-client stack: SSSD, NSS, Kerberos and realmd. It parses sssd.conf (with conf.d merging and per-domain analysis), checks LDAP transport security, credential exposure, access-control gaps, nsswitch ordering and krb5 crypto. Secrets are always masked, findings are mapped to CWE and MITRE ATT&CK, and reports export to TXT, Markdown, JSON, CSV or SARIF.

---

## ✨ Features


- sssd.conf parser with conf.d snippet merging and per-domain analysis (ldap/ad/ipa/krb5/proxy)
- Transport checks: ldap:// without StartTLS, tls_reqcert never/allow, TLS-disable kill switch
- Credential exposure: plaintext/obfuscated bind passwords (masked) and offline password caching
- Access control: permit / missing access_provider, empty allow lists, permissive GPO, min_id
- nsswitch.conf source/ordering hygiene and krb5.conf weak-crypto (DES/RC4), rdns and lifetime checks
- File-permission checks, CWE+ATT&CK mapping, score/grade and TXT/MD/JSON/CSV/SARIF export

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OSssdX --scan -f sarif -o sssd.sarif
./OSssdX --sssd /etc/sssd/sssd.conf --krb5 /etc/krb5.conf
./OSssdX --root /mnt/image --fail-on high
./OSssdX --demo
./OSssdX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
