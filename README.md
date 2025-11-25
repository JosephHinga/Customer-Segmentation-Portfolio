## 🌟 Customer Segmentation Using K-Means ### 

### 📌 Project Overview
This project applies unsupervised machine learning (K-Means clustering) to segment customers based on their spending score and annual income.

It demonstrates your ability to:
- Explore and clean data
- Build a clustering model
- Select the optimal number of clusters
- Visualize insights
- Translate technical results into business strategy
  
****

### 🧠 Business Problem ###
Businesses often struggle to understand diverse customer behavior.

Segmenting customers helps companies:
- Design personalized marketing campaigns
- Identify profitable groups
- Allocate resources wisely
- Improve customer retention

****


### 🔍 Data Description ###

| Column                 | Description                  |
| ---------------------- | ---------------------------- |
| CustomerID             | Unique customer identifier   |
| Gender                 | Male / Female                |
| Age                    | Age of customer              |
| Annual Income (k$)     | Income in thousands          |
| Spending Score (1–100) | How much the customer spends |

***

 ### 🛠️ Tools & Technologies Used ### 
- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn (KMeans)
- Jupyter Notebook

***
 ### Exploratory Data Analysis ### 
Your notebook includes:
- Distribution plots
- Age vs Spending analysis
- Gender comparisons
- Income vs Spending scatter

***
### 🧪 Model Building: K-Means Clustering
 ###  1️⃣ Prepare Data
 Selected features for clustering: 

       X = data[['Annual Income (k$)', 'Spending Score (1-100)']]

 ### 2️⃣ Determine Number of Clusters
Used the Elbow Method:

      inertia = []
     for k in range(1, 11):
         kmeans = KMeans(n_clusters=k)
         kmeans.fit(X)
        inertia.append(kmeans.inertia_)

### 3️⃣ Train Final Model
    kmeans = KMeans(n_clusters=5, random_state=42)
    labels = kmeans.fit_predict(X)

***
### 🧩 Cluster Insights (Personas)
 ### Cluster 0 — Standard Spenders
- Medium income
- Medium spending
- Respond to seasonal offers

### Cluster 1 — Premium Customers
- High income
- High spending
- Ideal segment for luxury product targeting

### Cluster 2 — High Income, Low Spend
- Wealthy but less engaged
- Opportunity for upselling

### Cluster 3 — Low Income, Low Spend
- Price-sensitive group
- Best for budget-focused promotions

### Cluster 4 — Low Income, High Spend
- Very engaged despite lower income
- Loyal customers with high lifetime value

***
### Future Improvements
- Add age as a third dimension (3D clustering)
- Use DBSCAN or hierarchical clustering for comparison
- Build an interactive dashboard with Streamlit
- Deploy as a web app
