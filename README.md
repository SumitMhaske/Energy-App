# Energy_App

---

## 🔌 AI-Based Energy Estimation and Optimization

This Streamlit-based web application estimates and optimizes electricity consumption and monthly costs for home appliances using **XGBoost regression**. By analyzing seasonal appliance usage data and power consumption, the app allows users to:

- Predict the estimated **monthly electricity bill** for various home appliances.
- **Optimize usage hours** for appliances to minimize electricity costs.
- Simulate energy usage across **different seasons** (Summer, Winter, Rainy).
- Input **appliance quantity**, usage time, and energy rates.

### 🚀 Features

- 📊 Uploads and reads normalized appliance energy data.
- ⚡ Uses **XGBoost** to train a regression model for cost estimation.
- 🧠 Suggests optimal usage hours to reduce monthly bills.
- 🔎 Search-enabled appliance selector for better UX.
- 📉 Visual display of individual and total energy costs.

### 📁 Dataset Format

The app requires a `Normalized_Energy_Consumption.csv` file in the root directory, with the following structure:

| Appliance | Minimum_kW | Summer_kWh | Winter_kWh | Rainy_kWh | Standby_kWh |
|-----------|-------------|-------------|-------------|------------|--------------|
| Fan       | 0.05        | 0.1         | 0.15        | 0.12       | 0.01         |
| AC        | 0.8         | 1.2         | 0.3         | 0.6        | 0.05         |
| ...       | ...         | ...         | ...         | ...        | ...          |

### 📌 Column Description

| Column Name     | Description                                                                 |
|-----------------|-----------------------------------------------------------------------------|
| `Appliance`     | Name of the electrical appliance (e.g., Fan, AC, TV).                       |
| `Minimum_kW`    | Minimum power consumption of the appliance in kilowatts.                   |
| `Summer_kWh`    | Energy consumed per hour (in kWh) during Summer.                            |
| `Winter_kWh`    | Energy consumed per hour (in kWh) during Winter.                            |
| `Rainy_kWh`     | Energy consumed per hour (in kWh) during Rainy season.                      |
| `Standby_kWh`   | Energy consumed per hour (in kWh) when the appliance is in standby mode.    |

> ⚠️ Make sure this file is located in the same folder as `app.py`.

### 🛠 Tech Stack

- 🐍 Python
- 📦 Pandas, NumPy
- ⚙️ XGBoost
- 🌐 Streamlit

### 🧮 How It Works

1. **Load CSV data** about appliances and their seasonal power consumption.
2. **Train an XGBoost model** using simulated usage patterns.
3. Input:
   - Appliance name
   - Usage hours per day
   - Appliance quantity
   - Season
   - Cost per unit (₹/kWh)
4. Get:
   - Estimated monthly electricity cost
   - Optimal usage time to minimize cost

### ▶️ Run the App

```bash
pip install -r requirements.txt
streamlit run XGBoost.py
```

## 📸 Screenshots

Here are some screenshots showcasing different aspects of the application:

### 📊 Model Comparison
![Model Comparison](Screenshots/fig0.jpeg)

### 📌 Performance Comparison of Machine Learning Models Using MAE, RMSE, and R² Metrics
![Screenshot UI](Screenshots/Screenshot%202024-10-07%20092601.png)

### 🖥️ User Interface – Appliance Selection
![Appliance Selection UI](Screenshots/fig1.jpeg)

### 🖥️ User Interface – Selection of season and cost per KWh
![Appliance Configuration UI](Screenshots/fig2.jpeg)

### 📈 Estimation Results – Monthly Bill
![Estimated Bill Results](Screenshots/fig3.jpeg)

### 🧠 Optimized Usage Hours – Cost Reduction
![Optimized Hours Result](Screenshots/fig4.jpeg)
![Appliance Cost Breakdown](Screenshots/fig5.jpeg)

### 🔁 Program Flow
![Program Flow](Screenshots/flowchart.drawio.png)

### 🧱 System Architecture
![System Architecture](Screenshots/System%20Architecture.jpeg)

---
