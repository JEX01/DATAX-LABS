## 📊 Feature Selection & Preprocessing

### 🗑️ Removed Attributes

| Attribute     | Reason                                          |
| ------------- | ----------------------------------------------- |
| ID            | Unique identifier; provides no predictive value |
| Z_CostContact | Constant value across all records               |
| Z_Revenue     | Constant value across all records               |

### ⚙️ Feature Engineering

| Original Attribute(s)     | Transformation                                         |
| ------------------------- | ------------------------------------------------------ |
| Year_Birth                | Converted to **Age**                                   |
| Income                    | Checked for missing values and outliers                |
| Education                 | Encoded into numerical categories                      |
| Marital_Status            | Encoded into numerical categories                      |
| Dt_Customer               | Converted into customer tenure (days since enrollment) |
| Kidhome + Teenhome        | Combined into **Total Children**                       |
| Mnt* columns              | Combined into **Total Spending**                       |
| Num* purchase columns     | Combined into **Total Purchases**                      |
| AcceptedCmp1–5 + Response | Combined into **Total Campaign Acceptance**            |

### 🎯 Key Features Used

* Age
* Income
* Total Children
* Recency
* Total Spending
* Total Purchases
* NumWebVisitsMonth
* Campaign Acceptance Count
* Complaint Status

---

## 🤖 Machine Learning Approaches

### Customer Segmentation (Unsupervised Learning)

* PCA + K-Means Clustering ⭐
* Hierarchical Clustering
* DBSCAN

**Recommended:** PCA + K-Means for identifying customer segments and purchasing behavior patterns.

### Campaign Response Prediction (Supervised Learning)

**Target Variable:** `Response`

Models evaluated:

* Random Forest
* XGBoost ⭐
* LightGBM
* Logistic Regression (Baseline)

**Recommended:** XGBoost due to its strong performance on structured customer datasets and ability to handle complex feature interactions.
