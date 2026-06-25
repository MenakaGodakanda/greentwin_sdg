(venv) mcyber@mcyber-Apple-Virtualization-Generic-Platform:~/greentwin_sdg$ bash run_pipeline.sh

══════════════════════════════════════════════
  STEP 01 — World Bank WDI (API + published fallback)
══════════════════════════════════════════════

  Kuala Lumpur  (MYS)
    electrification_rate              [published, API]
    clean_cooking_access              [published, API]
    safe_water_access                 [published]
    urban_population_pct              [API]
    pm25_national_mean                [published]

  Singapore  (SGP)
    electrification_rate              [published, API]
    clean_cooking_access              [published, API]
    safe_water_access                 [published]
    urban_population_pct              [API]
    pm25_national_mean                [published]

  Bangkok  (THA)
    electrification_rate              [published, API]
    clean_cooking_access              [published, API]
    safe_water_access                 [published]
    urban_population_pct              [API]
    pm25_national_mean                [published]

  Jakarta  (IDN)
    electrification_rate              [published, API]
    clean_cooking_access              [published, API]
    safe_water_access                 [published]
    urban_population_pct              [API]
    pm25_national_mean                [published]

  Manila  (PHL)
    electrification_rate              [published, API]
    clean_cooking_access              [published, API]
    safe_water_access                 [published]
    urban_population_pct              [API]
    pm25_national_mean                [published]

  Ho Chi Minh City  (VNM)
    electrification_rate              [published, API]
    clean_cooking_access              [published, API]
    safe_water_access                 [published]
    urban_population_pct              [API]
    pm25_national_mean                [published]

  Phnom Penh  (KHM)
    electrification_rate              [published, API]
    clean_cooking_access              [published, API]
    safe_water_access                 [published]
    urban_population_pct              [API]
    pm25_national_mean                [published]

  Yangon  (MMR)
    electrification_rate              [published, API]
    clean_cooking_access              [published, API]
    safe_water_access                 [published]
    urban_population_pct              [API]
    pm25_national_mean                [published]

====================================================
  Saved → /home/mcyber/greentwin_sdg/data/raw/worldbank_wdi.csv  (24, 8)

  Data source summary (API = live World Bank; published = fallback):
source            API  published
city                            
Bangkok             7          8
Ho Chi Minh City    7          8
Jakarta             7          8
Kuala Lumpur        7          8
Manila              7          8
Phnom Penh          7          8
Singapore           7          8
Yangon              7          8
  ✓  worldbank_wdi.csv written

══════════════════════════════════════════════
  STEP 02 — UN SDG Targets (SDSN 2023 published values)
══════════════════════════════════════════════
  Saved → /home/mcyber/greentwin_sdg/data/raw/un_sdg_indicators.csv  ((96, 5))

  Mean gap score per city (Health & Environment):
    Bangkok                 29.4
    Ho Chi Minh City        31.3
    Jakarta                 32.4
    Kuala Lumpur            15.2
    Manila                  36.8
    Phnom Penh              59.8
    Singapore               5.5
    Yangon                  64.2
  ✓  un_sdg_indicators.csv written

══════════════════════════════════════════════
  STEP 03 — Real Air Quality (Open-Meteo CAMS, no API key)
══════════════════════════════════════════════

  Source : Open-Meteo Air Quality API (CAMS reanalysis)
  Period : 2022–2024
  Cities : 8

  [Kuala Lumpur]  lat=3.139  lon=101.6869
    2022: 8,760 hours  |  PM2.5 valid=3,592  mean=36.9 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=40.4 µg/m³
    2024: 8,784 hours  |  PM2.5 valid=8,784  mean=37.9 µg/m³
    ✓  26,304 hourly records  |  DCI=80.4%  |  saved → openmeteo_hourly_kuala_lumpur.parquet
  [Singapore]  lat=1.3521  lon=103.8198
    2022: 8,760 hours  |  PM2.5 valid=3,592  mean=21.0 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=18.2 µg/m³
    2024: 8,784 hours  |  PM2.5 valid=8,784  mean=14.3 µg/m³
    ✓  26,304 hourly records  |  DCI=80.4%  |  saved → openmeteo_hourly_singapore.parquet
  [Bangkok]  lat=13.7563  lon=100.5018
    2022: 8,760 hours  |  PM2.5 valid=3,593  mean=53.0 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=38.2 µg/m³
    2024: 8,784 hours  |  PM2.5 valid=8,784  mean=24.5 µg/m³
    ✓  26,304 hourly records  |  DCI=80.4%  |  saved → openmeteo_hourly_bangkok.parquet
  [Jakarta]  lat=-6.2088  lon=106.8456
    2022: 8,760 hours  |  PM2.5 valid=3,593  mean=57.8 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=63.9 µg/m³
    2024: 8,784 hours  |  PM2.5 valid=8,784  mean=62.9 µg/m³
    ✓  26,304 hourly records  |  DCI=80.4%  |  saved → openmeteo_hourly_jakarta.parquet
  [Manila]  lat=14.5995  lon=120.9842
    2022: 8,760 hours  |  PM2.5 valid=3,592  mean=15.1 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=15.8 µg/m³
    2024: 8,784 hours  |  PM2.5 valid=8,784  mean=14.5 µg/m³
    ✓  26,304 hourly records  |  DCI=80.4%  |  saved → openmeteo_hourly_manila.parquet
  [Ho Chi Minh City]  lat=10.8231  lon=106.6297
    2022: 8,760 hours  |  PM2.5 valid=3,593  mean=27.9 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=24.1 µg/m³
    2024: 8,784 hours  |  PM2.5 valid=8,784  mean=22.7 µg/m³
    ✓  26,304 hourly records  |  DCI=80.4%  |  saved → openmeteo_hourly_ho_chi_minh_city.parquet
  [Phnom Penh]  lat=11.5564  lon=104.9282
    2022: 8,760 hours  |  PM2.5 valid=3,593  mean=18.4 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=18.2 µg/m³
    2024: 8,784 hours  |  PM2.5 valid=8,784  mean=16.1 µg/m³
    ✓  26,304 hourly records  |  DCI=80.4%  |  saved → openmeteo_hourly_phnom_penh.parquet
  [Yangon]  lat=16.8661  lon=96.1951
    2022: 8,760 hours  |  PM2.5 valid=3,594  mean=26.2 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=21.3 µg/m³
    2024: 8,784 hours  |  PM2.5 valid=8,784  mean=17.1 µg/m³
    ✓  26,304 hourly records  |  DCI=80.4%  |  saved → openmeteo_hourly_yangon.parquet

==========================================================
  Cities fetched     : 8 / 8
  Total hourly rows  : 210,432
  Years covered      : [2022, 2023, 2024]

  Pollutant summary (µg/m³):
    pm25    mean=   28.80  std=  26.43  missing=19.6%
    pm10    mean=   41.81  std=  37.53  missing=19.6%
    no2     mean=   29.58  std=  33.96  missing=19.6%
    o3      mean=   64.85  std=  59.59  missing=19.7%
    co      mean=  829.02  std=1082.33  missing=19.6%

  Combined  → /home/mcyber/greentwin_sdg/data/raw/openmeteo_combined.parquet
  Log       → /home/mcyber/greentwin_sdg/data/raw/fetch_log.txt
  ✓  openmeteo_combined.parquet written

══════════════════════════════════════════════
  STEP 04 — Pre-processing and QC
══════════════════════════════════════════════
  Loading openmeteo_combined.parquet ...
  Raw hourly rows : 210,432  |  cities : ['Bangkok', 'Ho Chi Minh City', 'Jakarta', 'Kuala Lumpur', 'Manila', 'Phnom Penh', 'Singapore', 'Yangon']

── Step 1: QC filtering

── Step 2: Data Completeness Index
  DCI range: 0.00 – 1.00  |  mean: 0.803

── Step 3: Monthly aggregation
  Monthly AQ rows : 288

── Step 4: Log-transformation

── Step 5: WB annual → monthly (24 annual rows)

====================================================
  monthly_aq.csv  (288 rows)
  monthly_wb.csv  (288 rows)
  Report → /home/mcyber/greentwin_sdg/data/processed/preprocessing_report.txt

  Pollutant coverage:
    pm25    81% non-null
    pm10    81% non-null
    no2     81% non-null
    o3      81% non-null
    co      81% non-null
  ✓  monthly_aq.csv + monthly_wb.csv written

══════════════════════════════════════════════
  STEP 05 — Feature Engineering (HEI, OBI, COP, SAS, DCI)
══════════════════════════════════════════════

  Feature matrix  : 288 rows × 29 features

  Feature                                     Mean       Std
  ----------------------------------------------------------
  pm25                                      28.812    18.768
  pm10                                      41.832    26.641
  no2                                       29.596    23.320
  o3                                        64.910    21.583
  co                                       829.984   763.131
  dci                                        0.803     0.395
  log_pm25                                   3.225     0.573
  log_pm10                                   3.592     0.565
  log_no2                                    3.094     0.859
  log_o3                                     4.136     0.325
  log_co                                     6.368     0.816
  hei                                        4.007     2.836
  obi                                        0.649     0.216
  cop                                      207.496   190.783
  sas                                       -0.201     0.941
  log_pm25_roll3                             3.229     0.542
  log_pm25_roll6                             3.237     0.506
  log_pm25_lag1                              3.237     0.560
  log_no2_roll3                              3.095     0.841
  log_no2_roll6                              3.107     0.823
  log_no2_lag1                               3.121     0.853
  hei_roll3                                  4.029     2.788
  hei_roll6                                  4.074     2.731
  hei_lag1                                   4.109     2.987
  clean_cooking_access                      74.781    23.128
  electrification_rate                      94.067    11.713
  pm25_national_mean                        26.742     9.963
  safe_water_access                         92.525     6.598
  urban_population_pct                      57.450    21.197

  Target cluster statistics:
    Health_Environment              mean=34.3  std=18.8  min=5.0  max=64.8
    Clean_Energy                    mean=20.4  std=17.4  min=5.0  max=54.7
    Climate_Action                  mean=41.7  std=8.5  min=28.1  max=59.4
    Institutional_Capacity          mean=38.9  std=14.4  min=10.2  max=61.3

  Saved → data/processed/feature_matrix.csv
  ✓  feature_matrix.csv written

══════════════════════════════════════════════
  STEP 06 — XGBoost Model Training
══════════════════════════════════════════════
  Features used : 29
  Total rows    : 288
  Cities        : ['Bangkok', 'Ho Chi Minh City', 'Jakarta', 'Kuala Lumpur', 'Manila', 'Phnom Penh', 'Singapore', 'Yangon']

────────────────────────────────────────────────────────────
  Cluster : Health_Environment
    Train:   145  Val:    29  Test:    58
    Train cities: ['Jakarta', 'Kuala Lumpur', 'Manila', 'Singapore', 'Yangon']
    Test  cities: ['Bangkok', 'Phnom Penh']
    Bayesian search (30 iterations) ...
    Best val MAE : 1.572
    Best params  : lr=0.279  depth=3  sub=0.86
    Test-set performance:
    XGBoost     MAE=8.05  RMSE=11.23  R²=0.475
    Ridge       MAE=5.35  RMSE=6.80  R²=0.808
    MAE improvement vs Ridge : -50.4%

────────────────────────────────────────────────────────────
  Cluster : Clean_Energy
    Train:   145  Val:    29  Test:    58
    Train cities: ['Jakarta', 'Kuala Lumpur', 'Manila', 'Singapore', 'Yangon']
    Test  cities: ['Bangkok', 'Phnom Penh']
    Bayesian search (30 iterations) ...
    Best val MAE : 3.593
    Best params  : lr=0.143  depth=6  sub=0.66
    Test-set performance:
    XGBoost     MAE=8.39  RMSE=9.30  R²=0.759
    Ridge       MAE=8.33  RMSE=8.91  R²=0.779
    MAE improvement vs Ridge : -0.7%

────────────────────────────────────────────────────────────
  Cluster : Climate_Action
    Train:   145  Val:    29  Test:    58
    Train cities: ['Jakarta', 'Kuala Lumpur', 'Manila', 'Singapore', 'Yangon']
    Test  cities: ['Bangkok', 'Phnom Penh']
    Bayesian search (30 iterations) ...
    Best val MAE : 0.936
    Best params  : lr=0.193  depth=5  sub=0.74
    Test-set performance:
    XGBoost     MAE=2.40  RMSE=2.76  R²=0.835
    Ridge       MAE=7.30  RMSE=8.20  R²=-0.450
    MAE improvement vs Ridge : 67.2%

────────────────────────────────────────────────────────────
  Cluster : Institutional_Capacity
    Train:   145  Val:    29  Test:    58
    Train cities: ['Jakarta', 'Kuala Lumpur', 'Manila', 'Singapore', 'Yangon']
    Test  cities: ['Bangkok', 'Phnom Penh']
    Bayesian search (30 iterations) ...
    Best val MAE : 0.260
    Best params  : lr=0.027  depth=5  sub=0.71
    Test-set performance:
    XGBoost     MAE=6.04  RMSE=7.10  R²=0.591
    Ridge       MAE=7.01  RMSE=7.98  R²=0.484
    MAE improvement vs Ridge : 13.8%

============================================================
  FINAL PERFORMANCE SUMMARY (XGBoost, test set)
============================================================
               Cluster   MAE   RMSE    R²  Δ vs Baseline (%)
    Health_Environment 8.046 11.232 0.475              -50.4
          Clean_Energy 8.393  9.301 0.759               -0.7
        Climate_Action 2.395  2.764 0.835               67.2
Institutional_Capacity 6.040  7.102 0.591               13.8

  Models saved  → /home/mcyber/greentwin_sdg/outputs/models
  Metrics CSV   → /home/mcyber/greentwin_sdg/outputs/results/performance_metrics.csv
  Report        → /home/mcyber/greentwin_sdg/outputs/results/training_report.txt
  ✓  Models + performance_metrics.csv written

══════════════════════════════════════════════
  STEP 07 — SHAP Explainability
══════════════════════════════════════════════

───────────────────────────────────────────────────────
  Cluster : Health_Environment
    Test records : 58
    Top-3 features (mean |SHAP|):
      electrification_rate                 |SHAP|=8.594  (41.2%)
      urban_population_pct                 |SHAP|=4.491  (21.5%)
      pm25_national_mean                   |SHAP|=4.143  (19.8%)
    Top-3 cumulative variance : 82.5%
    SHAP local accuracy residual (mean) : 0.00001

───────────────────────────────────────────────────────
  Cluster : Clean_Energy
    Test records : 58
    Top-3 features (mean |SHAP|):
      electrification_rate                 |SHAP|=8.842  (47.5%)
      safe_water_access                    |SHAP|=4.447  (23.9%)
      pm25_national_mean                   |SHAP|=1.662  (8.9%)
    Top-3 cumulative variance : 80.3%
    SHAP local accuracy residual (mean) : 0.00001

───────────────────────────────────────────────────────
  Cluster : Climate_Action
    Test records : 58
    Top-3 features (mean |SHAP|):
      electrification_rate                 |SHAP|=5.060  (45.5%)
      safe_water_access                    |SHAP|=2.199  (19.8%)
      pm25_national_mean                   |SHAP|=0.959  (8.6%)
    Top-3 cumulative variance : 73.8%
    SHAP local accuracy residual (mean) : 0.00001

───────────────────────────────────────────────────────
  Cluster : Institutional_Capacity
    Test records : 58
    Top-3 features (mean |SHAP|):
      pm25_national_mean                   |SHAP|=6.971  (43.7%)
      electrification_rate                 |SHAP|=4.357  (27.3%)
      safe_water_access                    |SHAP|=1.526  (9.6%)
    Top-3 cumulative variance : 80.6%
    SHAP local accuracy residual (mean) : 0.00002

=======================================================
  SHAP SUMMARY TABLE (Table III of paper)
=======================================================
           SDG Cluster        Top Feature 1        Top Feature 2      Top Feature 3  Cumulative Variance (%)
    Health_Environment electrification_rate urban_population_pct pm25_national_mean                     82.5
          Clean_Energy electrification_rate    safe_water_access pm25_national_mean                     80.3
        Climate_Action electrification_rate    safe_water_access pm25_national_mean                     73.8
Institutional_Capacity   pm25_national_mean electrification_rate  safe_water_access                     80.6

  SHAP values  → /home/mcyber/greentwin_sdg/outputs/results/shap_values_<cluster>.csv
  Importance   → /home/mcyber/greentwin_sdg/outputs/results/shap_importance_<cluster>.csv
  Summary tbl  → /home/mcyber/greentwin_sdg/outputs/results/shap_summary_table.csv
  Report       → /home/mcyber/greentwin_sdg/outputs/results/shap_report.txt
  ✓  shap_summary_table.csv written

══════════════════════════════════════════════
  STEP 08 — Figures (Fig 2 + Fig 3 only)
══════════════════════════════════════════════

── Step A: Generating full-dataset predictions (all cities)
  Feature matrix loaded: 288 rows  cities=['Bangkok', 'Ho Chi Minh City', 'Jakarta', 'Kuala Lumpur', 'Manila', 'Phnom Penh', 'Singapore', 'Yangon']
  Health_Environment              232 rows  cities=['Bangkok', 'Ho Chi Minh City', 'Jakarta', 'Kuala Lumpur', 'Manila', 'Phnom Penh', 'Singapore', 'Yangon']
  Clean_Energy                    232 rows  cities=['Bangkok', 'Ho Chi Minh City', 'Jakarta', 'Kuala Lumpur', 'Manila', 'Phnom Penh', 'Singapore', 'Yangon']
  Climate_Action                  232 rows  cities=['Bangkok', 'Ho Chi Minh City', 'Jakarta', 'Kuala Lumpur', 'Manila', 'Phnom Penh', 'Singapore', 'Yangon']
  Institutional_Capacity          232 rows  cities=['Bangkok', 'Ho Chi Minh City', 'Jakarta', 'Kuala Lumpur', 'Manila', 'Phnom Penh', 'Singapore', 'Yangon']

  Best-performing cluster : Climate_Action

── Figure 2: SHAP Beeswarm
  Fig 2 saved  →  /home/mcyber/greentwin_sdg/outputs/figures/Fig2_SHAP_Beeswarm.png

── Figure 3: SDG Gap Heatmap (all 8 cities)
  Fig 3 saved  →  /home/mcyber/greentwin_sdg/outputs/figures/Fig3_SDG_Heatmap.png

  Done. Figures → /home/mcyber/greentwin_sdg/outputs/figures/
  ✓  Fig2_SHAP_Beeswarm.png + Fig3_SDG_Heatmap.png written

══════════════════════════════════════════════
  ✓  Pipeline complete in 83s
══════════════════════════════════════════════

  Data sources used:
    Air quality : Open-Meteo CAMS Reanalysis API (REAL, free, no key)
    World Bank  : api.worldbank.org (REAL, free) or published fallback
    SDG targets : SDSN 2023 Sustainable Development Report (published)

  Key outputs:
    outputs/figures/Fig2_SHAP_Beeswarm.png
    outputs/figures/Fig3_SDG_Heatmap.png
    outputs/results/performance_metrics.csv
    outputs/results/shap_summary_table.csv
(venv) mcyber@mcyber-Apple-Virtualization-Generic-Platform:~/greentwin_sdg$ 
