# APSENS: Data Lineage, 3-Stage Partition & Anti-Leakage Handoff Registry

Generated: 2026-11-19T10:19:16.408392+00:00 | Total Canonical Disk Used: **1.762 MB** (out of 10.0 GB allocation).

## Strict Anti-Leakage Rules for Engineers & Agents
- **`substage_A_training`**: Use ONLY to fit scalers, PCA, IsolationForest, SequenceAutoencoder weights, and Welford priors.
- **`substage_B_retraining_learning`**: Use ONLY for regime-shift adaptation, post-overhaul baseline resets, and POF lead-table updates.
- **`substage_C_heldout_validation`**: Blind test sets for **Gates T1 to T7**. Never fit or tune any model parameter on Substage C.
- **`substage_D_live_replay_test`**: Ready-to-upload historian CSVs for the **'Bring Your Last Failure' Replay Challenge**.

## Complete File & SHA-256 Provenance Table

| Stage | Substage | File | Equipment & Fault | License & DOI | Rows x Cols | Size (KB) | SHA-256 (first 16 hex) |
|---|---|---|---|---|---|---|---|
| Stage 1 | `substage_A_training` | `cwru_normal_0_97.parquet` | bearing (`healthy`) | Open Academic Benchmark (https://engineering.case.edu/bearingdatacente) | 237 x 17 | 21.94 | `50d12f0b07fca1e9` |
| Stage 1 | `substage_C_heldout_validation` | `cwru_12k_Drive_End_IR007_0_105.parquet` | bearing (`bearing_inner_race`) | Open Academic Benchmark (https://engineering.case.edu/bearingdatacente) | 177 x 17 | 18.83 | `69ba662d650b90cc` |
| Stage 1 | `substage_B_retraining_learning` | `cwru_12k_Drive_End_B007_0_118.parquet` | bearing (`bearing_outer_race`) | Open Academic Benchmark (https://engineering.case.edu/bearingdatacente) | 178 x 17 | 18.87 | `32a00c9c78a1cebb` |
| Stage 1 | `substage_C_heldout_validation` | `cwru_12k_Drive_End_OR007@6_0_130.parquet` | bearing (`bearing_outer_race`) | Open Academic Benchmark (https://engineering.case.edu/bearingdatacente) | 178 x 17 | 18.87 | `101521ceb316b43e` |
| Stage 1 | `substage_A_training` | `nasa_ims_healthy_baseline_350c.parquet` | bearing (`healthy`) | US Government Public Domain (https://data.nasa.gov/dataset/ims-bearings | ) | 350 x 17 | 24.41 | `be1fad26febe578a` |
| Stage 1 | `substage_C_heldout_validation` | `nasa_ims_7day_outer_race_rtf.parquet` | bearing (`bearing_outer_race`) | US Government Public Domain (https://data.nasa.gov/dataset/ims-bearings | ) | 3936 x 17 | 180.82 | `0583ff3dc49ba0d6` |
| Stage 1 | `substage_D_live_replay_test` | `REPLAY_NASA_IMS_7DAY_BEARING_FAILURE.csv` | bearing (`bearing_outer_race`) | US Government Public Domain (https://data.nasa.gov/dataset/ims-bearings) | 3936 x 17 | 683.13 | `ce15cc52c936dd65` |
| Stage 1 | `substage_A_training` | `uci_ai4i2020_healthy_train.parquet` | motor (`healthy`) | CC BY 4.0 (https://doi.org/10.24432/C5HS5C | Matzka (202) | 5000 x 14 | 93.91 | `66da6a3977270ebf` |
| Stage 1 | `substage_C_heldout_validation` | `uci_ai4i2020_multimode_heldout.parquet` | motor (`motor_stator_winding`) | CC BY 4.0 (https://doi.org/10.24432/C5HS5C) | 5000 x 14 | 95.52 | `d25b606b765de71a` |
| Stage 1 | `substage_C_heldout_validation` | `zema_hydraulic_pump_leakage_heldout.parquet` | pump (`pump_valve_seat_wear`) | CC BY 4.0 (https://doi.org/10.5281/zenodo.1323611 | Helw) | 600 x 17 | 41.54 | `7181e1a2537272ed` |
| Stage 2 | `substage_B_retraining_learning` | `metropt3_compressor_regime_shifts.parquet` | compressor (`healthy`) | CC BY 4.0 (https://doi.org/10.5281/zenodo.6854240 | Velo) | 800 x 17 | 51.87 | `86f8e898b95f0b16` |
| Stage 2 | `substage_C_heldout_validation` | `metropt3_compressor_fouling_failure.parquet` | compressor (`compressor_fouling`) | CC BY 4.0 (https://doi.org/10.5281/zenodo.6854240) | 720 x 17 | 47.4 | `aea94d6b8d161e0d` |
| Stage 2 | `substage_D_live_replay_test` | `REPLAY_METROPT3_COMPRESSOR_FAILURE_30DAY.csv` | compressor (`compressor_fouling`) | CC BY 4.0 (https://doi.org/10.5281/zenodo.6854240) | 720 x 17 | 130.55 | `66ef3f8cc7ce4a02` |
| Stage 2 | `substage_C_heldout_validation` | `zenodo_centrifugal_pump_cavitation.parquet` | pump (`pump_cavitation`) | CC BY 4.0 (https://doi.org/10.5281/zenodo.15301820) | 600 x 17 | 41.25 | `e3c5721aca1482c1` |
| Stage 3 | `substage_C_heldout_validation` | `kelmarsh_50hz_generator_stator_overload.parquet` | generator_turbine (`generator_stator_insulation`) | CC BY 4.0 (https://doi.org/10.5281/zenodo.5841834 | Plum) | 720 x 17 | 47.42 | `d3cbe71eab012afb` |
| Stage 3 | `substage_D_live_replay_test` | `REPLAY_KELMARSH_50HZ_POWER_GENERATOR_FAULT.csv` | generator_turbine (`generator_stator_insulation`) | CC BY 4.0 (https://doi.org/10.5281/zenodo.5841834) | 720 x 17 | 139.02 | `e42967099d7e1807` |
| Stage 3 | `substage_C_heldout_validation` | `petrobras_3w_choke_wax_restriction.parquet` | valve (`valve_choke_fouling`) | CC BY 4.0 (https://doi.org/10.6084/m9.figshare.29205836 ) | 600 x 17 | 41.22 | `2cddaa82ef62b7e3` |
| Stage 3 | `substage_D_live_replay_test` | `REPLAY_PETROBRAS_3W_WELL_CHOKE_RESTRICTION.csv` | valve (`valve_choke_fouling`) | CC BY 4.0 (https://doi.org/10.6084/m9.figshare.29205836) | 600 x 17 | 107.27 | `be9e64f05c117522` |