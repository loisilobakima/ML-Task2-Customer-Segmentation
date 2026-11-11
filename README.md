# ML-Task2-Customer-Segmentation
# Task 2: Customer Segmentation

Customer segmentation using unsupervised learning (K-Means and DBSCAN) on the Mall Customers dataset.

## Objective
Group customers into segments based on their **annual income** and **spending score**, to understand different customer profiles.

## Dataset
- **Mall Customers** (Kaggle), 200 customers
- Columns used: `Annual Income (k$)` and `Spending Score (1-100)`
- No missing values, no duplicates

## Methods
1. Data exploration and visualization (histograms, scatter plot)
2. Feature scaling with `StandardScaler`
3. Choice of the number of clusters with the **elbow method** and the **silhouette score**
4. **K-Means** clustering (k = 5)
5. Cluster interpretation with average age, income and spending score
6. **Bonus:** comparison with **DBSCAN** (eps = 0.4, min_samples = 8)

## Results
| Segment | Customers | Profile |
|---|---|---|
| Standard Customers | 81 | Average income, average spending |
| Premium Customers | 39 | High income, high spending |
| Wealthy but Frugal | 35 | High income, low spending |
| Budget-Conscious | 23 | Low income, low spending |
| Young Big Spenders | 22 | Low income, high spending (youngest group) |

- k = 5 is confirmed by the scatter plot, the elbow method and the silhouette score.
- DBSCAN also finds 5 groups with 25 noise points. About 80% of customers fall in the equivalent K-Means group.

## Tools
Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

## Files
- `Task2_Customer_Segmentation.ipynb`: the full notebook
- `Mall_Customers.csv`: the dataset

## How to run
1. Open the notebook in Google Colab.
2. Upload `Mall_Customers.csv` in the Files tab.
3. Run all cells.
