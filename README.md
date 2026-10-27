# ubuntu22_stig — Ansible role (ubuntu22-stig)

**Ansible hardening role** for **Ubuntu 22.04 LTS**, generated from the Canonical Ubuntu 22.04 LTS Security Technical Implementation Guide (STIG) V2R7 profile in ComplianceAsCode SSG 0.1.82. Suitable for playbooks, Packer/Ansible provisioners, and golden-image pipelines. Search keywords: `ansible`, `ansible-role`, `compliance`, `devsecops`, `disa`, `disa-stig`, `hardening`, `infrastructure`, `jammy`, `openscap`, `security`, `stig`, `stigforge`, `ubuntu`.

StigForge-exported Ansible role **`ubuntu22_stig`** · release **`0.3.51`**.
Matrix cell status: **`green`**.

## Before you run this role

Each default below changes how a running host behaves. Read them before you apply the role to a host you depend on.

### rsyslog logs remote-access activity (auth, authpriv, daemon)

_Requirement: UBTU-22-652015 (ComplianceAsCode rule `rsyslog_remote_access_monitoring`)._

**What the role does.** Where rsyslog is installed, adds `auth.* /var/log/secure`, `authpriv.* /var/log/secure` and `daemon.* /var/log/messages` to /etc/rsyslog.d/50-default.conf, each only when that file has no line for the facility yet (a line for it in another rsyslog file does not stop the addition, so the facility can be logged twice).

**Who is affected.** Any host running rsyslog: authentication and daemon messages (logins, sudo, sshd) are also written to /var/log/secure and /var/log/messages, which grow faster, and a host that forwards those files sends more.

**How to change it.** Set `ubuntu22stig_rsyslog_remote_access_monitoring: false` (or its STIG id, `ubuntu22stig_UBTU_22_652015: false`) before the first run. If the role has already run, delete the three lines from /etc/rsyslog.d/50-default.conf and restart rsyslog.

**Effect on compliance.** With `ubuntu22stig_rsyslog_remote_access_monitoring` set to false, the role no longer remediates that STIG rule, and an OpenSCAP scan reports it as failing unless the host already meets it.

## Install

This repository root **is** the Ansible role (Galaxy-style layout). Release metadata and the
scoring helper live under `compliance/` and are not loaded when the role runs.

From **GitHub** (public):

```yaml
# requirements.yml
roles:
  - src: https://github.com/stigready/ubuntu22-stig
    scm: git
    version: v0.3.51   # or an immutable commit SHA
    name: ubuntu22_stig
```

```bash
ansible-galaxy role install -r requirements.yml -p ./roles
ansible-playbook -i inventory site.yml   # role: ubuntu22_stig
```

## Verification status (this release)

This release carries no per-role OpenSCAP score, and no OpenSCAP results ship with it. A container
cannot evaluate most hardening rules, so the role is not scored here. To score a host you hardened
with it, see *Score it yourself*. `compliance/releases/0.3.51/manifest.json` records this.

## Reports & review

- **[reports/index.html](reports/index.html)** — HTML report index
- **[CHANGELOG.md](CHANGELOG.md)** — release notes

## Score it yourself

This repository ships no OpenSCAP results (see *Verification status*). To score a host you
hardened with this role, run `oscap xccdf eval` on it and score the `results.xml` with this role's
exception list: see **[compliance/README.md](compliance/README.md)**.

## Notices

StigForge and StigReady are independent. They are not affiliated with, endorsed by or certified by the Center for Internet Security, Inc. (CIS), the Defense Information Systems Agency (DISA), the U.S. Department of Defense, NIST, Canonical or the ComplianceAsCode project. "CIS" and "CIS Benchmarks" are trademarks of the Center for Internet Security, Inc. DISA STIGs are DISA publications. Ubuntu is a trademark of Canonical Ltd. Linux is the registered trademark of Linus Torvalds in the U.S. and other countries. All trademarks are the property of their respective owners. This role applies ComplianceAsCode (SSG 0.1.82) remediation from SSG's Canonical Ubuntu 22.04 LTS Security Technical Implementation Guide (STIG) V2R7 profile. An OpenSCAP score is a measurement, not a certification.

**Login banner.** `remote_login_banner_contents` in `defaults/main.yml` defaults to the DoD Notice and Consent Banner (a U.S. Government information system warning). If the system is not a U.S. Government system, override it with your organization's own text. Overriding the banner text makes the OpenSCAP banner rules fail unless the scan's `login_banner_text` value is tailored to match it or those rules are recorded as exceptions.

## License

Copyright (c) 2026 StigReady.

- **[LICENSE](LICENSE)** (MIT) — StigForge export packaging
- **[NOTICE](NOTICE)** — ComplianceAsCode / BSD-3-Clause task body attribution

## Catalog

- [https://stigready.com/#stigforge](https://stigready.com/#stigforge)

