<h1 align="center">🔥 Digital Twin Framework for Forest Fire Prediction 🌲</h1>

<p align="center">
  Wildfire risk prediction and spread simulation for Karnataka, the Western Ghats and other fire-prone Indian states.<br>
  Final-year capstone project, Dept. of Information Science &amp; Engineering, BMS College of Engineering (2026).
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Streamlit-Dashboard-FF4B4B?style=flat-square&logo=streamlit&logoColor=white" alt="Streamlit">
  <img src="https://img.shields.io/badge/TensorFlow-CNN%2BLSTM-FF6F00?style=flat-square&logo=tensorflow&logoColor=white" alt="TensorFlow">
  <img src="https://img.shields.io/badge/XGBoost-Model-189AB4?style=flat-square" alt="XGBoost">
  <img src="https://img.shields.io/badge/scikit--learn-Random%20Forest-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" alt="scikit-learn">
  <img src="https://img.shields.io/badge/MySQL-Database-4479A1?style=flat-square&logo=mysql&logoColor=white" alt="MySQL">
  <img src="https://img.shields.io/badge/Google%20Maps-API-4285F4?style=flat-square&logo=googlemaps&logoColor=white" alt="Google Maps">
  <img src="https://img.shields.io/badge/NASA-FIRMS-0B3D91?style=flat-square&logo=nasa&logoColor=white" alt="NASA FIRMS">
</p>

<p align="center">
  <a href="https://forest-fire-twin.streamlit.app/Spread_Simulation">
    <img src="https://img.shields.io/badge/LAUNCH-LIVE%20APPLICATION-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Launch Live Application">
  </a>
</p>

<p align="center">
  <a href="https://forest-fire-twin.streamlit.app/Spread_Simulation">https://forest-fire-twin.streamlit.app/Spread_Simulation</a>
</p>

---

## 📸 Screenshots

### 🛰️ Command Center
Regional monitoring: status strip, alert panel, key metrics and live feed status.

<p align="center">
  <img src="screenshots/01-command-center.png" width="100%" alt="Command Center">
</p>

### 🗺️ Regional Risk Map
Model-predicted risk per grid zone with NASA FIRMS detections overlaid on Google satellite imagery.

<p align="center">
  <img src="screenshots/02-regional-risk-map.png" width="100%" alt="Regional Risk Map">
</p>

### 🧪 What-If Simulator
Set weather, location, ignition points and simulation domain for a hypothetical scenario.

<p align="center">
  <img src="screenshots/03-what-if-simulator.png" width="100%" alt="What-If Simulator">
</p>

### 🔥 Spread Simulation
Cellular Automata fire propagation with flames, smoke, burn scar and playback controls.

<p align="center">
  <img src="screenshots/04-spread-simulation.png" width="100%" alt="Spread Simulation">
</p>

---

## 🧭 Application Modules

| Module | Purpose |
|---|---|
| Command Center | Regional forest fire monitoring |
| What-If Simulator | Hypothetical fire scenario modelling |
| Spread Simulation | Cellular Automata-based fire propagation |
| Historical Time Machine | Historical fire detection analysis |
| Model Insights | Machine learning model insights |

---

## 📌 Project at a Glance

| Item | Details |
|---|---|
| **Problem** | Wildfires are detected late and spread unpredictably; raw accuracy hides poor fire detection (only ~4% of zone-days burn) |
| **Solution** | Live data ingestion, FWI computation, ML risk scoring, Cellular Automata spread simulation, authenticated dashboard |
| **Coverage** | Karnataka / Western Ghats (0.1° grid, validated) + 8 more states (0.5° grid) |
| **Data used** | 3 real fire seasons of satellite-confirmed detections; 2025 season held out for testing |
| **Users** | Admin (user management, history, alerts) and Viewer (full read access) |
| **Status** | Academic project, working end-to-end (offline demo mode available) |

---

## ✨ Key Features

| # | Feature | Description |
|---|---|---|
| 1 | **Live data ingestion** | NASA FIRMS fire detections + OpenWeatherMap weather (Meteostat for history) |
| 2 | **Fire Weather Index** | Full Canadian FWI system: FFMC, DMC, DC, BUI, FWI |
| 3 | **ML risk scoring** | Random Forest, XGBoost, CNN+LSTM per grid zone |
| 4 | **Fire-history features** | Previous-10-day fire activity, 5×5 neighbourhood activity, leave-one-season-out climatology |
| 5 | **Spread simulation** | Rate-of-spread Cellular Automaton (Canadian FBP equations) with slope, wind, fuel and DEM terrain |
| 6 | **What-If simulator** | Custom weather, ignition points, forest preset or any searched place, 1 min to 4 h duration |
| 7 | **Land-cover awareness** | OpenStreetMap-based fuel / non-fuel masks (water, roads, buildings, bare rock) |
| 8 | **3D map playback** | Google Maps WebGL overlay: flames, smoke, embers, ash, burn scar |
| 9 | **Alerts** | Email on *new* EXTREME zones only; opt-in emergency alerts via email / SMS (admin) |
| 10 | **Reports** | PDF / DOCX / printable simulation report, CSV + GeoJSON export |
| 11 | **Live Activity Log** | Every refresh, alert, simulation, sign-in and admin change (5 s updates) |
| 12 | **Background scheduler** | Refreshes data without the dashboard open (cron-like) |
| 13 | **Auth + roles** | Login-gated dashboard, admin / viewer roles |
| 14 | **Honest data status** | Feeds labelled `LIVE`, `CACHED`, `UNAVAILABLE`, `NOT CONFIGURED`, `DEMO`; synthetic data never shown as live |

---

## 🧰 Tech Stack & Tools

| Category | Technology | Used For |
|---|---|---|
| **Language** | Python 3.11 | Entire pipeline (TensorFlow needs 3.11 or lower) |
| **Dashboard** | Streamlit | Multi-page web UI, dark theme |
| **ML (classical)** | scikit-learn, XGBoost | Random Forest, XGBoost models |
| **ML (deep)** | TensorFlow / Keras | CNN+LSTM model |
| **Data** | pandas, NumPy | Feature engineering, grids, zone-days |
| **Simulation** | Custom Cellular Automaton | 2-hour regional and local spread |
| **Database** | MySQL 8 (SQLAlchemy + PyMySQL), SQLite fallback | Snapshots, alerts, users, activity log |
| **Maps** | Google Maps JavaScript API, Geocoding / Places API | Satellite map, search, 3D view |
| **Satellite data** | NASA FIRMS (VIIRS_SNPP_NRT) | Active fire detections |
| **Weather** | OpenWeatherMap, Meteostat | Live and historical weather |
| **Terrain** | Open-Topo-Data / Open-Meteo DEM | Slope for spread model |
| **Land cover** | OpenStreetMap (Overpass API) | Fuel / non-fuel classification |
| **Notifications** | SMTP (Gmail), Twilio | Email and SMS alerts |
| **Reports** | ReportLab, python-docx, Matplotlib | PDF / DOCX reports |
| **Testing** | pytest | Pipeline, leakage, storage, auth tests |
| **Deployment** | Streamlit Community Cloud | Hosting |
| **Config / Secrets** | `.env`, `.streamlit/config.toml` | Keys and theme |

---

## 🏗️ Architecture

| Layer | Responsibility | Location |
|---|---|---|
| 1. Data Acquisition | FIRMS + weather clients, grid builder | `src/data_ingestion/` |
| 2. Data Processing | Canadian FWI system | `src/data_processing/` |
| 3. ML Prediction | Models, risk tiers, model routing | `src/ml_models/` |
| 4. CA Simulation | Spread simulator, ROS model, ignition check | `src/simulation/` |
| 5. Digital Twin + UI | Twin state, alert engine, dashboard | `src/digital_twin/`, `src/dashboard/` |
| Persistence | MySQL / SQLite storage | `src/storage/database.py` |
| Notifications | Email alerts on new EXTREME zones | `src/notifications/email_notifier.py` |
| Scheduling | Background refresh loop | `src/scheduler/scheduler.py` |
| Auth | Login + role gating | `src/auth/auth_gate.py` |
| Regions | Indian fire-prone state presets | `src/regions.py` |

**Data flow:** `FIRMS + Weather → FWI → Fire-history features → ML models → Risk tiers → Digital Twin → CA Simulation → Dashboard / Alerts / Reports`

---

## 🤖 Model Results

Evaluated on the held-out 2025 season, never seen in training.

| Model | AUC-ROC | Avg Precision | Alert: Accuracy / Fires Caught | Early Warning: Accuracy / Fires Caught |
|---|---|---|---|---|
| Random Forest | 0.863 | 0.243 | 92.3% / 41% | 78.3% / 77% |
| **XGBoost** | **0.870** | 0.259 | 91.2% / 48% | 74.6% / **84%** |
| CNN+LSTM | 0.862 | **0.263** | 91.4% / **49%** | 74.6% / 82% |
| XGBoost v1 (weather only) | 0.807 | 0.143 | 92.4% / 22% | 71.9% / 75% |

> Thresholds were chosen on training data only. *Alert* = lowest threshold with 92% or higher validation accuracy. *Early Warning* = ~80% validation recall.

### 🚨 Alert Tiers

Tiers are anchored to measured hit rates.

| Tier | Zone-days Flagged | Fires Captured | Hit Rate (base rate 4.3%) |
|---|---|---|---|
| 🔴 EXTREME | 1.3% | 12.6% | 43.2% |
| 🟠 HIGH or above | 8.7% | 48.4% | 24.2% |
| 🟡 MODERATE or above | 28.3% | 83.5% | 12.8% |

---

## 🎯 Impact & Benefits

| Area | Impact / Benefit | Evidence |
|---|---|---|
| **Detection quality** | v2 fire-history features lifted fires caught at alert threshold from 22% to 48% | XGBoost v1 vs v2 |
| **Ranking quality** | AUC-ROC improved from 0.807 to 0.870 | Held-out 2025 season |
| **Alert reliability** | EXTREME tier hits 43.2% of the time (~10× the 4.3% base rate) | Alert tier table |
| **Early warning** | Up to 84% of fires caught at the early-warning operating point | XGBoost |
| **Resource targeting** | Top 8.7% of zone-days captures 48.4% of fires | Alert tier table |
| **Train / serve consistency** | One shared feature module for training and live inference, verified by a test | `fire_history.py` + tests |
| **Data integrity** | Static heat sources (steel plants, kilns, ~10% of detections) removed from labels and live feed | Learned static mask |
| **Always-on monitoring** | Scheduler refreshes and emails alerts with no dashboard open | `scheduler.py` |
| **No alert spam** | Email only when a zone *first* becomes EXTREME | `email_notifier.py` |
| **Planning tool** | What-If simulator lets officials test weather and ignition scenarios | What-If + Spread pages |
| **Transparency** | Every feed is labelled honestly; simulated output is always marked SIMULATED | Status badges |
| **Accountability** | Full audit trail of users, alerts and simulations | Activity Log, Admin page |
| **Accessibility** | Runs fully offline with synthetic data, no API keys needed | Demo mode |

> **Why not raw accuracy?** Predicting "no fire" everywhere scores 95.6% accuracy while catching nothing. AUC-ROC, average precision and recall at a fixed alert budget are the real metrics.

---

## 🌏 Regions Covered

| Region | Grid | Validation |
|---|---|---|
| Karnataka / Western Ghats | 0.1° | Validated on held-out season |
| Uttarakhand, Himachal Pradesh, Odisha, Chhattisgarh, Madhya Pradesh, Maharashtra, Andhra Pradesh / Telangana, Assam | 0.5° | Per-state metrics after running `build_india_regions_dataset.py --train` (pooled pan-India model) |
| Custom lat/lon box | n/a | Not validated |

---

## 🔥 Fire Spread Simulation

| Aspect | Details |
|---|---|
| **Model** | Rate-of-spread CA (`ros`, default) using Canadian FBP equations; original probability CA still available (`legacy`) |
| **Spread inputs** | FFMC, wind, BUI, slope (DEM), NDVI fuel continuity, ±25% fuel variability |
| **Neighbourhood** | 24 nearest neighbours with true-distance correction |
| **Cell size** | 5 / 10 / **25** / 50 m |
| **Duration** | 1 min to 4 h, always computed in full |
| **Domain** | Auto, Local 1 km, Small 2 km, Medium 5 km, Large 10 km, Custom (max 2 to 15 km) |
| **Ignition check** | Rejects roads, buildings, water, bare ground; accepts mapped vegetation |
| **Study region** | Bandipur Tiger Reserve boundary (official file if provided, else labelled approximate) |
| **Playback** | Play / pause / reset, 0.5× to 5×, layer toggles, camera presets (browser-side) |
| **Exports** | CSV (every step), GeoJSON (burned cells), PDF / DOCX report |

### 🌿 Fuel / Non-fuel Land Cover (OpenStreetMap)

| Class | OSM Features | Fire Behaviour |
|---|---|---|
| WATER | `natural=water`, rivers, canals, reservoirs | Never ignites or spreads into |
| BUILT | buildings, residential / industrial / commercial | Never ignites or spreads into |
| ROAD | paved highways, railways | Never ignites or spreads into |
| NON_FUEL | bare rock, scree, sand, quarries, runways | Never ignites or spreads into |
| FUEL | everything else | Unchanged |

---

## 📡 Data Sources & Status Labels

| Source | Data | Scope |
|---|---|---|
| NASA FIRMS | VIIRS_SNPP_NRT detections | Region: last 10 days. Location: 25×25 km box, last 2 days |
| OpenWeatherMap | Current weather | Region weather grid + selected location |
| Meteostat | Historical weather | Model training |
| Open-Topo-Data / Open-Meteo | DEM (~90 m lattice) | Slope for spread model |
| OpenStreetMap (Overpass) | Land cover, ignition checks | Simulation domain |
| Google Maps | Satellite map, geocoding | UI |

| Status | Meaning |
|---|---|
| 🟢 `LIVE` | Real data just delivered |
| 🟡 `CACHED` | Request failed; last real response shown with timestamp |
| 🔴 `UNAVAILABLE` | No data shown, nothing invented |
| ⚪ `NOT CONFIGURED` | API key missing |
| 🟣 `DEMO` | Synthetic data |

---

## ⚙️ Setup

**Requires Python 3.11** (TensorFlow does not yet support 3.12+).

```bash
git clone https://github.com/praveenkumar7i/digital-twin-framework-for-forest-fire-monitoring.git
cd digital-twin-framework-for-forest-fire-monitoring
python -m venv venv
venv\Scripts\activate          # Windows
# source venv/bin/activate     # macOS/Linux
pip install -r requirements.txt          # dashboard + scheduler (deployment)
pip install -r requirements-train.txt    # only for retraining / tests
pip install reportlab python-docx matplotlib   # reports
```

### 🔑 Environment Variables

Copy `.env.example` to `.env`.

| Variable | Purpose | Required |
|---|---|---|
| `FIRMS_MAP_KEY` | NASA FIRMS ([get key](https://firms.modaps.eosdis.nasa.gov/api/)) | Optional |
| `OWM_API_KEY` | OpenWeatherMap ([get key](https://home.openweathermap.org/api_keys)), activation up to 2 h | Optional |
| `GOOGLE_MAPS_API_KEY` | Maps JavaScript API + Geocoding / Places API | Optional |
| `GOOGLE_MAPS_MAP_ID` | Vector Map ID for 3D tilt / rotation | Optional |
| `DATABASE_URL` | `mysql+pymysql://USER:PASSWORD@HOST:PORT/DBNAME` (SQLite if unset) | Optional |
| `DATABASE_SSL` / `DATABASE_SSL_CA` | TLS for MySQL host | Optional |
| `SMTP_HOST`, `SMTP_USER`, `SMTP_PASSWORD` | Email alerts | Optional |
| `ALERT_RECIPIENT_EMAILS` | Alert recipients | Optional |
| `TWILIO_ACCOUNT_SID`, `TWILIO_AUTH_TOKEN`, `TWILIO_FROM_NUMBER` | SMS alerts | Optional |
| `ALERT_PROVIDER_MODE=mock` | Test alerts without sending | Optional |
| `DEFAULT_ADMIN_USERNAME`, `DEFAULT_ADMIN_PASSWORD` | Set before first run | Optional |

> With no keys, the system runs fully in **offline / demo mode** with synthetic data.

### 🔐 Default Login

| Username | Password |
|---|---|
| `admin` | `changeme123` |

Change the password from the Admin page after first sign-in.

---

## ▶️ Running

| Task | Command |
|---|---|
| Full pipeline (one shot) | `python main.py` |
| Pipeline with retraining | `python main.py --train` |
| Build Karnataka dataset | `python src/ml_models/build_real_dataset.py` |
| Train models | `python src/ml_models/train_real.py` |
| Build all-India data + train | `python scripts/build_india_regions_dataset.py --train` (needs `FIRMS_MAP_KEY`, ~1 to 2 h first time, resumable) |
| **Launch dashboard** | `streamlit run src/dashboard/app.py` |
| Scheduler (forever) | `python -m src.scheduler.scheduler` |
| Scheduler (single cycle, for cron / Task Scheduler) | `python -m src.scheduler.scheduler --once` |
| Migrate SQLite to MySQL | `python scripts/migrate_sqlite_to_mysql.py` |
| Run tests | `pytest tests/ -v` |
| Benchmarks | `python scripts/benchmark_phase3.py` and `python scripts/benchmark_ui_offline.py` |

---

## 🖥️ Dashboard Pages

| Page | Purpose | Access |
|---|---|---|
| Command Center | Status strip, alert panel, key metrics, regional risk map | All |
| What-If Simulator | Scenario weather, location, ignition setup | All |
| Spread Simulation | Run and play the fire spread | All |
| History | Past snapshots | All |
| Briefing | Summary view | All |
| Insights | Model and data insights | All |
| Admin | Users, raw history, notification setup, emergency alert audit | Admin |
| Activity Log | Live feed of all system / user actions | All |

---

## 🚨 Reports & Emergency Alerts

| Capability | Details |
|---|---|
| **Report** | PDF / DOCX / printable view, report ID `FFDT-…`, built from the stored run snapshot |
| **Emergency alert** | Admin only, opt-in: review dialog, recipients (enabled, verified channels), explicit confirmation |
| **Safety wording** | What-If alerts always state *"SIMULATION ONLY: hypothetical scenario, not confirmation of an active fire."* |
| **Audit** | Every attempt logged (Admin → Emergency alerts) |
| **Statuses** | Provider's own (accepted / queued / failed / not configured / mock), never "delivered" without confirmation |

---

## 📁 Project Structure

```
config/config.py                    Central configuration
main.py                             Single entry point for the full pipeline
src/
├── regions.py                      Indian region presets
├── data_ingestion/                 firms_client, weather_client, ingestion_module
├── data_processing/                feature_engineering (Canadian FWI)
├── ml_models/                      model_trainer, fire_history, risk_index, model_registry,
│                                   build_real_dataset, train_real, timeseries_builder, train
├── simulation/                     cellular_automata, ros_ca, fire_behaviour, ignition_site
├── digital_twin/                   twin_state (DigitalTwin + AlertEngine)
├── storage/                        database (SQLAlchemy)
├── notifications/                  email_notifier
├── scheduler/                      scheduler
├── auth/                           auth_gate
├── landcover/                      Optional research module (WorldCover + OSM + Sentinel-2)
└── dashboard/                      app.py, pages/1-5_*, 6_Admin, 7_Activity_Log, ui/, static/
scripts/                            build_india_regions_dataset, migrate_sqlite_to_mysql, benchmarks
tests/                              test_pipeline, test_fire_history, test_storage_auth_notifications
```

---

## ✅ Testing

| Test File | Covers |
|---|---|
| `test_pipeline.py` | Integration + regression |
| `test_fire_history.py` | Train / serve feature parity, leakage rules, India builder |
| `test_storage_auth_notifications.py` | Storage, auth, notifications, activity log |

---

## 🔮 Future Scope

| Idea | Benefit |
|---|---|
| Real NDVI / fuel-moisture rasters | Better fuel modelling |
| Recursive FWI carry-forward | More accurate moisture codes |
| Calibration against observed fire perimeters | Operational-grade spread forecasts |
| Firebreak, road and suppression modelling | More realistic scenarios |
| Ember spotting | Long-range spread |

---

## 📄 License

Academic project, BMS College of Engineering, 2026.
