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
