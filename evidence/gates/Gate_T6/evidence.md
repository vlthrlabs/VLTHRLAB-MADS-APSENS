# APSENS Lab Validation Evidence Sheet: Gate_T6

- **Run ID:** `RUN_20261119_132957_7gate_validation`
- **Gate Name:** SHA-256 Hash-Chained Epoch Tamper-Evidence Gate
- **Status:** **PASS**
- **Evidence Class:** `BENCHMARK_MEASURED`
- **Provenance JSON:** `provenance.json`
- **Metrics JSON:** `metrics.json`

## 1. Measured Metrics

| Metric | Value |
| :--- | :--- |
| `epochs_sealed` | `3` |
| `unmodified_chain_valid` | `True` |
| `single_field_tamper_detected` | `True` |
| `tamper_caught_at_epoch_index` | `1` |
| `tamper_governance_stamp` | `NOT DECISION-GRADE (EPOCH CONTENT TAMPERED)` |
| `genesis_hash_prefix` | `51bbc3561fa0dadc` |
| `head_hash_prefix` | `bf91b55d452c4902` |
| `elapsed_seconds` | `0.01` |

## 2. Gate Artifacts

- `artifacts/test_tamper_ledger.json`

## 3. Governance & Standards Alignment

- Aligned with **ISO 13374-1/2** (Blocks 1-6 condition monitoring data processing and decision support).
- Aligned with **ISO 8000-61** (Data quality and provenance lineage).
- *Disclaimer:* APSENS follows ISO guidance frameworks for engineering traceability; this laboratory evidence sheet does not claim third-party ISO certification and distinguishes `BENCHMARK_MEASURED`, `BENCHMARK_CALIBRATED`, and `SIMULATED` outputs.
