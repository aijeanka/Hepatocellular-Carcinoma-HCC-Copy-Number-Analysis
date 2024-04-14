# Hepatocellular Carcinoma (HCC) Copy Number Analysis

## Project Overview
This repository contains analysis of DNA copy number data for Hepatocellular Carcinoma (HCC) patients. The focus is on comparing patients with and without vascular invasion to identify key genomic differences.

## Data Description
- **Clinical Data**: Information on 198 patients, including those with HCC and those at a pre-cancer stage ("NON_TUMOR_CIRRHOTIC").
- **DNA Copy Number Data**: CINdex values representing chromosome instability index for 197 patients.

## Analysis Goals
Perform group comparison analysis on copy number data comparing patients that had Vascular Invasion (Yes) vs. those that did not (No).

## Repository Contents
- `input/PC_TAYLOR_cytobands_HIDS.csv` - Cytoband data related to the patients.
- `input/TopCytobandResults_HCC.csv` - Results related to the top cytoband findings.
- `input/hg19_cytoband.txt` - Genomic location data for cytobands.
- `input/PC_Taylor_Clinical_HIDSfinal.csv` - Final clinical data for the patients.
- `output/Aizhan_Uteubayeva_TopFeatures.tsv` - Lists top features based on your analysis criteria.
- `output/Aizhan_Uteubayeva_Circos.pdf` - Circos plot showing the genomic results.
- `output/Aizhan_Uteubayeva-TTestHW-06-Output.csv` - T-test results sorted by p-value.
- `datacheck/Aizhan_Uteubayeva_ClinCompIDs_HCC.tsv` - Clinical data for comparison group.
- `datacheck/Aizhan_Uteubayeva_ClinBaseIDs_HCC.tsv` - Clinical data for baseline group.
- `datacheck/Aizhan_Uteubayeva_CopyNumCompIDs_HCC.tsv` - Copy number data for comparison group.
- `datacheck/Aizhan_Uteubayeva_CopyNumBaseIDs_HCC.tsv` - Copy number data for baseline group.
- `datacheck/Aizhan_Uteubayeva_FeatureIDs.tsv` - Feature IDs list.
- `datacheck/Aizhan_Uteubayeva_checking.xlsx` - Excel file for checking patient IDs between clinical and copy number data.

## Steps to Run Analysis
1. Check clinical and molecular data.
2. Read in data.
3. Clean/filter data.
4. Identify groups for comparison.
5. Conduct T-tests, calculate fold change, q-values, and sort by p-value.
6. Export results and generate visualizations like the circos plot.

## How to Use
Details on how to run the R Markdown scripts and reproduce the findings are included in the Rmd files.

## Contributing
Guidelines for contributing to this project are provided.

## License
This project is released under the MIT License.

## Author
- Aizhan Uteubayeva - Initial analysis and documentation.
