# APSENS Validation Run Summary: `RUN_20261119_132957_7gate_validation`

- **Overall Verdict:** **PARTIAL**
- **VLTHR Lab Maturity Grade:** `BUILT_SYSTEM` (Lab-verified software; awaiting live 4-to-6-week client plant trial for `PROVEN_RESULT`)
- **UTC Timestamp:** `2026-11-19T13:30:20Z`
- **Execution Time:** `22.55 seconds`
- **Ontology Version:** `1.2.0` (18 Mechanisms across 7 Equipment Classes)
- **Code Manifest SHA-256:** `667f77090a37aa2767414f9fc946cda2663fa3ae8d1170c525e241eda60c3877`
- **Reproduction Command:** `py engine/replay_and_validation.py`

## 1. Per-Gate Isolated Evidence Matrix

| Gate ID | Folder | Validation Gate Name | Evidence Class | Key Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Gate_T1** | [`gates/Gate_T1/`](./gates/Gate_T1/evidence.md) | 200 MB CSV Speed & Messy Historian Torture | `BENCHMARK_MEASURED` | `387.29 MB` loaded in `0.942s`; `120` messy rows recovered | **PASS** |
| **Gate_T2** | [`gates/Gate_T2/`](./gates/Gate_T2/evidence.md) | 18/18 Mechanism Causal & Directional Discrimination | `BENCHMARK_MEASURED` | `18/18` mechanisms (`100.0%`) across 7 equipment classes | **PASS** |
| **Gate_T3** | [`gates/Gate_T3/`](./gates/Gate_T3/evidence.md) | Regime-Shift, Startup Transient (`M1`), Re-Anchor (`M2`) & Sensor Fault (`M3`) | `BENCHMARK_MEASURED` | `0` false alarms; `4` transients blanked; sensor fault isolated | **PASS** |
| **Gate_T4** | [`gates/Gate_T4/`](./gates/Gate_T4/evidence.md) | Blind Held-Out Generalization & 56h Lead-Time Gate | `BENCHMARK_MEASURED` (7/7 Raw Public Datasets) | Recall `100.0%`, Diag Acc `28.57%`, Mean Lead `409.2h`, Mean ROC-AUC `0.8654` | **FAIL** |
| **Gate_T5** | [`gates/Gate_T5/`](./gates/Gate_T5/evidence.md) | Paired 3-Twin Economic Ledger Audit (4 Industries, USD & NGN) | `SIMULATED` | `4/4` industry ledgers reconcile (`Twin A RTF` vs `Twin B TBM` vs `Twin C APSENS`) | **PASS** |
| **Gate_T6** | [`gates/Gate_T6/`](./gates/Gate_T6/evidence.md) | SHA-256 Hash-Chained Epoch Tamper Detection | `BENCHMARK_MEASURED` | 1-field modification caught at Epoch `1` (`NOT DECISION-GRADE (EPOCH CONTENT TAMPERED)`) | **PASS** |
| **Gate_T7** | [`gates/Gate_T7/`](./gates/Gate_T7/evidence.md) | Windows App Control Immunity & Code Manifest Integrity (`M10`) | `BENCHMARK_MEASURED` | `60` source files sealed in `APSENS_CODE_MANIFEST.sha256` | **PASS** |

## 2. Known Limitations & Open Risks (VLTHR Lab Transparency Standard)

1. **Raw Public Benchmark Coverage in Gate_T4:** All 7 held-out benchmarks in `Gate_T4` (`NASA IMS`, `CWRU`, `ZeMA Hydraulic`, `MetroPT-3 Compressor`, `Zenodo Centrifugal Pump`, `Kelmarsh 50 Hz Generator`, and `Petrobras 3W Oil Well`) are now `BENCHMARK_MEASURED` from raw open-source sensor files (`RAW_DOWNLOAD_RECEIPTS.json` records exact download URLs and SHA-256 hashes). Note that high-rate industrial streams were downsampled to uniform episode windows for rapid laptop reproduction.
2. **Financial Savings Are Counterfactual Simulations:** Gate_T5 USD and NGN figures are `SIMULATED` paired 3-Twin counterfactuals using facility parameters (`1,400 NGN/USD`). Realized plant ROI can only be stamped `CLIENT_MEASURED` after a live 4-to-6-week facility trial.
3. **No ISO Certification Claimed:** APSENS implements ISO 13374-1/2, ISO 20816-3, and ISO 8000-61 engineering guidance for auditability, not third-party certification.
