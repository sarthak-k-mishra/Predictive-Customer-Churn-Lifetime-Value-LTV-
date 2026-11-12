# Predictive Customer Churn & Lifetime Value (LTV)

**End-to-End Analytics Pipeline | Python · SQL · Power BI · Excel**

---

### Business Problem

E-commerce platforms often lose significant revenue to high single-order churn without knowing whether customer drop-off is driven by operational friction or structural buying behavior. The objective was to diagnose the root causes of a 97% baseline churn rate across 93,358 customers, segment high-value cohorts using RFM modeling, and quantify the revenue upside of targeted retention strategies.

---

### Key Findings

* **97% baseline churn rate** is structurally driven rather than operational—chi-square hypothesis testing statistically ruled out review scores (`p = 0.32`) and delivery delays (`p = 0.06`) as primary churn drivers

* **Counter-intuitive AOV drop** discovered among repeat buyers, spending **R$146** on average compared to **R$161** for one-time purchasers

* **Top 20% of customers generate 53.5% of total platform revenue**, identified through SQL-based RFM decile segmentation

* **+R$276K projected annual incremental revenue** unlocked by lifting the repeat-purchase rate from **3.00% to 5.00%** (~1,867 converted customers)

* **Logistic Regression repeat-purchase model** achieved a baseline **0.592 AUC**, establishing a statistical benchmark for behavioral churn prediction

<br>

### Power BI Executive Retention Dashboard<img width="1162" height="656" alt="image" src="https://github.com/user-attachments/assets/ade9cdf7-a30b-441f-b6c8-a7554f1bd920" />


---

### Tools & Technologies

| Tool | Purpose |
| :--- | :--- |
| Python (Pandas, Scikit-learn, SciPy) | EDA, chi-square testing, Logistic Regression |
| SQL (CTEs, Window Functions) | Relational joins, RFM decile segmentation |
| Power BI (DAX) | Executive retention & LTV dashboard |
| Excel (What-If Analysis) | Retention sensitivity & revenue modeling |

---

### Project Structure

#### Python Analysis Highlights

* Built an end-to-end EDA and predictive pipeline across **93,358 customers** and **96,478
