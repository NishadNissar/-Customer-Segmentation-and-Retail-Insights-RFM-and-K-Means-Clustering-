# 🛍️ Customer Segmentation Using RFM Analysis and K-Means Clustering

This project focuses on segmenting customers for a chips retail business using **RFM (Recency, Frequency, Monetary)** analysis and **K-Means clustering**. By analyzing purchase behavior, we identify customer groups that help target marketing strategies more effectively.

---

## 📌 Objectives

- Analyze customer transaction behavior
- Identify valuable customer segments using RFM analysis
- Apply K-Means clustering for customer grouping
- Visualize customer segments and top-selling brands

---

## 📁 Dataset

The dataset (`QVI_transaction_data.xlsx`) includes:
- `Customer_ID`: Unique customer identifier
- `Transaction_ID`: Purchase transaction ID
- `Product_Description`: Item purchased
- `Spend`: Amount spent
- `Date`: Date of transaction

---

## ⚙️ Workflow

### 1. **Data Cleaning**
- Converted date columns to `datetime`
- Removed duplicates
- Checked for and handled missing values

### 2. **Feature Engineering**
- Extracted `Pack_Size` and `Brand` from product descriptions
- Calculated:
  - Total Spend per customer
  - Purchase Frequency
  - Average Spend per transaction
  - Preferred Brand and Pack Size

### 3. **RFM Analysis**
- **Recency**: Days since last purchase
- **Frequency**: Number of purchases
- **Monetary**: Total spend
- Data was grouped and RFM features were calculated

### 4. **Customer Segmentation**
- Applied `StandardScaler` to normalize RFM values
- Performed `KMeans` clustering with 4 clusters
- Assigned a segment label (0–3) to each customer

### 5. **Visualizations**
- 📊 `spend_by_brand.png`: Top brands by total spend
- 📈 `customer_segments.png`: Customer clusters plotted by Frequency and Monetary values

---

## 📂 Output Files

├── QVI_transaction_data.xlsx # Raw transaction dataset
├── spend_by_brand.png # Bar plot of brand-wise spending
├── customer_segments.png # Scatter plot of customer segments
└── customer_segmentation_rfm.py # Main Python script

yaml
Copy
Edit

---

## 📌 Key Insight

- **Segment 0** customers had a **Recency of 0**, meaning they made purchases on the **most recent day** in the dataset — likely your most engaged or loyal buyers.

---

## 🛠️ Tech Stack

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
