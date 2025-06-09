# Vendor-Performance-Analysis

#Exploratory Data Analysis
Previously, we examined the various tables in the database to identify key variables, understand their relationships, and determine which ones should be included in the final analysis.
In this phase of EDA, we will analyze the resultant table to gain insights into the distribution of each column. This will help us understand data patterns, identify anomalies, and ensure data quality before proceeding with further analysis.

#Summary Statistics Insights:¶
#Negative & Zero Values:
Gross Profit: Minimum value is -52,002.78, indicating losses. Some products or transactions may be selling at a loss due to high costs or selling at discounts lower than the purchase price.
Total Sales Quantity & Sales Dollars: Minimum values are 0, meaning some products were purchased but never sold. These could be slow-moving or obsolete stock.
Profit Margin: Has a minimum of -infinite, which suggests cases where revenue is zero or even lower than costs.
Outliers Indicated by High Standard Deviations:
Purchase & Actual Prices: The max values (5,681.81 & 7,499.99) are significantly higher than the mean (24.39 & 35.64), indicating potential premium products.
Freight Cost: Huge variation, from 0.09 to 257,032.07, suggests logistics inefficiencies or bulk shipments.
Stock Turnover: Ranges from 0 to 274.5, implying some products sell extremely fast while others remain in stock indefinitely. Value more than 1 indicates that Sold quantity for that product is higher than purchased quantity due to either sales are being fulfilled from older stock.

#Correlation Insights
PurchasePrice has weak correlations with TotalSalesDollar(-0.012) and GrossProfit(-0.016), suggesting that price variations do not significantly impact sales revenue or profit
Strong Correlation between total purchase quantity and total sales quantity(0.999), confirming efficient inventory turnover
Negative correlation between profit margin & total sales price (-0.179) suggests that as sales prices increases, margins decrease, possibly due to competitive pricing pressure.
StockTurnover has weak negative correlations with both GrossProfit(-0.038) and ProfitMargin(-0.055), indicating that faster turnover does not necessarily result in higher profitability.

#Data Analysis
Identify Brands that needs Promotional or pricing Adjustments which exihibit lower sales performance but highr profit margins.
Vendors buying in bulk (Large Order Size) get the lowest unit price ($10.78 per unit), meaning higher margins if they can manage inventory efficiently.
The price difference between Small and Large orders is substantial (~72% reduction in unit cost)
This suggests that bulk pricing strategies successfully encourage vendors to purchase in larger volumes, leading to higher overall sales despite lower per-unit revenue.

Which vendor have low inventory turnover, indicating excess stock and slow-moving products?
The confidence interval for low-performing vendors (40.48% to 42.62%) is significantly higher than that of top-performing vendors (30.74% to 31.61%).
This suggests that vendors with lower sales tend to maintain higher profit margins, potentially due to premium pricing or lower operational costs
For High-Performing Vendors: If they aim to improve profitability, they could explore selective price adjustments, cost optimization, or bundling strategies.
For Low-Performing Vendors: Despite higher margins, their low sales volume might indicate a need for better marketing, competitive pricing, or improved distribution strategies.
Is there a significant difference in profit margins between top-performing and low-performing vendors?
Hypothesis:
Ho (Null Hypothesis): There is no significant difference in the mean profit margins of top-performing and low-performing vendors.
H₁ (Alternative Hypothesis): The mean profit margins of top-performing and low-performing vendors are significantly different.
