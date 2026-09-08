# HARVEST — State of the Art for Early Crop-Yield Forecasting from EO Time Series

## Subject

Establish the degree of novelty and scientific and technological relevance of the HARVEST project and its already available preliminary results in relation to the national and international state of the art.

## Project Context

HARVEST addresses early crop-yield forecasting from Earth Observation time series, with particular emphasis on Sentinel-2 observations.

The enterprise partner, Field Data Zoom SRL, has already developed the operational OGOR Yield Forecast System. HARVEST builds upon this existing capability.

The central scientific limitation addressed by HARVEST is that, at any prediction date before harvest, only the vegetation trajectory observed up to that date is available. The future part of the crop-development trajectory, which contains information relevant to final yield, has not yet been observed.

HARVEST investigates whether modelling, forecasting or reconstructing the unobserved future part of the vegetation trajectory can improve early-season yield estimation compared with approaches relying only on the partial EO observations available at prediction time.

## What I Want to Understand

- What is the international state of the art in crop-yield prediction using Sentinel-2 and other EO time series.
- What research, operational and commercial crop-yield forecasting systems currently exist.
- What algorithms and methodological pipelines these systems use.
- What EO, meteorological, historical, crop-model and other input data they use.
- At what dates or phenological stages yield predictions are produced.
- What spatial and temporal resolutions are used.
- What prediction performance is reported, including R2, RMSE, MAE or equivalent metrics.
- How yield-prediction performance changes with prediction date and incomplete or partial growing-season observations.
- Existing approaches for early-season or within-season crop-yield forecasting.
- Methods that forecast, extrapolate, reconstruct or complete future vegetation-index or EO time-series trajectories.
- Whether predicted future EO or vegetation trajectories have explicitly been used as inputs for final crop-yield prediction.
- Relevant approaches based on Random Forest, XGBoost, SVR, CNN, LSTM, GRU, Seq2Seq, TCN, Transformers, temporal foundation models, Gaussian Processes, generative models or other methods applicable to incomplete EO trajectories.
- How HARVEST differs scientifically from approaches that directly predict yield from the observed partial season.
- How HARVEST differs from approaches that use weather forecasts, crop-growth models, historical climatology or other auxiliary information to compensate for incomplete seasonal observations.
- Existing operational and commercial crop-yield forecasting systems and, where publicly documented, the methodological principles they use.
- The Romanian state of the art in EO-based crop-yield forecasting and any comparable operational systems.
- Which preliminary OGOR/HARVEST capabilities can legitimately be described as already demonstrated results and which elements represent the new research contribution.
- What specific scientific and technological gap HARVEST fills at national and international level.

## Key Methodological Comparison

Explicitly distinguish between four methodological categories:

1. Direct yield prediction from the partial EO trajectory observed up to the prediction date.
2. Yield prediction using partial EO observations plus meteorological, historical or crop-model information.
3. Forecasting or reconstructing the future EO or vegetation trajectory.
4. Full HARVEST-type pipeline: partial EO trajectory → future trajectory forecasting/reconstruction → completed full-season trajectory → yield prediction.

Determine specifically whether approach 4 has already been demonstrated in peer-reviewed literature or operational systems.

If similar approaches exist, identify the closest prior art and establish precisely how HARVEST differs.

## Required State-of-the-Art Outputs

The research must produce a technical state-of-the-art suitable for the HARVEST funding proposal.

### 1. Systems Landscape

For each relevant research, operational or commercial crop-yield forecasting system or representative study, extract where available:

- system, project or publication name;
- country, institution or company;
- crop or crops;
- EO data and other input data;
- spatial and temporal resolution;
- prediction date or phenological stage;
- forecasting methodology;
- algorithms or models used;
- reported accuracy;
- operational maturity;
- limitations;
- relevance and difference relative to OGOR/HARVEST.

### 2. Algorithms and Methods Landscape

Organize existing methods according to the four methodological categories defined above.

Identify representative algorithms and explain what role each algorithm plays in the forecasting pipeline.

Distinguish between algorithms used for:
- direct yield prediction;
- multimodal EO-weather yield prediction;
- temporal forecasting of vegetation or EO trajectories;
- reconstruction or completion of missing future trajectories;
- final yield prediction from completed trajectories.

### 3. HARVEST Gap Analysis

Determine whether published or operational systems already implement the complete category-4 pipeline.

Do not claim novelty solely because no identical system was found.

Search specifically for prior art that could contradict the HARVEST novelty claim.

Identify the closest approaches and explain precisely:
- what they do;
- which components overlap with HARVEST;
- which components differ;
- whether the difference is scientifically significant.

### 4. Romanian State of the Art

Identify Romanian:
- research groups;
- peer-reviewed publications;
- EO agricultural monitoring projects;
- operational yield-forecasting systems;
- relevant national or EU-funded projects.

Position OGOR and HARVEST relative to these capabilities.

### 5. Required Synthesis Tables

Produce:
- a comparative table of crop-yield forecasting systems and representative studies;
- a comparative table of algorithms and methodological families;
- a table comparing the closest prior approaches directly with OGOR and HARVEST.

## Evidence Requirements

Prioritize:
- peer-reviewed journal and conference papers;
- systematic reviews and benchmark studies;
- official Copernicus, ESA, JRC, FAO and EU documentation;
- authoritative documentation of operational systems;
- original sources rather than secondary summaries.

Every important state-of-the-art claim must be traceable to reliable evidence.

For novelty claims, actively search for counterexamples and potential prior art.

Distinguish clearly between:
- established state of the art;
- closely related work;
- apparent research gaps;
- genuine evidence of novelty;
- claims for which available evidence is insufficient.

Do not infer novelty merely from the absence of an easily found publication.

## Completion Criteria

- Identify the principal international crop-yield forecasting systems and representative research approaches.
- Identify the main algorithms and methodological families used in EO-based yield forecasting.
- Characterize early-season and partial-season forecasting approaches.
- Characterize methods for forecasting or reconstructing future EO and vegetation trajectories.
- Determine whether the complete HARVEST-type category-4 pipeline has previously been demonstrated.
- Identify the closest international approaches to HARVEST.
- Establish the Romanian state of the art.
- Distinguish demonstrated OGOR capabilities from new HARVEST research.
- Establish which aspects of HARVEST are incremental and which may constitute genuine novelty.
- Every important state-of-the-art claim must be supported by reliable sources.
- Potential counterexamples to the claimed novelty must be explicitly investigated.
- Unresolved contradictions must be reported rather than hidden.
- Produce sufficient evidence to support a funding-proposal section entitled "Novelty and Relevance of the Preliminary Results in Relation to the National and International State of the Art."

## Out of Scope

- General descriptions of precision agriculture without relevance to yield forecasting.
- Generic AI or remote-sensing literature without a clear connection to the research question.
- Unsupported promotional claims about commercial products.
- Novelty claims that cannot be supported by evidence.
