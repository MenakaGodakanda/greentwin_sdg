(venv) mcyber@mcyber-Apple-Virtualization-Generic-Platform:~/greentwin_sdg$ bash run_pipeline.sh

======================================================
  PRE-FLIGHT CHECK
======================================================
  All SDSN 2024 scores filled in.

======================================================
  STEP 01 - World Bank WDI (API only, no fallback)
======================================================
  Checking World Bank API connectivity ...
  ✓ API reachable


  Malaysia (MYS)
    electrification_rate              ✓ 2 years with data: [2022, 2023]
    clean_cooking_access              ✓ 2 years with data: [2022, 2023]
    safe_water_access                 ✗ no data returned from API  missing: [2022, 2023]
    urban_population_pct              ✓ 2 years with data: [2022, 2023]
    pm25_national_mean                ✗ no data returned from API  missing: [2022, 2023]

  Singapore (SGP)
    electrification_rate              ✓ 2 years with data: [2022, 2023]
    clean_cooking_access              ✓ 2 years with data: [2022, 2023]
    safe_water_access                 ✗ no data returned from API  missing: [2022, 2023]
    urban_population_pct              ✓ 2 years with data: [2022, 2023]
    pm25_national_mean                ✗ no data returned from API  missing: [2022, 2023]

  Thailand (THA)
    electrification_rate              ✓ 2 years with data: [2022, 2023]
    clean_cooking_access              ✓ 2 years with data: [2022, 2023]
    safe_water_access                 ✗ no data returned from API  missing: [2022, 2023]
    urban_population_pct              ✓ 2 years with data: [2022, 2023]
    pm25_national_mean                ✗ no data returned from API  missing: [2022, 2023]

  Indonesia (IDN)
    electrification_rate              ✓ 2 years with data: [2022, 2023]
    clean_cooking_access              ✓ 2 years with data: [2022, 2023]
    safe_water_access                 ✗ no data returned from API  missing: [2022, 2023]
    urban_population_pct              ✓ 2 years with data: [2022, 2023]
    pm25_national_mean                ✗ no data returned from API  missing: [2022, 2023]

  Philippines (PHL)
    electrification_rate              ✓ 2 years with data: [2022, 2023]
    clean_cooking_access              ✓ 2 years with data: [2022, 2023]
    safe_water_access                 ✗ no data returned from API  missing: [2022, 2023]
    urban_population_pct              ✓ 2 years with data: [2022, 2023]
    pm25_national_mean                ✗ no data returned from API  missing: [2022, 2023]

  Vietnam (VNM)
    electrification_rate              ✓ 2 years with data: [2022, 2023]
    clean_cooking_access              ✓ 2 years with data: [2022, 2023]
    safe_water_access                 ✗ no data returned from API  missing: [2022, 2023]
    urban_population_pct              ✓ 2 years with data: [2022, 2023]
    pm25_national_mean                ✗ no data returned from API  missing: [2022, 2023]

  Cambodia (KHM)
    electrification_rate              ✓ 2 years with data: [2022, 2023]
    clean_cooking_access              ✓ 2 years with data: [2022, 2023]
    safe_water_access                 ✗ no data returned from API  missing: [2022, 2023]
    urban_population_pct              ✓ 2 years with data: [2022, 2023]
    pm25_national_mean                ✗ no data returned from API  missing: [2022, 2023]

  Myanmar (MMR)
    electrification_rate              ✓ 2 years with data: [2022, 2023]
    clean_cooking_access              ✓ 2 years with data: [2022, 2023]
    safe_water_access                 ✗ no data returned from API  missing: [2022, 2023]
    urban_population_pct              ✓ 2 years with data: [2022, 2023]
    pm25_national_mean                ✗ no data returned from API  missing: [2022, 2023]

============================================================
  World Bank API Download Summary
============================================================
  Total API calls made : 40
  Total values fetched : 48
  Countries × years    : 8 × 2 = 16 expected rows

  Coverage per indicator (% of country-year cells with real data):
    electrification_rate              16/16 rows  (100%)
    clean_cooking_access              16/16 rows  (100%)
    urban_population_pct              16/16 rows  (100%)

  Saved → /home/mcyber/greentwin_sdg/data/raw/worldbank_wdi.csv  (16, 6)
  Report → /home/mcyber/greentwin_sdg/data/raw/worldbank_api_report.txt
  [OK] worldbank_wdi.csv written

======================================================
  STEP 02 - SDSN 2024 Goal Scores (user-entered, from real source)
======================================================
  Source : SDSN 2024 (Sachs et al., 2024) — user-entered goal scores
  URL    : https://dashboards.sdgindex.org/profiles/<country>
  Countries : ['Malaysia', 'Singapore', 'Thailand', 'Indonesia', 'Philippines', 'Vietnam', 'Cambodia', 'Myanmar']

  Malaysia
    Health_Environment            gap= 17.5  [SDG3=83(gap=17.0) + SDG11=82(gap=18.0)]
    Clean_Energy                  gap= 33.0  [SDG7=67(gap=33.0)]
    Climate_Action                gap= 22.0  [SDG13=78(gap=22.0)]
    Institutional_Capacity        gap= 32.0  [SDG16=65(gap=35.0) + SDG17=71(gap=29.0)]

  Singapore
    Health_Environment            gap=  5.5  [SDG3=94(gap=6.0) + SDG11=95(gap=5.0)]
    Clean_Energy                  gap= 29.0  [SDG7=71(gap=29.0)]
    Climate_Action                gap= 49.0  [SDG13=51(gap=49.0)]
    Institutional_Capacity        gap= 37.5  [SDG16=84(gap=16.0) + SDG17=41(gap=59.0)]

  Thailand
    Health_Environment            gap= 26.0  [SDG3=79(gap=21.0) + SDG11=69(gap=31.0)]
    Clean_Energy                  gap= 27.0  [SDG7=73(gap=27.0)]
    Climate_Action                gap= 11.0  [SDG13=89(gap=11.0)]
    Institutional_Capacity        gap= 31.0  [SDG16=65(gap=35.0) + SDG17=73(gap=27.0)]

  Indonesia
    Health_Environment            gap= 37.5  [SDG3=69(gap=31.0) + SDG11=56(gap=44.0)]
    Clean_Energy                  gap= 31.0  [SDG7=69(gap=31.0)]
    Climate_Action                gap=  9.0  [SDG13=91(gap=9.0)]
    Institutional_Capacity        gap= 36.0  [SDG16=65(gap=35.0) + SDG17=63(gap=37.0)]

  Philippines
    Health_Environment            gap= 31.0  [SDG3=62(gap=38.0) + SDG11=76(gap=24.0)]
    Clean_Energy                  gap= 38.0  [SDG7=62(gap=38.0)]
    Climate_Action                gap=  5.0  [SDG13=95(gap=5.0)]
    Institutional_Capacity        gap= 39.5  [SDG16=49(gap=51.0) + SDG17=72(gap=28.0)]

  Vietnam
    Health_Environment            gap= 25.5  [SDG3=76(gap=24.0) + SDG11=73(gap=27.0)]
    Clean_Energy                  gap= 21.0  [SDG7=79(gap=21.0)]
    Climate_Action                gap= 11.0  [SDG13=89(gap=11.0)]
    Institutional_Capacity        gap= 31.5  [SDG16=65(gap=35.0) + SDG17=72(gap=28.0)]

  Cambodia
    Health_Environment            gap= 38.0  [SDG3=64(gap=36.0) + SDG11=60(gap=40.0)]
    Clean_Energy                  gap= 30.0  [SDG7=70(gap=30.0)]
    Climate_Action                gap=  4.0  [SDG13=96(gap=4.0)]
    Institutional_Capacity        gap= 44.0  [SDG16=53(gap=47.0) + SDG17=59(gap=41.0)]

  Myanmar
    Health_Environment            gap= 48.5  [SDG3=47(gap=53.0) + SDG11=56(gap=44.0)]
    Clean_Energy                  gap= 48.0  [SDG7=52(gap=48.0)]
    Climate_Action                gap=  2.0  [SDG13=98(gap=2.0)]
    Institutional_Capacity        gap= 47.0  [SDG16=52(gap=48.0) + SDG17=54(gap=46.0)]

============================================================
  SDSN 2024 Cluster Gap Score Summary
============================================================
cluster      Clean_Energy  Climate_Action  Health_Environment  Institutional_Capacity
country                                                                              
Cambodia             30.0             4.0                38.0                    44.0
Indonesia            31.0             9.0                37.5                    36.0
Malaysia             33.0            22.0                17.5                    32.0
Myanmar              48.0             2.0                48.5                    47.0
Philippines          38.0             5.0                31.0                    39.5
Singapore            29.0            49.0                 5.5                    37.5
Thailand             27.0            11.0                26.0                    31.0
Vietnam              21.0            11.0                25.5                    31.5

  Records written  : 768 (8 countries × 2 years × 12 months × 4 clusters)
  Goal scores file → /home/mcyber/greentwin_sdg/data/raw/sdsn_2024_scores.csv
  Cluster targets  → /home/mcyber/greentwin_sdg/data/raw/sdsn_cluster_targets.csv
  [OK] sdsn_cluster_targets.csv written

======================================================
  STEP 03 - Real Air Quality (Open-Meteo CAMS, no API key)
======================================================
  Checking Open-Meteo CAMS API connectivity ...
  ✓ API reachable

  [Malaysia]  lat=3.139  lon=101.6869
    2022: 8,760 hours  |  PM2.5 valid=3,592  mean=36.9 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=40.4 µg/m³
    ✓  17,520 total hours  |  DCI=70.5%
       QC flagged 19 o3 outliers
  [Singapore]  lat=1.3521  lon=103.8198
    2022: 8,760 hours  |  PM2.5 valid=3,592  mean=21.0 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=18.2 µg/m³
    ✓  17,520 total hours  |  DCI=70.5%
  [Thailand]  lat=13.7563  lon=100.5018
    2022: 8,760 hours  |  PM2.5 valid=3,593  mean=53.0 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=38.2 µg/m³
    ✓  17,520 total hours  |  DCI=70.5%
       QC flagged 160 o3 outliers
  [Indonesia]  lat=-6.2088  lon=106.8456
    2022: 8,760 hours  |  PM2.5 valid=3,593  mean=57.8 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=63.9 µg/m³
    ✓  17,520 total hours  |  DCI=70.5%
       QC flagged 13 o3 outliers
  [Philippines]  lat=14.5995  lon=120.9842
    2022: 8,760 hours  |  PM2.5 valid=3,592  mean=15.1 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=15.8 µg/m³
    ✓  17,520 total hours  |  DCI=70.5%
       QC flagged 1 o3 outliers
  [Vietnam]  lat=10.8231  lon=106.6297
    2022: 8,760 hours  |  PM2.5 valid=3,593  mean=27.9 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=24.1 µg/m³
    ✓  17,520 total hours  |  DCI=70.5%
       QC flagged 13 o3 outliers
  [Cambodia]  lat=11.5564  lon=104.9282
    2022: 8,760 hours  |  PM2.5 valid=3,593  mean=18.4 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=18.2 µg/m³
    ✓  17,520 total hours  |  DCI=70.5%
       QC flagged 1 no2 outliers
  [Myanmar]  lat=16.8661  lon=96.1951
    2022: 8,760 hours  |  PM2.5 valid=3,594  mean=26.2 µg/m³
    2023: 8,760 hours  |  PM2.5 valid=8,760  mean=21.3 µg/m³
    ✓  17,520 total hours  |  DCI=70.5%

============================================================
  CAMS API Download Summary
============================================================
  Countries fetched     : 8 / 8
  Total hourly rows     : 140,160
  Years covered         : [2022, 2023]

  Per-pollutant valid readings (non-null):
    pm25    valid=98,822 (70.5%)  mean=30.61  std=28.15  [µg/m³]
    pm10    valid=98,822 (70.5%)  mean=44.86  std=40.24  [µg/m³]
    no2     valid=98,821 (70.5%)  mean=32.49  std=38.45  [µg/m³]
    o3      valid=98,616 (70.4%)  mean=66.71  std=63.94  [µg/m³]
    co      valid=98,822 (70.5%)  mean=912.48  std=1159.86  [µg/m³]

  Combined → /home/mcyber/greentwin_sdg/data/raw/cams_combined.parquet
  Report   → /home/mcyber/greentwin_sdg/data/raw/cams_api_report.txt
  [OK] cams_combined.parquet written

======================================================
  STEP 04 - Pre-processing (no fallback values)
======================================================
  Loading cams_combined.parquet ...
  Raw hourly rows : 140,160  |  countries : ['Cambodia', 'Indonesia', 'Malaysia', 'Myanmar', 'Philippines', 'Singapore', 'Thailand', 'Vietnam']

── Step 1: QC filtering

── Step 2: Data Completeness Index
  DCI range: 0.00 – 1.00  |  mean: 0.704

── Step 3: Monthly aggregation
  Monthly AQ rows (before empty-month removal): 192

  REMOVING 56 country-month rows with ZERO real CAMS hours (no synthetic substitution):
    Cambodia         7 months removed: 2022-01, 2022-02, 2022-03, 2022-04, 2022-05, 2022-06, 2022-07
    Indonesia        7 months removed: 2022-01, 2022-02, 2022-03, 2022-04, 2022-05, 2022-06, 2022-07
    Malaysia         7 months removed: 2022-01, 2022-02, 2022-03, 2022-04, 2022-05, 2022-06, 2022-07
    Myanmar          7 months removed: 2022-01, 2022-02, 2022-03, 2022-04, 2022-05, 2022-06, 2022-07
    Philippines      7 months removed: 2022-01, 2022-02, 2022-03, 2022-04, 2022-05, 2022-06, 2022-07
    Singapore        7 months removed: 2022-01, 2022-02, 2022-03, 2022-04, 2022-05, 2022-06, 2022-07
    Thailand         7 months removed: 2022-01, 2022-02, 2022-03, 2022-04, 2022-05, 2022-06, 2022-07
    Vietnam          7 months removed: 2022-01, 2022-02, 2022-03, 2022-04, 2022-05, 2022-06, 2022-07

  Monthly AQ rows (after empty-month removal): 136

── Step 4: Log-transformation

── Step 5: WB annual → monthly interpolation (16 annual rows)

  World Bank feature coverage after interpolation (real data only):
    clean_cooking_access              100% non-null
    electrification_rate              100% non-null
    urban_population_pct              100% non-null

=======================================================
  monthly_aq.csv  (136 rows)
  monthly_wb.csv  (192 rows)
  Report → /home/mcyber/greentwin_sdg/data/processed/preprocessing_report.txt
  [OK] monthly_aq.csv + monthly_wb.csv written

======================================================
  STEP 05 - Feature Engineering
======================================================
  AQ rows  : 136
  WB rows  : 192
  SDG rows : 768

── Building composite features
  HEI, OBI, COP, SAS, rolling/lag features  ✓

  Feature matrix after WB merge: (136, 30)

-- Checking remaining missing values (real API gaps, no fallback)

  Rows after target merge: 136 (dropped 0 with no labels)

=======================================================
  feature_matrix.csv  →  136 rows × 34 cols
  Feature columns used in model: 27

  Target cluster statistics:
    Health_Environment              mean=28.7  std=12.5  min=5.5  max=48.5
    Clean_Energy                    mean=32.1  std=7.6  min=21.0  max=48.0
    Climate_Action                  mean=14.1  std=14.4  min=2.0  max=49.0
    Institutional_Capacity          mean=37.3  std=5.6  min=31.0  max=47.0

  Feature summary → /home/mcyber/greentwin_sdg/data/processed/feature_summary.txt
  [OK] feature_matrix.csv written

======================================================
  STEP 06 - XGBoost Model Training
======================================================
  Feature matrix : 136 rows × 27 features
  Countries      : ['Cambodia', 'Indonesia', 'Malaysia', 'Myanmar', 'Philippines', 'Singapore', 'Thailand', 'Vietnam']
  Years          : [2022, 2023]

────────────────────────────────────────────────────────────
  Cluster : Health_Environment
    Train:   85  (['Malaysia', 'Myanmar', 'Philippines', 'Thailand', 'Vietnam'])
    Val  :   17  (['Indonesia'])
    Test :   34  (['Cambodia', 'Singapore'])
    Best val MAE = 7.863  |  lr=0.017  depth=3
    Test-set performance:
    XGBoost     MAE=11.828  RMSE=12.929  R²=0.367
    Ridge       MAE=7.095  RMSE=7.571  R²=0.783
    MAE < 6 threshold : FAIL
    MAE Δ vs Ridge    : -66.7%

────────────────────────────────────────────────────────────
  Cluster : Clean_Energy
    Train:   85  (['Indonesia', 'Malaysia', 'Singapore', 'Thailand', 'Vietnam'])
    Val  :   17  (['Philippines'])
    Test :   34  (['Cambodia', 'Myanmar'])
    Best val MAE = 9.892  |  lr=0.014  depth=4
    Test-set performance:
    XGBoost     MAE=9.371  RMSE=11.252  R²=-0.563
    Ridge       MAE=6.169  RMSE=7.191  R²=0.362
    MAE < 6 threshold : FAIL
    MAE Δ vs Ridge    : -51.9%

────────────────────────────────────────────────────────────
  Cluster : Climate_Action
    Train:   85  (['Cambodia', 'Malaysia', 'Myanmar', 'Philippines', 'Singapore'])
    Val  :   17  (['Indonesia'])
    Test :   34  (['Thailand', 'Vietnam'])
    Best val MAE = 7.177  |  lr=0.090  depth=3
    Test-set performance:
    XGBoost     MAE=3.197  RMSE=3.845  R²=0.000
    Ridge       MAE=3.162  RMSE=4.387  R²=0.000
    MAE < 6 threshold : PASS
    MAE Δ vs Ridge    : -1.1%

────────────────────────────────────────────────────────────
  Cluster : Institutional_Capacity
    Train:   85  (['Cambodia', 'Malaysia', 'Singapore', 'Thailand', 'Vietnam'])
    Val  :   17  (['Indonesia'])
    Test :   34  (['Myanmar', 'Philippines'])
    Best val MAE = 0.948  |  lr=0.041  depth=4
    Test-set performance:
    XGBoost     MAE=4.179  RMSE=4.846  R²=-0.670
    Ridge       MAE=17.001  RMSE=21.731  R²=-32.581
    MAE < 6 threshold : PASS
    MAE Δ vs Ridge    : +75.4%

============================================================
  FINAL PERFORMANCE (XGBoost, test set)
============================================================
               cluster    mae   rmse     r2  delta_pct  threshold_pass
    Health_Environment 11.828 12.929  0.367      -66.7           False
          Clean_Energy  9.371 11.252 -0.563      -51.9           False
        Climate_Action  3.197  3.845  0.000       -1.1            True
Institutional_Capacity  4.179  4.846 -0.670       75.4            True

  Models  → /home/mcyber/greentwin_sdg/outputs/models/
  Metrics → /home/mcyber/greentwin_sdg/outputs/results/performance_metrics.csv
  [OK] Models + performance_metrics.csv written

======================================================
  STEP 07 - SHAP Explainability
======================================================

───────────────────────────────────────────────────────
  Cluster : Health_Environment
    Test records : 34
    SHAP baseline : 30.985
    Local accuracy residual : 0.000011  PASS
    Top-3 features:
      electrification_rate              |SHAP|=4.4235  (43.1%)
      clean_cooking_access              |SHAP|=2.5993  (25.3%)
      urban_population_pct              |SHAP|=1.9010  (18.5%)
    Cumulative variance (top-3, over ALL features): 86.9%

───────────────────────────────────────────────────────
  Cluster : Clean_Energy
    Test records : 34
    SHAP baseline : 29.859
    Local accuracy residual : 0.000007  PASS
    Top-3 features:
      clean_cooking_access              |SHAP|=5.4403  (51.7%)
      urban_population_pct              |SHAP|=3.2911  (31.3%)
      pm25                              |SHAP|=0.9143  (8.7%)
    Cumulative variance (top-3, over ALL features): 91.7%

───────────────────────────────────────────────────────
  Cluster : Climate_Action
    Test records : 34
    SHAP baseline : 15.088
    Local accuracy residual : 0.000003  PASS
    Top-3 features:
      urban_population_pct              |SHAP|=4.0238  (31.6%)
      clean_cooking_access              |SHAP|=3.1004  (24.3%)
      electrification_rate              |SHAP|=2.7001  (21.2%)
    Cumulative variance (top-3, over ALL features): 77.1%

───────────────────────────────────────────────────────
  Cluster : Institutional_Capacity
    Test records : 34
    SHAP baseline : 35.352
    Local accuracy residual : 0.000005  PASS
    Top-3 features:
      log_no2_roll3                     |SHAP|=4.0773  (52.0%)
      log_no2_roll6                     |SHAP|=1.3631  (17.4%)
      hei_roll6                         |SHAP|=0.9311  (11.9%)
    Cumulative variance (top-3, over ALL features): 81.3%

=======================================================
  SHAP SUMMARY (Table III)
=======================================================
           SDG Cluster        Top Feature 1        Top Feature 2        Top Feature 3  Cumulative Variance (%)
    Health_Environment electrification_rate clean_cooking_access urban_population_pct                     86.9
          Clean_Energy clean_cooking_access urban_population_pct                 pm25                     91.7
        Climate_Action urban_population_pct clean_cooking_access electrification_rate                     77.1
Institutional_Capacity        log_no2_roll3        log_no2_roll6            hei_roll6                     81.3
  [OK] shap_summary_table.csv written

======================================================
  STEP 08 - Figures (Fig 2 + Fig 3)
======================================================
-- Step A: Generating full-dataset predictions (all countries)
  Feature matrix: 136 rows  countries=['Cambodia', 'Indonesia', 'Malaysia', 'Myanmar', 'Philippines', 'Singapore', 'Thailand', 'Vietnam']
  Health_Environment            136 rows  countries=['Cambodia', 'Indonesia', 'Malaysia', 'Myanmar', 'Philippines', 'Singapore', 'Thailand', 'Vietnam']
  Clean_Energy                  136 rows  countries=['Cambodia', 'Indonesia', 'Malaysia', 'Myanmar', 'Philippines', 'Singapore', 'Thailand', 'Vietnam']
  Climate_Action                136 rows  countries=['Cambodia', 'Indonesia', 'Malaysia', 'Myanmar', 'Philippines', 'Singapore', 'Thailand', 'Vietnam']
  Institutional_Capacity        136 rows  countries=['Cambodia', 'Indonesia', 'Malaysia', 'Myanmar', 'Philippines', 'Singapore', 'Thailand', 'Vietnam']

  Best-performing cluster: Climate_Action

-- Figure 2: SHAP Beeswarm
  Fig 2 saved -> /home/mcyber/greentwin_sdg/outputs/figures/Fig2_SHAP_Beeswarm.png

-- Figure 3: SDG Gap Heatmap (all countries)
  Fig 3 saved -> /home/mcyber/greentwin_sdg/outputs/figures/Fig3_SDG_Heatmap.png

  Done. Figures -> /home/mcyber/greentwin_sdg/outputs/figures/
  [OK] Fig2_SHAP_Beeswarm.png + Fig3_SDG_Heatmap.png written

======================================================
  Pipeline complete in 69s
======================================================

  Data sources used (ALL REAL, NO SYNTHETIC/FALLBACK):
    Air quality : Open-Meteo CAMS API (live fetch)
    World Bank  : api.worldbank.org (live fetch, no fallback)
    SDG targets : SDSN 2024 user-entered from sdgindex.org

  Key outputs:
    data/raw/worldbank_api_report.txt   <- WB data volume report
    data/raw/cams_api_report.txt        <- CAMS data volume report
    outputs/results/performance_metrics.csv
    outputs/results/shap_summary_table.csv
    outputs/figures/Fig2_SHAP_Beeswarm.png
    outputs/figures/Fig3_SDG_Heatmap.png
(venv) mcyber@mcyber-Apple-Virtualization-Generic-Platform:~/greentwin_sdg$ 

