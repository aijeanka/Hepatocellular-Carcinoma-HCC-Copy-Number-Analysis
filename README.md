# **Hepatocellular Carcinoma (HCC) Copy Number Analysis**

## **Project Overview**

This repository contains an analysis of DNA copy number data for Hepatocellular Carcinoma (HCC) patients. The primary objective is to compare patients with and without vascular invasion to identify key genomic differences, focusing on chromosome instability and top features derived from copy number data.

## **Data Description**

- **Clinical Data**: Clinical details for 198 patients, including those diagnosed with HCC and those at a pre-cancer stage (*“NON_TUMOR_CIRRHOTIC”*).
- **DNA Copy Number Data**: Chromosome instability (CINdex) values for 197 patients.

---

## **Analysis Goals**

1. **Group Comparison**: Compare copy number data between patients with vascular invasion (**Yes**) and those without (**No**).
2. **Feature Identification**: Identify differentially expressed features and cytobands associated with vascular invasion.
3. **Visualization**: Generate a circos plot to visualize genomic differences.

---

## **Repository Contents**

### **Input Data**

- `PC_TAYLOR_cytobands_HIDS.csv` ➔ **Rename to**: `HCC_cytobands.csv`  
  *Cytoband data for HCC patients.*

- `PC_Taylor_Clinical_HIDSfinal.csv` ➔ **Rename to**: `HCC_clinical_data.csv`  
  *Clinical data for HCC patients.*

- `TopCytobandResults_HCC.csv`  
  *Results highlighting the top cytoband findings.*

- `hg19_cytoband.txt`  
  *Genomic location data for cytobands (hg19 human genome build).*

### **Output Data**

- `Aizhan_Uteubayeva_TopFeatures.tsv` ➔ **Rename to**: `HCC_top_features.tsv`  
  *Top features identified based on analysis.*

- `Aizhan_Uteubayeva_Circos.pdf.pdf` ➔ **Rename to**: `HCC_circos_plot.pdf`  
  *Circos plot visualizing genomic differences.*

- `Aizhan_Uteubayeva-TTestHW-06-Output.csv` ➔ **Rename to**: `HCC_ttest_results.csv`  
  *T-test results sorted by p-value.*

### **Data Checks**

- `Aizhan_Uteubayeva_ClinBaseIDs_HCC.tsv` ➔ **Rename to**: `clinical_baseline_group.tsv`  
  *Baseline group clinical data.*

- `Aizhan_Uteubayeva_ClinCompIDs_HCC.tsv` ➔ **Rename to**: `clinical_comparison_group.tsv`  
  *Comparison group clinical data.*

- `Aizhan_Uteubayeva_CopyNumBaseIDs_HCC.tsv` ➔ **Rename to**: `copynum_baseline_group.tsv`  
  *Baseline group copy number data.*

- `Aizhan_Uteubayeva_CopyNumCompIDs_HCC.tsv` ➔ **Rename to**: `copynum_comparison_group.tsv`  
  *Comparison group copy number data.*

- `Aizhan_Uteubayeva_FeatureIDs.csv` ➔ **Rename to**: `feature_ids.csv`  
  *List of feature IDs.*

- `Aizhan_Uteubayeva_FeatureIDs.tsv` ➔ **Rename to**: `feature_ids.tsv`  
  *Feature IDs in TSV format.*

- `Aizhan_Uteubayeva_checking.xlsx` ➔ **Rename to**: `id_checking.xlsx`  
  *Excel file for checking patient IDs.*

### **Scripts**

- `Aizhan-Uteubayeva-TTestHW-02-a-Code.Rmd.Rmd` ➔ **Rename to**: `HCC_ttest_analysis.Rmd`  
  *R Markdown script for the T-test analysis.*

- `Aizhan-Uteubayeva-TTestHW-02-b-Code.html` ➔ **Rename to**: `HCC_ttest_analysis.html`  
  *HTML output of the T-test analysis.*

---

## **Steps to Run Analysis**

1. **Check Data**: Verify consistency between clinical and copy number datasets.
2. **Data Preparation**: Clean and filter data to remove extraneous or junk rows.
3. **Group Identification**: Create subsets for comparison (vascular invasion: Yes vs. No).
4. **Statistical Analysis**: Conduct T-tests, calculate fold changes, and sort by p-values.
5. **Visualization**: Generate circos plots to visualize the genomic differences.
6. **Export Results**: Output the top features and analysis results.

---

## **How to Use**

1. Place the input data files in the `input/` folder.
2. Run the R Markdown script `HCC_ttest_analysis.Rmd` to reproduce the analysis.
3. Review the outputs in the `output/` and `datacheck/` folders.

---

## **Skills Demonstrated**

- **Bioinformatics Analysis**: Copy number analysis, differential feature identification.
- **Data Cleaning**: Ensuring dataset integrity and consistency.
- **Statistical Analysis**: Performing T-tests and interpreting results.
- **Data Visualization**: Creating circos plots to summarize findings.
- **Reproducible Research**: Documenting workflows in R Markdown.

---

## **Author**

**Aizhan Uteubayeva**  
*Initial analysis and documentation.*

## **License**

This project is released under the MIT License.
