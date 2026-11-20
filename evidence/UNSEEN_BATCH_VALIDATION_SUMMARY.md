# APSENS Zero-Shot Unseen Batch Validation Report: `RUN_20261119_132940_unseen_batch_validation`

- **Overall Verdict:** **PASS (40/40 UNSEEN FILES)**
- **Total Unseen Files Processed (`data/unseen/`):** `40` CSV files (`269,351` total raw telemetry rows)
- **Total Execution Time:** `14.89 seconds`
- **Evidence Class:** `BENCHMARK_MEASURED` (100% unseen external datasets, zero training overlap)

## Per-File Zero-Shot Validation Matrix

| Unseen Dataset File | Rows | Health | Stage | Lead Time (h) | FAR (%) | Healed / Quar. | TDAE Trust | Status |
| :--- | ---: | ---: | :--- | ---: | ---: | :--- | ---: | :--- |
| `Kaggle Municipal Water Pump Sensor Data/sensor.csv` | `220,320` | `33.0` | `FAILURE` | `3473.7` | `0.0` | `8 / 0` | `92.7%` | **PASS** |
| `nasa_cmapss_gas_turbine/NASA_CMAPSS_FD001_TURBINE1_READY_TO_UPLOAD.csv` | `192` | `81.4` | `PROGRESSIVE` | `140.0` | `0.0` | `0 / 4` | `91.1%` | **PASS** |
| `nasa_cmapss_gas_turbine/NASA_CMAPSS_FD001_TURBINE2_READY_TO_UPLOAD.csv` | `287` | `42.7` | `ACCELERATED` | `206.0` | `0.0` | `0 / 4` | `91.1%` | **PASS** |
| `nasa_cmapss_gas_turbine/NASA_CMAPSS_FD001_TURBINE3_READY_TO_UPLOAD.csv` | `179` | `44.1` | `PROGRESSIVE` | `131.0` | `0.0` | `0 / 4` | `91.1%` | **PASS** |
| `skab_water_loop_valve_pump/anomaly-free_anomaly-free.csv` | `9,405` | `2.0` | `FAILURE` | `352.5` | `0.0` | `0 / 0` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/other_1.csv` | `745` | `78.8` | `ACCELERATED` | `163.8` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/other_10.csv` | `1,327` | `2.0` | `FAILURE` | `310.2` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/other_11.csv` | `1,190` | `90.2` | `CRITICAL` | `270.2` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/other_12.csv` | `1,048` | `87.3` | `CRITICAL` | `239.8` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/other_13.csv` | `923` | `79.4` | `ACCELERATED` | `210.5` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/other_14.csv` | `905` | `70.5` | `FAILURE` | `198.5` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/other_2.csv` | `780` | `44.5` | `ACCELERATED` | `173.0` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/other_3.csv` | `1,137` | `81.9` | `ACCELERATED` | `262.5` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/other_4.csv` | `1,191` | `80.2` | `ACCELERATED` | `277.2` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/other_5.csv` | `1,155` | `83.0` | `CRITICAL` | `267.0` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/other_6.csv` | `1,147` | `94.7` | `ACCELERATED` | `259.8` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/other_7.csv` | `1,090` | `43.3` | `FAILURE` | `252.2` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/other_8.csv` | `1,147` | `23.4` | `ACCELERATED` | `256.5` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/other_9.csv` | `1,144` | `15.2` | `CRITICAL` | `265.0` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve1_0.csv` | `1,147` | `13.0` | `CRITICAL` | `261.8` | `0.0` | `0 / 1` | `92.0%` | **PASS** |
| `skab_water_loop_valve_pump/valve1_1.csv` | `1,145` | `70.5` | `CRITICAL` | `266.0` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve1_10.csv` | `1,146` | `94.7` | `CRITICAL` | `265.5` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve1_11.csv` | `1,141` | `91.9` | `FAILURE` | `264.2` | `0.0` | `0 / 1` | `92.0%` | **PASS** |
| `skab_water_loop_valve_pump/valve1_12.csv` | `1,140` | `81.3` | `CRITICAL` | `257.5` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve1_13.csv` | `1,140` | `95.0` | `PROGRESSIVE` | `262.8` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve1_14.csv` | `1,139` | `81.5` | `ACCELERATED` | `262.2` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve1_15.csv` | `1,150` | `93.9` | `CRITICAL` | `264.5` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve1_2.csv` | `1,075` | `89.6` | `CRITICAL` | `248.5` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve1_3.csv` | `1,148` | `81.1` | `ACCELERATED` | `266.8` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve1_4.csv` | `1,095` | `91.4` | `CRITICAL` | `252.8` | `0.0` | `0 / 1` | `92.0%` | **PASS** |
| `skab_water_loop_valve_pump/valve1_5.csv` | `1,154` | `72.5` | `ACCELERATED` | `268.2` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve1_6.csv` | `1,154` | `79.7` | `CRITICAL` | `262.8` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve1_7.csv` | `1,094` | `93.9` | `PROGRESSIVE` | `253.2` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve1_8.csv` | `1,144` | `24.4` | `ACCELERATED` | `265.0` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve1_9.csv` | `1,148` | `80.0` | `ACCELERATED` | `262.0` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve2_0.csv` | `1,125` | `79.1` | `ACCELERATED` | `257.5` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve2_1.csv` | `1,063` | `93.7` | `PROGRESSIVE` | `243.8` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve2_2.csv` | `1,129` | `81.3` | `ACCELERATED` | `259.5` | `0.0` | `0 / 1` | `92.3%` | **PASS** |
| `skab_water_loop_valve_pump/valve2_3.csv` | `995` | `78.2` | `PROGRESSIVE` | `224.2` | `0.0` | `0 / 1` | `87.3%` | **PASS** |
| `uci_secom_manufacturing_nan_stress/UCI_SECOM_REAL_NAN_STRESS_TEST_READY_TO_UPLOAD.csv` | `1,567` | `80.9` | `CRITICAL` | `911.4` | `0.0` | `8 / 1` | `81.8%` | **PASS** |
