# APSENS Lab Validation Evidence Sheet: Gate_T4

- **Run ID:** `RUN_20261119_132957_7gate_validation`
- **Gate Name:** Blind Held-Out Generalization & 56h Mobilization Lead-Time Gate
- **Status:** **FAIL**
- **Evidence Class:** `BENCHMARK_MEASURED (7/7 Raw Public Benchmarks)`
- **Provenance JSON:** `provenance.json`
- **Metrics JSON:** `metrics.json`

## 1. Measured Metrics

| Metric | Value |
| :--- | :--- |
| `heldout_benchmarks_evaluated` | `7` |
| `raw_public_measured_count` | `7` |
| `doi_calibrated_count` | `0` |
| `early_detection_recall_pct` | `100.0` |
| `mechanism_diagnostic_accuracy_pct` | `28.57` |
| `mean_detection_lead_time_hours` | `409.2` |
| `mean_roc_auc` | `0.8654` |
| `min_detection_lead_time_hours` | `31.5` |
| `elapsed_seconds` | `1.74` |

## 2. Gate Artifacts

- `artifacts/benchmark_runs.json`

## 3. Governance & Standards Alignment

- Aligned with **ISO 13374-1/2** (Blocks 1-6 condition monitoring data processing and decision support).
- Aligned with **ISO 8000-61** (Data quality and provenance lineage).
- *Disclaimer:* APSENS follows ISO guidance frameworks for engineering traceability; this laboratory evidence sheet does not claim third-party ISO certification and distinguishes `BENCHMARK_MEASURED`, `BENCHMARK_CALIBRATED`, and `SIMULATED` outputs.
