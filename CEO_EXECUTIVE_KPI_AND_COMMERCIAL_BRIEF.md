# CEO Executive Brief: APSENS Proposed KPIs, Problem Statement, Buyers & Commercial Economics

**Product:** APSENS (*Adaptive Problem Solving Experiential Navigation System*)
**Authored By:** VLTHR Lab ([vlthrlab.app](https://vlthrlab.app) | `vlthrlabs@gmail.com`)
**Primary Author & Product/KPI Owner:** Daniel Amlasawole (Head of Business, Product & Evidence Governance)
**Technical & Verification Contributors:** Saviour (Ufuoma) Amlasawole (Systems Build Lead), Victoria Ayinla Saviour (Head of Validation & Tools), and Blessing Obakpololo Amlasawole (Head of Verification, Controls & Provenance)
**Maturity Grade:** `BUILT_SYSTEM` (Lab-verified software; next milestone: `PROVEN_RESULT` via 4-to-6-Week Free Plant Trial)
**Industries Served:** Power Generation (50 Hz Grid), Upstream Oil & Gas Flowstations, Water & Utilities Treatment, and Manufacturing & Process Plants

---

## 1. What Exact Problems Are We Trying to Solve?

Industrial facilities do not suffer from a shortage of dashboards or Excel charts. They lose millions of dollars per year to **5 operational blind spots** that standard SCADA alarms and generic BI tools fail to solve:

1. **Late Alarms That Beat Nobody's Mobilization Window:** Standard SCADA high-high alarms fire when a bearing temperature hits 95 C or vibration hits 10 mm/s, leaving 2 to 6 hours before seizure. In Nigerian and global industrial operations, procuring a seal cartridge, crane, or OEM bearing and scheduling a safe shutdown takes **48 to 56 hours**. By the time SCADA rings, an unplanned trip is already guaranteed.
2. **Unspared Bottleneck Trips & Standby Start-Failure:** On a single-train Induced Draft Fan (Power Plant), Gas Lift Compressor (Oil & Gas), or Main Mill Drive Motor (Manufacturing), one unscheduled trip halts the entire plant (`$16,800` to `$312,000` / day lost output). Even on N+1 spared pumps, standby units suffer an empirical ~6% fail-to-start rate when called under emergency load.
3. **False-Alarm Fatigue & Blind Teardowns:** Naive ML anomaly detectors trigger constantly during normal load swings, motor startups, and standby cycles, or misdiagnose a broken $150 transmitter wire as a $180,000 mechanical failure. Operators mute them within two weeks.
4. **Messy, Unaudited Data Silos:** Plant engineers export 100 to 250 MB CSV/Excel files full of `"I/O Timeout"`, `"Bad"`, European decimal commas, and mixed date formats. Without cryptographic provenance (SHA-256) and ISO 8000 data-quality gating, no reliability director or insurer will trust an automated report.
5. **Zero Financial Translation for Leadership:** Maintenance engineers talk in `mm/s` and `kurtosis`; CFOs and Operations Directors approve budgets in **USD ($)** and **NGN (Naira)**. Without a counterfactual financial ledger proving how much money an early catch saved versus Run-to-Failure (RTF) and Calendar Time-Based Maintenance (TBM), reliability budgets get rejected.

**APSENS solves all 5 problems in one local, zero-cloud-lock-in, read-only desktop platform** combining (1) High-Speed 200+ MB Historian Intake & Replay, (2) Multi-Twin Physics + Dual-ML + 7-Layer TDAE Root-Cause Analyser, and (3) Financial Counterfactual Advisor & ISO 13374 Engineering Reporter.

---

## 2. All KPIs Proposed by APSENS (Targets vs. Current Lab Evidence)

| KPI Category | KPI Name | Target Threshold | Current Lab Status | Evidence Class |
| :--- | :--- | :--- | :--- | :--- |
| **Engineering / Lead Time** | Early Detection Lead Time Before Failure | `>= 56.0 hours` (beats spare-parts & crew mobilization window) | `>= 56.0h` achieved across held-out benchmarks (`Gate_T4`) | `BENCHMARK_MEASURED` |
| **Engineering / Detection** | Blind Held-Out Fault Recall & ROC-AUC | Recall `>= 90%`, ROC-AUC `>= 0.90` | Passing `Gate_T4` | `BENCHMARK_MEASURED` |
| **Engineering / Root Cause** | Multi-Equipment Mechanism Classification Accuracy | `>= 85%` across 7 equipment classes & 18 mechanisms | **18/18 (`100%`)** directional precedence (`Gate_T2`) | `BENCHMARK_MEASURED` |
| **Operational / Noise** | False Alarm Rate on Healthy Load Shifts & Startups (`M1`/`M6`) | `<= 1` false alarm per asset per day (`0` during startup/standby) | **0 false alarms** across 120 transitions; `4/4` startups blanked (`Gate_T3`) | `BENCHMARK_MEASURED` |
| **Operational / Sensor** | Sensor-vs-Machine Disambiguation (`M3`) | Isolate single-channel transmitter wire breaks before teardown | Single-channel `+45 sigma` spike isolated cleanly (`Gate_T3`) | `BENCHMARK_MEASURED` |
| **Data & Speed** | 200+ MB Historian CSV Ingestion & Rollup Speed (`M9`) | `< 5.0 seconds` load on standard laptop; `100%` messy SCADA recovery | **234.9 MB (`2M` rows) in `1.94s`**; `120/120` messy rows recovered (`Gate_T1`) | `BENCHMARK_MEASURED` |
| **Governance & Security** | Cryptographic Tamper Detection & Enterprise WDAC Safety | `100%` 1-byte tamper catch; `0` blocked `.pyd` DLL crashes | 1-field tamper caught at Epoch 1 (`Gate_T6`); `100%` WDAC-safe (`Gate_T7`) | `BENCHMARK_MEASURED` |
| **Commercial / Value** | Trial-to-Paid Conversion & Verified Client ROI | `>= 10x` Net Client ROI on single verified avoided shutdown | `10x` to `20x` ROI modeled across all 4 industries (`Gate_T5`) | `SIMULATED` (Target `CLIENT_MEASURED` in Trial) |

---

## 3. Who Pays for the Solution? (Buyer Personas & Budget Owners)

APSENS is NOT sold to individual junior technicians out of pocket. It is funded from **Plant Maintenance OPEX / Asset Integrity Budgets** by four decision-makers:

1. **Economic Buyer (Signs the Check):** **Chief Operations Officer (COO) / Plant Director / VP of Operations** (Power GenCos, Marginal Oil & Gas Producers, Cement/Process Plants, Water Corporations). Their bonus and P&L depend directly on plant availability (`>= 95%` uptime) and preventing unplanned downtime penalties.
2. **Technical Champion (Drives the 4-to-6-Week Trial):** **Reliability & Asset Integrity Manager / Maintenance Superintendent**. They own the rotating equipment roster, suffer directly from weekend emergency callouts, and need auditable ISO 13374 Decision Passports to justify planned shutdown windows to operations.
3. **Financial Gatekeeper (Validates the Scorecard):** **Chief Financial Officer (CFO) / Commercial Manager**. They sign off on the **6-Week Trial Value Scorecard** comparing Twin A (RTF exposure) vs. Twin C (APSENS planned intervention) in USD and NGN.
4. **IT / OT Security Approver (Clears Deployment):** **OT Cybersecurity / SCADA Lead**. Approves APSENS immediately because it runs 100% locally on an air-gapped or read-only workstation, has zero PLC write functions in code, triggers zero Windows Smart App Control blocks, and operates under a read/inspect NDA.

---

## 4. What Will the Cost of the Solution Be When It Gets Solved?

To eliminate buyer friction after an initial pitch, APSENS uses a **Zero-Risk Entry -> Proven Value Commercial Model**:

### Phase 1: 4-to-6-Week Free Pilot Trial (`$0` / `NGN 0`)
- Client uploads their last failure CSV ("Bring Your Last Failure and We Replay It") and runs APSENS locally on 1 critical bottleneck train (4 to 10 assets) for 42 days.
- At Day 42 (`M10` Handshake), APSENS automatically prints the **6-Week Trial Value Scorecard** audited against operator shift verdicts (`M5`).

### Phase 2: Post-Trial Commercial Pricing (Client Chooses Best Fit)

| Industry Tier | Typical Single-Trip Exposure (1 Day + Repair) | Option A: Fixed Monthly Facility Retainer (SaaS / Local License) | Option B: Value-Share Anchor (5% to 10% of Verified Avoided Loss) |
| :--- | :--- | :--- | :--- |
| **Water & Utilities Station** | `$16,800` - `$45,000` (`NGN 23.5M - 63M`) | **`$500 / month`** (`NGN 700,000 / mo`) | 5% - 8% of verified catch (`$2,250 - $3,600` per prevented trip) |
| **Manufacturing & Process Line** | `$54,000` - `$95,000` (`NGN 75.6M - 133M`) | **`$750 / month`** (`NGN 1,050,000 / mo`) | 5% - 8% of verified catch (`$4,750 - $7,600` per prevented trip) |
| **Power Generation Block (50 Hz)** | `$97,500` - `$240,000` (`NGN 136.5M - 336M`) | **`$1,200 / month`** (`NGN 1,680,000 / mo`) | 5% - 8% of verified catch (`$12,000 - $19,200` per prevented trip) |
| **Upstream Oil & Gas Flowstation** | `$145,000` - `$312,000` (`NGN 203M - 436.8M`) | **`$1,500 / month`** (`NGN 2,100,000 / mo`) | 5% - 8% of verified catch (`$15,600 - $24,960` per prevented trip) |

*(Default FX reference: `1,400 NGN/USD`, dynamically configurable in facility settings. Zero cloud hosting fee to client; runs on existing Windows hardware.)*

---

## 5. Why Would They Pay? (The Unignorable ROI Case)

1. **One Single Catch Pays for 5 to 15 Years of APSENS:** On a 4,000 bopd flowstation or 150 MW power block, preventing **one** unscheduled bearing/seal collapse saves `$145,000` to `$312,000` (`NGN 203M` to `NGN 436.8M`). Even at the highest monthly retainer (`$1,500/mo` = `$18,000/yr`), a single catch delivers an **8x to 17x net return** in year one.
2. **Zero Capital Risk (Pay Only After Proof):** Because the 4-to-6-week trial is free and anchored by the "Bring Your Last Failure" Replay Challenge, the buyer never has to gamble on slides or vendor promises.
3. **Solves What Enterprise APM Suites Charge `$150,000+/yr` For:** Legacy enterprise APM platforms (GE Predix, Aspen Mtell, AVEVA PI Vision + Analytics) require `$150,000` to `$500,000/yr`, 6-month cloud integration projects, and specialized data scientists. APSENS deploys locally in **10 minutes** for **`$500` to `$1,500/month`** with zero cloud lock-in and built-in Nigeria 50 Hz / NGN economics.
4. **Protects the Engineer's Job & Reputation:** Every alert ships with a **7-Layer TDAE Decision Passport** showing *what moved first*, *which alternative causes were ruled out*, *whether the sensor itself is healthy*, and *exact USD/NGN cost of waiting vs. acting*, turning the reliability engineer from a guesser into an auditable decision-maker.
