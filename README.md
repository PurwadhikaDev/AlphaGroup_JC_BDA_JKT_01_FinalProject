# Hotel Booking Data Analysis

This project analyzes hotel booking data to uncover insights about customer behavior, cancellations, and booking patterns.  
The dataset has been cleaned and processed to remove invalid entries, handle missing values, and cap unrealistic outliers.  
The analysis includes exploratory data analysis (EDA), visualizations, and segmentation of customers based on booking composition.

## Project Structure
- data/ → contains raw and cleaned datasets (CSV files)
- notebooks/ → Jupyter/Colab notebooks for cleaning, EDA, and visualization
- exports/ → CSV exports (e.g., customer segments, top countries, cleaned dataset)
- plots/ → saved charts and figures
- README.md → project documentation

## Data Cleaning
Steps taken to clean the dataset:
1. Removed invalid rows (e.g., bookings with 0 adults).
2. Capped extreme values for numerical features (lead time, nights stayed, number of guests, cancellations, etc.).
3. Handled missing values (e.g., replaced missing children and agent with reasonable defaults).
4. Created new features:
   - arrival_date (combined day, month, year into one column).
   - customer_segment (classified into Single, Couple, or Family).
   - Full country names mapped from ISO codes.

## Exploratory Data Analysis (EDA)
Key analyses and plots:
- Distribution of hotel types (City Hotel vs Resort Hotel).
- Cancellations by hotel type and overall cancellation rate.
- Distribution of lead time and ADR (Average Daily Rate).
- Guest composition (adults, children, babies) by hotel type.
- Top 10 countries of visitors (non-canceled bookings) with world map visualization.
- Seasonality analysis of arrivals (monthly booking patterns).

## Key Visualizations
- Pie charts: hotel type distribution, cancellation rates, customer segments.
- Histograms: lead time, ADR distribution.
- Scatterplots: stays in week vs weekend nights, adults vs children per booking.
- Heatmaps: correlation between numeric features.
- Choropleth maps: visitor country distribution.
- Line chart: monthly booking trends.

## Exported Datasets
- cleaned_hotel_bookings.csv → cleaned dataset ready for analysis.
- top_countries.csv → top 10 source countries of non-canceled bookings.
- customer_segments_by_hotel.csv → grouped data of customer segmentation by hotel.

## Usage
### Run in Google Colab
1. Upload the notebook and dataset.
2. Run all cells to clean, analyze, and visualize the data.
3. Export cleaned datasets and charts for further use (e.g., Looker Studio dashboards).

### Run Locally
```bash
git clone https://github.com/your-username/hotel-booking-analysis.git
cd hotel-booking-analysis
pip install -r requirements.txt
jupyter notebook
