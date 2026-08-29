# Global Superstore Power BI Analysis

An end-to-end Power BI project analyzing Global Superstore sales from 2011–2014. The project covers data cleaning, star-schema modeling, DAX measures, time intelligence, and interactive report design.

## Data model

```text
Stg_Superstore
├── DimCustomer ──┐
├── DimProduct  ──┤
├── DimLocation ──┼── FactSales
└── DimDate     ──┘
```

- Fact table grain: one row per order line
- 51,290 sales rows
- 4,873 customers
- 10,768 unique product keys
- 3,819 locations
- 1,461 calendar dates

The staging query provides a stable schema for every downstream table. Composite `Product Key` and `Location Key` fields prevent ambiguous relationships and keep the model one-to-many.

## Key measures

- Total Sales, Profit, Quantity, Orders, Customers, and Products
- Profit Margin, Average Order Value, and Sales per Customer
- Previous-Year Sales, YoY Change, and YoY Growth
- Average Discount

## Report pages

- **Executive Overview** — KPIs, monthly trends, category performance, market ranking, and segment mix
- **Product Performance** — subcategory sales and profit, Top 10 products, and discount-versus-profitability analysis
- **Customer & Market Analysis** — geographic sales and market customer value; customer ranking is in progress
- **Model Validation** — relationship and measure checks

## Tools

Power BI Desktop · Power Query · DAX
