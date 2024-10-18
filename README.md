# AtliQ_Hardware_Sales_Report
AtliQ Hardware's sales performance data was analyzed using advanced Excel techniques. By leveraging pivot tables, data validation, and complex formulas, dynamic reports were created to highlight key metrics such as customer performance, market sales versus targets, and gross margin analysis. This project focuses on analyzing AtliQ Hardware's sales performance data, which includes regional sales figures, customer growth, product performance, and market comparison against set targets. The goal is to provide insights that can drive data-driven decision-making for improving revenue streams, optimizing customer relationships, and identifying growth opportunities..

# 1. Background
AtliQ Hardware is a leading global manufacturer of computer hardware, producing a wide range of electronic components such as personal computers, keyboards, and mouse. The company caters to a diverse customer base, including prominent e-commerce platforms like Amazon and Flipkart, as well as retail chains like Chroma. AtliQ’s business operates through two key models: e-commerce and brick-and-mortar. The company uses a multi-channel approach to reach its customers, encompassing direct sales, retail partnerships, and distribution networks. This comprehensive strategy enables AtliQ to maintain a competitive presence in both online and physical marketplaces.

# 2. Project Objectives
- Generate a Customer Performance Report to evaluate major customers and their contributions to growth.
- Create a Sales Performance Report by Country to assess target achievement and identify growth opportunities.
- Develop a Top Products Report to highlight high-demand items and inform product strategy.
- Compile a Division Performance Report to showcase successful divisions and expansion potential.
- Produce a New Products Impact Report to analyze sales contributions from new product lines.
- Generate a Regional Sales Growth Report to identify opportunities for market expansion.
- Develop strategies for Top and Bottom Customers to nurture high performers and improve slower-growing accounts.

# 3. Technical Stacks

Data Visualization and Analysis : Advanced Excel (Power Query, Power Pivot, Data validation using Conditional formatting)

Data Source: Folder containing Sales, Product, Market, Customer and Monthly Target.

# 4. Data Understanding
The dataset contains over a million sales record and consists of the following features in each table:
- **Sales**: Date, Product ID, Customer ID, Revenue, Quantity, Manufacturing Cost, Freight Cost
- **Product**: Product ID, Division, Segment, Category, Product, and Variant
- **Customer**:  Customer ID, Market, Platform, and Channel.
- **Market**: Market, Sub Zone, and Region.
- **Target**: Market, Date, Target

# 5. Data Preprocessing
- **Remove Empty Columns and Rows**: Identify and remove any empty columns and rows.
- **Remove Duplicates**: Deduplication of data to avoid redundancy.
- **Rename Columns**: Ensure appropriate names are used for better analysis.
- **Change Data Types**: Ensure columns have appropriate data types (e.g., dates, numbers, text).
- **Handle null values**: Replaced null values with “Not Available”
- **Standardize Values**: Replaced and formatted values to maintain data consistency.
- **Feature Extraction**: Replaced the values with releveant data for accurate analysis.

# 6. Data Modelling
- Create Fact and Dimension Tables:
  - **Fact Table**: Sales, Target
  - **Dimension Tables**: Date, Product, Customer, Market, 
- Establish Relationship between Fact and Dimension Tables
- Data Formatting
- Generate Hierarchies
- DAX

# 7. DAX
**Calculated Measures**:
- Net Revenue = sum(Sales[Revenue])
- Net Sales 2018 = CALCULATE([Net Revenue], 'Date'[Fiscal Year]="2018")
- Net Sales 2019 = CALCULATE([Net Revenue], 'Date'[Fiscal Year]="2019")
- Net Sales 2020 = CALCULATE([Net Revenue], 'Date'[Fiscal Year]="2020")
- Net Sales 2021 = CALCULATE([Net Revenue], 'Date'[Fiscal Year]="2021")
- 2020 vs 2021 = divide([Net Sales 2021]-[Net Sales 2020], [Net Sales 2020], 0)
- 2021-Target = [Net Sales 2021]-[Net Target]
- Target % = divide([2021-Target], [Net Target], 0)
- Total Quantity = sum('Sales'[Quantity])

# 8. Report Summary
- **Performance vs Target by Country**
  - Despite growth, most countries did not meet their 2021 sales targets. India had the highest sales ($161.3M) but fell short by $9.6M (-5.59%). The USA, Canada, and South Korea also saw high sales but missed targets by significant margins, indicating global underperformance​.
  
- **Top Products**
  - The top-selling products saw a massive increase in sales from 2020 to 2021. For instance, AQ Electron 4 3600 Desktop Processor sales increased by 541%, and AQ Smash 2 surged by 2489%. This suggests a successful product lineup with high market demand​.

- **Division-Level Performance**
  - Every division saw strong growth. The "PC" division showed an outstanding 313.7% growth in sales from 2020 to 2021. Overall, sales increased by 204.5%, highlighting the company's expansion across all business areas​.

- **New Products**
  - New product lines in 2021, such as AQ Qwerty and AQ Gen Y, saw impressive sales, with AQ Qwerty leading at $22M. New products collectively contributed $176.2M to total sales, indicating the company’s successful strategy in product innovation​.
    
- **Top Countries**
  - India, USA, South Korea, and Canada led sales, contributing significantly to the total $598.9M sales in 2021, with India alone accounting for $161.3M​.

- **Top Customers**
  - Major customers like Amazon ($82.1M), Atliq E Store ($53M), and Atliq Exclusive ($61.1M) showed consistent growth, with Amazon increasing by 218.87% from 2020 to 2021. These large customers are key to sustaining overall growth​.

- **Fastest Growing Customers**
  - Companies such as Chiptec (722.03% growth) and Integration Stores (887.19%) represent emerging partners contributing significantly to the company’s expansion. The focus should shift toward maintaining strong relations with these high-growth customers​.
    
- **Regional Sales Growth**
  - Major regions like North America, Europe, and Asia saw exponential growth in net sales performance from 2019 to 2021, with Europe leading at 304.48%. This suggests potential opportunities for further market penetration in underperforming regions​.

- **Top and Bottom Customers**
  - While customers like Logic Stores grew by 515%, some like Novus exhibited slower growth rates. Emphasis should be placed on nurturing high-performing customers while devising strategies to boost sales from slower-growing customers.
  
# 9. Recommendations:
- **Product Strategy**: Focus on expanding production and marketing for top-performing products like AQ Smash 2 and AQ Electron Desktop Processor, which have seen massive year-over-year growth.
- **Market Expansion**: While India and the USA are strong markets, underperforming regions like Japan, Poland, and New Zealand should be reassessed for potential local market strategies to enhance sales and reduce target shortfalls.
- **Customer Relationships**: Strengthen relations with rapidly growing customers like Amazon, Chiptec, and Integration Stores to solidify market share in competitive regions.
- **Target Improvement**: Investigate the reasons behind countries missing sales targets despite growth (e.g., pricing, logistics, or competition) and implement region-specific corrective measures.
- **Innovation Focus**: Given the successful performance of new product lines, continued focus on R&D and introducing innovative products will ensure long-term growth.

# 10. Future Scope
- **Advanced Analytics**: Implement predictive analytics and machine learning models to forecast sales trends and enhance customer segmentation.
- **Expanded Reporting Features**: Develop interactive dashboards in Power BI for deeper insights into sales performance and real-time data visualization.
