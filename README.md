# ☀️ Photovoltaic (PV) Cell Performance Analysis

This project analyzes the **monthly solar power output** using real irradiance data, simulates the behavior of a **photovoltaic (PV) system**, and estimates energy production under different assumptions. The analysis includes system loss estimation, energy generation calculations, and data visualization using Python.

---

## 📊 Project Highlights

- 🔍 Monthly solar irradiance analysis
- 🔧 Realistic PV system modeling (with efficiency & losses)
- ⚡ Energy yield calculation (ideal vs expected)
- 📈 Beautiful visualizations using Matplotlib
- 🧠 Designed for academic use and research submissions

---

## 🧪 Methodology

The project performs the following steps:

1. **Data Import & Cleaning**
   - Source: `POWER_Point_Bangalore.csv` (NASA/POWER or similar)
   - Cleaned & formatted monthly solar irradiance values

2. **System Parameters**
   - Panel wattage: `325 W`
   - Panel efficiency: `16.7%`
   - Total panels: `16`
   - Area per panel: `1.946 m²`
   - Inverter efficiency: `96%`
   - Temperature loss: `4%`

3. **Energy Estimation**
   - Ideal Energy = Irradiance × Area × Efficiency
   - Realistic Energy = Ideal Energy × (1 - Total Losses)

4. **Visualization**
   - Bar plots showing expected vs ideal energy
   - Trends across months and years

---

## 📁 Project Structure

```
PV-Cell-Analysis/
├── PV_CELLS.ipynb            # Main Jupyter Notebook with analysis and plots
├── data/
│   └── POWER_Point_Bangalore.csv  # Monthly irradiance data (source: NASA POWER)
├── images/
│   ├── irradiance_plot.png       # Monthly irradiance graph
│   └── energy_comparison.png     # Expected vs ideal energy bar chart
├── results/
│   └── monthly_summary.csv       # Tabular results from calculations (optional)
├── requirements.txt              # Python dependencies
└── README.md                     # Project overview and instructions
```

