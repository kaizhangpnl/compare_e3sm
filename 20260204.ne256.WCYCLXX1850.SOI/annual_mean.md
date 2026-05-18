## ANN Spatial Analysis (lat-lon maps)

> DIFF panel = model − observation. Positive (warm/red) = model overestimates; negative (cool/blue) = model underestimates.  
> **TEST vs CTRL** label: `new` = TEST notably worse than CTRL (Δ nRMSE > +0.05); `inherited` = similar to CTRL; `improved` = TEST better than CTRL (Δ nRMSE < −0.05).

---

### Top 10 by nRMSE

---

<a id="tgcldlwp-ocn"></a>
#### 1. `TGCLDLWP_OCN`  (TEST nRMSE = +2.249, CTRL = +1.573, Δ = +0.676 | TEST nbias = -2.122) — **new** bias | ⚑ seasonal (nRMSE spread=0.9179 > 0.15 (Precipitation))
_Reference: SSMI_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/Cloud%20SSM/I/SSMI-TGCLDLWP_OCN-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b> — CTRL DIFF: Mean=-34 g/m², RMSE=38.51, CORR=0.69. TEST makes the deficit ~2× worse globally; Southern Ocean and NH midlatitudes most affected.<br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/Cloud%20SSM/I/SSMI-TGCLDLWP_OCN-ANN-global.png" width="420"></td>
</tr></table>

> **TEST vs CTRL:** CTRL already underestimates LWP globally (Mean DIFF −34 g/m², RMSE 38.51). TEST amplifies this deficit to ~−65 g/m² (RMSE ~54), making it the single largest regression from CTRL in this analysis. The Southern Ocean storm-track and NH midlatitude marine stratocumulus regions show the largest absolute worsening. The bias is **inherited** from v3 LR microphysics but **substantially amplified** by the ne256 EAMxx configuration, likely due to changes in cloud microphysics tuning.


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Southern Ocean (45°S–65°S) | − (underestimate) | Large | Insufficient supercooled liquid water in mixed-phase clouds; model glaciates too quickly at −10 to −30 °C, converting liquid to ice and suppressing microwave-observable LWP. _Canonical: Southern Ocean clouds are the most persistent GCM bias region. Models convert liquid → ice too readily at −5 to −20°C. The liquid water deficit here is the root cause of the "most critical" regional bias in CMIP models._ |
| NH midlatitude oceans (30°N–60°N, all basins) | − | Large | Same mixed-phase issue; marine boundary-layer cloud liquid under-represented at ne256 resolution. |
| Tropical Pacific / ITCZ (5°S–10°N) | − | Large | Near-equatorial LWP minimum likely reflects the double-ITCZ artifact: convective precipitation removes moisture before it can remain as liquid in boundary-layer clouds. |
| Subtropical stratocumulus decks (California, Namibia, Canary) | − | Moderate | Resolution-dependent: ne256 partially resolves stratocumulus decks, but cloud fraction and LWP are still under-represented without a prognostic cloud-fraction scheme. _Canonical: SE Pacific/SE Atlantic stratocumulus — observed cloud fraction ~80%; models ~50–65%. LWP too low by 20–50%._ |

_See also: `FLNS`, `LWCFSRF`, `SWCF` (downstream radiative consequences of the LWP deficit)_

---

<a id="shflx"></a>
#### 2. `SHFLX`  (TEST nRMSE = +0.815, CTRL = +0.727, Δ = +0.088 | TEST nbias = +0.656) — **new** bias | ⚑ seasonal (Δnrmse JJA−DJF = +0.349)
_Reference: ERA5_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-SHFLX-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b> — CTRL DIFF: Mean=+6.36 W/m², RMSE=9.89, CORR=0.63 — uniform weak positive bias. TEST adds strong regional overestimates especially Arabian Sea, Gulf of Guinea in boreal summer.<br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-SHFLX-ANN-global.png" width="420"></td>
</tr></table>

> **TEST vs CTRL:** CTRL has a mild, spatially uniform positive SHFLX bias (Mean +6.4 W/m², RMSE 9.89) that is much weaker than TEST. TEST worsens the bias substantially with strong regional hotspots (Arabian Sea, Gulf of Guinea, Maritime Continent) and introduces a large seasonal amplification (JJA nRMSE is 0.35 units higher than DJF). The **seasonal modulation is new** — CTRL's bias is relatively season-independent.


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Tropical western Pacific / Maritime Continent | + (overestimate) | Large | Excessive sensible heat flux over warm SSTs; likely related to boundary-layer parameterization producing too-vigorous turbulent mixing, or a warm coupled SST bias over the warm pool. _Canonical: Warm Pool SST warm bias of +0.5–1.5°C in CMIP models drives excess sensible heat flux. Deep convection too persistent and insufficiently organized._ |
| Arabian Sea / Bay of Bengal | + | Large | Strong positive bias during summer monsoon; the ne256 resolution may misrepresent coastal upwelling suppression and surface energy partitioning. _Canonical: South Asian monsoon LLJ strength bias ±2–3 m/s; surface energy partitioning errors over monsoon oceans are common in CMIP models._ |
| Gulf of Guinea / eastern tropical Atlantic | + | Large | Consistent with an upwelling-region warm SST bias in coupled mode, leading to inflated air–sea temperature gradients and excess sensible flux. |
| Southern Ocean (storm track) | mixed | Moderate | Negative anomaly where surface winds are too weak, partially counteracting the global positive bias. |


---

<a id="omega-850mb"></a>
#### 3. `OMEGA-850mb`  (TEST nRMSE = +0.698, CTRL = +0.715, Δ = -0.017 | TEST nbias = -0.039) — **inherited**
_Reference: ERA5_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-OMEGA-850-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-OMEGA-850-ANN-global.png" width="420"></td>
</tr></table>

> **TEST vs CTRL:** CTRL also exhibits the double-ITCZ signature in OMEGA-850mb (too-strong upward motion over the tropical Pacific ITCZ, too-weak descent in the subtropics). TEST is marginally improved (Δ nRMSE = −0.017) — both models are nearly identical in their low-level circulation biases, confirming this is an inherited structural issue from the E3SMv3 convection scheme rather than a ne256-specific regression.


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Tropical western Pacific / ITCZ | − (too strong ascent) | Moderate | Model places the primary convective ascent region too narrowly; excessive convergence near the ITCZ overestimates upward motion at 850 hPa. |
| South Asian monsoon region | − | Moderate | Monsoon convergence overly intense in the low-level jet corridor between the Arabian Sea and Bay of Bengal. _Canonical: South Asian monsoon convergence and LLJ intensity biases ±2–3 m/s are common in CMIP models._ |
| Subtropical descending branches (20°N–30°N, Pacific/Atlantic) | + (too weak descent) | Moderate | The Hadley cell descending branch is insufficiently strong, consistent with a slightly too-weak subtropical high. _Canonical: Subtropical descending branches are often too weak; related to equatorward jet displacement and Hadley cell width errors._ |
| Southern Ocean mid-latitudes (45°S–60°S) | mixed | Small | Synoptic variability differences between the high-resolution ne256 and ERA5 at 850 hPa in the storm track. |


---

<a id="t-200mb"></a>
#### 4. `T-200mb`  (TEST nRMSE = +0.693, CTRL = +0.876, Δ = -0.183 | TEST nbias = -0.548) — **improved** | ⚑ seasonal (Δnrmse JJA−DJF = -0.155)
_Reference: ERA5_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-T-200-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b> — CTRL DIFF: Mean=+0.27 K, RMSE=1.82, CORR=0.69 — opposite sign to TEST. TEST significantly improves T-200mb globally.<br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-T-200-ANN-global.png" width="420"></td>
</tr></table>

> **TEST vs CTRL:** CTRL has a **warm** bias in the NH (Eurasia, North America: +3 to +5 K; Arctic: +4 to +7 K) with a slight cold bias at 60°S–80°S. TEST **reverses** the NH sign to a cold bias, reducing overall RMSE from 1.82 to ~0.8 (Δ = −0.183). The warm NH upper-tropospheric bias in CTRL — likely due to insufficient poleward energy transport in the ne30 LR dynamics — is eliminated by the ne256 high-resolution dynamics, at the cost of introducing a mild pan-hemispheric cold tendency.


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Tropics (15°S–15°N) | − (cold bias) | Moderate–Large | Cold tropical tropopause layer (TTL); underpowered deep convective heating or excessive longwave cooling at 200 hPa. Consistent with the negative `TMQ` bias (drier upper troposphere inhibiting temperature increase). _Canonical: Upper-tropospheric temperature biases of ±1–2 K are common; cold TTL is often linked to insufficient deep convective detrainment or excess radiative cooling._ |
| NH subtropics–midlatitudes (20°N–60°N) | − | Large | Planetary-wave cold anomaly; possible contribution from insufficient poleward eddy heat flux at ne256 (known issue for high-resolution atmosphere on coarse coupling). |
| NH polar region (60°N–90°N) | − | Large | Arctic stratospheric influence may be over-mixed into the upper troposphere; alternatively, too little poleward heat flux from the tropics via resolved Rossby waves. |
| SH polar region (70°S–90°S) | + (slight warm bias) | Small | Near-zero to slight positive, consistent with the zonal-mean showing near-zero bias at the SH pole. |


---

<a id="flns"></a>
#### 5. `FLNS`  (TEST nRMSE = +0.680, CTRL = +0.533, Δ = +0.147 | TEST nbias = -0.182) — **new** bias | ⚑ seasonal (Δnbias JJA−DJF = +0.167)
_Reference: ceres_ebaf_surface_v4.1_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNS-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNS-ANN-global.png" width="420"></td>
</tr></table>


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Southern Ocean (40°S–65°S) | − (underestimate) | Large | Insufficient downward LW radiation reaching the surface — directly linked to too little low/mid-cloud liquid water (`TGCLDLWP_OCN` deficit), reducing cloud greenhouse trapping. _Canonical: The Southern Ocean cloud LW trapping deficit is a direct downstream consequence of the most persistent GCM bias (insufficient supercooled liquid water). Fixing the ice nucleation threshold and Bergeron process rate typically improves this._ |
| NH subtropical/tropical continents (North Africa, Middle East, South Asia) | + (overestimate) | Moderate–Large | Too little cloud cover over arid subtropical regions leads to excess surface LW emission (overheated land surface) and reduced downward LW shielding. |
| Arctic Ocean (70°N–90°N) | + | Moderate | Warm surface bias over melting sea ice increases surface LW emission above observed; or reduced Arctic cloud cover in summer. _Canonical: Arctic clouds — biases of ±10–20% in cloud fraction (retrievals uncertain); LW downwelling underestimated in winter by 10–20 W/m²._ |
| NH extratropical ocean (30°N–60°N) | + | Moderate | Consistent with excess sensible heat flux and warmer ocean surface in the coupled run. |

_See also: `TGCLDLWP_OCN` (root cause: liquid water deficit reduces downwelling LW trapping at surface)_

---

<a id="omega-200mb"></a>
#### 6. `OMEGA-200mb`  (TEST nRMSE = +0.658, CTRL = +0.753, Δ = -0.095 | TEST nbias = +0.020) — **improved**
_Reference: ERA5_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-OMEGA-200-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-OMEGA-200-ANN-global.png" width="420"></td>
</tr></table>


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Tropical Pacific ITCZ / warm pool | + (too weak upward motion at 200 hPa, i.e. positive Ω) | Moderate | The divergent outflow at 200 hPa in deep convection is underestimated; upward mass flux is lower than ERA5, indicating the convective parameterization detrains below 200 hPa. |
| South Asian monsoon / Bay of Bengal | − (too strong ascent) | Moderate | Monsoon upper-level divergence is overly vigorous, pushing 200 hPa upward motion stronger than observed — a split between the lower (850 hPa, too strong) and upper (200 hPa, locally too strong) levels over South Asia. |
| Extratropical Pacific storm track (40°N–55°N) | + | Small | Weak ascent in the baroclinic cyclone zone at 200 hPa, consistent with slightly under-resolved transient eddies. |


---

<a id="netcf"></a>
#### 7. `NETCF`  (TEST nRMSE = +0.653, CTRL = +0.702, Δ = -0.049 | TEST nbias = -0.248) — **inherited** | ⚑ seasonal (Δnrmse JJA−DJF = +0.166)
_Reference: ceres_ebaf_toa_v4.1_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-NETCF-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-NETCF-ANN-global.png" width="420"></td>
</tr></table>


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Southern Ocean storm track (50°S–65°S) | + (model NETCF less negative than obs = insufficient cloud cooling) | Large | Insufficient liquid water in Southern Ocean storm-track clouds (consistent with TGCLDLWP_OCN deficit) reduces SW reflection; model SW cooling is weaker than CERES-observed, making NETCF less negative. Despite the positive DIFF, this reflects too-few/thin clouds, not too many. _Canonical: Southern Ocean SWCF deficit is the most critical regional cloud bias in GCMs; insufficient supercooled liquid water makes clouds less reflective at these latitudes._ |
| Tropical western Pacific / ITCZ (5°S–15°N) | − (NETCF too negative = too much net cloud cooling) | Large | Insufficient high cirrus cloud optical depth in the tropics, or too much SW reflection without compensating LW trapping, resulting in net cloud cooling stronger than observed. |
| NH subtropics (15°N–30°N, eastern ocean basins) | − | Moderate | Stratocumulus cloud decks too reflective or too extensive over the subtropical ocean, producing excess shortwave cloud forcing. |

_See also: `SWCF`, `TGCLDLWP_OCN` (Southern Ocean: LWP deficit reduces cloud cooling)_

---

<a id="omega-500mb"></a>
#### 8. `OMEGA-500mb`  (TEST nRMSE = +0.632, CTRL = +0.672, Δ = -0.040 | TEST nbias = -0.003) — **inherited** | ⚑ seasonal (DJF-JJA bias sign reversal)
_Reference: ERA5_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-OMEGA-500-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-OMEGA-500-ANN-global.png" width="420"></td>
</tr></table>

> **TEST vs CTRL:** Both CTRL and TEST exhibit the same tropical mid-tropospheric ascent bias (double-ITCZ artifact, too-strong ITCZ updraft at 500 hPa). TEST is slightly improved over CTRL (Δ nRMSE = −0.040, RMSE ~1.4 vs CTRL ~1.5), likely because the ne256 dynamical core partially improves tropical circulation symmetry. The double-ITCZ bias at 500 hPa is **inherited** from v3 LR dynamics.


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Tropical Pacific warm pool / ITCZ | − (too strong upward motion at 500 hPa) | Moderate | Consistent with 850 hPa picture: the tropical convective updraft column is too intense through the mid-troposphere. |
| Monsoon Asia (5°N–25°N) | − | Moderate | Deep convective mass flux too strong in the monsoon column at 500 hPa; similarly seen at 850 hPa. _Canonical: Deep convective mass flux biases are common in CMIP models; the mid-tropospheric circulation error reflects parameterized convection detraining at the wrong level._ |
| NH extratropical Pacific (40°N–60°N) | + (too weak ascent) | Small | Storm-track mid-tropospheric ascent slightly weaker than reanalysis. |


---

<a id="prect"></a>
#### 9. `PRECT`  (TEST nRMSE = +0.579, CTRL = +0.512, Δ = +0.067 | TEST nbias = +0.056) — **new** bias
_Reference: GPCP_v3.2_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/GPCP_v3.2/GPCP_v3.2-PRECT-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b> — CTRL DIFF: Mean=+0.03 mm/day, RMSE=1.42, CORR=0.83 vs GPCP — same double-ITCZ pattern as TEST but slightly weaker. Note: CTRL seasonal plots use ERA5 reference.<br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/GPCP_v3.2/GPCP_v3.2-PRECT-ANN-global.png" width="420"></td>
</tr></table>

> **TEST vs CTRL:** Both models exhibit the double-ITCZ artifact (positive bias tropical Pacific, negative warm pool). CTRL has RMSE 1.42 vs ERA5 while TEST is slightly worse (RMSE ~1.5 vs GPCP). The ne256 high-resolution grid concentrates ITCZ precipitation into a narrower band, intensifying the spurious Southern tropical Pacific convergence zone. The **double-ITCZ is inherited** from v3 LR dynamics but marginally worsened in TEST.


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Tropical Pacific ITCZ (5°N–15°N) | + (overestimate) | Large | ITCZ is too narrow and intense at ne256; excessive grid-scale precipitation in the resolved-convection regime. |
| Southern tropical Pacific (5°S–15°S) | + | Large | Classic double-ITCZ artifact: spurious convergence zone south of the equator in the coupled model produces anomalous precipitation. _Canonical CMIP range: +0.5 to +2.0 mm/day in S. ITCZ region; observed DITCZ index ≈ −1.0 to −1.5 mm/day (N > S)._ |
| Western Pacific warm pool / Maritime Continent | − (underestimate) | Moderate–Large | Convective parameterization suppresses warm-pool precipitation while resolution-induced spurious ascent displaces rain to the ITCZ stripe. _Canonical: warm pool precipitation too frequent but too light ("drizzle bias"); convective parameterization trigger sensitivity._ |
| South Asian monsoon (Bay of Bengal, Indian sub-continent) | − | Moderate | Monsoon precipitation organizes too far north/west; the Bay of Bengal precipitation maximum is underrepresented. _Canonical: South Asian monsoon onset typically 5–15 days too late; Western Ghats precipitation underestimated (resolution-dependent); Bay of Bengal convection often misplaced._ |
| Sahel / West Africa (10°N–20°N) | − | Moderate | West African monsoon onset is delayed or suppressed at high resolution due to the same double-ITCZ dynamical pattern. _Canonical: Sahel dry bias −0.5 to −1.5 mm/day; Guinea Coast wet bias +1–2 mm/day; monsoon jump poorly timed._ |
| Southern Ocean (45°S–65°S) | + | Small | Frontal precipitation slightly overestimated in the Southern Hemisphere storm track. |


---

<a id="lwcfsrf"></a>
#### 10. `LWCFSRF`  (TEST nRMSE = +0.568, CTRL = +0.541, Δ = +0.027 | TEST nbias = +0.066) — **inherited** | ⚑ seasonal (nRMSE spread=0.0825 > 0.08 (Radiation))
_Reference: ceres_ebaf_surface_v4.1_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-LWCFSRF-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-LWCFSRF-ANN-global.png" width="420"></td>
</tr></table>


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Southern Ocean (50°S–70°S) | − (model LW cloud forcing at surface too weak) | Large | Direct consequence of `TGCLDLWP_OCN` deficit: insufficient liquid-containing clouds trap less longwave radiation at the surface. _Canonical: The Southern Ocean LW surface cloud forcing deficit is a direct downstream consequence of the TGCLDLWP_OCN liquid water deficit — the most persistent GCM bias globally._ |
| NH extratropical / Arctic (60°N–80°N) | − | Moderate | Lack of cloud liquid water in Arctic mixed-phase clouds reduces downwelling LW at the surface. _Canonical: Arctic mixed-phase clouds — LW downwelling underestimated in winter by 10–20 W/m²; insufficient liquid water at subfreezing temperatures._ |
| Tropical warm pool / ITCZ (10°S–15°N) | + (LW cloud forcing too strong) | Moderate | Thick deep convective anvil clouds trap more LW at the surface than observed, overcompensating for the liquid water deficit. |
| NH midlatitude land (30°N–60°N) | + | Small | Continental cloud cover, particularly in summer stratus/altostratus, traps more LW than CERES observes. |

_See also: `TGCLDLWP_OCN` (root cause), `FLNS` (all-sky counterpart)_

---

### Top 5 by |nbias| (not in nRMSE list above)

---

<a id="tmq"></a>
#### 11. `TMQ`  (TEST |nbias| rank 6 | TEST nbias = -0.177, nRMSE = +0.265) — **new** bias
_Reference: ERA5_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-TMQ-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-TMQ-ANN-global.png" width="420"></td>
</tr></table>


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Tropical ITCZ / warm pool (10°S–15°N) | − (dry bias) | Large | Deficient atmospheric moisture in the deep convective region; consistent with the cold `T-200mb` bias — a colder tropical upper troposphere holds less water vapor and inhibits organized convective moistening. _Canonical: TMQ bias ±3 kg/m² is within ERA5 uncertainty. However, the tropical concentration of the deficit, co-located with the double-ITCZ, suggests convective over-precipitation removes moisture from the column._ |
| NH subtropics (15°N–30°N) | − | Moderate | Dry subtropical moisture transport is underrepresented; the descending Hadley circulation diverges moisture too aggressively. |
| SH midlatitudes (30°S–60°S) | − | Small | Consistent zonal drying in the SH midlatitude atmosphere, possibly related to the Southern Ocean cold bias. |


---

<a id="psl"></a>
#### 12. `PSL`  (TEST |nbias| rank 7 | TEST nbias = -0.172, nRMSE = +0.281) — **inherited** | ⚑ seasonal (nRMSE spread=0.1010 > 0.08 (Dynamics))
_Reference: ERA5_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-PSL-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-PSL-ANN-global.png" width="420"></td>
</tr></table>


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Arctic Ocean / North Pole (70°N–90°N) | − (model PSL too low) | Large | Negative PSL bias in the Arctic consistent with an anomalously deep polar vortex or excessive cyclonic activity; the coupled ne256 may generate more frequent polar lows at high resolution. _Canonical: Arctic surface pressure biases of ±2–4 hPa are typical in CMIP models; cold bias and sea ice errors often contribute._ |
| Aleutian Low / North Pacific (45°N–60°N) | − | Moderate | The Aleutian Low is too deep in the model climatology, suggesting excess extratropical storm-track intensity in the NH winter. _Canonical: NH Pacific storm track often displaced 2–5° equatorward; intensity underestimated by 10–25%. An overly deep Aleutian Low is consistent with excess storm-track activity._ |
| Southern Ocean / Antarctic belt (55°S–70°S) | − | Moderate | Consistent with an overly strong Southern Annular Mode (SAM) positive phase in the model; wind-driven oceanography consequences for Southern Ocean heat uptake. _Canonical: SH westerly jet is often displaced equatorward by 2–5°; too strong by 1–3 m/s at 850 hPa. This PSL pattern is consistent with the canonical equatorward jet displacement._ |
| Subtropical Pacific highs (20°N–40°N, 20°S–40°S) | + (model PSL too high) | Small | The subtropical ridges are slightly stronger than observed, consistent with a slightly over-strengthened Hadley circulation. |


---

<a id="swcf"></a>
#### 13. `SWCF`  (TEST |nbias| rank 8 | TEST nbias = -0.168, nRMSE = +0.546) — **inherited** | ⚑ seasonal (Δnrmse JJA−DJF = +0.147)
_Reference: ceres_ebaf_toa_v4.1_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-SWCF-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-SWCF-ANN-global.png" width="420"></td>
</tr></table>


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Southern Ocean storm track (50°S–65°S) | + (SWCF less negative = less SW cooling = too few/thin clouds) | Large | Contrary to the `TGCLDLWP_OCN` result, here the DIFF shows model SWCF is less negative than observed, meaning there is too little shortwave cloud forcing from Southern Ocean clouds. The apparent contradiction is resolved by noting that SSM/I LWP and CERES SWCF measure different aspects of cloud state — the model may have the right cloud fraction but incorrect liquid fraction. _Canonical CMIP range: SWCF bias +10 to +20 W/m² over Southern Ocean (40°S–65°S). This model (+5–10 W/m²) falls below the multi-model mean, suggesting partial mitigation of the SH cloud bias._ |
| Tropical Pacific / ITCZ (5°S–15°N) | − (SWCF too negative = too much SW cooling from deep cloud anvils) | Large | Thick convective anvils over the ITCZ reflect too much sunlight; excess SW cloud forcing in the active convection regime. _Canonical: SWCF bias +5 to +15 W/m² in tropical Pacific ITCZ region due to insufficient stratocumulus and too-thick deep convective anvils._ |
| NH extratropics (40°N–65°N) | + | Moderate | Insufficient low/mid-level cloud cover over the NH storm track reduces SW cloud cooling relative to CERES. |

_See also: `TGCLDLWP_OCN` (root cause: liquid water deficit reduces SW reflection)_

---

<a id="flnsc"></a>
#### 14. `FLNSC`  (TEST |nbias| rank 9 | TEST nbias = +0.117, nRMSE = +0.548) — **new** bias | ⚑ seasonal (Δnbias JJA−DJF = +0.220)
_Reference: ceres_ebaf_surface_v4.1_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNSC-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FLNSC-ANN-global.png" width="420"></td>
</tr></table>


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Southern Ocean (50°S–70°S) | + (clear-sky LW flux at surface too high in model) | Large | The clear-sky LW surface flux in the model exceeds CERES, suggesting the model surface in these latitudes is too warm, driving stronger clear-sky LW emission. Combined with the `FLNS` liquid-cloud deficit, this implies the model SST/sea-surface in SH midlatitudes is biased warm. _Canonical: Clear-sky surface LW bias at SO independently confirms SST warm bias expected from the SWCF deficit feedback loop. The warm SST is a downstream consequence of insufficient cloud SW reflection._ |
| NH subtropics / desert regions (15°N–35°N) | + | Moderate | Very dry conditions lead to surface overheating; high surface temperatures increase upwelling LW radiation, which is reflected in the clear-sky diagnostic. |
| Arctic (70°N–90°N) | + | Moderate | Consistent with a warm Arctic surface bias in the coupled run; sea-ice extent may be insufficient, exposing warm ocean to emit LW without cloud masking. |


---

<a id="flutc"></a>
#### 15. `FLUTC`  (TEST |nbias| rank 10 | TEST nbias = -0.096, nRMSE = +0.153) — **inherited**
_Reference: ceres_ebaf_toa_v4.1_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUTC-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUTC-ANN-global.png" width="420"></td>
</tr></table>


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Tropics (15°S–15°N) | − (model clear-sky OLR too low) | Moderate | Consistent with the `T-200mb` cold bias: a colder upper troposphere in the tropics reduces clear-sky OLR, as the emitting level is at a lower temperature. _Canonical: Tropical OLR deficit is consistent with the T-200mb cold bias via the Stefan-Boltzmann relationship; a 1.5 K cold bias at the emitting level reduces OLR by ~3–4 W/m²._ |
| NH midlatitudes (30°N–60°N) | − | Small | Cold upper-tropospheric temperatures in the NH midlatitudes reduce emission at TOA. |
| SH polar region (60°S–90°S) | + (model OLR too high) | Small | Slightly too warm Antarctic surface or reduced Antarctic ice emissivity, driving excess clear-sky LW emission. |


---

### Additional Variables

---

<a id="trefht"></a>
#### 16. `TREFHT`  (TEST nRMSE = +0.091, CTRL = +0.112, Δ = -0.021 | TEST nbias = -0.003) — **improved** | ⚑ seasonal (DJF-JJA bias sign reversal)
_Reference: ERA5_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-TREFHT-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b> — RMSE = 1.58 K, CORR = 0.995 — Mean DIFF = −0.67 K<br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-TREFHT-ANN-global.png" width="420"></td>
</tr></table>

> **TEST vs CTRL:** CTRL has a pervasive cold bias of −0.67 K globally (ERA5), strongest over NH land (−1.28 K over land). TEST nearly eliminates the global-mean cold bias (−0.04 K) but overcorrects over land to a warm bias of +0.95 K (ERA5). The global nRMSE improves from 0.112 (CTRL) to 0.091 (TEST), Δ = −0.021. However, JJA CONUS surface temperatures degrade substantially: TEST nRMSE = 0.446 vs CTRL = 0.213, a +0.233 worsening driven by a +2.68 K summer warm bias over the continental US.


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| NH midlatitude land (30°N–60°N) | + | Moderate (+1–2 K) | Warm bias especially in JJA; possible soil moisture or BL mixing issue _Canonical: +2 to +4°C warm bias over eastern continental interiors in summer is a well-documented GCM bias, driven by soil moisture depletion and boundary-layer over-mixing._ |
| CONUS (JJA only) | + | Large (+2.7 K) | Summer warm bias; insufficient evapotranspiration or land-atm coupling _Canonical: Great Plains / Central US summer warm bias +1–4°C (soil moisture–temperature feedback). This model's +2.7 K is within the canonical CMIP range. Causes include wrong diurnal cycle of convection, insufficient nocturnal low-level jet, and MCS propagation errors._ |
| Tropics (ocean) | ~0 | Small (< 0.5 K) | Well-constrained SSTs in coupled run |
| Southern Ocean / Antarctic | − | Small (−0.5 K) | Residual cold bias from insufficient cloud LW trapping |

_See also: `SHFLX` (surface energy partitioning), `T-200mb` (upper tropospheric temperature)_

---

<a id="sst"></a>
#### 17. `SST`  (TEST nRMSE = +0.126, CTRL = +0.101, Δ = +0.025 | TEST nbias = +0.115) — **degraded** | ⚑ seasonal (Δnbias sign reversal: DJF +0.034, JJA −0.052)
_Reference: HadISST_PI_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/SST_PI_HadISST/HadISST_PI-SST-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/SST_PI_HadISST/HadISST_PI-SST-ANN-global.png" width="420"></td>
</tr></table>

> **TEST vs CTRL:** TEST shows lower RMSE (0.81 vs 1.15 K) and higher correlation (1.00 vs 0.99) than CTRL, but slightly larger normalized warm bias. TEST significantly improves cold tongue pattern and reduces NH extratropical warm bias relative to CTRL.


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Equatorial E. Pacific cold tongue (5°S–5°N, 210–280°E) | − (cold bias) | Large (−1 to −2 K) | Excessive equatorial upwelling or overly strong Walker circulation; coupled ocean bias reinforces cold tongue extension. _Canonical: Cold tongue bias is one of the top 10 GCM biases (#4). Typical cold bias of 1–3 K extending too far west, connected to Walker circulation strength and Bjerknes feedback._ |
| Southern Ocean (40°S–65°S) | + (warm bias) | Moderate (+1 to +2 K) | Insufficient SW cloud cooling (SWCF too weak) allows excess solar heating of the ocean surface. _Canonical: The SO SW bias (#2) directly warms the ocean when SWCF is insufficiently negative._ |
| SE Pacific / SE Atlantic stratocumulus regions | + (warm bias) | Moderate (+1 K) | Insufficient stratocumulus cloud fraction drives SST warm bias through SWCF–SST feedback chain. _Canonical: SE Pacific Sc deficit (#3)._ |
| North Atlantic subpolar gyre / Gulf Stream | −/mixed | Moderate | Gulf Stream separation point displaced; warm water advection path errors in coupled ocean. |
| Western Pacific warm pool (120°E–180°E) | + (warm bias) | Small–Moderate (+0.5 to +1 K) | Excess latent heat flux convergence and reduced cloud cooling. _Canonical: Warm pool SST bias (#7)._ |

_See also: ['SWCF', 'NETCF', 'SHFLX', 'RESTOM']_

---

<a id="restom"></a>
#### 18. `RESTOM`  (TEST nRMSE = +0.164, CTRL = +0.155, Δ = +0.009 | TEST nbias = -0.018) — **inherited** | ⚑ seasonal (DJF-JJA bias sign reversal)
_Reference: ceres_ebaf_toa_v4.1_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-RESTOM-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-RESTOM-ANN-global.png" width="420"></td>
</tr></table>

> **TEST vs CTRL:** TEST RMSE (8.70 W/m²) slightly better than CTRL (9.16 W/m²), with smaller global mean bias (−0.66 vs −1.02 W/m²). nRMSE Δ = −0.009 — classified as inherited.


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Tropical Pacific warm pool (10°S–10°N, 120–180°E) | + (excess absorbed radiation) | Large (+20 to +40 W/m²) | Insufficient high-cloud coverage reduces OLR, while warm pool SST bias increases absorbed SW. _Canonical: Warm pool deep convection bias (#7) interacts with TOA energy balance._ |
| Tropical East Pacific ITCZ (5°N–15°N) | + (excess) | Large (+20 to +30 W/m²) | Double-ITCZ redistributes cloud cover; reduced SWCF means more net downward SW. |
| Southern Ocean (40°S–65°S) | − (deficit) | Moderate (−10 to −20 W/m²) | Net TOA deficit despite insufficient SWCF, dominated by reduced absorbed SW at high solar zenith. _Canonical: SO radiation bias feeds back to ocean heat uptake._ |
| SE Pacific / SE Atlantic stratocumulus | + (excess) | Moderate (+10 to +20 W/m²) | Insufficient Sc SWCF allows excess SW absorption at TOA. _Canonical: Sc SWCF deficit (#3)._ |
| Arctic (70°N–90°N) | − (deficit) | Moderate (−10 to −15 W/m²) | Excess cloud cover or albedo reduces net absorbed radiation. |

_See also: ['SWCF', 'NETCF', 'FLUTC', 'FLNS']_

---

<a id="u-850mb"></a>
#### 19. `U-850mb`  (TEST nRMSE = +0.228, CTRL = +0.177, Δ = +0.051 | TEST nbias = +0.025) — **degraded** | ⚑ seasonal (DJF-JJA bias sign reversal)
_Reference: ERA5_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/ERA5/ERA5-U-850-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/ERA5/ERA5-U-850-ANN-global.png" width="420"></td>
</tr></table>

> **TEST vs CTRL:** TEST has lower RMSE (0.94 vs 1.29 m/s) and higher correlation (0.986 vs 0.980). nRMSE is worse (0.228 vs 0.177), degradation Δ = −0.051 is moderate.


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| SH westerly jet (40°S–60°S) | + (too strong / equatorward shifted) | Moderate (+1 to +2 m/s) | SH jet equatorward displacement linked to SO cloud radiative errors. _Canonical: SH jet position bias (#6) — typical 2–5° equatorward shift tied to SO SW bias through cloud–radiation–dynamics feedback._ |
| Tropical Pacific trades (10°S–10°N, 150°E–280°E) | +(weakened easterlies) | Small–Moderate (+0.5 to +1 m/s) | Weaker trades linked to double-ITCZ and reduced Walker cell. _Canonical: Dynamically linked to double-ITCZ (#1) and cold tongue SST (#4)._ |
| NH Pacific jet (30°N–50°N, 140°E–240°E) | + (slightly too strong) | Small (+0.5 m/s) | Slight intensification consistent with resolution-dependent storm track intensity. |
| NH Atlantic jet (40°N–60°N, 280°E–360°E) | mixed | Small | Atlantic jet position/tilt resolution-sensitive; ne256 captures tilt better than coarser grids. |
| Indian Ocean (5°S–20°N, 40°E–100°E) | + (weakened monsoon westerlies in JJA) | Small–Moderate | Weak Somali jet consistent with Indian Monsoon precipitation deficit. _Canonical: Monsoon circulation (#9) — weak LLJ implies deficient moisture transport._ |

_See also: ['PSL', 'PRECT', 'SWCF']_

---

<a id="fsntoa"></a>
#### 20. `FSNTOA`  (TEST nRMSE = +0.136, CTRL = +0.133, Δ = +0.003 | TEST nbias = -0.039) — **inherited**
_Reference: ceres_ebaf_toa_v4.1_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FSNTOA-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FSNTOA-ANN-global.png" width="420"></td>
</tr></table>

> **TEST vs CTRL:** TEST vs CTRL: Both simulations share the same spatial bias pattern (SO excess, tropical deficit). CTRL has a slightly smaller nRMSE (0.133 vs 0.136, Δ = +0.003) and a weaker global negative bias (nbias = −0.020 vs −0.039). The degradation is marginal and within inherited range — the TOA SW budget error is structurally the same in both configurations.


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Southern Ocean (55–65°S) | + | large | Excess absorbed SW due to insufficient cloud reflectivity (SWCF too weak); the TGCLDLWP_OCN deficit allows more solar radiation through. _Canonical: Southern Ocean SW bias (#2)._ |
| Tropical Pacific ITCZ (5°S–15°N) | − | moderate | Too much cloud reflection from thick deep-convective anvils; SW deficit consistent with SWCF being too negative in the ITCZ. _Canonical: Double-ITCZ (#1)._ |
| SE Pacific / SE Atlantic Stratocumulus | + | moderate | Insufficient stratocumulus SWCF allows excess TOA SW absorption. _Canonical: Stratocumulus (#3)._ |
| NH high latitudes (50–80°N) | + | moderate | Excess absorbed SW over NH continents and Arctic; consistent with reduced cloud cover or snow/ice albedo feedback too weak. |
| Sahara / Middle East (15–35°N) | − | small | Slight deficit in absorbed SW over bright desert surfaces; surface albedo may be slightly too high. |

_See also: SWCF, FSNS, RESTOM_

---

<a id="flut"></a>
#### 21. `FLUT`  (TEST nRMSE = +0.239, CTRL = +0.223, Δ = +0.016 | TEST nbias = -0.084) — **inherited**
_Reference: ceres_ebaf_toa_v4.1_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUT-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-TOA-v4.1/ceres_ebaf_toa_v4.1-FLUT-ANN-global.png" width="420"></td>
</tr></table>

> **TEST vs CTRL:** TEST vs CTRL: Both share the structural OLR deficit pattern. CTRL nRMSE = 0.223 vs TEST 0.239 (Δ = +0.016), with CTRL also showing a negative global bias (nbias = −0.016 vs −0.084). TEST has a notably worse mean bias, suggesting the ne256 configuration amplifies the high-cloud trapping of LW radiation — possibly through stronger resolved deep convection producing more extensive anvil clouds. The spatial pattern is inherited but the magnitude is worse.


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Tropical warm pool / Maritime Continent (10°S–10°N, 90–180°E) | − | large | Model OLR too low; consistent with too much high cloud (deep convective anvils trap LW) or a cold upper-troposphere bias (T-200mb cold bias of −1.5 K). _Canonical: Warm Pool convection (#7)._ |
| Tropical South America / Amazon | − | moderate | Reduced OLR over the Amazon consistent with excessive high cloud cover from deep convection; linked to PRECT redistribution errors. |
| SH midlatitudes (40–60°S) | − | moderate | OLR deficit in the Southern Ocean storm track; consistent with cold SST bias and excessive cloud optical depth. |
| Sahara / Middle East / Central Asia (15–40°N, 20W–80°E) | + | moderate | Excess OLR over arid regions; surface temperature too warm or insufficient low-level moisture, leading to enhanced LW emission through the clear-sky atmospheric window. |
| NH polar (60–90°N) | − | small | Arctic OLR slightly too low; consistent with excess cloud cover or cold surface temperature bias. |

_See also: T-200mb, FLUTC, RESTOM, FSNTOA_

---

<a id="fsns"></a>
#### 22. `FSNS`  (TEST nRMSE = +0.209, CTRL = +0.212, Δ = -0.003 | TEST nbias = +0.006) — **inherited**
_Reference: ceres_ebaf_surface_v4.1_

<table><tr>
<td align="center" width="50%"><b>ne256_SOI</b><br><img src="https://portal.nersc.gov/project/e3sm/wlin/E3SMv4_dev/20260204.ne256.WCYCLXX1850.SOI/e3sm_diags/model_vs_obs_0001-0010/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FSNS-ANN-global.png" width="420"></td>
<td align="center" width="50%"><b>E3SMv3_LR</b><br><img src="https://web.lcrc.anl.gov/public/e3sm/diagnostic_output/wlin/E3SMv3/v3.LR.piControl/e3sm_diags/atm_monthly_180x360_aave/model_vs_obs_0001-0030/lat_lon/CERES-EBAF-surface-v4.1/ceres_ebaf_surface_v4.1-FSNS-ANN-global.png" width="420"></td>
</tr></table>

> **TEST vs CTRL:** TEST vs CTRL: CTRL nRMSE = 0.212 vs TEST 0.209 (Δ = −0.003), virtually identical. Global mean bias is also comparable (CTRL nbias = +0.004 vs TEST +0.006). This is one of the few variables where TEST marginally improves. The spatial pattern of compensating errors (SO excess vs tropical deficit) is inherited from CTRL; the ne256 configuration does not significantly change the surface SW budget.


| Region | Bias Sign | Magnitude | Possible Physical Cause |
|---|---|---|---|
| Southern Ocean (55–65°S) | + | large | Excess surface SW reaching the surface due to insufficient cloud reflectivity (SWCF too weak → more SW transmitted). _Canonical: Southern Ocean SW bias (#2)._ Confirms the FSNTOA SO excess propagates to the surface. |
| South America / Amazon | + | large | Excess surface SW absorption over tropical South America; possibly insufficient cloud cover or too-transparent clouds over the Amazon. May partially explain the TREFHT warm bias (+1–2 K) over the Amazon. |
| Tropical Pacific ITCZ (5°S–15°N) | − | moderate | Surface SW deficit from excessive deep-convective cloud anvils reflecting too much SW. Mirrors the FSNTOA tropical deficit. _Canonical: Double-ITCZ (#1)._ |
| SE Pacific / SE Atlantic Stratocumulus | − | moderate | Stratocumulus cloud decks partially shield excess; FSNS shows deficit where SWCF is too strong in the Sc regions. |
| NH high latitudes (50–80°N) | + | moderate | Excess surface SW reaching the surface, matching the FSNTOA NH excess. Cloud cover too thin or albedo feedback too weak. |

_See also: FSNTOA, SWCF, RESTOM_

---
