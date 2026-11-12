# 📱 Smartphone Price Prediction Model

An end-to-end Machine Learning regression project that predicts smartphone prices in INR based on hardware specifications and brand features.

## 📂 Repository Structure
- `smartphone.ipynb` — Complete Jupyter Notebook covering data preprocessing, EDA, model training, evaluation, and interactive price inference.
- `smartphones.csv` — Raw dataset containing 1,020 smartphone listings with hardware and pricing attributes.

## 📊 Dataset & Preprocessing
- **Data Cleaning:** Handled missing values, stripped currency symbols (`₹`) and commas from prices, and filtered extreme hardware/price outliers (`ram_gb` between 1–24 GB, `price` ≤ ₹2,00,000), retaining **979 clean records**.
- **Feature Engineering:** Extracted numerical metrics (`ram_gb`, `stor_gb`, `battery_mah`, and `fast_chr_watt`) from unstructured text columns using Regular Expressions (Regex) and applied One-Hot Encoding across smartphone brands.

## 📈 Exploratory Data Analysis (EDA)
- Visualized overall price distributions and RAM-to-price scaling trends.
- Compared price spreads across the top 8 smartphone brands (Xiaomi, Samsung, Vivo, Realme, OPPO, Motorola, Apple, OnePlus) using boxplots.
- Built a correlation heatmap to identify key price drivers such as RAM, internal storage, and user ratings.

## 🤖 Model Benchmarking & Results
Trained and evaluated two regression models using an 80-20 train-test split (`700` training samples, `175` testing samples):

| Model | $R^2$ Score | Mean Absolute Error (MAE) |
| :--- | :---: | :---: |
| **Linear Regression** | 0.212 | ₹12,633.01 |
| **Random Forest Regressor** | **0.652** | **₹7,532.04** |

- **Key Takeaway:** Random Forest significantly outperformed Linear Regression by capturing non-linear relationships between hardware specs and pricing, increasing the $R^2$ score to **0.652** and reducing MAE by **~40%**.

## 🛠️ Tech Stack
- **Language:** Python 3
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
- **Environment:** Jupyter Notebook

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/KESHAVGUPTA-00/Phone-Price-Prediction.git](https://github.com/KESHAVGUPTA-00/Phone-Price-Prediction.git)
   cd Phone-Price-Prediction

   