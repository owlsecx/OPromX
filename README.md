# 🦉 OPromX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OPromX** — Prometheus Monitoring-Stack Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Prometheus / Alertmanager / exporter configuration security auditor

---

## ✨ Features

- Stdlib YAML-subset parser with per-key line numbers
- prometheus.yml / web-config.yml / alertmanager.yml / blackbox.yml + component flags (systemd ExecStart, /etc/default, pasted command lines)
- Admin / lifecycle APIs, 0.0.0.0 listeners, TLS, bcrypt, inline secrets (masked), http remote_write / webhooks, unencrypted gossip, textfile dir, blackbox SSRF, perms
- Score + grade A+…F, CWE + MITRE ATT&CK on every rule
- TXT / MD / JSON / CSV / SARIF, --demo, --fail-on

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OPromX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
