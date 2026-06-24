(venv) mcyber@mcyber-Apple-Virtualization-Generic-Platform:~/greentwin_sdg$ bash run_pipeline.sh

══════════════════════════════════════════════
  STEP 01 — World Bank WDI (API + published fallback)
══════════════════════════════════════════════

  Kuala Lumpur  (MYS)
    electrification_rate              [published, API]
    clean_cooking_access              [published, API]
    safe_water_access                 [published]
    urban_population_pct              [API]
    pm25_national_mean                [published, API]

  Singapore  (SGP)
    electrification_rate              [published, API]
    clean_cooking_access              [published, API]
    safe_water_access                 [published]
    urban_population_pct              [API]
    pm25_national_mean                [published, API]

  Bangkok  (THA)
    electrification_rate              [published, API]
    clean_cooking_access              [published, API]
    safe_water_access                 [published]
    urban_population_pct              [API]
    pm25_national_mean                [published, API]

  Jakarta  (IDN)
    electrification_rate              [published, API]
    clean_cooking_access              [published, API]
    safe_water_access                 [published]
    urban_population_pct              [API]
    pm25_national_mean                [published, API]

  Manila  (PHL)
    electrification_rate              [published, API]
    clean_cooking_access              [published, API]
    safe_water_access                 [published]
    urban_population_pct              [API]
    pm25_national_mean                [published, API]

  Ho Chi Minh City  (VNM)
    electrification_rate              [published, API]
    clean_cooking_access              [published, API]
    safe_water_access                 [published]
    urban_population_pct              [API]
    pm25_national_mean                [published, API]

  Phnom Penh  (KHM)
    electrification_rate              [published, API]
    clean_cooking_access              [published, API]
    safe_water_access                 [published]
    urban_population_pct              [API]
    pm25_national_mean                [published, API]

  Yangon  (MMR)
    electrification_rate              [published, API]
    clean_cooking_access              [published, API]
    safe_water_access                 [published]
    urban_population_pct              [API]
    pm25_national_mean                [published, API]

====================================================
  Saved → /home/mcyber/greentwin_sdg/data/raw/worldbank_wdi.csv  (40, 8)

  Data source summary (API = live World Bank; published = fallback):
source            API  published
city                            
Bangkok            14         11
Ho Chi Minh City   14         11
Jakarta            14         11
Kuala Lumpur       14         11
Manila             14         11
Phnom Penh         14         11
Singapore          14         11
Yangon             14         11
  ✓  worldbank_wdi.csv written

══════════════════════════════════════════════
  STEP 02 — UN SDG Targets (SDSN 2023 published values)
══════════════════════════════════════════════
  Saved → /home/mcyber/greentwin_sdg/data/raw/un_sdg_indicators.csv  ((160, 5))

  Mean gap score per city (Health & Environment):
    Bangkok                 31.6
    Ho Chi Minh City        32.7
    Jakarta                 35.1
    Kuala Lumpur            16.9
    Manila                  39.1
    Phnom Penh              62.2
    Singapore               7.0
    Yangon                  66.1
  ✓  un_sdg_indicators.csv written

══════════════════════════════════════════════
  STEP 03 — Real Air Quality (Open-Meteo CAMS, no API key)
══════════════════════════════════════════════

  Source : Open-Meteo Air Quality API (CAMS reanalysis)
  Period : 2020–2024
  Cities : 8

  [Kuala Lumpur]  lat=3.139  lon=101.6869
    2020: 8,784 hours  |  PM2.5 valid=0  mean=nan µg/m³
    2021: 8,760 hours  |  PM2.5 valid=0  mean=nan µg/m³
    2022: 8,760 hours  |  PM2.5 valid=3,592  mean=36.9 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=40.4 µg/m³
    2024: 8,784 hours  |  PM2.5 valid=8,784  mean=37.9 µg/m³
    ✓  43,848 hourly records  |  DCI=48.2%  |  saved → openmeteo_hourly_kuala_lumpur.parquet
  [Singapore]  lat=1.3521  lon=103.8198
    2020: 8,784 hours  |  PM2.5 valid=0  mean=nan µg/m³
    2021: 8,760 hours  |  PM2.5 valid=0  mean=nan µg/m³
    2022: 8,760 hours  |  PM2.5 valid=3,592  mean=21.0 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=18.2 µg/m³
    2024: 8,784 hours  |  PM2.5 valid=8,784  mean=14.3 µg/m³
    ✓  43,848 hourly records  |  DCI=48.2%  |  saved → openmeteo_hourly_singapore.parquet
  [Bangkok]  lat=13.7563  lon=100.5018
    2020: 8,784 hours  |  PM2.5 valid=0  mean=nan µg/m³
    2021: 8,760 hours  |  PM2.5 valid=0  mean=nan µg/m³
    2022: 8,760 hours  |  PM2.5 valid=3,593  mean=53.0 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=38.2 µg/m³
    2024: 8,784 hours  |  PM2.5 valid=8,784  mean=24.5 µg/m³
    ✓  43,848 hourly records  |  DCI=48.2%  |  saved → openmeteo_hourly_bangkok.parquet
  [Jakarta]  lat=-6.2088  lon=106.8456
    2020: 8,784 hours  |  PM2.5 valid=0  mean=nan µg/m³
    2021: 8,760 hours  |  PM2.5 valid=0  mean=nan µg/m³
    2022: 8,760 hours  |  PM2.5 valid=3,593  mean=57.8 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=63.9 µg/m³
    2024: 8,784 hours  |  PM2.5 valid=8,784  mean=62.9 µg/m³
    ✓  43,848 hourly records  |  DCI=48.2%  |  saved → openmeteo_hourly_jakarta.parquet
  [Manila]  lat=14.5995  lon=120.9842
    2020: 8,784 hours  |  PM2.5 valid=0  mean=nan µg/m³
    2021: 8,760 hours  |  PM2.5 valid=0  mean=nan µg/m³
    2022: 8,760 hours  |  PM2.5 valid=3,592  mean=15.1 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=15.8 µg/m³
    2024: 8,784 hours  |  PM2.5 valid=8,784  mean=14.5 µg/m³
    ✓  43,848 hourly records  |  DCI=48.2%  |  saved → openmeteo_hourly_manila.parquet
  [Ho Chi Minh City]  lat=10.8231  lon=106.6297
    2020: 8,784 hours  |  PM2.5 valid=0  mean=nan µg/m³
    2021: 8,760 hours  |  PM2.5 valid=0  mean=nan µg/m³
    2022: 8,760 hours  |  PM2.5 valid=3,593  mean=27.9 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=24.1 µg/m³
    2024: 8,784 hours  |  PM2.5 valid=8,784  mean=22.7 µg/m³
    ✓  43,848 hourly records  |  DCI=48.2%  |  saved → openmeteo_hourly_ho_chi_minh_city.parquet
  [Phnom Penh]  lat=11.5564  lon=104.9282
    2020: 8,784 hours  |  PM2.5 valid=0  mean=nan µg/m³
    2021: 8,760 hours  |  PM2.5 valid=0  mean=nan µg/m³
    2022: 8,760 hours  |  PM2.5 valid=3,593  mean=18.4 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=18.2 µg/m³
    2024: 8,784 hours  |  PM2.5 valid=8,784  mean=16.1 µg/m³
    ✓  43,848 hourly records  |  DCI=48.2%  |  saved → openmeteo_hourly_phnom_penh.parquet
  [Yangon]  lat=16.8661  lon=96.1951
    2020: 8,784 hours  |  PM2.5 valid=0  mean=nan µg/m³
    2021: 8,760 hours  |  PM2.5 valid=0  mean=nan µg/m³
    2022: 8,760 hours  |  PM2.5 valid=3,594  mean=26.2 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=21.3 µg/m³
    2024: 8,784 hours  |  PM2.5 valid=8,784  mean=17.1 µg/m³
    ✓  43,848 hourly records  |  DCI=48.2%  |  saved → openmeteo_hourly_yangon.parquet

==========================================================
  Cities fetched     : 8 / 8
  Total hourly rows  : 350,784
  Years covered      : [2020, 2021, 2022, 2023, 2024]

  Pollutant summary (µg/m³):
    pm25    mean=   28.80  std=  26.43  missing=51.8%
    pm10    mean=   41.81  std=  37.53  missing=51.8%
    no2     mean=   29.58  std=  33.96  missing=51.8%
    o3      mean=   64.85  std=  59.59  missing=51.9%
    co      mean=  829.02  std=1082.33  missing=51.8%

  Combined  → /home/mcyber/greentwin_sdg/data/raw/openmeteo_combined.parquet
  Log       → /home/mcyber/greentwin_sdg/data/raw/fetch_log.txt
  ✓  openmeteo_combined.parquet written

══════════════════════════════════════════════
  STEP 04 — Pre-processing and QC
══════════════════════════════════════════════
  Loading openmeteo_combined.parquet ...
  Raw hourly rows : 350,784  |  cities : ['Bangkok', 'Ho Chi Minh City', 'Jakarta', 'Kuala Lumpur', 'Manila', 'Phnom Penh', 'Singapore', 'Yangon']

── Step 1: QC filtering

── Step 2: Data Completeness Index
  DCI range: 0.00 – 1.00  |  mean: 0.482

── Step 3: Monthly aggregation
  Monthly AQ rows : 480

── Step 4: Log-transformation

── Step 5: WB annual → monthly (40 annual rows)

====================================================
  monthly_aq.csv  (480 rows)
  monthly_wb.csv  (480 rows)
  Report → /home/mcyber/greentwin_sdg/data/processed/preprocessing_report.txt

  Pollutant coverage:
    pm25    48% non-null
    pm10    48% non-null
    no2     48% non-null
    o3      48% non-null
    co      48% non-null
  ✓  monthly_aq.csv + monthly_wb.csv written

══════════════════════════════════════════════
  STEP 05 — Feature Engineering (HEI, OBI, COP, SAS, DCI)
══════════════════════════════════════════════

  Feature matrix  : 480 rows × 29 features

  Feature                                     Mean       Std
  ----------------------------------------------------------
  pm25                                      28.812    18.768
  pm10                                      41.832    26.641
  no2                                       29.596    23.320
  o3                                        64.910    21.583
  co                                       829.984   763.131
  dci                                        0.482     0.499
  log_pm25                                   3.225     0.573
  log_pm10                                   3.592     0.565
  log_no2                                    3.094     0.859
  log_o3                                     4.136     0.325
  log_co                                     6.368     0.816
  hei                                        4.007     2.836
  obi                                        0.649     0.216
  cop                                      207.496   190.783
  sas                                       -0.121     0.735
  log_pm25_roll3                             3.229     0.542
  log_pm25_roll6                             3.237     0.506
  log_pm25_lag1                              3.247     0.539
  log_no2_roll3                              3.095     0.841
  log_no2_roll6                              3.107     0.823
  log_no2_lag1                               3.163     0.840
  hei_roll3                                  4.029     2.788
  hei_roll6                                  4.074     2.731
  hei_lag1                                   4.229     3.144
  clean_cooking_access                      74.993    22.463
  electrification_rate                      94.240    10.504
  pm25_national_mean                        24.778     8.925
  safe_water_access                         93.097     6.222
  urban_population_pct                      56.984    21.250

  Target cluster statistics:
    Health_Environment              mean=36.4  std=19.1  min=5.0  max=70.1
    Clean_Energy                    mean=21.6  std=17.6  min=5.0  max=58.6
    Climate_Action                  mean=42.9  std=9.1  min=25.6  max=62.5
    Institutional_Capacity          mean=40.3  std=14.9  min=11.8  max=67.2

  Saved → data/processed/feature_matrix.csv
  ✓  feature_matrix.csv written

══════════════════════════════════════════════
  STEP 06 — XGBoost Model Training
══════════════════════════════════════════════
  Features used : 29
  Total rows    : 480
  Cities        : ['Bangkok', 'Ho Chi Minh City', 'Jakarta', 'Kuala Lumpur', 'Manila', 'Phnom Penh', 'Singapore', 'Yangon']

────────────────────────────────────────────────────────────
  Cluster : Health_Environment
    Train:   145  Val:    29  Test:    58
    Train cities: ['Jakarta', 'Kuala Lumpur', 'Manila', 'Singapore', 'Yangon']
    Test  cities: ['Bangkok', 'Phnom Penh']
    Bayesian search (30 iterations) ...
    Best val MAE : 0.588
    Best params  : lr=0.017  depth=3  sub=0.89
    Test-set performance:
    XGBoost     MAE=5.34  RMSE=7.81  R²=0.757
    Ridge       MAE=4.37  RMSE=5.10  R²=0.897
    MAE improvement vs Ridge : -22.2%

────────────────────────────────────────────────────────────
  Cluster : Clean_Energy
    Train:   145  Val:    29  Test:    58
    Train cities: ['Jakarta', 'Kuala Lumpur', 'Manila', 'Singapore', 'Yangon']
    Test  cities: ['Bangkok', 'Phnom Penh']
    Bayesian search (30 iterations) ...
    Best val MAE : 5.470
    Best params  : lr=0.143  depth=6  sub=0.66
    Test-set performance:
    XGBoost     MAE=7.47  RMSE=9.02  R²=0.755
    Ridge       MAE=7.66  RMSE=8.27  R²=0.794
    MAE improvement vs Ridge : 2.5%

────────────────────────────────────────────────────────────
  Cluster : Climate_Action
    Train:   145  Val:    29  Test:    58
    Train cities: ['Jakarta', 'Kuala Lumpur', 'Manila', 'Singapore', 'Yangon']
    Test  cities: ['Bangkok', 'Phnom Penh']
    Bayesian search (30 iterations) ...
    Best val MAE : 1.148
    Best params  : lr=0.238  depth=6  sub=0.78
    Test-set performance:
    XGBoost     MAE=5.77  RMSE=6.82  R²=0.106
    Ridge       MAE=3.42  RMSE=4.01  R²=0.691
    MAE improvement vs Ridge : -68.9%

────────────────────────────────────────────────────────────
  Cluster : Institutional_Capacity
    Train:   145  Val:    29  Test:    58
    Train cities: ['Jakarta', 'Kuala Lumpur', 'Manila', 'Singapore', 'Yangon']
    Test  cities: ['Bangkok', 'Phnom Penh']
    Bayesian search (30 iterations) ...
    Best val MAE : 0.219
    Best params  : lr=0.057  depth=3  sub=0.80
    Test-set performance:
    XGBoost     MAE=4.19  RMSE=5.22  R²=0.696
    Ridge       MAE=4.99  RMSE=6.51  R²=0.529
    MAE improvement vs Ridge : 15.9%

============================================================
  FINAL PERFORMANCE SUMMARY (XGBoost, test set)
============================================================
               Cluster   MAE  RMSE    R²  Δ vs Baseline (%)
    Health_Environment 5.337 7.812 0.757              -22.2
          Clean_Energy 7.470 9.017 0.755                2.5
        Climate_Action 5.768 6.817 0.106              -68.9
Institutional_Capacity 4.192 5.225 0.696               15.9

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
      electrification_rate                 |SHAP|=7.060  (33.9%)
      pm25_national_mean                   |SHAP|=6.003  (28.8%)
      clean_cooking_access                 |SHAP|=5.191  (24.9%)
    Top-3 cumulative variance : 87.6%
    SHAP local accuracy residual (mean) : 0.00001

───────────────────────────────────────────────────────
  Cluster : Clean_Energy
    Test records : 58
    Top-3 features (mean |SHAP|):
      clean_cooking_access                 |SHAP|=8.624  (42.8%)
      electrification_rate                 |SHAP|=4.521  (22.4%)
      safe_water_access                    |SHAP|=3.123  (15.5%)
    Top-3 cumulative variance : 80.8%
    SHAP local accuracy residual (mean) : 0.00001

───────────────────────────────────────────────────────
  Cluster : Climate_Action
    Test records : 58
    Top-3 features (mean |SHAP|):
      clean_cooking_access                 |SHAP|=5.499  (44.0%)
      urban_population_pct                 |SHAP|=1.828  (14.6%)
      electrification_rate                 |SHAP|=1.749  (14.0%)
    Top-3 cumulative variance : 72.7%
    SHAP local accuracy residual (mean) : 0.00002

───────────────────────────────────────────────────────
  Cluster : Institutional_Capacity
    Test records : 58
    Top-3 features (mean |SHAP|):
      pm25_national_mean                   |SHAP|=6.701  (43.3%)
      electrification_rate                 |SHAP|=3.149  (20.3%)
      clean_cooking_access                 |SHAP|=2.559  (16.5%)
    Top-3 cumulative variance : 80.2%
    SHAP local accuracy residual (mean) : 0.00001

=======================================================
  SHAP SUMMARY TABLE (Table III of paper)
=======================================================
           SDG Cluster        Top Feature 1        Top Feature 2        Top Feature 3  Cumulative Variance (%)
    Health_Environment electrification_rate   pm25_national_mean clean_cooking_access                     87.6
          Clean_Energy clean_cooking_access electrification_rate    safe_water_access                     80.8
        Climate_Action clean_cooking_access urban_population_pct electrification_rate                     72.7
Institutional_Capacity   pm25_national_mean electrification_rate clean_cooking_access                     80.2

  SHAP values  → /home/mcyber/greentwin_sdg/outputs/results/shap_values_<cluster>.csv
  Importance   → /home/mcyber/greentwin_sdg/outputs/results/shap_importance_<cluster>.csv
  Summary tbl  → /home/mcyber/greentwin_sdg/outputs/results/shap_summary_table.csv
  Report       → /home/mcyber/greentwin_sdg/outputs/results/shap_report.txt
  ✓  shap_summary_table.csv written

══════════════════════════════════════════════
  STEP 08 — Figures (Fig 2 + Fig 3 only)
══════════════════════════════════════════════
  Best-performing cluster : Institutional_Capacity

── Figure 2: SHAP Beeswarm
  Fig 2 saved  →  /home/mcyber/greentwin_sdg/outputs/figures/Fig2_SHAP_Beeswarm.png
── Figure 3: SDG Gap Heatmap (all 8 cities)
  Fig 3 SKIP — allcity_preds_Institutional_Capacity.csv not found

  Done. Figures → /home/mcyber/greentwin_sdg/outputs/figures/
  ✓  Fig2_SHAP_Beeswarm.png + Fig3_SDG_Heatmap.png written

══════════════════════════════════════════════
  ✓  Pipeline complete in 125s
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

