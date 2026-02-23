<div align="center">
  <h1>🍔 Zomato Sales Dashboard 🚀</h1>
  <p><strong>Transforming Raw Orders into Actionable Insights</strong></p>
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Power BI Badge" />
  <img src="https://img.shields.io/badge/Data_Analytics-0052CC?style=for-the-badge&logo=Google+Analytics&logoColor=white" alt="Analytics Badge" />
  <img src="https://img.shields.io/badge/DAX-20232A?style=for-the-badge&logo=microsoft&logoColor=61DAFB" alt="DAX Badge" />
</div>

<br />

Welcome to the **Zomato Sales Analysis** repository! We took massive datasets spanning from user demographics to granular restaurant menus, and engineered a dynamic, high-performance Power BI dashboard to track revenue, gauge user sentiment, and measure operational volume.

### ✨ Dashboard Preview

[**🚀 View the Live Interactive Dashboard Snapshot (PDF)**](https://saibuvanesh.github.io/Zomato-Sales-Dashboard/) 

*(GitHub strips out direct PDF embeds in READMEs, so we've set up a dedicated live page for an uncompromised viewing experience. Click the link above!)*

---

## 🏗️ Project Architecture

This repository is organized intentionally to separate our raw data, the analytical engine, and our documentation.

- 📊 **[Zomato Sales.pbix](./Zomato%20Sales.pbix)**: The core Power BI file containing the interconnected data model, DAX measures, and front-end visualizations.
- 🗃️ **[Data.md](./Data.md)**: A deep dive into our 6 core datasets (`users`, `restaurant`, `menu`, `food`, `orders`, `orders_Type`), explaining their structure and value.
- 📈 **[Dashboard.md](./Dashboard.md)**: The engine room. Explains the exact logic behind our DAX measures (like `ActiveUsers`, `GainCust`, and `TOPN Sale`), interactive slicers, and performance KPIs.
- 📄 **[Zomato Sales.pdf](./Zomato%20Sales.pdf)**: Static export of the fully rendered dashboard.
- 📁 **Datasets/**: The raw `.xlsx` files powering the Star schema.
- 🖼️ **Images/**: Premium UI assets and icons utilized within the dashboard.

---

## 🚀 Getting Started

To explore the dashboard locally on your machine:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/SaiBuvanesh/Zomato-Sales-Dashboard.git
   ```
2. **Open the Dashboard:** Open `Zomato Sales.pbix` in Power BI Desktop.
3. **Refresh Data Connections:** Ensure the file paths to the `Datasets` folder match your local directory structure so Power Query can pull the latest numbers.
4. **Interact:** Explore the slicers, view Year-over-Year growth, and analyze top-performing assets!

<br />

<div align="center">
  <i>Built with precision for clean data and fast insights.</i>
</div>
