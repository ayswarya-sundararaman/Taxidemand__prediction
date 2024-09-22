

# Taxi Demand Prediction in New York City

This project aims to predict taxi demand in various regions of New York City using historical trip data. The model identifies areas with high demand at specific times to improve taxi availability.

## Dataset
- **Source**: New York City Taxi and Limousine Commission (TLC) trip record data (Jan-Mar 2015 and 2016).
- **Features**: Pickup and dropoff locations, trip distance, passenger count, fare, and timestamp.
- **Target**: Predict the number of taxi pickups in specific regions and time intervals.

## Key Techniques
1. **Data Preprocessing**:
   - Removed outliers based on location (outside NYC boundaries), trip duration, speed, and fare.
   - Cleaned data and calculated trip times and speeds.
   - Applied **clustering** (K-Means) on pickup locations to divide NYC into regions.

2. **Clustering**:
   - Created clusters based on pickup coordinates using MiniBatchKMeans.
   - Optimized the number of clusters to ensure spatial granularity.

3. **Time-Series Forecasting**:
   - Grouped pickups into 10-minute intervals (bins).
   - Used historical pickup data to forecast demand in future time bins.
   - Smoothed missing pickup data using averages.

## Results
- **Model Performance**: Achieved accurate predictions for taxi demand in specific regions, helping drivers optimize routes and improve service.
- **Visualizations**: Generated maps showing pickup clusters and time-based demand trends.

## Conclusion
This project helps predict taxi demand at specific locations and times, providing valuable insights for improving taxi availability and reducing wait times for passengers.

