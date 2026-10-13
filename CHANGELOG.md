# Changelog

Format based on [Keep a Changelog](https://keepachangelog.com/).

## [0.3.6] - 2026-10-13

### Changed
- StigForge export refresh for `ubuntu22_stig` at `0.3.6`.

### Verified (OpenSCAP)


### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/38350247629
- Factory commit: `02902407784d466753ecdaf97fa5db4040c623b5`

## [0.3.5] - 2026-10-12

### Changed
- StigForge export refresh for `ubuntu22_stig` at `0.3.5`.

### Verified (OpenSCAP)


### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/38329301726
- Factory commit: `336dce42410a74ebf84c3ffdfeeaa46ec14a7108`

## [0.3.4] - 2026-10-12

### Changed
- StigForge export refresh for `ubuntu22_stig` at `0.3.4`.

### Verified (OpenSCAP)


### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/38315937317
- Factory commit: `36862dbb274fcb2b459ffd56ffde7f6d357ac644`

## [0.3.3] - 2026-10-11

### Changed
- StigForge export refresh for `ubuntu22_stig` at `0.3.3`.

### Verified (OpenSCAP)


### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/38138148799
- Factory commit: `01b17bb3b1afea0172a458e4b6939a28a8d5948d`

## [0.3.2] - 2026-10-06

### Changed
- StigForge export refresh for `ubuntu22_stig` at `0.3.2`.

### Verified (OpenSCAP)


### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/37460773443
- Factory commit: `ca7184140d15b42d7648291c4a61d617876f2d5c`

## [0.3.1] - 2026-09-20

### Changed
- StigForge export refresh for `ubuntu22_stig` at `0.3.1`.

### Verified (OpenSCAP)


### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/35529346593
- Factory commit: `9a161e04bbdab156d492c2cb0f6afb2ab43beb30`

## [0.3.0] - 2026-09-12

### Changed
- StigForge export refresh for `ubuntu22_stig` at `0.3.0`.

### Verified (OpenSCAP)

- **`stig`** — score **94.12%** (floor 90.0%) · gate **PASS** · evidence `20260912T130456Z`
  - Remaining counted failures: `sssd_certification_path_trust_anchor, sssd_enable_user_cert`

### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/34693316989
- Factory commit: `562a1f7c1a8e19235ee26e972174d1be6c88998c`

## [0.2.4] - 2026-07-30

### Changed
- StigForge export refresh for `ubuntu22_stig` at `0.2.4`.

### Verified (OpenSCAP)

- **`stig`** — score **100.0%** (floor 90.0%) · gate **PASS** · evidence `20260729T223213Z`

### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/30496236357
- Factory commit: `7f7cafc85a392bf2a7eb04f1b979185dbcdf5530`

## [0.2.4-private-review] - 2026-07-29

### Changed
- StigForge export refresh for `ubuntu22_stig` at `0.2.4-private-review`.

### Verified (OpenSCAP)

- **`stig`** — score **100.0%** (floor 90.0%) · gate **PASS** · evidence `20260729T100151Z`

### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/30440754045
- Factory commit: `c481b47d629f5bc2357a86a933aa6f94f5245fce`

## [0.2.3-private-review] - 2026-07-29

### Added
- Initial StigForge export of matrix role `ubuntu22_stig`.
- OpenSCAP verify evidence bundles per profile under `compliance/releases/`.

### Verified (OpenSCAP)

- **`stig`** — score **100.0%** (floor 90.0%) · gate **PASS** · evidence `20260729T082911Z`

### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/30435216810
- Factory commit: `e8e323a3af3258bee63ebc1a873ba26c0cc12049`

## [0.2.1-private-review] - 2026-07-28

### Changed
- Galaxy-style layout: Ansible role at repository root; evidence under `compliance/`.
- Private review tag `v0.2.1-private-review` (supersedes nested `roles/<role>/` export).

## [0.2.0-private-review] - 2026-07-26

### Added
- First private StigForge export to `stigready/*` (factory review; nested role path).
