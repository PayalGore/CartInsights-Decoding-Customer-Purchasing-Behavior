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

## 🔍 **Exploratory Data Analysis (EDA)**

### **1. Most Popular Aisles**
The plot below shows the **most popular aisles** based on the total number of products bought. Fresh fruits and vegetables dominate the list, indicating high demand for these categories.

<p align="center">
  <img width="600" height="300" src="https://github.com/manishdevdi/Instacart-Market-Basket-Analysis/blob/main/Plots/popular-aisles.png">
</p>

### **2. Reorder Percentage by Aisle**
The reorder percentage of **day-to-day food items** (e.g., fresh fruits, vegetables) is high, while items like vitamins, first-aid, and beauty products have a lower reorder percentage. This makes sense, as groceries are purchased regularly, while other items are bought less frequently.

<p align="center">
  <img width="400" height="220" src="https://github.com/manishdevdi/Instacart-Market-Basket-Analysis/blob/main/Plots/aisle-high-reorder.png"> 
  <img width="400" height="220" src="https://github.com/manishdevdi/Instacart-Market-Basket-Analysis/blob/main/Plots/aisle-low-reorder.png"> 
</p>

### **3. Popular Departments**
The plot below shows the **most popular departments**. The store layout should be designed so that popular departments (e.g., produce, dairy) are close to each other, improving the shopping experience.

<p align="center">
  <img width="600" height="300" src="https://github.com/manishdevdi/Instacart-Market-Basket-Analysis/blob/main/Plots/popular-departments.png">
</p>

### **4. Most Popular Products**
The plot below shows the **most popular products**. Interestingly, many of the top products are **organic**, suggesting a growing preference for organic items.

<p align="center">
  <img width="600" height="300" src="https://github.com/manishdevdi/Instacart-Market-Basket-Analysis/blob/main/Plots/Most-popular-products.png">
</p>

### **5. Organic vs. Inorganic Products**
While there are fewer organic products, their **mean reorder percentage** is higher than inorganic products. This suggests that customers who buy organic products are more loyal and likely to repurchase.

<p align="center">
  <img width="400" height="250" src="https://github.com/manishdevdi/Instacart-Market-Basket-Analysis/blob/main/Plots/Total-organic-inorganic-products.png">
  <img width="400" height="250" src="https://github.com/manishdevdi/Instacart-Market-Basket-Analysis/blob/main/Plots/Reorder-organic-inorganic-products.png">
</p>

### **6. Add-to-Cart Order vs. Reorder Percentage**
The plot below shows that products added to the cart earlier have a **higher reorder percentage**. This makes sense, as customers tend to prioritize essential items (e.g., milk, bread) over discretionary purchases.

<p align="center">
  <img width="600" height="300" src="https://github.com/manishdevdi/Instacart-Market-Basket-Analysis/blob/main/Plots/Add-to-cart-VS-reorder.png">
</p>

### **7. Reorder Percentage vs. Total Orders**
The plot below shows a **ceiling effect**: Many customers try a product once but do not reorder it. However, some products have a high reorder percentage, indicating strong customer loyalty.

<p align="center">
  <img width="600" height="300" src="https://github.com/manishdevdi/Instacart-Market-Basket-Analysis/blob/main/Plots/reorder-total-orders.png">
</p>

### **8. Cumulative Users per Product**
The plot below shows that **85% of users buy only 10,000 out of 49,688 products**. This insight can be used for **shelf space optimization**, focusing on high-demand products.

<p align="center">
  <img width="600" height="300" src="https://github.com/manishdevdi/Instacart-Market-Basket-Analysis/blob/main/Plots/cumsum_products.png">
</p>

---

## 🧑‍🤝‍🧑 **Customer Segmentation**
Using **K-Means clustering** on customer purchase data, we segmented customers into **5 distinct groups**:
1. **Fresh Veggie Lovers**: Customers who primarily buy fresh vegetables.
2. **Organic Enthusiasts**: Customers who prefer organic products.
3. **Frequent Shoppers**: Customers who buy a wide variety of products.
4. **Water Lovers**: Customers who frequently purchase sparkling water.
5. **Packaged Produce Buyers**: Customers who prefer packaged fruits and vegetables.

<p align="center">
  <img width="600" height="400" src="https://github.com/manishdevdi/Instacart-Market-Basket-Analysis/blob/main/Plots/cluster.png">
</p>

---

## 🛒 **Market Basket Analysis**
Using **association rule mining**, we identified **28 product pairs** with high lift (e.g., limes and large lemons). These insights can be used for **cross-selling** and **store layout optimization**.

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

---

## 🤖 **Predictive Modeling**
We built **XGBoost** and **Neural Network** models to predict product reorders, achieving an **AUC-ROC score of 0.85**. Key features included product popularity, customer behavior, and aisle/department trends.

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
