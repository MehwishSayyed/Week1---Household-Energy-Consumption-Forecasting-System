# 🏠 Cleaned UCI Household Energy Consumption Dataset

This repository contains a cleaned and preprocessed version of the UCI Individual Household Electric Power Consumption Dataset.
The data records the electric power usage of a single household between December 2006 and November 2010, with measurements taken every minute.

ℹ️ Original Dataset Information

Source: UCI Machine Learning Repository
Time Period: December 2006 to November 2010 (47 months)
Sampling Rate: 1 minute
Number of Measurements: 2,075,259 measurements originally

📊 Dataset Overview
Column	                   Description	                              Unit
DateTime	                 Combined date and time column      	        —
Global_active_power	       Total active power consumed	              kilowatts (kW)
Global_reactive_power	     Reactive power                    	        kilowatts (kW)
Voltage	                   Average voltage	                          volts (V)
Global_intensity	         Current intensity	                        amperes (A)
Sub_metering_1	           Energy sub-metering 1 (kitchen)	          watt-hour (Wh)
Sub_metering_2	           Energy sub-metering 2 (laundry)	          watt-hour (Wh)
Sub_metering_3	           Energy sub-metering 3 (AC & water heater)	watt-hour (Wh)


🧹 Cleaning Steps Performed

Combined Date and Time columns into a single DateTime column.

Replaced missing values (?) with NaN and removed incomplete rows.

Converted numeric columns to the correct float data type.

Set DateTime as index for time-series analysis.

Saved cleaned dataset as a CSV file for direct use in analysis or ML models.


📦 Files Included

household_energy_cleaned.csv → Final cleaned dataset

cleaning_script.py → Python script used for data cleaning

README.md → This documentation file

⚙️ Example Usage
import pandas as pd

# Load cleaned dataset
df = pd.read_csv('household_energy_cleaned.csv', parse_dates=['DateTime'], index_col='DateTime')

# Display info
print(df.info())
print(df.head())


🧠 Potential Use Cases

Energy consumption forecasting

Anomaly detection in power usage

Time-series analysis

Renewable energy optimization research


🏷️ Source

Original data: UCI Machine Learning Repository – Individual household electric power consumption

📜 License

This cleaned dataset is released for educational and research purposes only.
Please cite the original UCI dataset if used in publications.

🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.


👩‍💻 Author

Maintained by Sayyed Mehwish, Computer Science Engineering student.
This repository demonstrates dataset cleaning and preparation for ML-based energy forecasting projects.
