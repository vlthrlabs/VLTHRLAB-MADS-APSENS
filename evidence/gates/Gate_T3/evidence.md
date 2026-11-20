# APSENS Lab Validation Evidence Sheet: Gate_T3

- **Run ID:** `RUN_20261119_132957_7gate_validation`
- **Gate Name:** Regime-Shift, Startup Transient (M1), Re-Anchor (M2) & Sensor Fault (M3) Gate
- **Status:** **PASS**
- **Evidence Class:** `BENCHMARK_MEASURED`
- **Provenance JSON:** `provenance.json`
- **Metrics JSON:** `metrics.json`

## 1. Measured Metrics

| Metric | Value |
| :--- | :--- |
| `healthy_regime_shift_cycles` | `120` |
| `false_alarms_on_healthy_transitions` | `0` |
| `startup_transients_suppressed_m1` | `4` |
| `standby_cycles_gated_m6` | `3` |
| `instrument_fault_disambiguated_m3` | `True` |
| `post_overhaul_reanchor_clean_m2` | `True` |
| `elapsed_seconds` | `0.02` |

## 3. Governance & Standards Alignment

- Aligned with **ISO 13374-1/2** (Blocks 1-6 condition monitoring data processing and decision support).
- Aligned with **ISO 8000-61** (Data quality and provenance lineage).
- *Disclaimer:* APSENS follows ISO guidance frameworks for engineering traceability; this laboratory evidence sheet does not claim third-party ISO certification and distinguishes `BENCHMARK_MEASURED`, `BENCHMARK_CALIBRATED`, and `SIMULATED` outputs.
