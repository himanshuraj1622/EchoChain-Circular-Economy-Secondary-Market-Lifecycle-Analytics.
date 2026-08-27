# ♻️ EchoChain: Circular Economy & Secondary Market Lifecycle Analytics

## 📌 Project Overview

**EchoChain: Circular Economy & Secondary Market Lifecycle Analytics** is an end-to-end **Data Analytics and Business Intelligence** project designed to analyze the complete post-sale lifecycle of electronic products.

Manufacturers often track products extensively until the point of sale, but after the product reaches the customer, its lifecycle becomes a **data blind spot**. EchoChain addresses this gap by combining **internal manufacturing data, Bills of Materials (BOM), warranty claims, product lifecycle records, and secondary-market data** to understand product recovery, refurbishment, resale, recycling, and landfill outcomes.

The solution provides an interactive **Power BI dashboard** that helps sustainability and operations teams identify products and components with strong circular-economy potential and support data-driven **refurbishment, recovery, resale, and buy-back decisions**.

The project demonstrates a complete analytics workflow—from **data ingestion and validation in Databricks** to **data modeling, DAX analysis, and interactive dashboard development in Power BI**.

---

## 👨‍💻 Project Developer

**Himanshu Raj**  
*Individual Project*

---

## 🎯 Problem Statement

Traditional manufacturing analytics primarily focuses on products until the point of sale. Once products enter the secondary market or are returned, repaired, refurbished, recycled, or discarded, organizations often lack a unified view of their lifecycle.

This makes it difficult to measure:

- ♻️ True circularity performance
- 🌱 Environmental impact
- 🗑️ Landfill diversion
- 💰 Recovery and resale potential
- 🔧 Refurbishment opportunities
- ⚠️ Component failure patterns
- 📈 Secondary-market demand

**EchoChain** addresses this problem by connecting product, component, warranty, lifecycle, and secondary-market information into a unified analytical model.

---

## 🚀 Project Objectives

The project aims to:

- Analyze the complete post-sale lifecycle of electronic products.
- Integrate product and manufacturing information with **BOM component data**.
- Analyze component-level warranty failures and associated costs.
- Evaluate secondary-market listings, sales, demand, and sell-through performance.
- Measure product recovery, refurbishment, resale, recycling, and landfill outcomes.
- Calculate key circular-economy KPIs.
- Identify products/components with high refurbishment potential.
- Measure landfill diversion and recovery performance.
- Provide actionable insights for sustainability and operations teams.
- Develop an interactive **Power BI dashboard** for lifecycle and circularity analysis.

---

## 🛠️ Technology Stack

| Category | Technology |
|---|---|
| ☁️ Cloud Data Platform | Databricks |
| 🗄️ Data Storage | Delta Lake |
| 📊 Data Visualization | Power BI |
| 🔄 Data Transformation | Power Query |
| 📈 Data Modeling | Power BI |
| 🧮 Analytics & Calculations | DAX |
| 🗃️ Database Querying | SQL |
| 📂 Source Data | CSV |
| 🔗 Version Control | Git & GitHub |

---

## 📊 Dataset Information

The project uses **five simulated/mock datasets** representing different stages of the product lifecycle.

Together, these datasets create a unified view of the product from:

**Manufacturing → Usage → Failure → Secondary Market → Recovery/Recycling**

### 📁 Core Datasets

| Dataset | Description |
|---|---|
| `product_master.csv` | Product identity, brand, category, pricing, manufacturing and lifecycle information |
| `bom_components.csv` | Product Bill of Materials, component costs, quantities, and circularity attributes |
| `warranty_claims.csv` | Component failures, warranty claims, repair/replacement costs, severity and downtime |
| `secondary_market.csv` | Secondary-market listings, selling prices, demand, seller information and sales performance |
| `lifecycle.csv` | Product returns, refurbishment, recovery, resale, recycling and landfill outcomes |

---

# 🔍 Dataset Details

## 🏭 Product Master

Contains the core product-level information required to identify and analyze products.

### Key Attributes

- Product ID
- Brand
- Product Model
- Product Category
- Release Year
- Launch Date
- Manufacturing Date
- Original Price
- Operating System
- Processor Family
- Lifecycle Status

---

## 🔧 Bill of Materials (BOM)

The BOM dataset provides component-level information for each product.

### Key Attributes

- BOM ID
- Product ID
- Component ID
- Component Name
- Component Category
- Quantity
- Unit Cost
- Component Weight
- Expected Life
- Reusable Flag
- Refurbishable Flag
- Recyclable Flag

This dataset helps identify components that have potential for **reuse, refurbishment, and recycling**.

---

## 🛠️ Warranty Claims

The warranty dataset captures component failure and warranty information.

### Key Attributes

- Claim ID
- Product ID
- Component ID
- Component Name
- Failure Date
- Purchase Date
- Failure Type
- Severity
- Warranty Status
- Repair Cost
- Replacement Cost
- Downtime Days
- Return Flag
- Resolution

This allows analysis of **frequently failing components, repair costs, replacement costs, and downtime**.

---

## 🛒 Secondary Market

The secondary-market dataset represents listings and transactions from platforms such as **eBay and other secondary marketplaces**.

### Key Attributes

- Listing ID
- Product ID
- Component ID
- Component Name
- Platform
- Listing Type
- Listing Date
- Sale Date
- Condition
- Listing Price
- Sold Price
- Sold Flag
- Days to Sell
- Demand Score
- Seller Type
- Location

This dataset helps measure:

- Secondary-market demand
- Sales performance
- Pricing
- Sell-through rate
- Days to sell
- Component-level market performance

---

## ♻️ Product Lifecycle

The lifecycle dataset captures what happens to products after their original use.

### Key Attributes

- Lifecycle ID
- Product ID
- Purchase Date
- Return Date
- Product Age
- Return Reason
- Recovery Channel
- Refurbishment Cost
- Recovered Value
- Resale Price
- Net Recovery Value
- Recycled Weight
- Landfill Weight
- Landfill Diversion %

This dataset is particularly important for evaluating **recovery, refurbishment, resale, recycling and environmental outcomes**.

---

# 🔄 Data Architecture & Workflow

The project follows a structured analytics pipeline:

```text
CSV Datasets
      ↓
Databricks
      ↓
Schema Creation
      ↓
Delta Lake Tables
      ↓
Data Validation & SQL Analysis
      ↓
Power BI Connection
      ↓
Data Modeling & Relationships
      ↓
DAX Measures
      ↓
Interactive Dashboard
      ↓
Circular Economy Insights


# 📊 Dashboard Development

---

# 📄 Page 1 — Executive Overview

## 🎯 Dashboard Objective

The **Executive Overview Dashboard** provides a centralized view of product circularity, post-sale lifecycle outcomes, refurbishment potential, and recovery performance.

The dashboard enables sustainability and product strategy stakeholders to quickly understand how products perform after the point of sale and identify opportunities to improve **refurbishment, recovery, recycling, and landfill diversion**.

### 📌 KPI Cards

- 📦 Total Products
- 🛠️ Total Warranty Claims
- 🛒 Total Secondary Market Listings
- 🔄 Total Lifecycle Records
- ♻️ Circularity Score
- 🔧 Refurbishment Opportunity Score
- 🌱 Landfill Diversion %
- 💰 Recovery Score

### 📈 Visualizations

- 📊 Refurbishment Opportunity by Product Category
- 🍩 Post-Sale Lifecycle Distribution
- 💰 Recovered Value by Lifecycle Status

---

# 📄 Page 2 — Secondary Market Performance

## 🎯 Dashboard Objective

The **Secondary Market Performance Dashboard** focuses on the post-sale market activity of products and individual components.

It provides insights into secondary-market listings, component sales, customer demand, listing prices, and selling speed. This helps identify components with strong resale potential and supports data-driven refurbishment and buy-back strategies.

### 📌 KPI Cards

- 🛒 Total Secondary Market Listings
- 💰 Component Market Sales
- 📈 Sell Through Rate
- 💵 Average Listing Price

### 📈 Visualizations

- 📊 Market Listings vs Sales by Component
- 📈 Average Demand Score by Component
- 💰 Average Listing Price by Component
- ⏱️ Average Days to Sell by Component

### 🔍 Key Analytical Areas

- Component-level secondary-market activity
- Demand patterns across components
- High-value components in the resale market
- Components with faster selling cycles
- Comparison between market listings and actual sales
- Identification of components with strong refurbishment potential

---

# 📄 Week 2 — Executive Overview & Secondary Market Dashboard

## 🔴 Business Problem

Manufacturers typically have strong visibility into products during production and until the point of sale. However, post-sale product activity is often fragmented across warranty systems, secondary markets, and lifecycle records.

This creates challenges in answering important business questions such as:

- Which products have the highest refurbishment potential?
- Which components have strong secondary-market demand?
- Which components retain the highest resale value?
- How quickly do different components sell?
- What proportion of products are refurbished, resold, recovered, recycled, or sent to landfill?
- How much value is recovered from products after their initial sale?
- Where are opportunities available to improve circularity and reduce landfill dependency?

Without a centralized analytics solution, these insights are difficult to identify and require manual analysis across multiple data sources.

---

## ✅ Solution Implemented

Developed the **EchoChain Power BI Analytics Dashboard** to consolidate product, warranty, secondary-market, BOM, and lifecycle information into an interactive analytical solution.

The dashboard combines multiple project datasets to provide a unified view of **post-sale product intelligence, circularity, recovery, and secondary-market performance**.

### Key Features

**📌 Executive Overview**

- Total Products
- Total Warranty Claims
- Total Secondary Market Listings
- Total Lifecycle Records
- Circularity Score
- Refurbishment Opportunity Score
- Landfill Diversion %
- Recovery Score

**📊 Circular Economy Analysis**

- Refurbishment Opportunity by Product Category
- Post-Sale Lifecycle Distribution
- Recovered Value by Lifecycle Status

**🛒 Secondary Market Analysis**

- Market Listings vs Sales by Component
- Average Demand Score by Component
- Average Listing Price by Component
- Average Days to Sell by Component

**📈 Analytical Enhancements**

- Component-level ranking
- Top-N analysis for high-value components
- Sorting and filtering of analytical visuals
- Blank-value handling
- KPI formatting and consistency
- Executive-focused dashboard layout and visual hierarchy

---

## 🎯 Business Outcome

The EchoChain dashboard enables sustainability and product strategy teams to:

- Gain a centralized view of post-sale product performance.
- Measure overall product circularity and recovery performance.
- Identify products with stronger refurbishment opportunities.
- Understand post-sale lifecycle outcomes across products.
- Identify high-demand components in the secondary market.
- Determine which components retain higher resale value.
- Analyze how quickly components move through the secondary market.
- Compare market listings with actual component sales.
- Identify opportunities for refurbishment and buy-back programs.
- Monitor landfill diversion and recovered value.
- Support data-driven circular economy strategies.
- Reduce manual analysis by consolidating multiple post-sale data sources into a single interactive dashboard.
