<p align="center">
  <img src="Wolf_Analytics_Logo.png" width="350">
</p>

# Synthetic ELISA Immunoassay Analytics Portfolio Project

This project analyzes a fully synthetic 25-plate ELISA dataset using Python for scientific data analysis, immunoassay QC, visualization, and laboratory decision support.

**📊 [View the complete ELISA QC analysis notebook](notebooks/elisa_qc_analysis.ipynb)**

## Dataset

- **25 synthetic 96-well ELISA plates**
- 8-point standard curve in duplicate
- Blank wells in duplicate
- Low, mid, and high QC samples in duplicate
- 36 synthetic unknown samples in duplicate per plate
- **2,400 total well records**

## Data safety

**All data are fully synthetic and were generated solely for this portfolio. They contain no patient, client, employer, proprietary, confidential, or unpublished experimental data.**

## Analysis performed

The Python notebook:

- Fits an independent 4-parameter logistic (4PL) standard curve to each ELISA plate
- Back-calculates concentrations directly from OD450 measurements
- Applies dilution correction to unknown samples
- Calculates duplicate precision and QC recovery
- Evaluates blank background and standard curve fit
- Applies automated plate-level QC criteria
- Investigates possible edge effects and read order drift
- Classifies plates as **Pass**, **Review**, or **Fail**
- Compares the detected anomalies with the known synthetic design only after the analysis is complete

## Key results

- **25 complete 96-well ELISA plates analyzed**
- **2,400 well records analyzed**
- **19 plates classified Pass**
- **1 plate classified Review**
- **5 plates classified Fail**
- **6 of 6 deliberately planted anomaly plates identified**
- **19 of 19 routine plates classified Pass**

The workflow detected examples of high background, duplicate imprecision, poor QC recovery, standard curve abnormalities, positional bias, and read order drift.

## Illustrative QC criteria

These criteria are simplified for portfolio use and are **not a validated regulatory SOP**:

- Mean blank OD ≤ **0.150**
- Standard curve R² ≥ **0.990**
- QC duplicate CV ≤ **20%**
- QC recovery **80% to 120%**
- Duplicate CV for quantifiable unknown samples > **20%**: review
- Illustrative assay range: **20 to 1800 pg/mL** before dilution correction
- Read order residual slope > **|0.00025 OD/read|**: review

## Files

- `notebooks/elisa_qc_analysis.ipynb`
- `data/synthetic_elisa_25_plate_data.csv`
- `data/synthetic_elisa_plate_summary.csv`
- `data/synthetic_elisa_data_dictionary.csv`
- `data/synthetic_elisa_injected_issues.csv`
- `generation_spec.json`
- `workbook/Synthetic_ELISA_GitHub_Portfolio_Starter.xlsx`

## Portfolio relevance

This project combines assay science with Python to support reproducible laboratory data analysis, transparent QC review, and consistent QC decisions across multiple assay plates.

**Methods used:** ELISA · 4PL nonlinear regression · assay QC · precision · recovery · dilution correction · anomaly detection · data visualization · Python · scientific decision support
