```
Name :INESH N
Register number : 21222322006
```
# Experiment 1: EDA in IPL Dataset

## Aim:
To perform Exploratory Data Analysis (EDA) on the IPL matches dataset and derive insights about matches per season, winning teams, toss decisions, and top venues.

## Algorithm / Procedure:

### 1.Import Libraries
  Import pandas for data handling.
  Import matplotlib and seaborn for visualization.
### 2.Load Dataset
  Use pd.read_csv() to load the IPL matches dataset.
  Check dataset shape using .shape.
  View first 5 rows using .head().
### 3.Matches per Season (Univariate Analysis)
  Group data by season and count matches.
  Plot a bar chart to visualize growth/decline in matches.
### 4.Top Winning Teams (Univariate Analysis)
  Use value_counts() on the winner column.
  Plot top 5 winning teams in a bar chart.
### 5.Toss Decisions (Univariate Analysis)
  Count toss decision preferences (bat vs field).
  Plot results using a bar chart.
### 6.Top Venues (Univariate Analysis)
  Count matches per venue.
  Display top 5 venues with a horizontal bar chart.
### 7.Draw Insights
  Observe patterns in toss decisions.
  Identify teams with consistent winning trends.

## Program

### Basic info about dataset:
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df=pd.read_csv("/content/matches.csv")
df.shape

df.head()
```
### Matches per season:
```python
season_count=df['season'].value_counts().sort_index()
season_count

plt.figure(figsize=(14, 6))
plt.bar(season_count.index, cseason_ount.values)
plt.xlabel("Season")
plt.ylabel("Number of Matches")
plt.title("Number of IPL Matches Played Per Season")
plt.show()
```
### Top Winning Teams:

```python
winners=df['winner'].value_counts()
winners.head()

plt.figure(figsize=(14, 5))
plt.bar(winners.head(5).index, winners.head(5).values)
plt.xlabel("Team")
plt.ylabel("Number of Wins")
plt.title("Top 5 Teams with Most Wins in IPL")
plt.show()
```
### Toss Decisions:
```python
decisions = df['toss_decision'].value_counts()
decisions

plt.figure(figsize=(6, 4))
plt.bar(decisions.index,decisions.values)
plt.xlabel("Toss Decision")
plt.ylabel("Count")
plt.title("Toss Decision Preference in IPL")
plt.show()
```

### Toss Venues:
```python
top_venues = df['venue'].value_counts().head(5)
top_venues

plt.figure(figsize=(15, 6))
plt.bar(top_venues.index, top_venues.values)
plt.xlabel("Venue")
plt.ylabel("Number of Matches Hosted")
plt.title("Top 5 Venues Hosting Most IPL Matches")
plt.show()
```

## Output

### Basic info about dataset:


<img width="1743" height="321" alt="image" src="https://github.com/user-attachments/assets/36f89469-5cba-4711-b061-180ee5fa48a7" />

### Matches per season:

<img width="1329" height="571" alt="image" src="https://github.com/user-attachments/assets/3619ae87-3ff3-4ab0-b527-ab9de6143535" />

### Top Winning Teams:
<img width="1284" height="487" alt="image" src="https://github.com/user-attachments/assets/a930894b-c46e-49e7-96e7-488f508bdabc" />


### Toss Decisions:
<img width="839" height="546" alt="image" src="https://github.com/user-attachments/assets/43ff5936-c348-4a7d-8250-c855a846f09f" />


### Top Venues:

<img width="1241" height="520" alt="image" src="https://github.com/user-attachments/assets/7015803e-39a6-4180-b7eb-08276a7b1373" />
  
## Result
  This experiment is executed successfully
