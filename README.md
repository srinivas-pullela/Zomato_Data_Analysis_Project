# Zomato Data Analysis Project

This repository contains an exploratory data analysis (EDA) of a small Zomato dataset performed using a Jupyter notebook. The analysis inspects restaurant types, votes, ratings and online-order spending patterns to extract insights useful for product and marketing decisions.

Notebook
- Zomato_Data_Analysis.ipynb — the main analysis notebook (see the linked notebook for code and visualizations).

Dataset
- Zomato_data .csv — the CSV used in the notebook.
- The notebook loads the dataset (about 148 rows) and uses the following columns:
  - name
  - online_order
  - book_table
  - rate
  - votes
  - approx_cost(for two people)
  - listed_in(type)

What I did
1. Imported libraries: pandas, numpy, matplotlib, seaborn.
2. Loaded the dataset and inspected its structure and sample rows.
3. Cleaned and converted the `rate` column from strings like `4.1/5` to numeric floats.
4. Verified missing values and data types.
5. Performed exploratory analysis and plotted charts to answer specific questions.

Key questions answered (see notebook for full code and plots)
- Q1 — Which types of restaurants do most customers order from?
  - Visualized restaurant counts per `listed_in(type)`. Conclusion: majority falls under the "Dining" category.
- Q2 — How many votes has each type of restaurant received?
  - Aggregated votes by restaurant type and plotted results. Conclusion: Dining restaurants received the most votes overall.
- Q3 — What ratings do most restaurants receive?
  - Plotted rating distribution. Conclusion: most restaurants have ratings around 3.5–4.5.
- Q4 — For customers who order online (e.g., couples), what is the average spending per order?
  - Notebook calculates average approx. cost for restaurants that accept online orders to estimate per-order spending for online customers.

How to run
1. Install dependencies (recommended in a virtual environment):
   - Python 3.8+
   - pandas, numpy, matplotlib, seaborn, jupyter
   Example:
   ```
   pip install pandas numpy matplotlib seaborn jupyterlab
   ```
2. Open the notebook:
   ```
   jupyter notebook Zomato_Data_Analysis.ipynb
   ```
   or
   ```
   jupyter lab
   ```
3. Run cells in order. Ensure `Zomato_data .csv` is in the same directory as the notebook or update the path in the notebook.

Results & Insights
- Dining restaurants dominate in count and total votes in the sample.
- Ratings are concentrated between approximately 3.5 and 4.5.
- The notebook includes plots (countplot, line/plot for votes, histogram for ratings) to visualize these findings.
- These insights can inform targeted promotions, pricing strategy, or feature prioritization for online ordering.

Limitations
- Small sample size (~148 rows) — results are indicative but not definitive.
- The dataset appears to be pre-filtered and may not represent broader geographic or category distributions.
- `approx_cost(for two people)` is used as a proxy for spending; actual order-level spending would be better if available.

Possible improvements / next steps
- Increase dataset size and include location and cuisine columns for richer segmentation.
- Clean and standardize other columns (e.g., `votes` outliers, `approx_cost` currency/format).
- Compute per-order spending if transactional order-level data is available.
- Add statistical tests or correlation analysis between rating, cost, and votes.
- Create an interactive dashboard (e.g., using Plotly Dash or Streamlit).

License
- Add a license if you intend to share/redistribute (e.g., MIT).

Contact
- Repository owner: srinivas-pullela
- For questions about the analysis, open an issue or PR in the repository.
