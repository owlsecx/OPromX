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

OPromX is an offline, read-only configuration auditor for the Prometheus monitoring stack. It parses Prometheus, Alertmanager, Pushgateway and exporter configurations along with component command-line flags, and flags exposure, TLS, authentication and secret-handling issues. Each finding carries a grade, CWE and MITRE ATT&CK reference.

---

## ✨ Features

- Stdlib YAML-subset parser with per-key line numbers
- Audits prometheus.yml, alertmanager.yml, blackbox.yml, web-config.yml and component flags
- Detects admin/lifecycle API exposure, 0.0.0.0 listeners, missing TLS and weak auth
- Flags inline secrets (masked), insecure remote_write/webhooks and blackbox SSRF
- Score and A+ to F grade with CWE and MITRE ATT&CK mapping
- TXT/MD/JSON/CSV/SARIF export, rule catalogue, templates and CI gates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OPromX /etc/prometheus/prometheus.yml
./OPromX --scan --root /mnt/collected --sarif -o report.sarif
./OPromX --cmd "alertmanager --cluster.peer=..." --fail-on high
./OPromX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
