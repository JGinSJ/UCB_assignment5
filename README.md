# Data Analysis Project: Will the Customer Accept the Coupon?

## Project Overview
The goal of this project is to use data visualizations and probability distributions to deliniate between customers who have accepted a driving coupon versus those who have not accepted a coupon.

Several apps today already deliver just-in-time coupons based on proximity to a business (i.e., restaurants). What are the factors that cause you to be more likely to accept the coupon? Proximity is a factor to coupon delivery, but do other factors like weather, time of day, whether you have passengers, and who those passengers might be affect your propensity to accept the coupon? This assignment attempts to draw conclusions or ‘insights’ using a dataset from the UCI Machine Learning Repository, collected via a survey on Amazon Mechanical Turk.

## Data Cleaning & Preparation
To ensure accurate statistical modeling, missing and problematic data was handled methodically:
- Feature Dropping: The `car` column was dropped entirely as it contained over 99% missing values.
- Row Dropping: Rows containing `NaN` values were dropped. 
- Data Retention: Out of the original 12,684 observations, 605 rows were dropped. Because this accounts for only 4.77% of the data, the removal is not statistically significant, leaving 12,079 observations for the analysis.

## Key Findings

### 1. Habitual Behavior (Bar Coupons)
- Drivers who already frequently visit bars (more than once a month) accepted bar coupons at a rate of over 70%.
- Drivers who were "budget-conscious" (income under $50k, frequent ‘cheap’ restaurant patrons) had significantly lower bar coupon acceptance, observed at less than 45% acceptance.
- Other factors such as the presence of children in the vehicle causes bar coupon acceptance to plummet.

### 2. Time-Bound Receptiveness (Coffee House Coupons)
Acceptance of coffee coupons is highly dependent on the time of day, whether there is a passenger, and who that passenger is:
- Acceptance rates peak sharply at 10 AM and 2 PM, indicating that drivers are highly receptive to coupons during standard morning breaks and when trying to beat the "mid-afternoon slump."
- Drivers are significantly more likely to accept coffee coupons if they are riding with friends or partners specifically, rather than when traveling alone or with children.

## Recommendations
1. Deploy Behavioral Algorithms: Shift the marketing algorithm to prioritize users with a documented history of visiting those specific types of establishments.
2. Context-Aware Push Notifications: Implement "passenger context" filtering. Do not send bar coupons if the passenger is a kid. Ideal coupon recipients are in younger demographics (under 30), traveling with friends in the late afternoon/evening.

## Repository Structure
- `jg_assignment5.ipynb`: The main Jupyter Notebook containing the code, data cleaning, pandas filtering logic, and visualizations.
- `data/coupons.csv`: The dataset used for the analysis.
- `README.md`: This executive summary of the project.

## Technologies Used
- **Python** (Pandas, NumPy)
- **Data Visualization** (Matplotlib, Seaborn)
- **Jupyter Notebook**

