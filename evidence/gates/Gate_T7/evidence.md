# APSENS Lab Validation Evidence Sheet: Gate_T7

- **Run ID:** `RUN_20261119_132957_7gate_validation`
- **Gate Name:** Windows Application Control Immunity, Resource Headroom & Code Integrity Gate
- **Status:** **PASS**
- **Evidence Class:** `BENCHMARK_MEASURED`
- **Provenance JSON:** `provenance.json`
- **Metrics JSON:** `metrics.json`

## 1. Measured Metrics

| Metric | Value |
| :--- | :--- |
| `active_ml_backend` | `numpy_scipy_blas_whitelisted` |
| `wdac_application_control_safe` | `True` |
| `source_files_sealed_in_manifest` | `60` |
| `manifest_file` | `APSENS_CODE_MANIFEST.sha256` |
| `manifest_sha256` | `667f77090a37aa2767414f9fc946cda2663fa3ae8d1170c525e241eda60c3877` |
| `elapsed_seconds` | `0.02` |

## 3. Governance & Standards Alignment

- Aligned with **ISO 13374-1/2** (Blocks 1-6 condition monitoring data processing and decision support).
- Aligned with **ISO 8000-61** (Data quality and provenance lineage).
- *Disclaimer:* APSENS follows ISO guidance frameworks for engineering traceability; this laboratory evidence sheet does not claim third-party ISO certification and distinguishes `BENCHMARK_MEASURED`, `BENCHMARK_CALIBRATED`, and `SIMULATED` outputs.
