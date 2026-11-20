# AGENTS.md - VLTHR Lab Engineering, Provenance & Repository Policy (APSENS)

**Authored By:** VLTHR Lab ([vlthrlab.app](https://vlthrlab.app) | `vlthrlabs@gmail.com`)
**Policy & Architecture Owner:** Saviour (Ufuoma) Amlasawole (Founder & Systems Build Lead)
**Verification & Manifest Owner:** Blessing Obakpololo Amlasawole (Head of Verification, Controls & Provenance)
**Validation & Evidence Governance:** Victoria Ayinla Saviour (Head of Validation & Tools) & Daniel Amlasawole (Head of Business, Product & Evidence Governance)

> **Scope:** This file governs all AI agents, human engineers, and automated workflows operating inside the `APSENS` repository. Every contribution must strictly obey these organizational, scientific integrity, and provenance rules.

---

## 1. Repository Organization & Indexing Standard

Never dump mixed file types (`.md`, `.json`, `.pdf`, `.csv`, logs) into a single flat directory. Every artifact must live in its designated class:

```text
APSENS/
  AGENTS.md                        # Mandatory lab rules and agent governance (this file)
  REPRODUCE.md                     # Step-by-step reproducibility & independent critique guide
  README.md                        # Executive overview & quick-start index
  APSENS_CODE_MANIFEST.sha256      # Cryptographic SHA-256 seal of all engine & UI source files
  Launch_APSENS.bat                # One-click native app-window launcher

  docs/                            # Classified specification & audit documentation
    INDEX.md                       # Master searchable documentation index
    01_strategy_and_prd/           # Product identity, strategy, Q&A log, PRD, value pricing
    02_architecture_and_audit/     # Reference code audit, 9-bug audit, master consolidated spec
    03_data_and_standards/         # Dataset registry, 3-stage data plan, ISO standards & test plan
    04_assets/                     # Fonts (BitcountPropDouble.ttf) and UI reference copy

  engine/                          # Core Python engine & whitelisted Dual-Backend ML
    solution_src/                  # Patched physics, DSE, DCE, TDAE, Dual-ML modules
    intake.py                      # DuckDB 200 MB CSV/Excel/Parquet intake & ISO 8000 trust
    presets.py                     # 4 multi-industry facility presets (50 Hz, USD & NGN)
    dataset_manager.py             # 3-Stage x 4-Substage anti-leakage dataset builder
    replay_and_validation.py       # 'Bring Your Last Failure' replay & 7-Gate run archiver
    scorecard_and_report.py        # 6-Week Trial Scorecard & 10-Section ISO PDF generator
    server.py                      # Local HTTP server (127.0.0.1:8765)

  ui/                              # 1:1 demo.html UI (Bitcount Prop Double) + live engine bridge
    index.html
    apsens_bridge.js
    mad_src/                       # Reference JavaScript 3-twin simulation modules

  data/                            # Strict 3-Stage x 4-Substage anti-leakage data lake
    DATA_LINEAGE_HANDOFF.md        # Human-readable SHA-256 lineage table
    DATA_REGISTRY_AND_LINEAGE.json # Machine-readable provenance registry
    stage1_component_physics/      # substage_A .. substage_D
    stage2_utility_process_streams/# substage_A .. substage_D
    stage3_power_and_oilgas_fleets/# substage_A .. substage_D
    canonical/                     # POF lead table and canonical test fixtures
    drop_folder/                   # Watched client upload drop folder

  runs/                            # Immutable, timestamped execution & test evidence archive
    INDEX.json                     # Machine-readable master index of every run
    INDEX.md                       # Human-readable searchable run ledger
    RUN_<YYYYMMDD_HHMMSS>_<task>/  # Unique folder per run/test/task
      RUN_SUMMARY.md               # Executive verdict, limits, and reproduction command
      run_metadata.json            # Host OS, Python version, git/code manifest hash, seed, duration
      run_manifest.sha256          # SHA-256 hashes of every file produced in this run
      gates/                       # Per-test isolated subfolders (no flat file dumps)
        Gate_T1/
          evidence.md
          provenance.json
          metrics.json
          artifacts/               # Raw outputs or ledgers specific to Gate_T1
        Gate_T2/ ... Gate_T7/
      reports/                     # Generated PDFs for this specific run

  public/                          # Curated, publishable external submission package
    README.md                      # Public portfolio & evidence summary (VLTHR Lab format)
    REPRODUCE.md                   # Independent reproduction & critique instructions
    MANIFEST.sha256                # Cryptographic verification of every public file
    evidence/                      # Latest verified public evidence sheets & JSON summaries
    reports/                       # Sample 10-Section ISO Engineering PDF Report
    audits/                        # Reference 9-Bug Audit & Dataset Commercial Licensing Registry
```

---

## 2. Mandatory Lab Rules & Scientific Integrity Policies

### Rule 1: Unique Folder Per Run, Test, and Task
- Every validation run, experiment, benchmark, or client failure replay MUST write its outputs into a **new, unique folder** under `APSENS/runs/RUN_<YYYYMMDD_HHMMSS>_<task_slug>/`.
- Never overwrite a previous run folder. Historical runs remain immutable for auditability.
- Within a run folder, each individual test or gate MUST have its own subfolder (`gates/<Gate_ID>/`) separating markdown evidence (`evidence.md`), structured provenance (`provenance.json`), raw metrics (`metrics.json`), and test artifacts (`artifacts/`).
- Every completed run MUST append an entry to `APSENS/runs/INDEX.json` and regenerate `APSENS/runs/INDEX.md`.

### Rule 2: Honest VLTHR Lab Maturity Grading & Evidence Classification
Every claim, table, chart, and report MUST state its exact **Maturity Grade** and **Evidence Class**. Agents are strictly forbidden from blurring simulated or calibrated results with real field measurements.

- **VLTHR Lab Maturity Grades:**
  1. `IDEA` - Problem statement and hypothesis only.
  2. `PROTOTYPE` - Working code tested on synthetic or lab fixtures.
  3. `BUILT_SYSTEM` - Integrated end-to-end software passing all lab validation gates (`Gate_T1` to `Gate_T7`) with cryptographic provenance and reproducibility.
  4. `PROVEN_RESULT` - Validated on real client plant historian data during a live 4-to-6-week field trial with verified operator verdicts.
- **Evidence Classes (Mandatory Stamp on Every Metric):**
  - `BENCHMARK_MEASURED`: Computed directly from real, unmodified public benchmark measurements (e.g., NASA IMS, CWRU `.mat`, UCI AI4I 2020, 234.9 MB DuckDB load speed, SHA-256 tamper detection).
  - `BENCHMARK_CALIBRATED`: Computed from physics-informed trajectories calibrated to published DOI fault signatures where raw multi-GB archives were not yet downloaded locally. Must be explicitly disclosed as calibrated, never claimed as raw sensor recordings.
  - `CLIENT_MEASURED`: Computed from actual client facility CSV/Excel/Parquet or read-only SCADA data.
  - `SIMULATED`: Paired 3-Twin financial counterfactuals (`Twin A RTF` vs. `Twin B TBM` vs. `Twin C APSENS`). Must never be presented as realized financial profit.

### Rule 3: Anti-Leakage Data Discipline (3-Stage x 4-Substage)
- `substage_A_training`: Fit scalers, PCA, Isolation Forest, and Sequence Autoencoder weights ONLY here.
- `substage_B_retraining_learning`: Regime-shift adaptation and post-overhaul re-anchoring ONLY here.
- `substage_C_heldout_validation`: Blind test evaluation ONLY. Never fit or tune parameters on Substage C.
- `substage_D_live_replay_test`: Read-only historian exports for live replay demonstrations.

### Rule 4: Zero Overclaiming & Standards Disclaimer
- APSENS aligns with **ISO 13374-1/2**, **ISO 17359**, **ISO 20816-3**, **ISO 13381-1**, and **ISO 8000-61** engineering guidance.
- Agents MUST NOT claim third-party ISO certification.
- Every report MUST document known limitations, assumptions, and open risks alongside passing metrics.

### Rule 5: Cryptographic Provenance & Code Integrity
- Every source code change in `engine/` or `ui/` requires regenerating `APSENS_CODE_MANIFEST.sha256`.
- Every run folder requires a `run_manifest.sha256` sealing all artifacts in that run.
- Any tampered epoch ledger MUST be stamped `NOT DECISION-GRADE`.

### Rule 6: Formatting & Environment Constraints
- **Zero Em Dashes:** Do not use em dashes (Unicode `U+2014`) in documentation, UI copy, reports, or code comments. Use hyphens (`-`), colons (`:`), or commas.
- **Windows Application Control Immunity:** Runtime code in `engine/` must execute on whitelisted `numpy`, `scipy`, `pandas`, `duckdb`, `pyarrow`, `openpyxl`, and `reportlab` without requiring unsigned `.pyd` DLLs (`sklearn`/`torch`/`tensorflow`) at top-level import.
- **Public vs. Internal Hygiene:** Only vetted, non-confidential artifacts with verified SHA-256 manifests may be copied into `APSENS/public/`. Never place `.env` files, API keys, proprietary source code (`.py`, `.js`, `.html`), client proprietary data, or temporary scratch files in `public/`.

### Rule 7: Mandatory Pre-Publish Audit & Git Discipline
- Before any external submission, `vlthrlab.app` publication, or `git push`, the agent or engineer MUST run:
  ```powershell
  py engine/pre_publish_audit.py
  ```
- Publication is **BLOCKED** if any check fails (zero em dashes, `APSENS_CODE_MANIFEST.sha256`, `public/MANIFEST.sha256`, latest `run_manifest.sha256`, secret scan, or public boundary check).
- Keep large raw staging archives (`data/staging_raw/`), Python caches (`__pycache__/`), and live session uploads (`data/drop_folder/`) strictly excluded via `.gitignore`.

