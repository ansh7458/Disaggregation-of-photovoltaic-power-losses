# ☀️ Disaggregation of Photovoltaic Power Losses

A data-driven analysis of photovoltaic (PV) system performance, focusing on breaking down power losses into distinct categories like wiring, soiling, aging, and module mismatch. This project uses real irradiance data and realistic system parameters to compute expected vs actual power output, and visualizes the loss breakdown in a clear and informative manner.

---

## 🚀 Project Highlights

- 📅 **Time-series solar irradiance analysis**
- ⚙️ **Realistic PV system modeling**
- 📉 **Residual loss calculation**
- 🧮 **Disaggregation of losses** into key categories
- 📊 **Clean visualizations** (bar charts & pie chart)
- 🧠 Designed for academic submission & technical evaluation

---

## ⚠️ Understanding Photovoltaic Losses

In this project, we have analyzed the following key loss components:
- ⚡ **Wiring Losses**: Some energy is lost due to resistance in the electrical wiring connecting the panels and inverter.
- 🧽 **Soiling Losses**: Dirt, dust, and debris accumulating on panels reduce the effective irradiance reaching the cells.
- ⚙️ **Mismatch Losses**: Variability in panel performance (due to shading or manufacturing differences) leads to overall efficiency reduction.
- 🧓 **Aging Losses**: Over time, panels naturally degrade and generate slightly less power each year.

These losses are quantified to estimate the realistic power output from the ideal energy estimate. By breaking them down, we gain insights into where improvements can be made to enhance PV system performance.

---


## 🧪 Methodology

1. **📂 Data Processing**
   - Import CSV data: `POWER_Point_Bangalore.csv`
   - Clean and merge `YEAR`, `MO`, `DY` columns into a single date column
   - Remove null or malformed entries

2. **⚡ System Modeling**
   - **Panel specs:** 325W, 16.7% efficiency, 1.946 m² area
   - **Panel count:** 16
   - **Inverter efficiency:** 96%
   - **Temperature loss:** 4%
   - Compute **expected generation** using:
     ```
     Expected (kWh) = (Total Capacity × 5 hours / 1000) 
                      × Inverter Efficiency × (1 - Temp Loss)
     ```

3. **📏 Residual Loss Calculation**
   - Subtract measured output from expected generation
   - Clip negatives to 0
   - Disaggregate total loss into:
     - 🔌 **Wiring Loss** – 10%
     - 🧼 **Soiling Loss** – 30%
     - 🧩 **Module Mismatch Loss** – 25%
     - 🧓 **Aging Loss** – 35%

4. **📊 Visualization**
 Visualization

-📊 Bar plots showing expected vs ideal energy output
-🌞 Monthly irradiance graphs to understand solar availability trends
-🔻 Loss distribution pie chart representing relative losses from different sources
-📉 Line graphs to compare trends in actual vs. theoretical power generation

---

