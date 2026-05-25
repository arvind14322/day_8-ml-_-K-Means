# K-Means Customer Segmentation on Online Retail Data

This project performs customer segmentation using the **K-Means clustering**
algorithm on the Online Retail dataset. The workflow builds customer‑level features
from transactional data, applies preprocessing and scaling, identifies an appropriate
number of clusters using the elbow method, and visualizes the resulting customer groups.
A well‑structured README helps repository visitors quickly understand what the project does,
why it is useful, and how to run it on GitHub.

## Project Overview

The notebook uses transactional retail data to group customers based on purchasing behavior.
It derives three core features commonly used for customer segmentation:

- **Recency**: How recently a customer made a purchase.
- **Frequency**: How often a customer made purchases.
- **Monetary**: How much a customer spent in total.

These RFM‑style features are widely used in customer analytics and appear frequently 
in K‑Means segmentation examples built on the Online Retail dataset.

## Objectives

- Clean and preprocess retail transaction data.
- Create customer‑level features from raw transactions.
- Remove outliers from the main clustering variables.
- Standardize features before clustering.
- Use the elbow method to estimate the optimal number of clusters.
- Train a K‑Means model for customer segmentation.
- Visualize clusters and centroids for interpretation.

## Dataset

This project uses the **Online Retail** dataset, a transactional dataset commonly used for 
customer segmentation and clustering tasks.

Suggested dataset sources:

- UCI Machine Learning Repository: [Online Retail](https://archive.ics.uci.edu/dataset/352/online+retail)
- Kaggle mirror: [Online Retail Data Set](https://www.kaggle.com/datasets/vijayuv/onlineretail)

## Workflow

The notebook follows these main steps:

1. Import required libraries.
2. Load the retail dataset.
3. Inspect data types, missing values, and summary statistics.
4. Drop rows with missing customer or product description data.
5. Convert `CustomerID` and `InvoiceDate` into suitable formats.
6. Create `Amount` from `Quantity * UnitPrice`.
7. Build customer‑level `Amount`, `Frequency`, and `Recency` features.
8. Merge these features into a final analysis dataframe.
9. Detect and remove outliers using an IQR‑based filtering approach.
10. Scale the selected features using `StandardScaler`.
11. Use the elbow method to choose the value of `k`.
12. Fit the K‑Means model and assign cluster labels.
13. Visualize customer clusters and centroids.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- scikit‑learn
- Jupyter Notebook / Google Colab

## Repository Structure

.
├── day_8(ml)_.ipynb
├── README.md
└── data/
    └── Online_Retail.xlsx

If the dataset is not stored in the repository, update the file path in the notebook before
running it.

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

2. Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

3. Download the dataset from UCI or Kaggle and place it in the project folder or update
the notebook path accordingly.

4. Open the notebook in Jupyter Notebook or Google Colab.

5. Run the notebook cells in order.

## Results

The model segments customers into clusters based on behavioral similarity after scaling the 
selected features. The final notebook also includes an elbow plot for choosing `k` and a
scatter plot that shows the cluster groups and their centroids for interpretation.

## Use Cases

Customer segmentation from this workflow can support:

- Personalized marketing campaigns
- Customer retention strategies
- High‑value customer identification
- Shopping behavior analysis
- Business decision‑making based on customer groups

These are standard applications of K‑Means‑based customer segmentation in retail analytics.

## Future Improvements

- Add silhouette score or Davies‑Bouldin score for cluster evaluation.
- Compare K‑Means with hierarchical clustering or DBSCAN.
- Build a dashboard for interactive cluster exploration.
- Add richer visualizations for all feature combinations.
- Create customer personas for each cluster.

## Author

**Your Name**  
MSc Data Science Student  
University of Hertfordshire

## License

This project can be released under the MIT License if you want to make it open for reuse on
GitHub. GitHub recommends including clear repository documentation such as a README, along 
with optional supporting files like a license, to help visitors understand the project 
quickly.
