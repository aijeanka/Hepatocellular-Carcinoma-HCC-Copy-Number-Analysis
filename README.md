# **Hepatocellular Carcinoma (HCC) Copy Number Analysis**

## **Project Overview**

This repository contains data, code, and results for a bioinformatics study analyzing DNA copy number data in Hepatocellular Carcinoma (HCC) patients. The goal is to identify key genomic differences between patients with and without vascular invasion, focusing on chromosome instability and identifying significant cytobands and genomic features.

---

## **Highlights**

- **Packages Used**:  
  - `tidyverse` – Data manipulation and visualization  
  - `dplyr` – Data filtering and wrangling  
  - `ggplot2` – Data visualization  
  - `circlize` – Generating circos plots  
  - `knitr` – Reproducible report generation  

- **Code**:  
  R Markdown script for data cleaning, statistical analysis, and visualization.

- **Reproduced Figures**:  
  - Circos plots showing genomic differences  
  - Top features identified through T-tests  

---

## **Repository Organization**

For improved reproducibility and clarity, the repository is organized as follows:

```
HCC_CopyNumber_Analysis/
│
├── data/                        # Raw and processed data files
│   ├── PC_TAYLOR_cytobands_HIDS.csv
│   ├── hg19_cytoband.txt
│   └── PC_Taylor_Clinical_HIDSfinal.csv
│
├── analysis/                    # Scripts and compiled reports
│   ├── Aizhan-Uteubayeva-TTestHW-02-a-Code.Rmd.Rmd
│   └── Aizhan-Uteubayeva-TTestHW-02-b-Code.html
│
├── output/                      # Results and visualization outputs
│   ├── Aizhan_Uteubayeva_TopFeatures.tsv
│   ├── Aizhan_Uteubayeva_Circos.pdf.pdf
│   └── Aizhan_Uteubayeva-TTestHW-06-Output.csv
│
├── datacheck/                   # Data consistency check files
│   ├── Aizhan_Uteubayeva_ClinBaseIDs_HCC.tsv
│   ├── Aizhan_Uteubayeva_ClinCompIDs_HCC.tsv
│   ├── Aizhan_Uteubayeva_CopyNumBaseIDs_HCC.tsv
│   ├── Aizhan_Uteubayeva_CopyNumCompIDs_HCC.tsv
│   ├── Aizhan_Uteubayeva_FeatureIDs.csv
│   ├── Aizhan_Uteubayeva_FeatureIDs.tsv
│   └── Aizhan_Uteubayeva_checking.xlsx
│
└── README.md                    # Project documentation
```

---

## **Methodology**

### **Step 1: Data Import**

- **Clinical Data**: `PC_Taylor_Clinical_HIDSfinal.csv`  
  - Contains clinical details for 198 patients, including vascular invasion status.  

- **Cytoband Data**: `PC_TAYLOR_cytobands_HIDS.csv` and `hg19_cytoband.txt`  
  - Cytoband and genomic location data for chromosome analysis.  

**Code Example**:  
```r
clinData <- read.csv("data/PC_Taylor_Clinical_HIDSfinal.csv")
cytobandData <- read.csv("data/PC_TAYLOR_cytobands_HIDS.csv")
```

### **Step 2: Data Cleaning and Transformation**

- **Filter Clinical Data**: Select patients with and without vascular invasion.  
- **Filter Copy Number Data**: Ensure consistency with clinical data and remove extraneous rows.  

**Outputs**:  
- `datacheck/Aizhan_Uteubayeva_ClinBaseIDs_HCC.tsv`  
- `datacheck/Aizhan_Uteubayeva_ClinCompIDs_HCC.tsv`  

### **Step 3: Group Identification**

- **Groups**:  
  - Patients with vascular invasion (**Yes**)  
  - Patients without vascular invasion (**No**)  

**Code Example**:  
```r
baselineGroup <- clinData[clinData$Vascular_Invasion == "No", ]
comparisonGroup <- clinData[clinData$Vascular_Invasion == "Yes", ]
```

### **Step 4: Statistical Analysis**

- **Perform T-Tests**: Compare copy number data between the two groups.  
- **Identify Significant Features**: Export T-test results with p-values and fold changes.  

**Outputs**:  
- `output/Aizhan_Uteubayeva-TTestHW-06-Output.csv`: Full T-test results.  
- `output/Aizhan_Uteubayeva_TopFeatures.tsv`: Top features based on p-values.

### **Step 5: Visualization**

- **Generate Circos Plot**: Visualize genomic differences between the groups.  

**Output**:  
- `output/Aizhan_Uteubayeva_Circos.pdf.pdf`: Circos plot showing significant genomic features.

---

## **Steps to Run Analysis**

1. **Set Up Environment**:  
   Install the required R packages:  
   ```r
   install.packages(c("tidyverse", "dplyr", "ggplot2", "circlize", "knitr"))
   ```

2. **Clone the Repository**:  
   ```bash
   git clone https://github.com/yourusername/HCC_CopyNumber_Analysis.git
   cd HCC_CopyNumber_Analysis
   ```

3. **Prepare Data**:  
   Ensure all input files are placed in the `data/` directory.

4. **Run Analysis Script**:  
   Execute the R Markdown script:  
   ```r
   rmarkdown::render("analysis/Aizhan-Uteubayeva-TTestHW-02-a-Code.Rmd.Rmd")
   ```

5. **View Results**:  
   - **HTML Report**: `analysis/Aizhan-Uteubayeva-TTestHW-02-b-Code.html`  
   - **Top Features**: `output/Aizhan_Uteubayeva_TopFeatures.tsv`  
   - **Circos Plot**: `output/Aizhan_Uteubayeva_Circos.pdf.pdf`

---

## **Skills Demonstrated**

- **Bioinformatics Analysis**: Copy number variation analysis, differential feature identification.  
- **Data Cleaning**: Ensuring alignment between clinical and genomic datasets.  
- **Statistical Analysis**: T-tests, p-value calculation, and feature extraction.  
- **Data Visualization**: Generating circos plots and summarizing results.  
- **Reproducible Research**: Using R Markdown to document workflows.

---

## **Author**

**Aizhan Uteubayeva**  
*Initial analysis and documentation.*

---

## **License**

This project is licensed under the **MIT License**. See the `LICENSE` file for details.
