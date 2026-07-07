# E-Commerce Shipping — Exploratory Data Analysis

A classic **data analytics EDA project** (Jupyter Notebook) analysing an
**e-commerce shipping** dataset of 10,999 orders. The central question is **what
makes a delivery arrive late**. This is the Python EDA companion to the original
**SQL** project — same data, analysed and visualised with pandas, matplotlib and
seaborn.

## 📓 What's inside

```
ecommerce-shipping-eda/
├─ Ecommerce_Shipping_EDA.ipynb   # the main notebook (run this)
├─ data/
│   ├─ Ecommerce_Shipping_Data.csv # the dataset (10,999 rows)
│   └─ original_sql_queries.sql    # the SQL from the original project
├─ requirements.txt
└─ README.md
```

## 🔎 What it covers

A standard end-to-end analysis workflow:

1. **Business understanding** — the questions we want to answer
2. **Data loading** — read the dataset
3. **Data inspection** — structure, dtypes, summary stats, missing values, duplicates
4. **Data cleaning & preparation** — rename the awkward target column, create a
   readable `Delivery_Status` (On Time / Late) plus a numeric `Late_Flag`, tidy
   categories, and bucket weight and discount into bands
5. **Exploratory Data Analysis**
   - Delivery Performance Overview (late rate KPIs, on-time vs late)
   - Logistics (warehouse block & shipment mode: volume and late rate)
   - Products, Weight & Discounts (distributions + late-rate drivers)
   - Customer Signals (care calls, prior purchases, rating, gender)
   - Correlation heatmap (which features drive lateness)
6. **Key insights** (computed from the data)
7. **Conclusion & recommendations**
8. **Future work**

Charts use **matplotlib** and **seaborn**: histogram, bar, pie, box plot and
heatmap.

## ⚠️ Important note on the target column

The target `Reached.on.Time_Y.N` is coded as **`1` = did NOT reach on time
(late)** and **`0` = reached on time**. The notebook decodes this into a clear
`Delivery_Status` label so the charts are easy to read.

## ⚙️ How to run

```bash
cd ecommerce-shipping-eda
pip install -r requirements.txt
jupyter notebook Ecommerce_Shipping_EDA.ipynb
```

Then in Jupyter: **Kernel → Restart & Run All** to execute every cell top to
bottom. (Also works in VS Code with the Jupyter extension, or in Google Colab —
just upload the `data/` folder too.)

## 🛠 Tech stack

Python · pandas · numpy · matplotlib · seaborn · Jupyter

## 📊 Example insights produced

- Overall late-delivery rate across all orders
- Late rate by warehouse block and shipment mode
- How discount level and shipment weight relate to lateness
- Customer-care-call and prior-purchase patterns
- Correlation of each numeric feature with late delivery
