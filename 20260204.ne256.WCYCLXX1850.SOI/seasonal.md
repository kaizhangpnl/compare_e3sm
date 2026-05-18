## Seasonal Analysis (lat-lon maps)

- [Seasonal Analysis (lat-lon maps)](#seasonal-analysis-lat-lon-maps)
  - [TGCLDLWP_OCN — Seasonal Progression](#tgcldlwp_ocn--seasonal-progression)
  - [SHFLX — Seasonal Progression](#shflx--seasonal-progression)
  - [OMEGA-850mb — Seasonal Progression](#omega-850mb--seasonal-progression)
  - [T-200mb — Seasonal Progression](#t-200mb--seasonal-progression)
  - [FLNS — Seasonal Progression](#flns--seasonal-progression)
  - [OMEGA-200mb — Seasonal Progression](#omega-200mb--seasonal-progression)
  - [NETCF — Seasonal Progression](#netcf--seasonal-progression)
  - [OMEGA-500mb — Seasonal Progression](#omega-500mb--seasonal-progression)
  - [PRECT — Seasonal Progression](#prect--seasonal-progression)
  - [LWCFSRF — Seasonal Progression](#lwcfsrf--seasonal-progression)
  - [TMQ — Seasonal Progression](#tmq--seasonal-progression)
  - [PSL — Seasonal Progression](#psl--seasonal-progression)
  - [SWCF — Seasonal Progression](#swcf--seasonal-progression)
  - [FLNSC — Seasonal Progression](#flnsc--seasonal-progression)
  - [FLUTC — Seasonal Progression](#flutc--seasonal-progression)
  - [TREFHT — Seasonal Progression](#trefht--seasonal-progression)
  - [SST — Seasonal Progression](#sst--seasonal-progression)
  - [RESTOM — Seasonal Progression](#restom--seasonal-progression)
  - [U-850mb — Seasonal Progression](#u-850mb--seasonal-progression)
  - [FSNTOA — Seasonal Progression](#fsntoa--seasonal-progression)
  - [FLUT — Seasonal Progression](#flut--seasonal-progression)
  - [FSNS — Seasonal Progression](#fsns--seasonal-progression)

---

### `TGCLDLWP_OCN` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/Cloud%20SSM/I/SSMI-TGCLDLWP_OCN-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/Cloud%20SSM/I/SSMI-TGCLDLWP_OCN-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/Cloud%20SSM/I/SSMI-TGCLDLWP_OCN-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/Cloud%20SSM/I/SSMI-TGCLDLWP_OCN-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/Cloud%20SSM/I/SSMI-TGCLDLWP_OCN-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/Cloud%20SSM/I/SSMI-TGCLDLWP_OCN-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/Cloud%20SSM/I/SSMI-TGCLDLWP_OCN-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/Cloud%20SSM/I/SSMI-TGCLDLWP_OCN-SON-global.png" width="250"> |

**Seasonal pattern:** The underestimate is year-round and global, without seasonal reversal. The Southern Ocean deficit peaks in DJF (austral summer), when observed LWP is highest and mixed-phase conditions are most extensive; the model fails to generate the observed summertime LWP peak, suggesting the microphysics transition from liquid to ice occurs too readily even in relatively warm conditions (T > −20 °C). Note that SSM/I only observes DJF and JJA (MAM/SON are absent from the e3sm-diags output), so the year-round character is inferred from the two available seasons plus the ANN climatology.

---

### `SHFLX` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-SHFLX-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-SHFLX-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-SHFLX-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-SHFLX-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-SHFLX-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-SHFLX-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-SHFLX-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-SHFLX-SON-global.png" width="250"> |

**Seasonal pattern:** The positive sensible heat flux bias is present year-round but strongest in JJA (JJA−DJF Δ nRMSE = +0.35, confirming boreal summer as the dominant bias season), particularly over the western tropical Pacific and the Arabian Sea. In DJF, the warm pool excess is strongest; in JJA, the bias shifts toward the South Asian and West African monsoon domain (Bay of Bengal, Gulf of Guinea), where surface energy partitioning during active monsoon conditions overestimates the sensible-to-latent heat ratio. The bias moderates slightly in MAM and SON transition seasons but never reverses sign.

---

### `OMEGA-850mb` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-OMEGA-850-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-OMEGA-850-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-OMEGA-850-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-OMEGA-850-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-OMEGA-850-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-OMEGA-850-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-OMEGA-850-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-OMEGA-850-SON-global.png" width="250"> |

**Seasonal pattern:** The ascent bias over the ITCZ is year-round. The South Asian monsoon bias (too strong ascent) appears exclusively in JJA. In DJF, the bias shifts to the Southern tropical Pacific as the ITCZ migrates southward and the double-ITCZ precipitation anomaly reinforces anomalous low-level convergence.

---

### `T-200mb` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-T-200-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-T-200-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-T-200-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-T-200-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-T-200-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-T-200-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-T-200-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-T-200-SON-global.png" width="250"> |

**Seasonal pattern:** The cold bias at 200 hPa is present year-round across all latitudes except the SH polar cap. It is strongest in DJF over the NH polar region (where stratospheric cold anomaly descends into the upper troposphere) and in JJA over the tropical warm pool (where active convection overshoots the cold-point tropopause but fails to adequately warm the 200 hPa level). The bias shows no sign reversal in any season, consistent with a systematic structural cold bias rather than a tuning-related issue.

---

### `FLNS` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNS-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNS-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNS-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNS-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNS-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNS-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNS-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNS-SON-global.png" width="250"> |

**Seasonal pattern:** The JJA FLNS map (rendered above) shows the most striking biases: a large negative anomaly (−20 to −49 W/m²) over the Southern Ocean and SH midlatitudes in the austral winter, and a widespread positive anomaly (+10 to +30 W/m²) over NH continents in boreal summer. This seasonal asymmetry suggests the Southern Ocean cloud deficit reduces LW trapping most severely when the sun is low and LW is the dominant term, while in NH summer the hot land surfaces emit more LW than in the observational climatology. The DJF bias is more symmetric globally, with the Southern Ocean deficit shifting to austral summer geography.

---

### `OMEGA-200mb` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-OMEGA-200-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-OMEGA-200-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-OMEGA-200-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-OMEGA-200-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-OMEGA-200-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-OMEGA-200-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-OMEGA-200-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-OMEGA-200-SON-global.png" width="250"> |

**Seasonal pattern:** The 200 hPa level shows more complexity than 850/500 hPa because of the competing effects of convective outflow and radiatively driven subsidence. The tropical warm pool bias (too weak upward motion at 200 hPa) is persistent but weaker in JJA; in DJF the double-ITCZ signature appears again as anomalous upward motion in the Southern tropical Pacific.

---

### `NETCF` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-NETCF-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-NETCF-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-NETCF-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-NETCF-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-NETCF-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-NETCF-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-NETCF-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-NETCF-SON-global.png" width="250"> |

**Seasonal pattern:** The tropical NETCF deficit (model too negative = too much cloud cooling) is year-round but peaks in JJA when deep convection over South Asia and the Indian Ocean intensifies. The Southern Ocean NETCF positive anomaly (over-cooling) is largest in DJF (austral summer) when solar insolation over the storm track is highest, making the reflective cloud errors most consequential. There is no sign reversal between seasons.

---

### `OMEGA-500mb` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-OMEGA-500-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-OMEGA-500-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-OMEGA-500-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-OMEGA-500-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-OMEGA-500-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-OMEGA-500-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-OMEGA-500-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-OMEGA-500-SON-global.png" width="250"> |

**Seasonal pattern:** Closely mirrors the 850 hPa picture. The tropical ITCZ ascent bias is year-round; the South Asian monsoon bias dominates in JJA. The Southern tropical Pacific ascent bias (double-ITCZ) is largest in DJF and SON.

---

### `PRECT` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/GPCP_v3.2/GPCP_v3.2-PRECT-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/GPCP_v3.2/GPCP_v3.2-PRECT-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/GPCP_v3.2/GPCP_v3.2-PRECT-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/GPCP_v3.2/GPCP_v3.2-PRECT-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/GPCP_v3.2/GPCP_v3.2-PRECT-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/GPCP_v3.2/GPCP_v3.2-PRECT-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/GPCP_v3.2/GPCP_v3.2-PRECT-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/GPCP_v3.2/GPCP_v3.2-PRECT-SON-global.png" width="250"> |

**Seasonal pattern:** The DJF plot (rendered above) shows the double-ITCZ most clearly: a dark green (positive, +3 to +5 mm/day) band in the Southern tropical Pacific and a brown (negative, −3 to −5 mm/day) dry band in the Maritime Continent/warm pool — this pattern intensifies when the ITCZ migrates to its southernmost position in DJF. The JJA plot (also rendered) shows the monsoon precipitation deficit is most severe over South Asia and the West African Sahel in boreal summer, while the equatorial Pacific bias becomes more symmetric. The double-ITCZ artifact persists in all seasons but is largest in DJF and SON.

---

### `LWCFSRF` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-LWCFSRF-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-LWCFSRF-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-LWCFSRF-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-LWCFSRF-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-LWCFSRF-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-LWCFSRF-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-LWCFSRF-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-LWCFSRF-SON-global.png" width="250"> |

**Seasonal pattern:** The Southern Ocean LW surface cloud forcing deficit persists all year, reaching its maximum in austral summer (DJF) when the sun is present and cloud LW trapping is reduced. The tropical positive bias (excess LW cloud trapping) is strongest in boreal summer (JJA) when deep convective anvils are most extensive over the warm pool. There is a slight sign reversal at NH midlatitudes between DJF (positive) and JJA (negative), possibly because summer continental cloud cover exceeds CERES while winter stratus coverage is underestimated.

---

### `TMQ` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-TMQ-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-TMQ-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-TMQ-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-TMQ-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-TMQ-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-TMQ-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-TMQ-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-TMQ-SON-global.png" width="250"> |

**Seasonal pattern:** The tropical dry bias is year-round but strongest in boreal summer (JJA), when the active monsoon systems over South Asia and West Africa are peak moisture sources that the model underestimates. The mid-latitude drying shows mild seasonal modulation with a slight winter reduction. No sign reversal is found at any latitude.

---

### `PSL` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-PSL-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-PSL-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-PSL-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-PSL-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-PSL-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-PSL-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-PSL-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-PSL-SON-global.png" width="250"> |

**Seasonal pattern:** The Arctic low-pressure bias is strongest in DJF (NH winter), when the polar vortex is well-established and any systematic displacement or deepening of the vortex is most apparent at the surface. The Southern Ocean low-pressure bias is most intense in JJA (austral winter). The subtropical ridge positive bias is a summer feature in both hemispheres, intensifying when Hadley circulation is at its strongest.

---

### `SWCF` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-SWCF-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-SWCF-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-SWCF-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-SWCF-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-SWCF-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-SWCF-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-SWCF-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-SWCF-SON-global.png" width="250"> |

**Seasonal pattern:** The Southern Ocean positive SWCF bias (insufficient SW cloud cooling) peaks in DJF (austral summer) when SW radiation is maximal — this is when the liquid water path deficit has the largest energetic consequence. The tropical SWCF bias (insufficient SW cloud cooling, model less negative than CERES) is year-round but peaks in JJA in the Bay of Bengal and North Indian Ocean.

---

### `FLNSC` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNSC-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNSC-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNSC-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNSC-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNSC-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNSC-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNSC-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNSC-SON-global.png" width="250"> |

**Seasonal pattern:** The Southern Ocean positive clear-sky LW bias is most pronounced in DJF and MAM (austral summer/autumn), consistent with a warm SST surface bias that intensifies during the period of maximum solar heating. The subtropical/desert positive bias peaks in JJA when surface temperatures are highest. Year-round character with seasonal amplitude modulation; no sign reversals.

---

### `FLUTC` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUTC-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUTC-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUTC-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUTC-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUTC-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUTC-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUTC-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUTC-SON-global.png" width="250"> |

**Seasonal pattern:** The tropical clear-sky OLR deficit (model too cold aloft) is year-round. In DJF the SH polar positive anomaly is most apparent (warm Antarctic surface in austral summer driving excess LW emission). The NH polar negative anomaly is strongest in NH winter (DJF), when stratospheric influence on the upper troposphere is greatest.

---

### `TREFHT` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-TREFHT-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-TREFHT-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-TREFHT-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-TREFHT-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-TREFHT-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-TREFHT-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-TREFHT-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-TREFHT-SON-global.png" width="250"> |

**Seasonal pattern:** The global TREFHT bias is small year-round (|bias| < 0.4 K in every season vs ERA5), but the land warm bias shows striking seasonality: JJA land bias = +2.10 K (ERA5) is 6× the ANN mean, concentrated over NH continental interiors. CONUS JJA nRMSE (0.446 vs CRU) is 3× the ANN value (0.177), indicating a severe boreal summer warm bias that may reflect insufficient evapotranspiration, soil moisture depletion, or boundary-layer mixing. DJF is comparatively well-controlled globally.

---

### `SST` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/SST_PI_HadISST/HadISST_PI-SST-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/SST_PI_HadISST/HadISST_PI-SST-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/SST_PI_HadISST/HadISST_PI-SST-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/SST_PI_HadISST/HadISST_PI-SST-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/SST_PI_HadISST/HadISST_PI-SST-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/SST_PI_HadISST/HadISST_PI-SST-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/SST_PI_HadISST/HadISST_PI-SST-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/SST_PI_HadISST/HadISST_PI-SST-SON-global.png" width="250"> |

**Seasonal pattern:** SST biases reverse seasonally: DJF shows net warm bias (nbias=+0.034), while JJA shifts to cold (nbias=−0.052). The cold tongue cold bias intensifies in JJA–SON as seasonal upwelling strengthens. The Southern Ocean warm bias is largest in DJF (austral summer) when insolation is maximum.

---

### `RESTOM` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-RESTOM-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-RESTOM-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-RESTOM-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-RESTOM-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-RESTOM-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-RESTOM-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-RESTOM-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-RESTOM-SON-global.png" width="250"> |

**Seasonal pattern:** RESTOM bias has a strong seasonal cycle: MAM shows the largest deficit (nbias = −0.071, bias = −5.1 W/m²), while JJA and SON show slight positive bias (nbias ≈ +0.02–0.03). NH spring sees excess OLR or reduced SW absorption.

---

### `U-850mb` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-U-850-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-U-850-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-U-850-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-U-850-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-U-850-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-U-850-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-U-850-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-U-850-SON-global.png" width="250"> |

**Seasonal pattern:** JJA shows the largest nRMSE (0.258) as SH winter jet strengthens and monsoon circulation activates. MAM trade wind bias is most prominent (nbias = +0.064). DJF shows weakest bias (nbias = +0.007).

---

### `FSNTOA` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FSNTOA-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FSNTOA-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FSNTOA-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FSNTOA-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FSNTOA-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FSNTOA-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FSNTOA-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FSNTOA-SON-global.png" width="250"> |

**Seasonal pattern:** The bias has a clear seasonal modulation driven by the sunlit hemisphere. In DJF (RMSE = 13.9, mean DIFF = −4.36 W/m²), the Southern Ocean excess is at its peak because austral summer maximizes insolation over the SO cloud-deficit region, while the SH subtropical deficit deepens. In JJA (RMSE = 16.3, mean DIFF = −0.44 W/m²), the global mean bias nearly vanishes but the spatial error is larger: NH continents and the Arctic show a pronounced positive bias (+20 to +40 W/m² locally) while the tropical ITCZ deficit persists — the near-zero global mean masks a strong NH–SH compensation. MAM shows the worst nRMSE (0.159) and largest negative nbias (−0.089), driven by the spring transition when both hemispheres contribute cloud errors simultaneously.

---

### `FLUT` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUT-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUT-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUT-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUT-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUT-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUT-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUT-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUT-SON-global.png" width="250"> |

**Seasonal pattern:** The OLR deficit is persistent year-round but shows significant amplitude modulation. MAM has the worst nRMSE (0.308) and strongest negative global bias (nbias ≈ −0.108), when the deep convective systems over the tropical warm pool are most active and the model produces too much high-cloud shielding. DJF nRMSE = 0.275 with nbias = −0.087. JJA sees a reduction in the deficit (nRMSE = 0.254, nbias = −0.065) as the monsoon season shifts the dominant convective region from the warm pool toward South Asia — a region where the model's OLR bias is somewhat smaller. SON nRMSE = 0.279, intermediate. The Sahara positive bias is year-round but peaks in JJA when surface temperatures are highest.

---

### `FSNS` — Seasonal Progression

| Season | TEST | CTRL |
|---|---|---|
| DJF | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FSNS-DJF-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FSNS-DJF-global.png" width="250"> |
| MAM | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FSNS-MAM-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FSNS-MAM-global.png" width="250"> |
| JJA | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FSNS-JJA-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FSNS-JJA-global.png" width="250"> |
| SON | <img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FSNS-SON-global.png" width="250"> | <img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FSNS-SON-global.png" width="250"> |

**Seasonal pattern:** JJA is clearly the worst season (nRMSE = 0.237, RMSE = 18.2 W/m², mean DIFF = +2.30 W/m²), driven by the NH summer when large positive biases appear over NH continents, the Arctic, and the Southern Ocean. The NH excess in JJA is particularly notable: surface SW absorption is too high over North America, Europe, and Central Asia, consistent with the FSNTOA JJA pattern and suggesting insufficient summer cloud cover. DJF is the best season (nRMSE = 0.165), when the NH is in darkness and the main error is the Southern Ocean austral-summer excess. MAM (0.194) and SON (0.197) are intermediate. The sign_reversal flag is set because regional biases reverse between DJF (SH-dominated excess) and JJA (NH-dominated excess), though the global mean stays slightly positive in both seasons.

---
