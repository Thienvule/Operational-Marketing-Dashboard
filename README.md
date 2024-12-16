# Tactical Marketing Dashboard

## Business context
A marketing manager at Florae, a floral business, is seeking to enhance her team's productivity by optimizing marketing campaigns more efficiently. I am responsible for creating an interactive dashboard that reports key metrics in real time and identifies both effective and ineffective campaigns.

## Overview
Goal: This interactive dashboard will help measure the marketing effectiveness of various campaigns, with updates based on filters to identify underperforming campaigns for optimization.
How the dashboard operates:

![image](https://github.com/user-attachments/assets/eda97dfb-8db9-49f4-bfb9-9a359c233892)


Step 1: Specify the desired time frame and select the branch location responsible for the campaigns together with the desired campaign objective

![image](https://github.com/user-attachments/assets/40f27323-551c-4d31-a16b-8bbd20dc296a)

Step 2: Evaluate campaigns based on their efficiency

![image](https://github.com/user-attachments/assets/4caf37c5-6dd0-43a9-b322-41f554a5508d)

This table compares the CPM of the campaigns to the AVG CPM as decides their efficiency.

Step 3: Get a comprehensive overview of the key metrics.

![image](https://github.com/user-attachments/assets/f6dcaaf4-1b9b-48f3-9b7b-9dd7c93b9cd4)

These metrics can be customized to the need of the users. Here I input some of the metrics to get started with.

Some example metrics could be included:
- TOTAL SPENT: How much has been spent on the campaigns
- TOTAL MES: How many messages we got in total after the campaigns
- AVG CPM: Average cost per message, a metric used to identify the efficiency of the campaigns
- CTR: Click through rate

The dashboard can be customized and added more columns as needed.


### Main Functions used
- QUERY
- IFS
- ARRAYFORMULA
- REGEXMATCH
- TEXT
- SUMIFS
- Pivot table
- Calculated field
- Data visualization
- Data validation
- Conditional formatting 

## Building dashboard - let's get technical
### Interactive Data
This tab utilizes Aggregate Data to adjust and compile relevant metrics and columns, while crucially preserving the integrity of the raw dataset. The Interactive Data tab acts as the source for the filtered results displayed on the main dashboard. First, in the Aggregate Data tab, I created a 'Location' column extracted from the 'Campaign Name' column, which includes the branch's name following the naming convention. 

![image](https://github.com/user-attachments/assets/b9042806-d2bd-4e9a-92f4-d7bb8e4d83f5)

As for the InteractiveData tab - the core of the dashboard, this is the how it was created:

![image](https://github.com/user-attachments/assets/5dbf1e03-fecc-49c1-8fd2-e39f211bbc70)


This formula is designed to return a filtered dataset from a range from the Aggregate Data based on specific conditions set in the Dashboard sheet. It uses Excel functions like IF, OR, AND, ISBLANK, and QUERY.

The logic flow of building the dashboard:

In summary, the formula dynamically adjusts the query based on user inputs: 
- If both filters are "All", it returns all records.
- If the location is "All" but an objective is specified, it fetches records based on the objective and any specified date filters.
- If the objective is "All", it fetches records based on the location with any specified date filters.
- If both filters are specified, it combines them, allowing for further filtering by dates if applicable.


### Pivot table
To evaluate the relevant metrics and assess campaign efficiency, I use pivot tables along with calculated fields to effectively visualize the data in charts. As for the efficiency of the campaigns as requested, I would compare the CPM of each campaign with the average CPM and display accordingly.

![image](https://github.com/user-attachments/assets/7cb5cf88-d137-415e-8f9f-fb932f53f3f7)

Similarly, relevant metrics can also be obtained from this Pivot Table sheet. Finally, I transfer the created charts to the main dashboard and format them accordingly.

![image](https://github.com/user-attachments/assets/16925a85-5cf4-46a5-98d9-e25fd60b60d7)

## Final Thoughts
The predictive outcomes of the marketing operational dashboard indicate a significant potential for improved campaign efficiency, cost savings, and increased productivity. By focusing on data-driven decision-making, Florae marketing team is positioned to maximize its marketing investments, optimize resource allocation, and ultimately drive better business results. These enhancements will not only improve the efficacy of the campaigns but also yield a substantial positive impact on the overall marketing strategy and financial performance.

### Next Steps
Moving forward, we will continue to monitor these predictions closely and adjust our strategies as necessary to ensure ongoing optimization and success. Regular training for the marketing team on utilizing the dashboard effectively will also be a priority to fully leverage the capabilities of this valuable tool.





