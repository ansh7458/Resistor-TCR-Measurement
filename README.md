# Resistor-TCR-Measurement

This project investigates how the resistance of standard resistors (1 MΩ and 100 kΩ, 5% tolerance) changes with temperature. The resistors were heated inside a power resistor cavity, and their resistance was measured using a voltage divider circuit with an Arduino Uno. Temperature was recorded using a MAX6675 thermocouple module.

## 📁 Files Included
- `1M_Resistor.csv` — Resistance vs. temperature data for 1 MΩ resistor  
- `100K_Resistor.csv` — Resistance vs. temperature data for 100 kΩ resistor
- 
## 🔧 Hardware Used
- Arduino Uno  
- K-type thermocouple + MAX6675  
- Power resistor (5.8 Ω, wire-wound)  
- 1 MΩ and 100 kΩ resistors (5% tolerance)  
- Thermal paste (for improved thermal contact)  
- CoolTerm (for serial data logging)  

## 📊 Method Overview
- Resistors were inserted into a heated cavity with thermal compound.  
- Voltage drop across each resistor was measured using a voltage divider.  
- Data streamed to PC using Arduino and logged via CoolTerm.  
- Fitting was done using a cubic polynomial:  
  \[
  R(T) = R_0 + a\,\Delta T + b\,\Delta T^2 + c\,\Delta T^3
  \]
- TCR was calculated from the linear coefficient:  
  \[
  \text{TCR} = \frac{a}{R_0} \times 10^6~\text{ppm/°C}
  \]

## 📈 Results
- 1 MΩ TCR ≈ -2928 ppm/°C  
- 100 kΩ TCR ≈ -1774 ppm/°C  
- Resistance decreased nonlinearly with temperature in both cases.


