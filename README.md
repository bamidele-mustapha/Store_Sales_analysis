# Store Sales Analysis | Power BI Executive Dashboard

An interactive, five-page Power BI report analysing Superstore business transactions from **2011 to 2014**. It covers sales and profit performance, time trends, regional behaviour and customer behaviour, and turns them into executive-level insights.

> **Demo video:** [add link here]
> **Executive summary:** see [`docs/Store_Sales_Executive_Summary.docx`](docs/Store_Sales_Executive_Summary.docx)

---

## Business Questions

- Which markets, categories and products drive profit, and which erode it?
- Is growth translating into healthier margins?
- How much do shipping costs and shipping modes affect profitability?
- How concentrated is the customer base?

## Headline Numbers

| Metric | Value |
|---|---|
| Total Sales | $61.8M |
| Total Profit | $1.47M |
| Overall Profit Margin | ~2.4% |
| Total Orders | 51.29K |
| Units Sold | 178K |
| Countries Reached | 147 |
| Total Shipping Cost | $1.35M |

## Dashboard Pages

| Page | What it shows |
|---|---|
| **1. Overview** | Landing page with report title, scope (2011-2014) and navigation buttons |
| **2. Sales & Profit Analysis** | KPIs, profit by category and sub-category, profit and quantity by region, profit and sales by ship mode, segment and ship-mode splits, filtered by Market |
| **3. Time Series Analysis** | Sales and profit trend by year, profit distribution per year, shipping cost per year, orders and profit trend, quantity and profit trend, filtered by Region and Market |
| **4. Regional Analysis** | Quantity and profit by region and country, average shipping cost per country, profit trend by region, filtered by Year and Category |
| **5. Customer Behavior Analysis** | Top 10 customers, customer distribution map, ship-mode preference, customer profit trend, filtered by Region |

## Key Insights

1. **Growth without margin improvement.** Orders, sales and units roughly doubled from 2011 to 2014, but the margin held at about 2.4%.
2. **Profit is spread across three markets.** APAC (~30% of profit), EU (~25%) and US (~19%) generate roughly 75% of profit together.
3. **EMEA is the weakest market.** About 5K orders but a 1.3% margin. Canada has the best margin (7.5%) on very small volume.
4. **Technology earns the profit.** 45% of profit from 37% of sales (2.9% margin). Furniture ran at about 1.3% in 2014, and Tables are the only sub-category that loses money.
5. **Shipping cost nearly cancels out profit.** $1.35M of shipping cost against $1.47M of profit. Standard Class carries most of the volume.
6. **Low customer concentration.** The top 10 customers contribute only about 5% of total profit.

### Market snapshot

| Market | Sales | Profit | Margin |
|---|---|---|---|
| APAC | $18.3M | $437.6K | 2.4% |
| EU | $14.8M | $372.8K | 2.5% |
| US | $11.5M | $286.4K | 2.5% |
| LATAM* | ~$10.6M | ~$222K | ~2.1% |
| EMEA | $3.3M | $43.9K | 1.3% |
| Africa | $3.1M | $88.9K | 2.9% |
| Canada | $0.24M | $17.8K | 7.5% |

\*LATAM is derived by subtracting the other six markets from the totals and is approximate.

## Recommendations

1. Reduce shipping cost: renegotiate carrier rates, add free-shipping thresholds, review high-cost countries.
2. Fix EMEA and Furniture margins through pricing and discount review.
3. Prioritise Technology in growth and marketing spend.
4. Set a margin target so that growth improves profitability.
5. Study Canada's margin to see whether the approach can scale.

## Tools and Techniques

- **Power BI Desktop**: report design, slicers, page navigation buttons
- **DAX**: measures for total sales, profit, quantity, orders, countries reached and shipping cost
- **Visuals used**: KPI cards, column and area charts, ribbon charts, donut charts, map, slicers

## Repository Structure

```
.
├── README.md
├── report/
│   └── Store_analysis.pbix
├── data/
│   └── SampleSuperstore.xlsx
├── docs/
│   └── Store_Sales_Executive_Summary.docx
└── media/
    └── demo.mp4
```

*(Adjust to match your repository.)*

## How to Use

1. Download `Store_analysis.pbix` from the `report/` folder.
2. Open it in **Power BI Desktop**.
3. If prompted, update the data source path to point to the file in `data/`.
4. Use the navigation buttons or page tabs to move between pages, and the slicers (Market, Region, Year, Category) to filter.

## Known Limitations and Next Steps

- **Total Customer Reached** currently equals Total Orders, so it likely counts orders rather than distinct customers. This needs a distinct-count measure.
- **Average Shipping Fee** shows the same value under every filter, so the measure needs to respond to slicers.
- Several charts lack data labels. Adding them would improve readability.
- Planned: discount analysis, profit-margin visuals by market and category, and a shipping-cost-to-profit ratio KPI.

## Author

**[Your Name]**
[LinkedIn](#) · [Portfolio](#) · [Email](#)

---

*Data source: Sample Superstore dataset. This project is for learning and portfolio purposes.*
