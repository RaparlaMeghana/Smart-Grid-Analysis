# Smart-Grid-Analysis
# Smart Grid Analytics For Electric Power Systems
import pandas as pd
import matplotlib.pyplot as plt

data = {
    'Timestamp': pd.date_range(start='2024-02-25', periods=24, freq='H'),
    'Power Consumption (MW)': [300, 310, 320, 330, 340, 350, 360, 370, 380, 390, 400, 410, 420, 430, 440, 450, 460, 470, 480, 490, 500, 490, 480, 470],
    'Voltage (kV)': [230, 228, 225, 222, 220, 222, 225, 230, 235, 240, 245, 240, 235, 230, 225, 220, 215, 220, 225, 230, 235, 240, 245, 240],
    'Line Losses (%)': [2, 2.2, 2.5, 3, 3.5, 3, 2.5, 2, 1.8, 1.5, 1.2, 1.5, 1.8, 2, 2.5, 3, 3.5, 3, 2.5, 2, 1.8, 1.5, 1.2, 1.5]
}

df = pd.DataFrame(data)

print("Dataset Information:")
print(df.info())

print("\nFirst 5 rows of the dataset:")
print(df.head())

plt.figure(figsize=(10, 6))
plt.plot(df['Timestamp'], df['Power Consumption (MW)'], label='Power Consumption (MW)', marker='o')
plt.plot(df['Timestamp'], df['Voltage (kV)'], label='Voltage (kV)', marker='o')
plt.plot(df['Timestamp'], df['Line Losses (%)'], label='Line Losses (%)', marker='o')
plt.title('Smart Grid Analytics for Electrical Power Systems')
plt.xlabel('Timestamp')
plt.ylabel('Values')
plt.legend()
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()
