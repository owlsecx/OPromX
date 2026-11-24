# 🦉 OPromX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
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

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OPromX --help   # watch every network call
firejail --net=none ./OPromX --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
