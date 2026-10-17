# India E-Commerce Sales & Delivery Analytics

---

## 📌 Week Number & Objective

- **Week Number:** Week 1
- **Objective:** Ingest raw e-commerce transaction data, execute comprehensive data cleaning and preprocessing pipelines, conduct exploratory data analysis (EDA) to uncover sales and operational patterns, and build an interactive Power BI dashboard with visual reporting assets.

---

## 📂 Dataset Description

The project processes Indian retail e-commerce transactional data tracked across two stages:

- **Raw Data (`data/raw/ecommerce_india_raw_data.csv`):** Unprocessed transaction logs containing customer orders, order dates, product categories, quantities, unit prices, delivery statuses, payment modes, and geographical distribution across Indian states.
- **Cleaned Data (`data/cleaned/cleaned_ecommerce_data.csv`):** Cleaned, normalized dataset with imputed/removed missing values, standardized date formatting (`YYYY-MM`), verified numeric constraints (quantity, price, total amount), and categorical alignment.

---

## 🛠️ Tools & Libraries Used

- **Programming Language:** Python 3.8+
- **Data Manipulation & Analysis:** `pandas`, `numpy`
- **Data Visualization:** `matplotlib`, `seaborn`
- **Interactive Development:** Jupyter Notebook
- **Business Intelligence & Reporting:** Microsoft Power BI Desktop

---

## ⚙️ Key Steps Performed

1. **Data Ingestion & Quality Assessment:** Inspected raw schemas, verified column types, identified missing values, duplicated entries, and inconsistent data entries.
2. **Data Cleaning & Preprocessing:**
   - Handled missing and anomalous data points across order records.
   - Standardized order date fields and derived temporal attributes (`Year-Month`, day of week).
   - Validated derived financial columns such as `Total Amount = Quantity * Unit Price`.
   - Exported the finalized data directly to `data/cleaned/cleaned_ecommerce_data.csv`.
3. **Exploratory Data Analysis (EDA):**
   - Computed summary statistics on order quantities, sales volume, and order sizes.
   - Grouped sales distributions by product category to pinpoint top revenue drivers.
   - Analyzed monthly order quantity trends over time.
   - Assessed logistics and fulfillment efficiency across delivery status segments.
4. **Dashboard Development:**
   - Imported the cleaned dataset into Microsoft Power BI.
   - Designed KPI summary cards, distribution charts, and interactive categorical filters.
   - Exported visual reports to high-resolution PNG charts and compiled the `.pbix` report.

---

## 📈 Major Findings

- **Top Revenue Categories:** Product categories such as Electronics and Fashion account for the highest proportion of total sales value (`sum_of_totalamount_byCat_bar.png`).
- **Delivery Fulfillment Ratio:** Over **70%** of all orders reached **Delivered** status successfully, with the remainder distributed across **Shipped**, **Pending**, and minimal **Cancelled/Returned** orders (`sum_of_quantity_byDS_pie.png`).
- **Monthly Demand Trajectory:** The monthly sales volume chart (`sum_of_quantity_byYM_line.png`) demonstrates distinct demand peaks, highlighting strong festive and seasonal purchase surges in the Indian retail cycle.
- **Basket Size Distribution:** The vast majority of retail transactions consist of smaller basket quantities (1 to 3 items per order), pointing toward frequent, low-quantity purchasing behavior.

---

## 📁 Folder Structure

```plaintext
week1_submission/
│
├── data/
│   ├── raw/
│   │   └── ecommerce_india_raw_data.csv       # Raw unprocessed transaction data
│   └── cleaned/
│       └── cleaned_ecommerce_data.csv         # Cleaned, validated dataset
│
├── outputs/
│   ├── charts/                                # Exported exploratory visual charts
│   │   ├── sum_of_quantity.png                # Distribution of order quantities
│   │   ├── sum_of_quantity_byDS_pie.png       # Quantity share by delivery status
│   │   ├── sum_of_quantity_byYM_line.png      # Monthly quantity sales trajectory
│   │   └── sum_of_totalamount_byCat_bar.png   # Total sales amount by product category
│   │
│   └── dashboard/
│       ├── dashboard.png                      # Power BI dashboard export
│       └── Week1 Dashboard 1.pbix             # Dynamic Power BI dashboard file
│
├── reports/
│   └── week1_analysis (1).ipynb               # Primary Jupyter Notebook for EDA & cleaning
│
├── screenshots/                               # Project screenshots & visual assets
├── requirements.txt                           # Python package dependencies
└── README.md                                  # Project documentation

```

---

## 🚀 Execution Instructions

### 1. Set Up Environment

Ensure you have Python 3.8 or above installed on your system. Navigate to your project root folder:

```bash
cd "week1_submission (1)"

```

### 2. Install Dependencies

Install all required libraries using the provided `requirements.txt`:

```bash
pip install -r requirements.txt

```

### 3. Run EDA & Data Cleaning

Launch Jupyter Notebook to execute the data processing pipeline:

```bash
jupyter notebook "reports/week1_analysis (1).ipynb"

```

*Run all cells sequentially to regenerate the cleaned data file and analytical plots.*

### 4. View Power BI Dashboard

1. Install and launch **Microsoft Power BI Desktop**.
2. Open the dashboard file located at:
```plaintext
outputs/dashboard/Week1 Dashboard 1.pbix

```


3. If prompted to refresh data sources, verify the source points to `data/cleaned/cleaned_ecommerce_data.csv`.

---

## 👤 Author Details

* **Name:** Vedant Gadade
* **Role:** Data Science & Analytics Intern
* **Week:** Week 1 Submission
* **Email:** vgadade1008@gmail.com


```

```