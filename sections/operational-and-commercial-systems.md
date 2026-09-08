# Operational and Commercial Crop-Yield Forecasting Systems

## Scope and approach

This section surveys operational and commercial crop-yield forecasting systems and extracts only what is publicly and technically documented — official system descriptions, peer-reviewed validation studies, or institutional methodology pages. Systems for which no public technical documentation could be located are noted explicitly as undisclosed rather than assumed to use any particular method, per the project's evidence requirements.

**Confidence: HIGH | Depth: MEDIUM**

## JRC MARS Crop Yield Forecasting System (European Union)

The Joint Research Centre's MARS (Monitoring Agricultural Resources) system is the longest-running, most thoroughly documented operational crop-yield forecasting system identified, producing in-season EU and Member State-level yield forecasts monthly since 1993 under Article 25 of the CAP horizontal regulation (EU) 2021/2116, published in the MARS Bulletin [140][141].

**Data sources.** The system combines three streams: (1) observed meteorological data interpolated onto a 25 km grid and extended with the 10-day ECMWF forecast; (2) the WOFOST crop growth model, described as "a biophysically based, dynamic, and explanatory point model" producing biomass, yield, and soil-moisture outputs; and (3) more recently, 1 km-resolution satellite vegetation indicators for cereals, which the source authors themselves flag as an area where "improvements can be made, especially in the combined use with meteorological variables" [140].

**Modeling approach.** Forecasts are produced by the CoBo (Control Board) software using three combinable statistical techniques: trend analysis of historical yields (linear, exponential, etc.); multiple-linear regression linking past yield variability to meteorological and crop-model predictors; and a similarity/analogue-year method using Principal Component Analysis and cluster analysis to identify and weight historically similar seasons [140]. Critically, the system is described as "strongly analyst driven" — human forecasters interpret the statistical outputs and incorporate secondary information before publication, rather than the forecast being a fully automated model output [140].

**In-season forecast evolution.** MARS issues monthly forecasts through the season, with three characterized stages: an early trend-based estimate (March–April), a pre-harvest forecast (one month before harvest), and an end-of-campaign estimate. Reported EU-27 performance for 2006–2015 shows Mean Absolute Percentage Error declining as the season progresses — e.g., maize forecast error falls from about 12% at the first forecast to about 8% at the pre-harvest forecast — with median MAPE at pre-harvest ranging from 6.3% (potato) to 10.2% (durum wheat), and a systematic tendency to underestimate yield for soft wheat, rapeseed, and sugar beet [140].

**Relevance to HARVEST.** MARS is the clearest public exemplar of Key Comparison category 2 in the research goal: it combines partial-season observations with meteorological forecasts and a mechanistic crop-growth model (WOFOST) to compensate for the unobserved remainder of the season, rather than explicitly forecasting or reconstructing the future EO/vegetation trajectory itself. Its own documentation identifies deeper integration of satellite indicators with meteorological variables as an open improvement area, not as an already-solved problem [140]. No evidence was found of MARS using an explicitly forecasted or reconstructed future vegetation-index trajectory (Key Comparison category 3/4) as a model input.

**Confidence: HIGH | Depth: HIGH**

## GEOGLAM Crop Monitor (International / G20)

The GEO Global Agricultural Monitoring (GEOGLAM) Crop Monitor is a G20-endorsed international initiative, coordinated in part by NASA Harvest, providing monthly crop-condition assessments covering over 97% of global agricultural production through a partnership of more than 70 national, regional, and global monitoring organizations [142][143].

**Nature of the output.** The Crop Monitor's official methodology page makes clear that this is a **qualitative crop-condition assessment**, not a quantitative yield forecast: partner organizations characterize conditions using a "common crop condition classification system" rather than producing numerical yield predictions [142]. This distinguishes it categorically from MARS and from the yield-prediction task HARVEST addresses.

**Process.** Assessments are compiled through a consensus process: partners submit independent condition assessments via a web interface roughly ten days before each month's first-Thursday publication, drawing on their own EO data, crop masks, and crop calendars; submissions are cross-checked against EO-derived datasets; discrepancies between partner organizations are resolved through discussion and a joint video-conference review before publication [142]. A dedicated "Crop Monitor for Early Warning" stream, launched February 2016, applies the same consensus process specifically to countries at risk of food insecurity [143].

**Handling of incomplete-season data.** The publicly available methodology documentation does not specify a technical procedure for handling partial-season or temporally incomplete EO observations; it addresses only how monthly discrepancies between partner assessments are reconciled, not how within-season data gaps or the unobserved future portion of the growing season are treated [142]. This is an explicit documentation gap, not evidence that GEOGLAM has solved (or ignores) the problem.

**Relevance to HARVEST.** Because GEOGLAM produces qualitative condition classes rather than quantitative yield forecasts, it is not a direct methodological comparator to HARVEST's Key Comparison framework, but it establishes that international-scale operational EO agricultural monitoring at the qualitative level is already mature and consensus-based, which HARVEST's quantitative, model-based approach would complement rather than duplicate.

**Confidence: HIGH | Depth: MEDIUM**

## Commercial systems: Gro Intelligence, aWhere, Descartes Labs, Planet

Targeted searches for public technical documentation, whitepapers, or peer-reviewed validation studies of the proprietary yield-forecasting methodologies used by Gro Intelligence, aWhere, and Descartes Labs did not return any company-published technical methodology description, peer-reviewed validation, or conference paper detailing their internal modeling approach (searches conducted September 2026). Their yield-forecasting capabilities are marketed but, on the evidence available, **methodologically undisclosed** — no algorithmic, statistical, or model-architecture detail could be independently verified from primary sources. Per the research goal's evidence requirements, no claims about these companies' internal methods are made here; their absence from citable technical literature should not be read as evidence about what they do or do not implement.

**Planet Labs data — ESA-documented research pilot.** One well-documented example of Planet satellite data applied to crop-yield prediction is a University of Southampton project (BRECcIA), described on ESA's official Earth Online news page, which fused near-daily PlanetScope imagery with Copernicus Sentinel-2 data to estimate maize yields on smallholder farms in Malawi [144]. The stated rationale for the data fusion was spatial: PlanetScope's higher resolution served "as an intermediate data layer" to resolve small-field and inter-crop-area effects that degrade Sentinel-2-based estimates at 10–20 m resolution, per project lead Professor Jadu Dash [144]. Ground-truthing by field teams supplemented the satellite-derived estimates, and the reported result was "up to 60% level of confidence in the accuracy of predicting crop yields" [144]. This is explicitly a UK Global Challenge Research Fund-supported research pilot with a limited geographic and crop scope (Malawi, maize), not an operational commercial product of Planet Labs itself, and should not be conflated with a Planet-operated yield-forecasting service — no such service's methodology was located [144].

**Uncertainty:** No public technical documentation for Gro Intelligence's, aWhere's, or Descartes Labs' own operational yield-forecasting methodology was found. This absence is reported as an evidence gap consistent with the project's requirement to flag undisclosed methodology rather than infer it.

**Confidence: MEDIUM | Depth: LOW** (positive findings for the Planet/ESA pilot are well documented; the negative finding for Gro Intelligence/aWhere/Descartes Labs reflects search coverage as of September 2026, not certainty that no such documentation exists anywhere)

## Synthesis relevant to HARVEST

Across the systems with public methodology (JRC MARS, GEOGLAM), none was found to explicitly forecast, extrapolate, or reconstruct the *future, unobserved portion* of the EO/vegetation-index trajectory and then feed that reconstructed trajectory into a yield model — the Key Comparison category 4 approach central to HARVEST's novelty claim. MARS represents category 2 (partial EO/proxy observations plus meteorological forecast and crop-model compensation, human-analyst-mediated); GEOGLAM does not perform quantitative yield prediction at all. The Planet/ESA pilot [144] is a category-1-style direct estimation from fused partial-season high-resolution imagery, not a trajectory-forecasting approach. This is consistent with, but does not by itself establish, the novelty gap HARVEST claims — the absence of category-4 methodology among *publicly documented operational systems* does not rule out its presence in the academic literature, which must be checked separately against the peer-reviewed record rather than against operational-system documentation alone.

**Confidence: MEDIUM | Depth: MEDIUM**
