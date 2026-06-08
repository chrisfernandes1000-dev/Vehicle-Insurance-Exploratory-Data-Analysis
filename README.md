# Vehicle-Insurance-Exploratory-Data-Analysis
data analysis project showcasing EDA on vehicle insurance customer data using python

# EDA on Vehicle Insurance Customer Data

## Overview

This project performs Exploratory Data Analysis (EDA) on vehicle insurance customer data using Python. The goal is to understand customer demographics, vehicle details, and insurance behaviour — and to extract meaningful insights that can help an insurance company identify potential customers for cross-selling vehicle insurance policies.

---

## Dataset

Two CSV files are used in this project:

| File | Description |
|---|---|
| `customer_details.csv` | Contains customer demographic and vehicle information |
| `customer_policy_details.csv` | Contains policy-related information such as annual premium and customer response |

**Key columns:**

- `customer_id` — Unique identifier for each customer
- `gender` — Customer's gender
- `age` — Customer's age
- `driving_licence_presence` — Whether the customer holds a driving licence
- `region_code` — Region of the customer
- `previously_insured` — Whether the customer already has vehicle insurance
- `vehicle_age` — Age of the vehicle
- `vehicle_damage` — Whether the vehicle was previously damaged
- `annual_premium_INR` — Annual premium amount (in INR)
- `sales_channel_code` — Channel through which the customer was contacted
- `vintage` — Number of days the customer has been associated with the company
- `response` — Whether the customer is interested in vehicle insurance (target variable)

---

## Tools & Libraries

- **Python 3**
- **Pandas** — data loading, cleaning, and manipulation
- **Matplotlib** — data visualization
- **Jupyter Notebook** — interactive development environment

---

## Steps Performed

**1. Data Loading**
- Loaded two separate CSV files (`customer_details.csv` and `customer_policy_details.csv`) using Pandas.

**2. Data Cleaning**
- Identified and handled null values:
  - Dropped rows with missing `customer_id`
  - Filled missing numeric columns with **column mean**
  - Filled missing categorical columns with **column mode**
- Detected and treated outliers using the **IQR (Interquartile Range)** method — outlier values replaced with column mean.
- Removed leading/trailing whitespaces from string columns.
- Standardized text to lowercase for consistency.
- Dropped duplicate rows from both tables.

**3. Data Merging**
- Merged the two cleaned tables on `customer_id` to create a single master dataset.
- Renamed columns for clarity and readability.

**4. Exploratory Data Analysis**
- Calculated **gender-wise average annual premium**.
- Analysed **age-wise average annual premium** with a line plot.
- Checked **gender balance** in the dataset using male-to-female ratio.
- Analysed **vehicle-age-wise average annual premium**.
- Measured the **correlation between customer age and annual premium** to identify any linear relationship.

---

## Key Findings

- The dataset is slightly imbalanced in terms of gender distribution.
- Annual premium varies significantly across different vehicle age groups.
- There is no strong linear correlation between a customer's age and their annual premium.
- Customers with previously damaged vehicles show higher interest in insurance, indicating a key target segment.

---

## How to Run

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/eda-vehicle-insurance.git
   cd eda-vehicle-insurance
   ```

2. **Install required libraries:**
   ```bash
   pip install pandas matplotlib jupyter
   ```

3. **Place the dataset files** (`customer_details.csv` and `customer_policy_details.csv`) in the project folder.

4. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```

5. Open `EDA__on_vehicle_insurance_customer_data.ipynb` and run all cells sequentially.

---

## Project Structure

```
eda-vehicle-insurance/
│
├── EDA__on_vehicle_insurance_customer_data.ipynb   # Main notebook
├── customer_details.csv                             # Customer demographic data
├── customer_policy_details.csv                      # Policy data
└── README.md
```

---


**Your Name**
[LinkedIn](https://linkedin.com/in/your-profile) | [GitHub](https://github.com/your-username)
