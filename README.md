# airbnb-nyc-eda
“Exploratory data analysis of 20,770 NYC Airbnb listings using Python (Pandas, Seaborn,MatPlotlib)”.
Airbnb NYC Listings 2024: Exploratory Data Analysis
Exploratory analysis of 20,770 New York City Airbnb listings to understand what drives nightly prices, where listings are concentrated, and how room type, size, and location relate to price.

Tools: Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

Questions explored
How do prices differ across boroughs and room types?
Which factors are most related to price?
Where are listings concentrated, and how long do guests typically have to stay?
Dataset
20,770 listings and 22 columns (price, room type, borough, neighbourhood, coordinates, minimum nights, reviews, availability, beds, and more).
Source: [add the link to where you downloaded the dataset]. The CSV is not stored in this repo. Download it and save it next to the notebook as new_york_listings.csv.
Approach
Load and explore: shape, data types, summary statistics.
Clean: removed rows with missing values, dropped 12 duplicate rows, and fixed data types for ID columns.
Handle outliers: prices are heavily skewed (median 
188, maximum 
1,500 or more were excluded from the price analysis.
Feature engineering: created price per bed (price divided by number of beds) to compare listings of different sizes.
Analyze: price and availability distributions, price by borough and room type, price vs. reviews, a geographic scatter plot, and a correlation heatmap.
Key findings
Manhattan is the most expensive borough. Average nightly price: Manhattan 
155, Queens 
119, Bronx $108.
It stays the most expensive after adjusting for size. Average price per bed: Manhattan 
100, Queens 
75, Staten Island $68.
Room type matters. Entire homes/apartments cost more than private rooms in every borough. Hotel rooms in Manhattan are the priciest category, though there are only 109 hotel-room listings in total.
Number of beds is the strongest link with price (correlation 0.42). Price has a weak negative correlation with longitude (-0.19): listings further west, toward Manhattan, tend to cost more.
Reviews: total reviews and reviews per month are correlated (0.63), but reviews show almost no relationship with price.
Concentration: Manhattan and Brooklyn account for about 76% of listings.
Most listings are mid-term rentals. 81% require a minimum stay of exactly 30 nights.
Charts
Average nightly price by borough and room type

Price distribution	Correlation heatmap
Price distribution	Correlation heatmap
Geographical distribution of listings

How to run
git clone https://github.com/<your-username>/airbnb-nyc-eda.git
cd airbnb-nyc-eda
pip install -r requirements.txt
# download the dataset and save it as new_york_listings.csv in this folder
jupyter notebook airbnb_nyc_eda.ipynb
Limitations and next steps
Listings priced at $1,500 or more were excluded, so the results describe typical listings, not luxury ones.
This is exploratory analysis. It shows relationships, not causes.
Next: a regression model to predict price, and a Power BI dashboard on the cleaned data.
