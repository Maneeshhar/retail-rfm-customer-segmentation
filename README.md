# Retail RFM Customer Segmentation Dashboard

An interactive Power BI dashboard that applies **RFM (Recency, Frequency, Monetary) analysis** to segment retail customers, helping identify high-value customers, at-risk segments, and revenue trends using real transactional data.

## 📊 Dataset
- **Source:** UCI/Kaggle Online Retail Dataset
- **Size:** ~540,000 transactions, cleaned down to ~397,884 valid records
- **Fields:** Invoice number, Stock code, Description, Quantity, Invoice date, Unit price, Customer ID, Country

## 🛠️ Tools Used
- **Power BI Desktop** (data modeling, visualization)
- **Power Query** (data cleaning and transformation)
- **DAX** (RFM measures, scoring logic, customer segmentation)

## 🧹 Data Cleaning Process
- Removed cancelled orders (Invoice numbers starting with "C")
- Removed transactions with missing Customer IDs (guest checkouts)
- Removed invalid/negative unit prices
- Resolved date-format inconsistencies in the raw CSV (mixed US/UK date formats caused significant parsing errors — fixed by explicitly parsing with the correct locale)
- Built a standalone Calendar table for accurate time-based analysis

## 📈 Key Findings
1. **Revenue overview:** Generated ~£9M in total revenue across ~18,500 orders from ~4,300 unique customers, with visible seasonal spikes in the monthly sales trend.
2. **Market concentration:** The majority of sales are concentrated in the UK/Europe, indicating a primarily domestic customer base.
3. **Customer loyalty:** A significant proportion of customers fall into the "Champions" segment — recent, frequent, and high-spending — indicating a healthy loyal customer base.
4. **At-risk customers:** Segments like "Needs Attention" and "New Customers" highlight specific groups that could be targeted with re-engagement campaigns.
5. **Spending patterns vary:** Some customers make infrequent but high-value purchases, while others purchase frequently in smaller amounts — suggesting different customer profiles requiring different marketing strategies.

## 📁 Dashboard Pages
1. **Customer RFM Table** — Full customer-level detail with Recency, Frequency, Monetary values, RFM scores, and segment labels.
2. **Sales Overview** — Revenue, orders, and customer summary cards, monthly sales trend, top products, and sales by country.
3. **Customer Segmentation** — Visual breakdown of customers by Recency, Frequency, and Monetary scores.

## 🖼️ Screenshots

### Customer RFM Table
![RFM Table](screenshots%20of%20pj2/01_rfm_table.png)

### Sales Overview
![Sales Overview](screenshots%20of%20pj2/02_sales_overview.png)

### Customer Segmentation
![Customer Segmentation](screenshots%20of%20pj2/03_customer_segmentation.png)

## 🚧 Challenges Faced
The raw dataset contained significant date-formatting inconsistencies (mixed US and UK date conventions), which caused nearly 60% of records to fail parsing initially. Diagnosing and resolving this required rebuilding the data transformation pipeline with explicit locale handling — a valuable real-world lesson in how messy data can be even from well-known public datasets.

## 📬 Contact
Built by Maneesh as part of a Power BI portfolio project for data analyst roles.
