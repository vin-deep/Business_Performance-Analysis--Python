Business Performance Analysis Using Python & Pandas
Business Performance Analysis using Python and Pandas. Analyzed Revenue, Profit, Margin, and Product Performance to generate Business Insights and recommendations.

## Business Problem

Management wants to identify:

- Total company revenue
- Total company profit
- Best performing products
- Lowest performing products
- Products requiring additional attention

The goal is to support data-driven business decisions.
## Project Overview

This project analyzes product sales data using Python and Pandas.

The objective is to calculate:

- Total Revenue
- Total Cost
- Total Profit
- Profit Margin %
- Best Performing Products
- Lowest Performing Products

and provide business recommendations.

---

## Tools Used

- Python
- Pandas
- Google Colab

---

## Dataset

| Product | Sales | Cost |
|----------|---------:|---------:|
| Laptop | 50000 | 35000 |
| Mobile | 30000 | 22000 |
| TV | 80000 | 60000 |
| Tablet | 20000 | 18000 |
| Headphones | 15000 | 12000 |

---

## Python Code

```python
import pandas as pd

sales = {
    "Product":["Laptop","Mobile","TV","Tablet","Headphones"],
    "Sales":[50000,30000,80000,20000,15000],
    "Cost":[35000,22000,60000,18000,12000]
}

df = pd.DataFrame(sales)

df["Profit"] = df["Sales"] - df["Cost"]
| KPI           |    Value |
| ------------- | -------: |
| Total Revenue | ₹195,000 |
| Total Cost    | ₹147,000 |
| Total Profit  |  ₹48,000 |
Best Products
TV → Highest Revenue
Laptop → Highest Margin
Products Needing Attention
Tablet
Headphones
Business Recommendations
Continue promoting TV.
Increase focus on the laptop due to strong profitability.
Investigate low Tablet profit.
Review the headphone sales strategy.
df["Margin %"] = (df["Profit"]/df["Sales"])*100

print(df)
