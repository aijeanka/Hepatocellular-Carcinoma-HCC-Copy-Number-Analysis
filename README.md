# **Hepatocellular Carcinoma (HCC) Copy Number Analysis**

## **Project Overview**

This repository contains an analysis of DNA copy number data for Hepatocellular Carcinoma (HCC) patients. The primary objective is to compare patients with and without vascular invasion to identify key genomic differences, focusing on chromosome instability and identifying top features derived from copy number data.

## **Data Description**

- **Clinical Data**: Clinical details for 198 patients, including those diagnosed with HCC and those at a pre-cancer stage (*“NON_TUMOR_CIRRHOTIC”*).
- **DNA Copy Number Data**: Chromosome instability (CINdex) values for 197 patients.

---

## **Analysis Goals**

1. **Group Comparison**: Compare copy number data between patients with vascular invasion (**Yes**) and those without (**No**).
2. **Feature Identification**: Identify statistically significant cytobands and genomic features associated with vascular invasion.
3. **Visualization**: Generate a circos plot to visualize genomic differences.

---

## **Repository Contents**

### **Input Data**

- **Cytoband Data**:  
  - `PC_TAYLOR_cytobands_HIDS.csv`  
  - `hg19_cytoband.txt`  

- **Clinical Data**:  
  - `PC_Taylor_Clinical_HIDSfinal.csv`  

- **Top Cytoband Results**:  
  - `TopCytobandResults_HCC.csv`  

### **Output Data**

- **Top Features**:  
  - `Aizhan_Uteubayeva_TopFeatures.tsv`  

- **Circos Plot**:  
  - `Aizhan_Uteubayeva_Circos.pdf.pdf`  

- **T-Test Results**:  
  - `Aizhan_Uteubayeva-TTestHW-06-Output.csv`  

### **Data Check Files**

- **Clinical Group IDs**:  
  - `Aizhan_Uteubayeva_ClinBaseIDs_HCC.tsv`  
  - `Aizhan_Uteubayeva_ClinCompIDs_HCC.tsv`  

- **Copy Number Group IDs**:  
  - `Aizhan_Uteubayeva_CopyNumBaseIDs_HCC.tsv`  
  - `Aizhan_Uteubayeva_CopyNumCompIDs_HCC.tsv`  

- **Feature IDs**:  
  - `Aizhan_Uteubayeva_FeatureIDs.csv`  
  - `Aizhan_Uteubayeva_FeatureIDs.tsv`  

- **ID Check**:  
  - `Aizhan_Uteubayeva_checking.xlsx`  

### **Scripts**

- **R Markdown Analysis**:  
  - `Aizhan-Uteubayeva-TTestHW-02-a-Code.Rmd.Rmd`  

- **HTML Output**:  
  - `Aizhan-Uteubayeva-TTestHW-02-b-Code.html`  

---

## **Steps to Run Analysis**

1. **Check Data Consistency**:  
   Verify alignment between clinical data and copy number data using files in the `datacheck/` directory.

2. **Load Data**:  
   Import clinical and copy number data from the `input/` directory.

3. **Clean and Filter Data**:  
   Ensure data integrity by removing any extraneous rows or inconsistencies.

4. **Group Identification**:  
   Identify patients with vascular invasion (Yes) and those without (No).

5. **Statistical Analysis**:  
   - Perform T-tests on copy number data.  
   - Calculate fold changes and q-values.  
   - Export results sorted by p-values.

6. **Visualization**:  
   Generate circos plots to visualize significant genomic differences.

7. **Export Results**:  
   Review outputs in the `output/` directory, including top features and visualizations.

---

## **How to Use**

1. **Place Input Data**: Ensure all input files are located in the `input/` directory.
2. **Run Analysis Script**: Execute `Aizhan-Uteubayeva-TTestHW-02-a-Code.Rmd.Rmd` to perform the analysis.
3. **Review Results**: Check the output files and visualizations in the `output/` directory.

---

## **Skills Demonstrated**

- **Bioinformatics Analysis**: Copy number analysis and differential feature identification.
- **Data Cleaning**: Ensuring dataset consistency and integrity.
- **Statistical Analysis**: Conducting T-tests and interpreting genomic data.
- **Data Visualization**: Generating circos plots to visualize genomic differences.
- **Reproducible Research**: Using R Markdown for workflow documentation.

---

## **Author**

**Aizhan Uteubayeva**  
*Initial analysis and documentation.*

## **License**

This project is released under the MIT License.
