# Customer Segmentation Using K-Means
## Business Context
A retail company is looking to launch a tiered customer loyalty program to optimize marketing spend and improve campaign effectiveness.

The goal is to identify distinct customer segments and define criteria for tiered membership, enabling personalized communication and targeted promotions for each segment.

## Project Structure
```
customer-segmentation/
├── data/
│   └── customers.csv
├── customer_segmentation.ipynb
├── requirements.txt
└── README.md
```

## Dataset
2236 customers, 29 features after preprocessing

Source: provided as part of a course assignment

## Methods
- Data cleaning and feature transformation
- Statistical validation: Little's MCAR test, partial correlation analysis
- K-Means clustering (k selected via elbow + silhouette)
- PCA for visualization

## Key Findings

3 customer segments identified:
- **Budget Families** (~46%): lowest income, young children, minimal spendings across all categories, browsing without buying
- **Deal Seekers** (~28%): middle income, deal-oriented, wine enthusiasts
- **Premium Buyers** (~26%): highest income, maximum spendings across all categories, no children, prefer offline channels, heaviest wine spenders

## Cluster Visualization
<img width="1480" height="938" alt="image" src="https://github.com/user-attachments/assets/f31b0cb8-e6e9-4c39-8ddc-2cdb72efdf2c" />

## Business Recommendations

| Segment | Strategy |
|---------|----------|
| Budget Families | Online promotions, discount coupons, focus on essentials |
| Deal Seekers | Multi-channel deals, targeted wine promotions |
| Premium Buyers | In-store tastings, premium catalog, exclusive wine collections |

## Limitations
Most spending features correlate strongly with `Income`, limiting behavioral segmentation depth. The dataset captures total spending per category, not purchase frequency or individual transaction details. It reveals *how* customers buy (channels, deal-seeking behavior) more clearly than *why* they buy specific products.

## Libraries

`pandas`, `numpy` – data manipulation

`scikit-learn` – pipeline, preprocessing, model training

`pingouin` – partial correlation analysis

`pyampute` – Little's MCAR test for missing data

`seaborn`, `matplotlib` – visualization

## Setup
```
pip install -r requirements.txt
```

 
