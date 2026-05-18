
## Zonal Mean Analysis (ANN)

> ne256_SOI vs. E3SMv3_LR, both vs. the same reference dataset. Bottom panel = Model − Observation difference.

---

### `TGCLDLWP_OCN` — Zonal Mean (ANN, vs. SSMI)

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/zonal_mean_xy/Cloud%20SSM/I/SSMI-TGCLDLWP_OCN-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/zonal_mean_xy/Cloud%20SSM/I/SSMI-TGCLDLWP_OCN-ANN-global.png" width="420"></td>
</tr></table>



The model (black) lies approximately 50–60 g/m² below the SSM/I reference (red) at every latitude from 70°S to 70°N, demonstrating a near-uniform global liquid water path deficit. The difference panel shows a sharp minimum of −85 g/m² near 5°N, probably a combined effect of the ITCZ precipitation depletion of liquid water and a possible mixed SST/sea-ice artifact near the equatorial dateline.

| Latitude Band | Bias Sign | Magnitude |
|---|---|---|
| SH polar (60°S–90°S) | − | Large (−50 g/m²) |
| SH extratropics (30°S–60°S) | − | Large (−50 g/m²) |
| SH tropics (0°–30°S) | − | Large (−45 to −50 g/m²) |
| NH tropics (0°–30°N) | − | Very large (−40 to −85 g/m²) |
| NH extratropics (30°N–60°N) | − | Large (−55 g/m²) |
| NH polar (60°N–90°N) | − | Large (−55 g/m²) |

---

### `T-200mb` — Zonal Mean (ANN, vs. ERA5)

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/zonal_mean_xy/ERA5/ERA5-T-200-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/zonal_mean_xy/ERA5/ERA5-T-200-ANN-global.png" width="420"></td>
</tr></table>



The model upper-troposphere (black) is uniformly below ERA5 (red) everywhere except the SH polar cap. The cold bias begins at ≈ −60°S, strengthens through the tropics to −1.5 K, and reaches its maximum of −2 K at the NH pole. The SH polar region (80°S–90°S) shows a small positive offset of +0.5 K.

| Latitude Band | Bias Sign | Magnitude |
|---|---|---|
| SH polar (60°S–90°S) | + | Small (+0.5 K) |
| SH extratropics (30°S–60°S) | − | Moderate (−1.0 to −1.5 K) |
| SH tropics (0°–30°S) | − | Moderate (−1.5 K) |
| NH tropics (0°–30°N) | − | Moderate–Large (−1.5 K) |
| NH extratropics (30°N–60°N) | − | Moderate (−0.5 to −1.0 K) |
| NH polar (60°N–90°N) | − | Large (−2.0 K) |

---

### `FLNS` — Zonal Mean (ANN, vs. ceres_ebaf_surface_v4.1)

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/zonal_mean_xy/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNS-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/zonal_mean_xy/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNS-ANN-global.png" width="420"></td>
</tr></table>



The model surface LW flux (black) tracks the reference (red) reasonably well in pattern, but lies systematically below observed at 30°S–70°S (Southern Ocean; difference ≈ −10 W/m²) and above observed at 0°–60°N (NH tropics to midlatitudes; difference ≈ +3 to +8 W/m²). The polar extremes show positive model bias (excess LW surface flux at both poles), consistent with warm surface biases.

| Latitude Band | Bias Sign | Magnitude |
|---|---|---|
| SH polar (60°S–90°S) | + | Small (+4 W/m²) |
| SH extratropics (30°S–60°S) | − | Large (−8 to −10 W/m²) |
| SH tropics (0°–30°S) | −/0 | Small |
| NH tropics (0°–30°N) | + | Moderate (+5 W/m²) |
| NH extratropics (30°N–60°N) | + | Moderate (+3 to +5 W/m²) |
| NH polar (60°N–90°N) | + | Moderate (+5 to +7 W/m²) |

---

### `NETCF` — Zonal Mean (ANN, vs. ceres_ebaf_toa_v4.1)

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/zonal_mean_xy/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-NETCF-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/zonal_mean_xy/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-NETCF-ANN-global.png" width="420"></td>
</tr></table>



The model shows a pronounced positive spike at 60°S (+10 W/m²) — the SH storm-track clouds produce insufficient SW cooling relative to CERES (consistent with the TGCLDLWP_OCN liquid water deficit making clouds less reflective), so NETCF is less negative than observed. In contrast, the tropical band (30°S–30°N) shows a deep negative trough of −5 to −12 W/m² — cloud cooling in the tropics is stronger than observed, driven by optically thick deep-convective anvils. NH extratropics show a positive bias (+3 to +6 W/m²) indicating insufficient NH midlatitude cloud cooling.

---

### `PRECT` — Zonal Mean (ANN, vs. ERA5)

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/zonal_mean_xy/ERA5/ERA5-PRECT-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/zonal_mean_xy/ERA5/ERA5-PRECT-ANN-global.png" width="420"></td>
</tr></table>



The model ITCZ peak (≈ 7 mm/day at 5°N) exceeds the GPCP reference (≈ 6.5 mm/day) and is slightly sharper; the double-ITCZ appears as a secondary positive difference at ≈ 5°S. The SH midlatitude band (40°S–60°S) is slightly overestimated (+0.2–0.4 mm/day from Southern Ocean frontal precipitation). NH midlatitudes show a slight positive bias as well. The largest negative biases are near 5°N (just north of the ITCZ peak) and near 15°N–25°N (monsoon deficit), reflected in the difference panel as multiple sharp negative spikes.

| Latitude Band | Bias Sign | Magnitude |
|---|---|---|
| SH extratropics (30°S–60°S) | + | Small (+0.2–0.4 mm/day) |
| SH tropics (5°S–20°S) | + | Moderate (double-ITCZ, +0.4–0.6 mm/day) |
| Equatorial / ITCZ (5°S–10°N) | mixed | Large (sharp positive near equator, negative flanks) |
| NH tropics / monsoon (10°N–25°N) | − | Moderate (−0.2–0.3 mm/day) |
| NH extratropics (30°N–60°N) | + | Small (+0.1 mm/day) |

---

### `LWCFSRF` — Zonal Mean (ANN, vs. ceres_ebaf_surface_v4.1)

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/zonal_mean_xy/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-LWCFSRF-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/zonal_mean_xy/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-LWCFSRF-ANN-global.png" width="420"></td>
</tr></table>



The zonal mean shows a deficit (negative bias) at 55°S–65°S, where the model has insufficient surface LW cloud forcing — clouds trap too little LW at the surface, consistent with the TGCLDLWP_OCN liquid water deficit, followed by a sudden transition to too little cloud LW forcing equatorward of 60°S (−5 to −15 W/m² in the SH polar/sub-Antarctic zone). In the NH extratropics and polar regions the model under-traps LW (−3 to −15 W/m²). The tropical region is near-zero.

| Latitude Band | Bias Sign | Magnitude |
|---|---|---|
| SH polar (70°S–90°S) | − | Large (−15 W/m²) |
| SH extratropics / storm track (55°S–65°S) | + | Large (+10 W/m²) |
| SH subtropics–tropics (0°–30°S) | + | Small (+2 to +3 W/m²) |
| NH tropics (0°–30°N) | 0/slight − | Negligible |
| NH extratropics (30°N–60°N) | − | Moderate (−3 to −5 W/m²) |
| NH polar (60°N–90°N) | − | Large (−15 W/m²) |

---

### `TMQ` — Zonal Mean (ANN, vs. ERA5)

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/zonal_mean_xy/ERA5/ERA5-TMQ-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/zonal_mean_xy/ERA5/ERA5-TMQ-ANN-global.png" width="420"></td>
</tr></table>



The model is systematically dry relative to ERA5 from 30°S to 30°N, with the largest deficit of −7 kg/m² centered on the equator. Poleward of ±30°, the bias approaches zero and slightly reverses to near-zero positive at the midlatitudes. The deficit is most severe in the tropical warm pool–ITCZ zone, consistent with convective over-precipitation removing moisture from the column before it can persist as water vapor.

| Latitude Band | Bias Sign | Magnitude |
|---|---|---|
| SH extratropics (30°S–60°S) | 0/slight − | Negligible |
| SH tropics (0°–30°S) | − | Large (−3 to −6 kg/m²) |
| NH tropics (0°–30°N) | − | Very Large (−4 to −7 kg/m²) |
| NH extratropics (30°N–60°N) | 0/slight − | Small |
| NH polar (60°N–90°N) | 0 | Negligible |

---

### `SWCF` — Zonal Mean (ANN, vs. ceres_ebaf_toa_v4.1)

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/zonal_mean_xy/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-SWCF-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/zonal_mean_xy/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-SWCF-ANN-global.png" width="420"></td>
</tr></table>



The model SWCF is insufficient (less negative than CERES) at 50°S–65°S, consistent with the liquid water path deficit reducing cloud reflectivity and is insufficient throughout the tropics (positive difference of +5 to +12 W/m²), mirroring the `NETCF` zonal structure. The NH extratropics also show insufficient SW cloud cooling (+5 to +8 W/m²).

| Latitude Band | Bias Sign | Magnitude |
|---|---|---|
| SH storm track (50°S–65°S) | model less negative than obs | Moderate–Large (+5 to +10 W/m²) |
| SH subtropics–tropics (30°S–5°S) | model less negative than obs (+) | Large (+8 to +12 W/m²) |
| NH tropics (0°–20°N) | + | Large (+8 to +12 W/m²) |
| NH extratropics (30°N–60°N) | + | Moderate (+5 to +8 W/m²) |
| NH polar (60°N–90°N) | + | Moderate (+5 W/m²) |

---

### `FLNSC` — Zonal Mean (ANN, vs. ceres_ebaf_surface_v4.1)

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/zonal_mean_xy/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNSC-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/zonal_mean_xy/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNSC-ANN-global.png" width="420"></td>
</tr></table>


| Latitude Band | Bias Sign | Magnitude |
|---|---|---|
| SH polar (60°S–90°S) | + | Moderate (+5 to +10 W/m²) |
| SH extratropics (35°S–60°S) | + | Large (+8 to +15 W/m²) |
| SH tropics (0°–30°S) | + | Small (+2 to +4 W/m²) |
| NH tropics / subtropics (0°–35°N) | + | Moderate (+5 to +8 W/m²) |
| NH extratropics (35°N–60°N) | + | Small (+2 to +4 W/m²) |
| NH polar (60°N–90°N) | + | Moderate (+5 to +8 W/m²) |


The clear-sky surface LW flux zonal mean shows a strong positive bias throughout the Southern Ocean (35°S–70°S, +8 to +15 W/m²) and polar regions (+5 to +10 W/m²), consistent with a warm model surface (too-high SSTs or insufficient sea-ice extent) that emits more LW radiation than CERES observes under cloud-free conditions. NH subtropical and desert regions (15°N–35°N) also show a positive bias (+5 to +8 W/m²) driven by overheated land surfaces. The clear-sky signal is broadly similar in pattern to FLNS but amplified, confirming that the model's surface temperature errors — not just cloud errors — contribute to the LW surface flux bias.

---

### `FLUTC` — Zonal Mean (ANN, vs. ceres_ebaf_toa_v4.1)

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/zonal_mean_xy/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUTC-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/zonal_mean_xy/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUTC-ANN-global.png" width="420"></td>
</tr></table>



| Latitude Band | Bias Sign | Magnitude |
|---|---|---|
| SH polar (60°S–90°S) | + | Small (+2 W/m²) |
| SH extratropics (30°S–60°S) | − | Small (−1 to −2 W/m²) |
| Tropics (30°S–30°N) | − | Moderate (−2 to −5 W/m²) |
| NH extratropics (30°N–60°N) | − | Small (−1 to −3 W/m²) |
| NH polar (60°N–90°N) | + | Small (+3 W/m²) |

---

### `TREFHT` — Zonal Mean (ANN, vs. ERA5)

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/zonal_mean_xy/ERA5/ERA5-TREFHT-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/zonal_mean_xy/ERA5/ERA5-TREFHT-ANN-global.png" width="420"></td>
</tr></table>


| Latitude Band | Bias Sign | Magnitude |
|---|---|---|
| SH polar (70°S–90°S) | − | Small (−0.5 K) |
| SH extratropics (30°S–60°S) | ~0 | Near-zero |
| Tropics (30°S–30°N) | ~0 to + | Small (+0.3 K) |
| NH midlatitudes (30°N–60°N) | + | Moderate (+1 K) |
| NH polar (60°N–90°N) | + | Small (+0.5 K) |


The zonal mean TREFHT shows near-zero bias across most latitudes, with a slight warm bias of +0.5–1.0 K from 30°N–60°N (consistent with the land warm bias) and a small cold bias of −0.5 K in the Southern Ocean / Antarctic. Compared to CTRL, the NH cold bias is substantially reduced, but the sign reversal from cold (CTRL) to warm (TEST) over NH midlatitude land suggests the correction overshoots.

---

### `SST` — Zonal Mean (ANN, vs. HadISST_PI)

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/zonal_mean_xy/SST_PI_HadISST/HadISST_PI-SST-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/zonal_mean_xy/SST_PI_HadISST/HadISST_PI-SST-ANN-global.png" width="420"></td>
</tr></table>



The zonal mean profile shows the model tracking observations closely, with: (1) cold bias of ~1 K at the equator (cold tongue in zonal mean), (2) warm bias of ~0.5–1 K from 30°S–60°S (Southern Ocean), and (3) good agreement in NH midlatitudes. std ratio = 0.88 indicates underestimated SST variability.

---

### `RESTOM` — Zonal Mean (ANN, vs. ceres_ebaf_toa_v4.1)

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/zonal_mean_xy/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-RESTOM-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/zonal_mean_xy/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-RESTOM-ANN-global.png" width="420"></td>
</tr></table>



Zonal mean RESTOM shows the characteristic tropical surplus (~100–120 W/m² between 20°S–20°N) and polar deficit. The model overestimates tropical net absorption by ~10–20 W/m² (insufficient cloud reflection) while underestimating extratropical radiation by 5–10 W/m².

---

### `FSNTOA` — Zonal Mean (ANN, vs. ceres_ebaf_toa_v4.1)

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/zonal_mean_xy/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FSNTOA-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/zonal_mean_xy/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FSNTOA-ANN-global.png" width="420"></td>
</tr></table>


| Latitude Band | Bias Sign | Magnitude |
|---|---|---|
| SH polar (60°S–90°S) | + | small |
| SH extratropics (30°S–60°S) | + | large |
| SH tropics (0°–30°S) | − | moderate |
| NH tropics (0°–30°N) | − | moderate |
| NH extratropics (30°N–60°N) | + | small |
| NH polar (60°N–90°N) | + | moderate |


The zonal mean difference shows a clear tripolar structure: a sharp positive peak of +12 W/m² near 60°S (Southern Ocean cloud deficit), a broad negative trough of −8 to −10 W/m² across 30°S–10°N (tropical cloud excess), and a secondary positive peak of +5–8 W/m² at 60–70°N (NH high-latitude cloud deficit). The model tracks observations closely at 30°N and the SH polar cap. The tropical deficit is consistent with SWCF being too negative (too much cloud reflection) in the ITCZ region.

---

### `FLUT` — Zonal Mean (ANN, vs. ceres_ebaf_toa_v4.1)

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/zonal_mean_xy/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUT-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/zonal_mean_xy/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUT-ANN-global.png" width="420"></td>
</tr></table>


| Latitude Band | Bias Sign | Magnitude |
|---|---|---|
| SH polar (60°S–90°S) | − | moderate |
| SH extratropics (30°S–60°S) | − | moderate |
| SH tropics (0°–30°S) | − | large |
| NH tropics (0°–30°N) | mixed | moderate |
| NH extratropics (30°N–60°N) | − | small |
| NH polar (60°N–90°N) | − | small |


The zonal mean difference shows a distinctive V-shaped tropical structure: a strong negative trough of −6 W/m² centered at 15°S (SH tropics) and a secondary trough at 30°S, with a sharp positive spike of +5–6 W/m² at the equator. The equatorial excess likely reflects the double-ITCZ pattern: excess convection at the equator produces too much OLR locally, while insufficient convection in the off-equatorial tropics traps too much LW. Poleward of 30° in both hemispheres, the model is consistently 2–4 W/m² below observations, with the largest deficit at 90°S (−6 W/m²) and 60°S (−4 W/m²).

---

### `FSNS` — Zonal Mean (ANN, vs. ceres_ebaf_surface_v4.1)

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/zonal_mean_xy/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FSNS-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/zonal_mean_xy/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FSNS-ANN-global.png" width="420"></td>
</tr></table>


| Latitude Band | Bias Sign | Magnitude |
|---|---|---|
| SH polar (60°S–90°S) | − | moderate |
| SH extratropics (30°S–60°S) | + | large |
| SH tropics (0°–30°S) | − | moderate |
| NH tropics (0°–30°N) | mixed | small |
| NH extratropics (30°N–60°N) | + | moderate |
| NH polar (60°N–90°N) | + | moderate |


The zonal mean difference is strikingly similar to FSNTOA: a sharp positive peak of +12 W/m² at 60°S (Southern Ocean), a negative trough at 30°S–0° of −3 to −5 W/m², a secondary positive spike of +5 W/m² at 5°N, and then a broad positive region of +5–10 W/m² from 40°N to 70°N. The close correspondence between FSNS and FSNTOA zonal profiles (r ≈ 0.95 by inspection) indicates that the TOA SW excess in the Southern Ocean and NH high latitudes propagates almost entirely to the surface — atmospheric SW absorption errors are secondary.

---
