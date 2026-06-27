# Kj-ecommerce-sales-dashboard
Power BI dashboard for e-commerce sales analysis — profit, category, and state-wise breakdowns with interactive quarter and state filters.
# KJ Ecommerce Sales Dashboard (Power BI)

An interactive **Power BI dashboard** built to analyze e-commerce order data across Indian states. The dashboard — titled **"KJ Ecommerce Sales Dashboard"** — tracks sales amount, profit, quantity, and average order value, with breakdowns by month, category, payment mode, customer, and state, all filterable by quarter and state.

## 📖 About the Project

This project models a real-world e-commerce order dataset using two related tables — **Orders** and **Details** — joined on `Order ID`, and turns them into a single, interactive Power BI report page. The goal was to build a dashboard that lets a business user quickly answer:

- How much profit and revenue are we generating, and how does it trend by month?
- Which product categories and sub-categories are driving (or hurting) profit?
- Which payment methods are customers using most?
- Which states and customers are top performers?
- How do these numbers change when filtered by quarter or by state?

## 📊 Dataset Overview

The data model is built from two CSV source tables that are related on `Order ID`:

### `Orders.csv` — Order & Customer Information
| Detail | Value |
|---|---|
| Total rows | 500 orders |
| Columns | `Order ID`, `Order Date`, `CustomerName`, `State`, `City` |
| States represented | 19 |
| Cities represented | 25 |
| Top states by order volume | Maharashtra, Madhya Pradesh, Rajasthan, Gujarat, Uttar Pradesh |

### `Details.csv` — Order Line-Item Details
| Detail | Value |
|---|---|
| Total rows | 1,500 line items |
| Columns | `Order ID`, `Amount`, `Profit`, `Quantity`, `Category`, `Sub-Category`, `PaymentMode` |
| Categories | Electronics, Furniture, Clothing |
| Sub-categories | 17, including Phones, Chairs, Bookcases, Printers, Sarees, Kurtis, T-shirts, and more |
| Payment modes | COD, EMI, Credit Card, UPI, Debit Card |
| Total amount | ₹437,771 |
| Total profit | ₹36,963 |
| Total quantity sold | 5,615 units |

> Note: Some line items show a **negative profit**, meaning a number of orders were sold at a loss — useful to investigate further when filtering by category or sub-category.

## 📈 Dashboard Contents

The Power BI report (`kj_ecommerce_sales.pbix`) is built on a single report page titled **"KJ"**, combining KPI cards, charts, and interactive filters:

**KPI Cards**
- Sum of Amount — total order value
- Sum of Profit — total profit earned
- Sum of Quantity — total units sold
- Sum of AVG — average order value (calculated measure)

**Charts**
- **Profit by Month (Column Chart)** — Monthly profit trend based on Order Date
- **Profit by Sub-Category (Bar Chart)** — Profit broken down by product sub-category (e.g. Phones, Bookcases, Stole, Printers, Shirt)
- **Quantity by Category (Donut Chart)** — Share of quantity sold across Electronics, Furniture, and Clothing
- **Quantity by Payment Mode (Donut Chart)** — Share of quantity sold across COD, EMI, Credit Card, UPI, and Debit Card
- **Profit by Customer (Column Chart)** — Profit contribution by individual customers
- **Amount by State (Bar Chart)** — Total order amount broken down by state

**Interactive Filters**
- **Quarter Slicer** — Filter the entire report by Qtr 1–Qtr 4
- **State Slicer** — Filter the entire report by a specific Indian state (e.g. Andhra Pradesh, as shown in the dashboard view)

Because `Orders` and `Details` are related through `Order ID`, filtering by state or quarter updates every visual on the page — including profit, category, and payment mode breakdowns — in real time.

## 🛠️ Built With

- **Microsoft Power BI Desktop** — data modeling, relationships, and report visualization
- **CSV (Orders.csv, Details.csv)** — source data, related through `Order ID`

## 📁 Files

- `kj_ecommerce_sales.pbix` — The Power BI report file (includes the data model, table relationships, and report visuals)
- `Orders.csv` — Order-level data: date, customer, state, and city
- `Details.csv` — Line-item data: amount, profit, quantity, category, and payment mode

## 🚀 How to Open

1. Install **Power BI Desktop** (free, available from Microsoft)
2. Open `kj_ecommerce_sales.pbix` directly — both tables and their relationship are already embedded in the file's internal data model, so no separate data connection setup is required
3. Use the **Quarter** and **State** slicers at the top of the report to explore different segments of the data

## 🎯 Project Goals

- Practice modeling relational data in Power BI by joining two tables on a common key (`Order ID`)
- Build a multi-visual dashboard combining KPI cards, time-series trends, category breakdowns, and geographic/state-level comparisons
- Create calculated measures (such as average order value) on top of raw transactional data
- Design an interactive, filterable report that supports real business decision-making

## 📬 Contact

**Johit Kumar**
- 📧 Email: johitkumarjha@gmail.com
- 📍 Location: Jaipur, Rajasthan
- 📞 Phone: +91 8581902314

## 📄 License

This project uses sample e-commerce order data for educational and portfolio purposes.

---

© 2026 Johit Kumar — KJ Ecommerce Sales Dashboard
