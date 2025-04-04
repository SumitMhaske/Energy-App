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

| Appliance | Summer_kWh | Winter_kWh | Rainy_kWh | Standby_kWh |
|-----------|-------------|-------------|------------|--------------|
| Fan       | 0.1         | 0.15        | 0.12       | 0.01         |
| AC        | 1.2         | 0.3         | 0.6        | 0.05         |
| ...       | ...         | ...         | ...        | ...          |

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
streamlit run app.py
```

> Make sure `Normalized_Energy_Consumption.csv` is in the same directory as `app.py`.

---

Would you like a sample `requirements.txt` and `Normalized_Energy_Consumption.csv` too?
