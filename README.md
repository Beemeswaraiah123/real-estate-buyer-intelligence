# Machine Learning Based Buyer Segmentation and Investment Profiling for Real Estate Market Intelligence

## 📌 Project Overview

This project develops a **machine learning-based buyer segmentation and investment profiling system** for the real estate market.

The system analyzes buyer demographics, acquisition purposes, financing behavior, geographic information, satisfaction scores, and property transaction behavior to identify meaningful buyer segments.

The project uses **K-Means clustering** and **Hierarchical Clustering** to discover groups of buyers with similar characteristics. The results are presented through an interactive **Streamlit dashboard** for real estate market intelligence and decision-making.

---

## 🎯 Objectives

The main objectives of this project are:

- Identify distinct buyer segments using machine learning.
- Analyze buyer investment behavior.
- Understand the relationship between buyers and property transactions.
- Analyze loan usage and financing behavior.
- Identify geographic differences in buyer behavior.
- Profile buyer segments based on demographics and property activity.
- Provide interactive insights through a Streamlit dashboard.
- Support targeted marketing and real estate investment decisions.

---

## 📊 Dataset

The project uses two datasets:

### Clients Dataset

The buyer dataset contains information such as:

- `client_id`
- `client_type`
- `gender`
- `country`
- `region`
- `date_of_birth`
- `acquisition_purpose`
- `loan_applied`
- `referral_channel`
- `satisfaction_score`

### Properties Dataset

The property dataset contains information related to property transactions, including:

- Property/client reference
- Sale price
- Floor area
- Unit category
- Listing status
- Transaction information

The property data is linked to buyers using the client reference.

> **Note:** Original/raw client data should not be uploaded to a public GitHub repository if it contains personally identifiable or sensitive information.

---

## 🧠 Methodology

The project follows these major steps:

### 1. Data Cleaning

- Remove duplicate records.
- Clean categorical variables.
- Convert date fields.
- Calculate buyer age.
- Handle missing and invalid values.
- Clean property transaction information.

### 2. Feature Engineering

Buyer-level property features are created, including:

- Number of properties
- Number of sold properties
- Total property value
- Average property price
- Total area
- Average property area
- Sold property ratio

Additional behavioral indicators include:

- Investment buyer indicator
- Loan usage indicator
- Company buyer indicator

### 3. Exploratory Data Analysis

The project analyzes:

- Acquisition purpose
- Client type
- Loan behavior
- Country distribution
- Property values
- Buyer age
- Satisfaction scores
- Relationships between numerical variables

### 4. Data Preprocessing

Numerical variables are standardized using `StandardScaler`.

Categorical variables are converted using `OneHotEncoder`.

### 5. K-Means Clustering

K-Means clustering is used to identify groups of buyers with similar characteristics.

The optimal number of clusters is evaluated using:

- Elbow Method
- Silhouette Score

### 6. Hierarchical Clustering

Hierarchical clustering using Ward linkage is also applied to examine the structure of buyer groups.

### 7. Cluster Profiling

Each cluster is analyzed based on:

- Average age
- Average satisfaction
- Investment rate
- Loan rate
- Company buyer rate
- Number of properties
- Sold properties
- Average property value
- Average property price
- Property area
- Sold property ratio

---

## 📈 Buyer Segmentation

The system automatically interprets clusters based on observable buyer and property characteristics.

Possible segment interpretations include:

- **Company / Corporate Buyers**
- **Investment-Oriented Buyers**
- **Younger / Loan-Dependent Buyers**
- **High-Value Property Buyers**
- **General / Mixed Buyers**

The exact segment characteristics are determined from the machine learning results.

---

## 🖥️ Streamlit Dashboard

An interactive Streamlit dashboard is provided for exploring the machine learning results.

### Dashboard Features

#### 1. Buyer Segments

Displays:

- Buyer segment distribution
- Cluster sizes
- Buyer feature visualization
- Segment-level comparisons

#### 2. Investor Behavior

Displays:

- Acquisition purpose by cluster
- Loan behavior by cluster
- Average property value
- Average buyer age
- Behavioral summary

#### 3. Geographic Analysis

Displays:

- Buyers by country
- Global buyer distribution
- Regional buyer distribution
- Country and cluster analysis

#### 4. Segment Insights

Displays:

- Cluster profiles
- Buyer characteristics
- Investment behavior
- Loan behavior
- Property ownership behavior
- Suggested segment interpretations

---

## 🔎 Dashboard Filters

Users can interactively filter the dashboard by:

- Country
- Region
- Acquisition Purpose
- Client Type
- Cluster

The dashboard also provides an option to download filtered buyer data.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- SciPy
- Matplotlib
- Seaborn
- Plotly
- Streamlit
- Google Colab
- GitHub

---

## 📁 Project Structure

```text
real-estate-buyer-intelligence/
│
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
│
├── buyer_segmentation_results.csv
├── cluster_profile.csv
├── country_cluster_analysis.csv
└── region_cluster_analysis.csv
