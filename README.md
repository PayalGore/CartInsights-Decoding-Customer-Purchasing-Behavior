# CartInsights: Decoding Customer Purchasing Behavior

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-3776AB?style=for-the-badge&logo=xgboost&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white)

**CartInsights** is a data-driven project that uncovers the secrets behind customer purchasing behavior. By analyzing **3 million grocery orders** from **200,000 Instacart users**, this project provides actionable insights to optimize product recommendations, improve inventory management, and enhance customer segmentation.

---

## 🚀 **Project Overview**
The goal of **CartInsights** is to decode customer purchasing patterns and provide actionable insights for businesses. Using **transactional data**, this project applies **data science techniques** to:
- Identify **frequently bought-together products**.
- Segment customers based on their **buying habits**.
- Predict **future purchases** using machine learning models.

---

## 📂 **Dataset**
The dataset includes:
- **order_products_prior.csv**: Prior orders of users.
- **orders.csv**: Order metadata.
- **products.csv**: Product details.
- **aisles.csv**: Aisle details.
- **departments.csv**: Department details.

---

## 🔍 **Key Insights**
### **1. Popular Products and Aisles**
- Identified the **most popular aisles and products** (e.g., fresh fruits, organic items).
- Discovered that **organic products** have a higher reorder percentage, suggesting a growing demand.

<p align="center">
  <img width="600" height="300" src="https://github.com/manishdevdi/Instacart-Market-Basket-Analysis/blob/main/Plots/popular-aisles.png">
</p>

### **2. Customer Segmentation**
- Segmented customers into **5 distinct groups** using **K-Means clustering**:
  - **Fresh Veggie Lovers**: Customers who primarily buy fresh vegetables.
  - **Organic Enthusiasts**: Customers who prefer organic products.
  - **Frequent Shoppers**: Customers who buy a wide variety of products.
  - **Water Lovers**: Customers who frequently purchase sparkling water.
  - **Packaged Produce Buyers**: Customers who prefer packaged fruits and vegetables.

<p align="center">
  <img width="600" height="400" src="https://github.com/manishdevdi/Instacart-Market-Basket-Analysis/blob/main/Plots/cluster.png">
</p>

### **3. Market Basket Analysis**
- Applied **association rule mining** to identify **28 product pairs** with high lift (e.g., limes and large lemons).
- Provided recommendations for **cross-selling** and **store layout optimization**.

| Product A  | Product B | Lift |
| ------------- | ------------- | ---- |
| Limes  | Large Lemons  | 3 |
| Organic Strawberries | Organic Raspberries | 2.21 |
| Organic Avocado | Large Lemon | 2.12 |
| Organic Strawberries | Organic Blueberries | 2.11 |
| Organic Hass Avocado | Organic Raspberries | 2.08 |
| Banana | Organic Fuji Apple | 1.88 |
| Bag of Organic Bananas | Organic Raspberries | 1.83 |
| Organic Hass Avocado | Bag of Organic Bananas | 1.81 |
| Honeycrisp Apple | Banana | 1.77 |
| Organic Avocado | Organic Baby Spinach | 1.70 |

### **4. Predictive Modeling**
- Built **XGBoost** and **Neural Network** models to predict product reorders, achieving an **AUC-ROC score of 0.85**.
- Extracted **key features** such as product popularity, customer behavior, and aisle/department trends.

<p align="center">
  <img width="600" height="300" src="https://github.com/manishdevdi/Instacart-Market-Basket-Analysis/blob/main/Plots/XGBoost%20Performance.png">
</p>

---

## 🛠️ **Tools and Technologies**
- **Programming Languages**: Python (Pandas, NumPy, Matplotlib, Seaborn)
- **Machine Learning**: Scikit-Learn, XGBoost, TensorFlow (Neural Networks)
- **Data Analysis**: SQL, PCA, K-Means Clustering, Association Rule Mining (Apriori)
- **Visualization**: Matplotlib, Seaborn, Tableau (optional)

---

## 📊 **Business Impact**
- **Optimized Store Layout**: Identified popular aisles and departments to improve product placement.
- **Enhanced Cross-Selling**: Discovered product pairs with high lift for targeted promotions.
- **Improved Inventory Management**: Analyzed reorder patterns to prioritize high-demand products.
- **Personalized Marketing**: Segmented customers to tailor marketing strategies.

---

## 🚀 **Future Improvements**
- Implement **deep learning-based recommendation models**.
- Analyze **seasonal trends** in purchases.
- Integrate with **real-time transaction data** for live recommendations.

---

## ⚙️ **Installation & Setup**
1. Clone the repository:
   ```bash
   git clone https://github.com/manishdevdi/Instacart-Market-Basket-Analysis.git
   cd CartInsights
