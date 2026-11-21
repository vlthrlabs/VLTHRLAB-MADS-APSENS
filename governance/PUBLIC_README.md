# APSENS Public Evidence & Reproducibility Package (VLTHR Lab)

**Product:** APSENS (Adaptive Problem Solving Experiential Navigation System)
**Authored By:** VLTHR Lab ([vlthrlab.app](https://vlthrlab.app) | `vlthrlabs@gmail.com`)
**Current Maturity Grade:** `BUILT_SYSTEM` (Lab-verified software; awaiting live 4-to-6-week client facility trial for `PROVEN_RESULT`)
**Latest Verified Run ID:** `RUN_20261119_132957_7gate_validation` (`PARTIAL`)

---

## 0. Authorship, Governance & Ownership (VLTHR Lab)

This public evidence package is authored and maintained by **VLTHR Lab** under a strict four-person separation-of-duties model (builders never grade their own work):

| Head-Admin | Role at VLTHR Lab | Owned Artifacts in This Repository |
| :--- | :--- | :--- |
| **Saviour (Ufuoma) Amlasawole** | Founder, Systems Engineering & Build Lead | Core `APSENS` diagnostic & batch engine, 9-bug audit (`audits/05_REFERENCE_VALIDATION_AND_BUG_AUDIT.md`), `AGENTS.md` governance & LAWPES payload workflow |
| **Victoria Ayinla Saviour** | Head of Validation & Tools | `REPRODUCE.md`, anti-leakage splits, healthy control-set calibration (`0%` baseline FAR), `CHAOS-01..06` corrupt-data stress tests, 40-dataset unseen batch validation (`evidence/`) |
| **Daniel Amlasawole** | Head of Business, Product & Evidence Governance | Public evidence curation (`README.md`), `E0..E6` claims-to-evidence governance (`BENCHMARK_MEASURED` vs. `SIMULATED`), `06_COMMERCIAL_DATASET_REGISTRY_AND_HEADROOM.md` (`CC BY 4.0`), multi-department KPI translation (`reports/`, `CEO_EXECUTIVE_KPI_AND_COMMERCIAL_BRIEF.md`) |
| **Blessing Obakpololo Amlasawole** | Head of Verification, Controls & Provenance Governance | Blind raw-row metric recomputation, SHA-256 provenance seals (`MANIFEST.sha256`), `Gate_T6` 1-byte tamper detection, and automated 7-check pre-publish audit |

**Contact:** `vlthrlabs@gmail.com` | **Website:** [vlthrlab.app](https://vlthrlab.app)

---

## 1. What Is Published in This Folder

This `public/` directory contains **only** vetted, non-confidential engineering evidence, audits, and reproducibility artifacts safe for external publication, client technical review, or independent critique:

- [`CEO_EXECUTIVE_KPI_AND_COMMERCIAL_BRIEF.md`](./CEO_EXECUTIVE_KPI_AND_COMMERCIAL_BRIEF.md) - Proposed KPIs, industrial problem statement, buyer personas, pricing tiers (USD & NGN), and ROI case.
- [`REPRODUCE.md`](./REPRODUCE.md) - Step-by-step instructions to verify SHA-256 seals, re-run all 7 Lab Validation Gates, and critique known limitations.
- [`AGENTS.md`](./AGENTS.md) - VLTHR Lab repository organization, anti-leakage data discipline, and scientific integrity policy.
- [`evidence/LATEST_VALIDATION_SUMMARY.md`](./evidence/LATEST_VALIDATION_SUMMARY.md) - Executive 7-Gate verdict table with explicit `BENCHMARK_MEASURED` and `SIMULATED` badges.
- [`evidence/V5_ROTATING_VIBRATION_VALIDATION_REPORT.md`](./evidence/V5_ROTATING_VIBRATION_VALIDATION_REPORT.md) & [`evidence/v5_patched_metrics.json`](./evidence/v5_patched_metrics.json) - APSENS v5 Cross-Rig Rotating-Vibration Validation (`HUST`, `University of Ottawa`, `XJTU-SY` 15 RTF bearings, and `MAFAULDA` 8-channel; `5/5` Hard-Stop Anti-Bias QA Gates, `1.15% - 3.70%` OOF Healthy FAR, `0.966 - 0.999` OOF ROC-AUC, `0` synthetic rows).
- [`evidence/gates/`](./evidence/gates/) - Isolated per-gate evidence folders (`Gate_T1` through `Gate_T7`), each with `evidence.md`, `provenance.json`, `metrics.json`, and `artifacts/`.
- [`audits/05_REFERENCE_VALIDATION_AND_BUG_AUDIT.md`](./audits/05_REFERENCE_VALIDATION_AND_BUG_AUDIT.md) - Transparent record of 9 defects (`BUG-01` to `BUG-09`) discovered in legacy reference code and verified fixes.
- [`audits/07_V5_CODE_AND_METHODOLOGY_BUG_AUDIT.md`](./audits/07_V5_CODE_AND_METHODOLOGY_BUG_AUDIT.md) - Transparent record of 7 signal-physics and statistical-validation defects (`BUG-V5-01` to `BUG-V5-07`) uncovered and patched during the v5 review.
- [`audits/06_COMMERCIAL_DATASET_REGISTRY_AND_HEADROOM.md`](./audits/06_COMMERCIAL_DATASET_REGISTRY_AND_HEADROOM.md) - Commercial license audit (`CC BY 4.0`, `CC0`, US Gov Public Domain) and DOIs.
- [`audits/RAW_DOWNLOAD_RECEIPTS.json`](./audits/RAW_DOWNLOAD_RECEIPTS.json) - Cryptographic SHA-256 receipts and Zenodo/GitHub URLs for all raw `CC BY 4.0` datasets evaluated in `Gate_T4`.
- [`audits/DATA_LINEAGE_HANDOFF.md`](./audits/DATA_LINEAGE_HANDOFF.md) - 3-Stage x 4-Substage anti-leakage data partition SHA-256 registry.
- [`reports/`](./reports/) - Sample 10-Section ISO 13374 / ISO 20816 / ISO 8000 Engineering & Trial Value Scorecard PDFs for **Oil & Gas Flowstation** and **Power Generation (50 Hz)**.
- [`MANIFEST.sha256`](./MANIFEST.sha256) - Cryptographic SHA-256 seal of every file in this public release.

## 2. Explicit Scope & Transparency Statement

- **Proven (`BENCHMARK_MEASURED`):** 234.9 MB DuckDB ingestion speed, messy SCADA torture recovery, 18/18 physics degradation mechanism classification, zero false alarms on startup transients and regime shifts, blind held-out detection across **7/7 raw public benchmarks** (`NASA IMS`, `CWRU`, `ZeMA Hydraulic`, `MetroPT-3 Compressor`, `Zenodo Centrifugal Pump`, `Kelmarsh 50 Hz Generator`, `Petrobras 3W Oil Well`), SHA-256 tamper detection, and Windows Application Control immunity.
- **Simulated (`SIMULATED`):** Paired 3-Twin financial counterfactuals (`Twin A RTF` vs. `Twin B TBM` vs. `Twin C APSENS`) in USD and NGN.
- **Not Claimed:** Third-party ISO certification and realized client plant ROI (pending live 4-to-6-week facility trial).
