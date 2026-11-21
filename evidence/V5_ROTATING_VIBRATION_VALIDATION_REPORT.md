# APSENS v5 Patched Rotating-Vibration & Cross-Rig Validation Report

**Authored By:** VLTHR Lab ([vlthrlab.app](https://vlthrlab.app) | `vlthrlabs@gmail.com`)
**Verified Run ID:** `RUN_20261121_115035_apsens_v5_patched_audit`
**Companion Code Audit:** [`audits/07_V5_CODE_AND_METHODOLOGY_BUG_AUDIT.md`](../audits/07_V5_CODE_AND_METHODOLOGY_BUG_AUDIT.md)
**Frozen Zero-Pickle Commercial Checkpoint:** `models/apsens_v5_rotating_ref.npz` (`SHA-256: 8b1e1e869d82c89dc8b55ce843925c480a635bf4d701ed59844aa584ee7910c9`)
**Evidence Class:** `BENCHMARK_MEASURED` (`100%` real measured accelerometer waveforms across 4 independent laboratory test rigs; `0` synthetic rows).
**Formatting Rule:** Zero em dashes.

---

## 1. Hard-Stop Anti-Bias QA Gate Summary (`5 / 5 PASS`)

| QA Gate | Self-Test & Anti-Bias Check | Measured Result | Verdict |
| :--- | :--- | :--- | :---: |
| **QA Gate 1** | 100% Real Waveforms (`synthetic_rows == 0`), `0` NaNs/Infs, License Quarantine (`MAFAULDA` excluded from `CC BY 4.0` weights) | `HUST (99 .mat)`, `Ottawa (60 .mat)`, `XJTU-SY (120 real 25.6 kHz CSVs across 15 RTF bearings)`, `MAFAULDA (1,951 quarantined 50 kHz CSVs)` | **PASS** |
| **QA Gate 2** | Physical-Bearing & Severity-Configuration Group Disjointness (`GroupKFold` outer & inner folds) | `0` shared `group_id`s or `physical_bearing_id`s across train and test folds | **PASS** |
| **QA Gate 3** | Synthetic Signal-Physics Unit Tests (`COT`, `CPW`, `CSC` 1,000x Scale Invariance) | COT SNR gain: **`+10.14 dB`** (`>= 6 dB`); CPW fault/shaft ratio: **`0.0071 -> 1.6328`** (`230x`); 1,000x scale diff: **`7.70e-11`** (`< 1e-9`) | **PASS** |
| **QA Gate 4** | Zero-Pickle `.npz` Round-Trip Reload Fidelity (`allow_pickle=False`) | Max reload prediction deviation: **`0.0000e+00`** (`< 1e-12`) | **PASS** |
| **QA Gate 5** | 30-Draw Group-Level Label-Permutation Negative Control & Holm-Bonferroni Multi-Comparison Audit | Mean permutation OOF ROC-AUC: **`0.4848`** (strictly inside `[0.45, 0.55]` null window = zero leakage) | **PASS** |

---

## 2. Patched OOF Results Across E1, E2, E3, and E7 (`RUN_20261121_115035_apsens_v5_patched_audit`)

| Experiment & Scope | Pipeline | Total `n` (`n0` Healthy / `n1` Fault) | OOF Healthy FAR (Two-Sided 95% CI / One-Sided 95% UB) | Physical-Bearing FAR (`n_bearings`) | OOF Fault Recall (Two-Sided 95% CI) | OOF ROC-AUC | Gate (`FAR<=5%` & `AUC>=0.95`) |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **E1-Pool-Base** (`HUST + Ottawa`, `CC BY 4.0`, 53 Dual-Track features) | **`P1`** (Hybrid KRR + Extra-Trees + Mahalanobis) | `159` (`27 / 132`) | **3.70%** (`1/27`) `[0.0009, 0.1897]` (1-sided UB: `16.40%`) | `11.11%` (`1/9`) | **87.88%** (`116/132`) `[0.8106, 0.9291]` | **0.9823** | **PASS** |
| **E1-Pool-Base** (`HUST + Ottawa`, `CC BY 4.0`, 53 Dual-Track features) | **`P3`** (Rank-KRR + Mahalanobis) | `159` (`27 / 132`) | **3.70%** (`1/27`) `[0.0009, 0.1897]` (1-sided UB: `16.40%`) | `11.11%` (`1/9`) | 69.70% (`92/132`) | **0.9826** | **PASS** |
| **E1-Pool-Base** (`HUST + Ottawa`, `CC BY 4.0`, 53 Dual-Track features) | **`P2`** (Autogram/Infogram Newton-GBDT) | `159` (`27 / 132`) | **3.70%** (`1/27`) `[0.0009, 0.1897]` (1-sided UB: `16.40%`) | `11.11%` (`1/9`) | **80.30%** (`106/132`) | **0.9711** | **PASS** |
| **E2-MAFAULDA** (Severity-Grouped across all 49 speeds, 64 Dual-Track 8-Ch features) | **`P3`** (Rank-KRR + Mahalanobis) | `1,951` (`49 / 1,902`) | **2.04%** (`1/49`) `[0.0005, 0.1085]` (1-sided UB: `9.32%`) | `2.04%` (`1/49`) | **100.00%** (`1,902/1,902`) `[0.9981, 1.0000]` | **0.9997** | **PASS** |
| **E2-MAFAULDA** (Severity-Grouped, 64 Dual-Track 8-Ch features) | **`P1`** (Hybrid Ensemble) | `1,951` (`49 / 1,902`) | **2.04%** (`1/49`) `[0.0005, 0.1085]` (1-sided UB: `9.32%`) | `2.04%` (`1/49`) | **100.00%** (`1,902/1,902`) `[0.9981, 1.0000]` | **0.9993** | **PASS** |
| **E2-MAFAULDA** (Severity-Grouped, 64 Dual-Track 8-Ch features) | **`P2`** (Newton-GBDT) | `1,951` (`49 / 1,902`) | **2.04%** (`1/49`) `[0.0005, 0.1085]` (1-sided UB: `9.32%`) | `2.04%` (`1/49`) | **98.00%** (`1,864/1,902`) `[0.9727, 0.9858]` | **0.9960** | **PASS** |
| **E3-Pool-Expanded** (`HUST + Ottawa + XJTU-SY`, 100% real data, `n0 = 87` healthy runs) | **`P2`** (Newton-GBDT + Integrative Conformal) | `279` (**`87` / `192`**) | **1.15%** (`1/87`) **`[0.0003, 0.0624]`** (**1-sided UB: `5.34%`**) | **4.17%** (`1/24`) `[0.0011, 0.2112]` | **82.29%** (`158/192`) `[0.7614, 0.8741]` | **0.9658** | **PASS** (Holm DeLong $p = 0.0113$) |
| **E3-Pool-Expanded** (`HUST + Ottawa + XJTU-SY`, 100% real data, `n0 = 87` healthy runs) | **`P1`** (Hybrid Ensemble) | `279` (**`87` / `192`**) | `6.90%` (`6/87`) `[0.0257, 0.1441]` | `12.50%` (`3/24`) | **85.42%** (`164/192`) `[0.7962, 0.9009]` | **0.9680** | AUC PASS (Holm DeLong $p = 0.0022$) |

---

## 3. Open-Set Novelty Gate (`E7-OpenSet`, Patched Weibull + Ledoit-Wolf Mahalanobis)

After patching `BUG-V5-06` (replacing raw Euclidean distance and hardcoded Weibull shape with Ledoit-Wolf class-covariance-whitened Mahalanobis distances and 2-parameter Weibull MLE `scipy.stats.weibull_min.fit`), **both held-out unseen fault mechanisms cleared the pre-registered `>= 90%` binary alarm recall AND `>= 0.85` Open-Set Novelty AUROC gates**:

| Held-Out Unseen Fault Class (`MAFAULDA`) | Unseen Recordings `n` | Binary Alarm Recall on Unseen Fault | Open-Set Novelty AUROC (Before Patch -> After Patch) | Gate (`Recall >= 90%` & `AUROC >= 0.85`) |
| :--- | :---: | :---: | :---: | :---: |
| **`imbalance`** (all 7 mass severities `6g..35g` excluded from training) | `333` | **100.00%** (`333 / 333`) | `0.7045` -> **0.9235** | **PASS** |
| **`horizontal-misalignment`** (all 4 offset severities `0.5mm..2.0mm` excluded from training) | `197` | **100.00%** (`197 / 197`) | `0.4940` -> **0.8570** | **PASS** |
