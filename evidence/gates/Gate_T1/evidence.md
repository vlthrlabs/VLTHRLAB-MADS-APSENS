# APSENS Lab Validation Evidence Sheet: Gate_T1

- **Run ID:** `RUN_20261119_132957_7gate_validation`
- **Gate Name:** 200 MB CSV Speed & Messy Historian Torture Test
- **Status:** **PASS**
- **Evidence Class:** `BENCHMARK_MEASURED`
- **Provenance JSON:** `provenance.json`
- **Metrics JSON:** `metrics.json`

## 1. Measured Metrics

| Metric | Value |
| :--- | :--- |
| `benchmark_file_size_mb` | `387.29` |
| `benchmark_rows` | `2000000` |
| `duckdb_2m_load_seconds` | `0.942` |
| `duckdb_hourly_rollup_seconds` | `1.86` |
| `rollup_buckets` | `556` |
| `torture_csv_rows_recovered` | `120` |
| `torture_header_skip_lines` | `3` |
| `torture_scada_bad_tokens_cleaned` | `6` |
| `torture_decimal_commas_converted` | `354` |
| `torture_iso8000_trust_score` | `90.3` |
| `elapsed_seconds` | `20.54` |

## 3. Governance & Standards Alignment

- Aligned with **ISO 13374-1/2** (Blocks 1-6 condition monitoring data processing and decision support).
- Aligned with **ISO 8000-61** (Data quality and provenance lineage).
- *Disclaimer:* APSENS follows ISO guidance frameworks for engineering traceability; this laboratory evidence sheet does not claim third-party ISO certification and distinguishes `BENCHMARK_MEASURED`, `BENCHMARK_CALIBRATED`, and `SIMULATED` outputs.
