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

* Built an end-to-end EDA and predictive pipeline across **93,358 customers** and **96,478 delivered orders**
* Engineered a **Logistic Regression** repeat-purchase classifier achieving **0.592 AUC**
* Executed **chi-square significance tests** ruling out review score (`p=0.32`) and delivery delay (`p=0.06`) as churn catalysts
* Uncovered the repeat-buyer Average Order Value compression (**R$146 vs R$161**)

#### SQL Highlights

* Engineered a multi-table relational pipeline joining **orders, customers, items, and payments** across 93,358 delivered-order customers
* Built **RFM decile segmentation** using `NTILE()` and `RANK()` window functions
* Isolated revenue concentration showing the **top 20% cohort drives 53.5%** of platform revenue

#### Power BI Dashboard

* **Executive retention dashboard** powered by **4 custom DAX measures**
* **Expected-LTV matrix** highlighting top-tier customer revenue concentration (53.5%)
* **Cohort retention heatmap** incorporating an explicit **right-censoring flag** to prevent distorted tail metrics
* **Geographic repeat-rate map** across **27 Brazilian states** paired with a dynamic **revenue-at-risk table**

#### Excel Modeling

* Built a **What-If Analysis revenue model** simulating retention lift scenarios
* Quantified that increasing repeat-purchase conversion from **3.00% to 5.00%** (~1,867 customers) yields **+R$276K** in annual incremental revenue

---

### Dataset

**[Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)**  
Source: Kaggle (Uploaded by *Olist*)  
Scope: Relational e-commerce dataset covering 96,478 delivered orders, 93,358 unique customers, order payments, items, and customer reviews across 27 states.

---

### Key Business Recommendation

Shift retention budget away from broad post-delivery service recovery—since neither review scores nor delivery delays drive churn—and deploy targeted second-order incentives aimed at converting **~1,867 high-potential first-time buyers**. Lifting repeat conversion from **3.00% to 5.00%** captures **+R$276K in annual incremental revenue** while protecting the top 20% customer tier generating over half of platform sales.
