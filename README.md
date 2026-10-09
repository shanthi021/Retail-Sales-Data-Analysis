# Retail Sales Data Analysis and Visualization Using Python

**Student:** Kalyanam Shanthi Priya  
**Email:** kalyanamshanthipriya021@gmail.com  
**Degree:** B.Tech Information Technology  
**Institution:** Mohan Babu University, Tirupati, Andhra Pradesh, India  
**Internship:** AICTE | IBM SkillsBuild Data Analytics with AI Internship 2026

## Project overview
This beginner-friendly project analyzes historical online retail transactions using Python, pandas, NumPy, Matplotlib, Seaborn, and Jupyter Notebook. It covers data quality, transaction value, product performance, monthly trends, country-level performance, customer activity, and evidence-based recommendations.

## Problem statement
Retail transaction records can contain duplicate rows, missing customer identifiers, cancellations, returns, and unusual values. The project provides a reproducible workflow to assess these issues and summarize historical transaction patterns without presenting descriptive statistics as profit or causal evidence.

## Objectives
- Inspect and clean transaction data transparently.
- Calculate positive transaction value and net transaction value.
- Identify products ranked highly by transaction value and units.
- Visualize monthly and country-level patterns.
- Examine customer purchase activity where IDs are present.
- Save charts and computed summary tables for documentation.
- Provide business recommendations grounded in the computed outputs.

## Dataset
**Name:** Online Retail  
**Official source:** https://archive.ics.uci.edu/dataset/352/online+retail  
**Citation:** Chen, D. (2015). *Online Retail* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5BW33.  
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0); provide attribution when using/adapting the dataset.

The dataset records transactions from a UK-based online retailer between December 2010 and December 2011. Columns include invoice number, product code, description, quantity, invoice date, unit price in GBP, customer ID, and country. Cancellation invoices may start with `C`; negative quantities may represent returns. Profit, discount, and product category fields are not available.

## Project folder structure
```text
Retail-Sales-Data-Analysis/
├── KalyanamShanthiPriya_RetailSalesAnalysis.ipynb
├── requirements.txt
├── KalyanamShanthiPriya_ProjectReport.docx
├── README.md
├── data/
│   └── README.md
└── outputs/
    └── .gitkeep
```

## Prerequisites
- Windows 10/11
- Python 3.10 or newer (64-bit recommended)
- VS Code with the Python and Jupyter extensions, or Jupyter Notebook
- Internet access to download the dataset once

## Installation (Windows PowerShell)
Open PowerShell in this project folder:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

If PowerShell blocks activation, use Command Prompt and run:
```bat
.venv\Scripts\activate.bat
```

## Download and place the dataset
1. Open the official UCI page: https://archive.ics.uci.edu/dataset/352/online+retail
2. Download `Online Retail.xlsx`.
3. Open the file in Microsoft Excel.
4. Choose **File → Save As** and select **CSV UTF-8 (Comma delimited)**.
5. Save the CSV as `Online Retail.csv` inside the `data` folder.

Expected path:
`data/Online Retail.csv`

The original dataset is not included in this repository. This keeps the repository lightweight and makes the data source and license clear.

## Run the notebook
```powershell
python -m jupyter notebook
```
Open `KalyanamShanthiPriya_RetailSalesAnalysis.ipynb` and select **Kernel → Restart Kernel and Run All Cells**. Alternatively, open the project folder in VS Code and run the notebook cells from top to bottom.

## Analysis features
- Data preview, shape, data types, descriptive statistics, missing values, duplicates
- Date and numeric type conversion
- Transaction value calculation
- Handling of cancellations, negative quantities, and non-positive prices
- Monthly transaction value chart
- Top products by net transaction value and positive units sold
- Country-level performance
- Customer summaries for known customer IDs
- Correlation heatmap for numeric transaction fields
- Computed findings and exported tables/charts

Generated outputs are saved under `outputs/`. Values are computed from the local dataset at runtime; this README does not claim unverified results.

## Findings
**Pending execution:** Run all notebook cells with the downloaded dataset to produce verified findings. The notebook writes `outputs/computed_findings.md` and summary CSV files. Use those outputs to complete the Results and Findings section of the Word report. Do not submit invented metrics.

## Data handling and limitations
- Missing customer IDs are retained for overall transaction analysis but excluded from customer-level summaries.
- Exact duplicates and rows with missing dates/quantity/prices are removed from the analysis table.
- Negative quantities are retained for net transaction-value calculations.
- Non-positive unit-price rows are excluded from primary sales-value analysis and counted separately.
- Outliers are flagged for review, not automatically removed.
- The dataset is historical; results should not be described as current business performance.
- No profit, discount, cost, or shipping columns are available.
- Customer-level conclusions are limited by missing IDs and the observed time window.

## Future scope
- Compare a seasonal-naive forecast with a time-series model using chronological validation.
- Build an interactive dashboard in Power BI, Tableau, or Plotly.
- Add profit and discount analysis if a suitable licensed dataset with those fields is selected.
- Add market basket analysis if product-level invoice baskets are studied carefully.

## Author
**Kalyanam Shanthi Priya**  
B.Tech Information Technology, Mohan Babu University, Tirupati, Andhra Pradesh, India  
Email: kalyanamshanthipriya021@gmail.com

## References
- Chen, D. (2015). *Online Retail* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5BW33
- UCI dataset page: https://archive.ics.uci.edu/dataset/352/online+retail
- pandas: https://pandas.pydata.org/docs/
- NumPy: https://numpy.org/doc/
- Matplotlib: https://matplotlib.org/stable/
- Seaborn: https://seaborn.pydata.org/

## License
The dataset is licensed CC BY 4.0 by its source; provide attribution. This project code and documentation are provided for educational use. Check your institution's submission rules before redistributing or publishing any dataset content.
