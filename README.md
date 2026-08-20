# Synthetic ELISA Immunoassay Analytics Portfolio Project

A portfolio-ready dataset for demonstrating scientific data analytics, immunoassay QC, Python automation, visualization, and decision-support skills.

## Dataset
- **25 synthetic 96-well ELISA plates**
- 8-point standard curve in duplicate
- Blank wells in duplicate
- Low, mid, and high QC samples in duplicate
- 36 synthetic unknown samples in duplicate per plate
- 2,400 total well-level records

## Safe-to-publish statement
**All data are fully synthetic and were generated solely for portfolio demonstration. They contain no patient, client, employer, proprietary, confidential, or unpublished experimental data.**

## Suggested portfolio questions
1. Fit an independent 4-parameter logistic (4PL) standard curve to each plate.
2. Calculate concentrations and dilution-corrected results for unknowns.
3. Apply duplicate CV and QC recovery rules.
4. Identify high background, replicate imprecision, edge effects, and read-order drift.
5. Compare analyst, instrument, batch, and well-position variability.
6. Generate an automated plate-level QC report.

## Illustrative QC criteria
These are simplified for portfolio use and **not a validated regulatory SOP**:
- Mean blank OD ≤ 0.150
- Standard replicate CV ≤ 15%
- QC replicate CV ≤ 20%
- QC recovery 80–120%
- Standard-curve R² ≥ 0.990
- Unknown duplicate CV ≤ 20% (otherwise review)
- Illustrative assay range: 20–1800 pg/mL before dilution correction

## Files
- `data/synthetic_elisa_25_plate_data.csv`
- `data/synthetic_elisa_plate_summary.csv`
- `data/synthetic_elisa_data_dictionary.csv`
- `data/synthetic_elisa_injected_issues.csv`
- `generation_spec.json`
- `workbook/Synthetic_ELISA_GitHub_Portfolio_Starter.xlsx`

## Recommended next step
Build a Python notebook that derives its results from the **raw CSV**, fits the 4PL curves, calculates QC metrics, flags failures, visualizes plate-position/read-order effects, and produces an automated QC summary.

**Portfolio positioning:** Scientific data analytics · Immunoassay QC · Python · Data visualization · Laboratory automation · Decision support
