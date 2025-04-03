# 🏡 Airbnb Market Analysis in Dublin

This project aims to provide insights into the Airbnb market in **Dublin**, based on user search behavior and host responses. A new Airbnb city manager wants to understand guest demand patterns and host acceptance trends to bridge the gap and increase bookings.

## 📊 Project Objective

- Understand what **guests are searching** for in Dublin.
- Identify which inquiries **hosts tend to accept**.
- Reveal **demand-supply gaps** to help the city manager boost host engagement and bookings.

## 📁 Datasets

The analysis is based on two datasets:

### 1. `searches.tsv`
Contains data on user searches for listings in Dublin.
- `ds`: Date of the search
- `ds_checkin`, `ds_checkout`: Date of check-in and check-out
- `n_searches`, `n_nights`, `n_guests_min`, `n_guests_max`
- `filter_price_min`, `filter_price_max`
- `filter_room_types`, `filter_neighborhoods`
- `origin_country`

### 2. `contacts.tsv`
Contains data on actual inquiries and interactions between guests and hosts.
- `ts_contact_at`, `ts_reply_at`, `ts_accepted_at`, `ts_booking_at`
- `ds_checkin`, `ds_checkout`
- `n_guests`, `n_messages`
- `id_guest`, `id_host`, `id_listing`

## 🧪 Methodology

1. **Data Preparation**
   - Loaded and cleaned both datasets.
   - Handled missing values, parsed dates, and applied skewness corrections (log and Box-Cox).
   - Merged and filtered data as needed for comparative insights.

2. **Exploratory Data Analysis (EDA)**
   - Distribution of searches and bookings over time.
   - Analysis by number of guests, price filters, room types, neighborhoods.
   - Day-of-week check-in patterns and their effect on bookings.
   - Host responsiveness and acceptance behavior.

3. **Visualizations**
   - Histograms, KDE plots, bar charts, and heatmaps.
   - Side-by-side transformations to assess skewness.
   - Time series plots for demand trends.

4. **Demand-Supply Gap Analysis**
   - Compared guest search preferences with actual host responses.
   - Identified underserved segments (e.g., large groups, long stays).
   - Flagged patterns where demand isn't being matched by supply.

## 📌 Key Findings

- **Most searches happen for 2-3 night stays**, especially on weekends.
- **Group sizes above 4 guests** are less likely to receive host acceptance.
- Certain **neighborhoods and room types** are over-searched but underbooked.
- Hosts tend to respond faster to **shorter stays and smaller groups**.

## 🔍 Recommendations

- Encourage hosts to list more properties for longer stays and bigger groups.
- Improve supply in high-demand neighborhoods and room types.
- Use predictive filters to suggest better-matching listings to guests.

## 📈 Tools & Libraries

- Python (Pandas, NumPy)
- Matplotlib & Seaborn
- Scipy (Box-Cox)
- Jupyter Notebook

## 📂 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/airbnb-dublin-market-analysis.git
   cd airbnb-dublin-market-analysis
   ```

2. Install dependencies (optional):
   ```bash
   pip install -r requirements.txt
   ```

3. Launch the notebook:
   ```bash
   jupyter notebook Main.ipynb
   ```

## 📩 Future Work

- Add geospatial visualizations to map demand hotspots.
- Build a simple model to predict booking success likelihood.
- Gather additional data like property amenities and reviews.

## 🙌 Acknowledgements

This project is part of an Airbnb market insight challenge to guide strategic decisions for new city managers.
