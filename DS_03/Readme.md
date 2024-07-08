# Bird Strike Analysis

This project analyzes the effect of bird strikes on aircraft at different altitudes using a dataset of bird strike incidents.

## Overview

We convert altitude bins to numeric values, group data by flight phase and damage effect, calculate average altitudes, and visualize the results.

## Dataset

Includes columns:
- `When: Phase of flight`
- `Altitude bin`
- `Effect: Indicated Damage`

## Code

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

# Load dataset
df = pd.read_csv('bird_strikes.csv')

# Convert altitude bins
def convert_altitude_bin(altitude_bin):
    bins = {
        '< 1000 ft': 500,
        '1000 - 2000 ft': 1500,
        '2000 - 3000 ft': 2500,
        '3000 - 4000 ft': 3500,
        '4000 - 5000 ft': 4500,
        '> 5000 ft': 5500
    }
    return bins.get(altitude_bin, np.nan)

df['Altitude'] = df['Altitude bin'].apply(convert_altitude_bin)

# Average altitude by phase of flight
avg_altitude_phase = df.groupby('When: Phase of flight')['Altitude'].mean().sort_values()
plt.figure(figsize=(12, 6))
avg_altitude_phase.plot(kind='bar', color='green')
plt.title('Average Altitude by Phase of Flight')
plt.xlabel('Phase of Flight')
plt.ylabel('Average Altitude (ft)')
plt.xticks(rotation=45)
plt.show()

# Average altitude by damage effect
effect_altitude = df.groupby('Effect: Indicated Damage')['Altitude'].mean().sort_values()
plt.figure(figsize=(12, 6))
effect_altitude.plot(kind='bar', color='blue')
plt.title('Effect of Bird Strikes at Different Altitudes')
plt.xlabel('Effect')
plt.ylabel('Average Altitude (ft)')
plt.xticks(rotation=45)
plt.show()


Requirements
Python 3.x
Pandas
NumPy
Matplotlib
Usage

Clone the repository.

Place bird_strikes.csv in the project directory.

Run the code.
