# ev_cars_data

# ⚡ Electric Vehicle (EV) Market Analysis

## 📌 Project Overview
This project analyzes the current electric vehicle market to identify "Value for Money" leaders, compare technological capabilities across manufacturers, and uncover pricing strategies.
Using **Python** for data cleaning and **SQL** for complex querying, I built a local database to simulate a real-world data analysis workflow.

## 🔍 Key Insights & Business Questions
During the analysis, I addressed several key business questions:

### 1. Which car offers the best Value for Money?
By calculating the "Range per Euro" ratio, I discovered that the **Citroen e-C3** is currently the most cost-efficient vehicle, offering the highest range for every Euro spent, followed closely by BYD models.

### 2. The "Efficiency Frontier"
I mapped the relationship between **Price** and **Range**.
* **Tesla** models consistently appear on the efficiency frontier (high range relative to price).
* There is a diminishing return on investment for luxury models (prices >€100k do not guarantee proportionally higher range).

### 3. Charging Speed Leaders
While Tesla is a market leader in sales, **Lotus** and **Porsche** lead the technology race in charging speeds, offering theoretic speeds of over 1000 km/h (adding range per hour of charging).

## 🛠️ Methodology & Data Decisions

### Data Cleaning (Python)
* **Raw Data:** Handled a dataset with mixed types (strings with units like 'km', 'kg', '€').
* **Cleaning:** Stripped units, handled null values, and converted currency strings to float.
* **Normalization:** Standardized column names for SQL compatibility.

### Strategic Decision: Market Selection
The dataset included prices for Germany, The Netherlands, and the UK.
**Decision:** I chose to base the analysis on **German market prices**.
**Reasoning:** An integrity check revealed that the German price column had significantly fewer missing values (**13**) compared to the UK column (**106**). This ensured a more robust and accurate comparison.

### Storage (SQLite)
Instead of analyzing solely in Pandas, I exported the cleaned data to a local **SQLite** database (`ev_cars.db`). This allowed for scalable SQL querying, simulating a production environment.

## 🧰 Tech Stack
* **Language:** Python 3.x
* **Libraries:** Pandas, NumPy, Seaborn, Matplotlib, SQLite3
* **Tools:** Google Colab, GitHub

## 📊 Visualizations

> The project includes visualizations for:
> * Price vs. Range (Scatter Plot)
> * Top 10 Fast Charging Brands (Bar Chart)

