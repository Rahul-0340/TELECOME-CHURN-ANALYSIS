# TELECOME-CHURN-ANALYSIS
## Overview
This project focuses on analyzing the recharge behavior and usage patterns of customers within a telecom dataset. The goal is to derive insights related to Average Revenue Per User (ARPU), usage metrics, and customer activity over several months, particularly examining how these factors may relate to customer churn.

## Dataset Description
The dataset used for this analysis is named `telecom_churn_data.csv` and contains the following columns:

- **mobile_number**: Unique identifier for each customer.
- **circle_id**: Identifier for the geographical area of the customer.
- **loc_og_t2o_mou**: Minutes of usage for local outgoing calls to other operators.
- **std_og_t2o_mou**: Minutes of usage for standard outgoing calls to other operators.
- **loc_ic_t2o_mou**: Minutes of usage for local incoming calls from other operators.
- **last_date_of_month_6**: Last activity date for the month of June.
- **last_date_of_month_7**: Last activity date for the month of July.
- **last_date_of_month_8**: Last activity date for the month of August.
- **last_date_of_month_9**: Last activity date for the month of September.
- **arpu_6**: Average Revenue Per User for June.
- **arpu_7**: Average Revenue Per User for July.
- **arpu_8**: Average Revenue Per User for August.
- **arpu_9**: Average Revenue Per User for September.
- **sachet_3g_9**: Indicator for 3G sachet usage in September.
- **fb_user_6**: Indicator for Facebook usage in June.
- **fb_user_7**: Indicator for Facebook usage in July.
- **fb_user_8**: Indicator for Facebook usage in August.
- **fb_user_9**: Indicator for Facebook usage in September.
- **aon**: Age on the network, indicating the number of days the customer has been with Operator T.
- **aug_vbc_3g, jul_vbc_3g, jun_vbc_3g, sep_vbc_3g**: Volume-based charges for 3G services in the respective months.

## Analysis Methodology
The analysis was conducted using Python and the Pandas library. The following steps were performed:

1. **Data Loading and Preparation**: The dataset was loaded into a Pandas DataFrame for exploration and analysis.
2. **ARPU Calculation**: Average Revenue Per User was calculated for the months of June to September.
3. **Usage Metrics Calculation**: Total voice usage was computed by summing up the relevant columns.
4. **Activity Analysis**: The last activity dates were analyzed to assess customer activity and potential recharge behavior.
5. **Recharge Frequency Analysis**: A recharge frequency metric was derived based on customer activity.
6. **Visualization**: Various visualizations were created to illustrate ARPU trends and usage metrics over time.

## Visualization
Visualizations were generated to better understand trends in the data:

- **Average Revenue Per User (ARPU)**: A bar chart showing ARPU over the months.
- **Total Usage**: A bar chart depicting total usage across different call types.

### Example Visualization Code
```python
import matplotlib.pyplot as plt

# Example code to plot ARPU
arpu_months.plot(kind='bar', title='Average Revenue Per User (ARPU) Over Months', ylabel='ARPU', xlabel='Month', figsize=(8, 5))
plt.xticks(rotation=0)
plt.show()
