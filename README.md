# 📊 Total Runs and Average Runs Comparison (Bar + Line Chart)

This visualization compares the **Total Runs** (as a bar chart) and **Average Runs** (as a line graph) of three cricket players: *Kohli*, *Rohit*, and *Dhawan*.

## 🔧 Libraries Used

- `matplotlib.pyplot`: For creating plots
- `numpy`: For numeric operations and positioning bars

## 📈 Chart Description

- **Bar Chart** (`plt.bar`) shows the **total career runs** of each player.
- **Line Chart** (`plt.plot`) displays the **average yearly runs** for the same players.
- `ggplot` style is applied for better aesthetics.
- Both graphs are overlaid for comparison.

## 🧮 Data Used

| Player | Total Runs | Average Runs |
|--------|------------|---------------|
| Kohli  | 5800       | 966.67        |
| Rohit  | 5500       | 916.67        |
| Dhawan | 5400       | 900           |

## 📊 Output Features

- Skyblue bars for total runs
- Green line with circular markers for average runs
- X-axis: Player names
- Y-axis: Runs
- Grid lines enabled for readability
- Title and legend included

## ✅ How to Run

Paste the following code into a Python environment or `.py` file:

```python
import matplotlib.pyplot as plt
import numpy as np

players = ['Kohli', 'Rohit', 'Dhawan']
total_runs = [5800, 5500, 5400]
avg_runs = [966.67, 916.67, 900]

x = np.arange(len(players))
width = 0.25

plt.style.use("ggplot")
plt.bar(x, total_runs, width = width, color = "skyblue", label = "Total Runs")
plt.plot(x, avg_runs, color = "green", marker = "o", linewidth = 2, label = "Average Run")
plt.legend()
plt.xlabel("Players")
plt.ylabel("Runs")
plt.xticks(x, players)
plt.grid(True)
plt.title("Total Runs and Average Runs")
plt.show()
