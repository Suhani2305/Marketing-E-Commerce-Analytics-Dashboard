# 📊 Marketing & E-Commerce Analytics Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/Status-Complete-success?style=for-the-badge)

> A comprehensive Power BI dashboard analyzing 100K customers, 1M+ events, and $8.37M revenue across marketing campaigns, product performance, and customer lifetime value.

---

## 🔗 Quick Links

| Link | Description |
|------|-------------|
| 🌐 **[Live Dashboard](https://app.powerbi.com/groups/me/reports/e11e5eed-d3fb-4806-81a0-ff97e1690c59/fa5a9db66a392632d09a?experience=power-bi)** | View Interactive Power BI Dashboard |
| 📄 **[Project Report PDF](https://drive.google.com/file/d/1k81fQ9V2JWc4qsUXY2CCXFaY4HewBgTk/view?usp=sharing)** | Complete Project Documentation |
| 📊 **[Download .pbix File](https://drive.google.com/drive/folders/1ifGgPByjF5Pp0ccNLeAHctmEU-iwWjHW?usp=sharing)** | Power BI Desktop File |
| 📸 **[Screenshots](https://drive.google.com/drive/folders/1cTFlQo0BltLTBKbrT-kHjLkNOuPXYbSW?usp=sharing)** | Dashboard Preview Images |

---

## 🎯 Project Overview

**Academic Project** | Data Science Minor Project | 2023-27  
**Author**: Suhani Rawat | **Institution**: Lovely Professional University

### Key Metrics Analyzed
- **Customers**: 100,000 across 7 countries
- **Products**: 2,000 items in 6 categories
- **Events**: 1,000,000+ user interactions
- **Revenue**: $8.37M total | $60.61 CLV
- **Campaigns**: 50+ marketing campaigns across 5 channels

---

## 📦 Dataset

**Source**: Kaggle - Marketing and E-Commerce Analytics Dataset  
**Size**: ~190 MB | **Tables**: 5 CSV files

| Table | Records | Key Data |
|-------|---------|----------|
| Customers | 100K | Demographics, loyalty tiers, acquisition channels |
| Products | 2K | Categories, brands, pricing (premium/standard) |
| Events | 1M+ | Views, clicks, cart adds, purchases, bounces |
| Transactions | 103K | Revenue, discounts, refunds, campaign attribution |
| Campaigns | 50+ | Channel, objective, target segment, expected uplift |

---

## 📊 5 Interactive Dashboards

### 1. 📈 **Marketing Overview**
- **KPIs**: 10% conversion, 3% refund, $58.78 AOV
- **Insights**: Loyalty tier distribution, revenue trends, campaign attribution (80%)

### 2. 🔄 **Customer Funnel Analysis**
- **Flow**: 1.04M views → 284K cart → 103K purchases
- **Key Finding**: 73% view-to-cart drop | 64% cart abandonment
- **Device**: Mobile 59% traffic, Desktop 11.8% conversion (best)

### 3. 🛍️ **Product Performance**
- **Top Category**: Electronics $3.46M (41% revenue)
- **Mix**: 50% premium, 50% standard products
- **Insight**: Top 10 products = 14% total revenue

### 4. 🎯 **Campaign Performance**
- **Revenue**: $6.68M from campaigns (80% attribution)
- **Best Channels**: Affiliate $2.1M | Email 10.1% conversion
- **Worst**: Social $380K (4.2% conversion)

### 5. 💎 **Customer Lifetime Value**
- **CLV**: $60.61 | **Active (30D)**: 3.6% only
- **Critical**: 64% customers at churn risk (90+ days inactive)
- **Repeat Rate**: 1.03 orders/customer (below 1.5-2.5 benchmark)

---

## 🔑 Key Insights

### ✅ Strengths
- Healthy conversion (10%) and refund rates (3%)
- Strong campaign performance (80% attribution)
- Premium markets (UK, Germany) show high CLV ($71-$78)

### ⚠️ Critical Issues
1. **Churn Crisis**: 64% customers inactive 90+ days
2. **Funnel Leak**: 73% drop view-to-cart (product page issue)
3. **Cart Abandonment**: 64% abandonment rate
4. **Low Repeat**: 1.03 orders/customer vs 1.5-2.5 industry avg
5. **Mobile Gap**: 3% lower conversion vs desktop

### 💡 Top 3 Actions
1. **Urgent**: Win-back campaigns for 64K at-risk customers
2. **High**: Optimize product pages (mobile-first)
3. **High**: Cart recovery automation + checkout optimization

---

## 🛠️ Tech Stack

- **Power BI Desktop** (v2.149.1252.0)
- **DAX** (50+ custom measures)
- **Power Query** (ETL & data transformation)
- **Star Schema** data modeling

---

## 🚀 Quick Setup

```bash
# 1. Clone repo
git clone https://github.com/SuhaniRG/marketing-analytics-dashboard.git

# 2. Download dataset from Kaggle & place in data/ folder

# 3. Open .pbix file in Power BI Desktop

# 4. Refresh data & explore!
```

**Requirements**: Windows 10/11, Power BI Desktop, 8GB+ RAM

---

## 📐 Sample DAX Measures

**Conversion Rate**
```dax
Conversion Rate = 
DIVIDE(
    CALCULATE(COUNTROWS(events), events[event_type] = "purchase"),
    CALCULATE(COUNTROWS(events), events[event_type] = "view"),
    0
)
```

**Customer Lifetime Value**
```dax
CLV = DIVIDE(SUM(transactions[gross_revenue]), DISTINCTCOUNT(customers[customer_id]), 0)
```

**Churn Risk**
```dax
Churn Risk = 
SWITCH(TRUE(),
    [Days Since Last Purchase] <= 30, "Active",
    [Days Since Last Purchase] <= 90, "At Risk",
    "High Risk"
)
```

📄 [View all 50+ DAX measures in project files]

---

## 📁 Project Structure

```
marketing-analytics-dashboard/
├── data/                    # 5 CSV files (190MB)
├── powerbi/                 # .pbix file + DAX measures
├── docs/                    # Project report (PDF/DOCX)
├── screenshots/             # Dashboard images
└── README.md
```

---

## 📸 Dashboard Previews

### Marketing Overview
![Dashboard 1](https://drive.google.com/uc?export=view&id=1q_MAv2A78ZGo0o75Cc0Kv6H0d_PvZdjN)

### Customer Funnel
![Dashboard 2](https://drive.google.com/uc?export=view&id=1je8T8yRU4n4ys4y5xj1XltThQwfhgqV5)

### Product Performance
![Dashboard 3](https://drive.google.com/uc?export=view&id=1K7_l-hHTECwOqq7VvIVgYT8Mxv7Fxk0Q)

### Campaign Performance
![Dashboard 4](https://drive.google.com/uc?export=view&id=1Z96cXgSOiM45cBn7FfxLhVKZtQZ6DYBw)

### CLV & Retention
![Dashboard 5](https://drive.google.com/uc?export=view&id=14jNX4e33jfrpIu6S_lfBHsd6fGTa_IhX)

---

## 🔮 Future Enhancements

- [ ] ML-based churn prediction model
- [ ] Real-time dashboard updates
- [ ] Multi-touch attribution modeling
- [ ] Mobile-responsive design
- [ ] Automated alerting system

---

## 📞 Contact

**Suhani Rawat**

📧 pushpendrarawat868@gmail.com  
💼 [LinkedIn](https://www.linkedin.com/in/suhanirawat2305/)  
🌐 [Portfolio](https://suhani-portfolio-five.vercel.app/)

---

## 📄 License

MIT License © 2025 Suhani Rawat

---

## 🙏 Acknowledgments

- **Dataset**: Geetha Sagar Bonthu (Kaggle)
- **Supervisor**: Dr. Mrinalini Rana (UID: 22138)
- **Institution**: Lovely Professional University
- **Tools**: Microsoft Power BI

---

<div align="center">

**⭐ If you found this helpful, please star the repo!**

Made with ❤️ for Data Science

[⬆ Back to Top](#-marketing--e-commerce-analytics-dashboard)

</div>
