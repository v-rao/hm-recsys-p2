# 🛍️ H&M Personalized Fashion Recommendation System
H&amp;M RecSys to provide personalized fashion and product recommendations based on previous purchases. This repository contains a solution for the **H&M Group Personalized Fashion Recommendations** challenge, hosted on [Kaggle](https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations). The goal is to predict the most likely articles a customer will purchase in a 7-day period based on their transaction history, customer metadata, article metadata, product descriptions, and images.

## 🧠 Project Overview

With 53 online markets and nearly 4,850 stores, **H&M Group** offers a massive product catalog. However, customers may experience decision fatigue, leading to fewer purchases and increased returns. This project leverages historical purchases and metadata to recommend relevant products, improving both customer experience and sustainability by reducing returns and shipment-related emissions.

### ✨ Key Highlights
- Predict articles customers are most likely to purchase in the week following the training period.
- Utilize structured metadata, natural language product descriptions, and image data.
- Explore collaborative filtering, deep learning, and hybrid recommendation systems.

---

## 📁 Dataset

The dataset provided by H&M includes:

- **transactions_train.csv**: Transaction history, including customer ID, article ID, and timestamp.
- **articles.csv**: Metadata for each article (e.g., garment type, product type, department, etc.).
- **customers.csv**: Metadata about each customer (e.g., age, fashion news frequency, etc.).
- **images/**: Folder containing product images organized in subfolders based on article ID prefix.
- **sample_submission.csv**: Example of the required submission format.

> 🔒 **Note**: The dataset is large and only available to competition participants via Kaggle. Please download from the [Kaggle competition page](https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations) and place files in the appropriate directories.

---

## 📊 Exploratory Data Analysis (EDA)

The **EDA** phase helps uncover patterns, trends, and anomalies within the dataset, guiding feature engineering and model design. Given the rich variety of H&M data—transactions, customers, articles, and images—EDA was approached from multiple angles.

### 🔍 Steps Performed

1. **Data Overview**
   - Inspected dataset sizes, column names, and data types for:
     - `transactions_train.csv`
     - `articles.csv`
     - `customers.csv`
   - Checked for missing values, duplicates, and inconsistencies.

2. **Transactions Analysis**
   - Measured purchase frequency per customer.
   - Explored temporal trends (daily, weekly, and seasonal patterns).
   - Identified top-selling articles overall and within customer groups.
   - Analyzed repeat purchases for the same article.

3. **Customer Insights**
   - Visualized distributions for age, membership status, and fashion news frequency.
   - Segmented customers into activity levels based on purchase history.
   - Examined relationships between demographics and buying patterns.

4. **Article Metadata Exploration**
   - Analyzed garment group, product type, department, and section distributions.
   - Explored price variation across categories.
   - Processed product descriptions for keyword frequency and patterns.

5. **Image Data Insights**
   - Verified the proportion of articles with available product images.
   - Conducted visual checks to confirm metadata-image consistency.

6. **Cross-Table Analysis**
   - Merged transactions with articles and customers for richer insights.
   - Studied correlations between customer preferences and product attributes.

7. **Data Quality Checks**
   - Flagged unrealistic values (e.g., extreme ages).
   - Validated date ranges and article IDs.

### 📈 Key Outcomes
- Identified high-value features for model training (e.g., garment group, price, seasonality).
- Detected purchase seasonality patterns for temporal modeling.
- Highlighted data cleaning needs before modeling.
- Better understanding of customer-product relationships for recommendation strategies.


## 🧰 Features & Tools

This project includes the following methodologies:

- **Collaborative Filtering** with matrix factorization
- **Content-Based Filtering** using article metadata
- **NLP** on product descriptions using Transformer models
- **Image Embeddings** using pretrained CNNs (e.g., ResNet, EfficientNet)
- **Hybrid Modeling** combining user behavior, text, and images
- **Candidate Generation + Ranking Pipeline** for efficient recommendation

---

## 📊 Evaluation Metric

The competition uses **Mean Average Precision at 12 (MAP@12)** as the evaluation metric. Only customers who made purchases during the prediction week are evaluated.

---

## 🧪 Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/hm-fashion-recommendation.git
   cd hm-fashion-recommendation
