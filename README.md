# Customer Segmentation Model

## Project Overview
This project segments customers based on their purchasing behaviors using **K-Means clustering** and then classifies new customer data into these segments using a **Decision Tree classifier**.  
It also includes a **Streamlit web app** that allows users to input customer details and predict the customer’s segment interactively.

---

## Methodology

1. **Data Preprocessing**
   - Load customer data from CSV.
   - Handle missing values by filling with mean values.
   - Remove irrelevant columns (e.g., `CUST_ID`).
   - Standardize features using `StandardScaler`.

2. **Exploratory Data Analysis**
   - Visualize distributions with KDE and histograms.
   - Correlation heatmaps to understand relationships between features.

3. **Dimensionality Reduction**
   - Apply PCA to reduce data dimensions for visualization.

4. **Clustering**
   - Use the Elbow method to find the optimal number of clusters.
   - Perform K-Means clustering to segment customers into 4 clusters.
   - Save the clustering model with `joblib`.
   - Save clustered data with cluster labels to CSV.

5. **Classification**
   - Train a Decision Tree classifier on the clustered data.
   - Evaluate using confusion matrix and classification report.
   - Save the classifier using `pickle` in a `.sav` file.

6. **Deployment**
   - A Streamlit app loads the saved classifier and clustered data.
   - Users enter customer feature values via a web form.
   - The app predicts the cluster and shows visualizations related to that cluster.

---

## Technologies & Libraries Used

- Python 3  
- pandas, numpy — Data processing  
- matplotlib, seaborn — Visualization  
- scikit-learn — StandardScaler, PCA, KMeans, DecisionTreeClassifier, model evaluation  
- joblib — Saving/loading the K-Means clustering model efficiently  
- pickle — Saving/loading the Decision Tree model  
- streamlit — Web app framework for interactive UI  

---

## Explanation of Model Saving Formats

- **joblib**: Optimized for saving large models with NumPy arrays (like K-Means). Saves faster and loads more efficiently.  
- **pickle**: Python’s built-in serialization module, used here for saving the Decision Tree model in `final_model.sav`.  
- **.sav files**: Just a naming convention for saved models serialized via pickle.

---

**Mohammed Jawad**  
  
• 📎 [LinkedIn](https://www.linkedin.com/in/a-m-jawad/)  

