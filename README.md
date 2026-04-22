Title: Student Marks Analysis using Python

Aim:
To analyze student marks and find average, best performer, and worst performer.

Procedure:

Import the pandas library
Load the CSV file
Calculate total and average marks
Identify best and worst performers
Display the results

Code:import pandas as pd

df = pd.read_csv("data.csv")

df["Total"] = df.iloc[:, 1:].sum(axis=1)
df["Average"] = df.iloc[:, 1:-1].mean(axis=1)

best = df.loc[df["Total"].idxmax()]
worst = df.loc[df["Total"].idxmin()]

print("Best Performer:", best["Name"])
print("Worst Performer:", worst["Name"])

Result:
The average marks, best performer, and worst performer were successfully identified.
