# 🧬 Breast Cancer Prediction Using NGS Data

This project predicts **breast cancer** using **Next Generation Sequencing (NGS)** data and a complete bioinformatics + machine learning pipeline — implemented entirely in a single Jupyter Notebook.

---

## 📁 Project Structure

| File/Folder                       | Description |
|----------------------------------|-------------|
| `MainProject.ipynb` | Main Jupyter Notebook (entire pipeline) |
| `sample_data/` *(optional)*      | Contains FASTQ, VCF, CSV samples (if included) 

---

## 🔬 Step-by-Step Pipeline

### 1. Data Acquisition
- Source: [NCBI SRA](https://www.ncbi.nlm.nih.gov/sra)
- Tool: `SRA Toolkit (fastq-dump)`

### 2. Quality Control & Preprocessing
- Tools: `FastQC`, `Trimmomatic`
- Actions: Adapter removal, quality trimming

### 3. Sequence Alignment
- Tools: `BWA` or `Bowtie2`, `SAMtools`
- Actions: Align to GRCh38, convert SAM to BAM, sort, and index

### 4. Variant Calling
- Tools: `SAMtools`, `BCFtools`
- Output: VCF files with SNPs & Indels

### 5. Variant Annotation
- Tools: `SnpEff` or `ANNOVAR`
- Focus: BRCA1, BRCA2, and other cancer-linked genes

### 6. Feature Extraction for ML
- Mutation presence/absence
- Gene-specific mutation counts
- Functional impact annotations

### 7. Machine Learning Model Development
- Tools: `pandas`, `scikit-learn`, `matplotlib`, `seaborn`
- Classifiers: Logistic Regression, Random Forest
- Metrics: Accuracy, Precision, Recall, F1-score

### 8. Results & Visualization
- Confusion matrix, ROC curve
- Feature importance analysis

### 9. Conclusion & Future Work
- Summarize findings
- Discuss limitations and future improvements

---

## 🛠 Tools & Libraries Used

| Bioinformatics Tools | ML Libraries |
|----------------------|--------------|
| SRA Toolkit, FastQC, Trimmomatic | pandas, numpy |
| Bowtie2 / BWA, SAMtools, BCFtools | scikit-learn |
| SnpEff / ANNOVAR | matplotlib, seaborn |

---

## 📌 Requirements

Install the Python dependencies:

```bash
pip install -r requirements.txt
