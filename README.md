# Hotel Booking Analysis - Power BI & Excel Data Project

This repository contains the Excel dataset, Power BI theme configuration, and documentation for the **Hotel Booking Analysis Project**.

---

## 📁 Repository Contents

1. **`HotelBookingAnalysis.xlsx`**: Excel workbook containing processed hotel booking records.
2. **`Hotel_Bookings_CLEANED_FullDataset.csv`**: Full cleaned dataset (87,232 records) ready for Power BI import.
3. **`Hotel_Bookings_RAW_Dataset.csv`**: Original raw dataset.
4. **`HotelBookingAnalysis_PowerBI_Theme.json`**: Custom Power BI theme JSON color scheme.
5. **`Hotel_Booking_Analysis_Project_Documentation.docx`**: Project overview documentation.

---

## 📊 Key DAX Measures

```dax
// 1. Total Revenue
Total Revenue = SUM(HotelBookings[total_revenue])

// 2. Total Bookings
Total Bookings = COUNT(HotelBookings[hotel])

// 3. Cancellation Rate (%)
Cancellation Rate = 
DIVIDE(
    CALCULATE(COUNT(HotelBookings[is_canceled]), HotelBookings[is_canceled] = 1),
    COUNT(HotelBookings[is_canceled]),
    0
)

// 4. Average Daily Rate (ADR)
Average ADR = AVERAGE(HotelBookings[adr])

// 5. Total Guests
Total Guests = SUM(HotelBookings[total_guests])
```

---

## 🎨 Power BI Setup Instructions
1. Open Power BI Desktop and click **Get Data** -> **Text/CSV** or **Excel Workbook**.
2. Load `Hotel_Bookings_CLEANED_FullDataset.csv` or `HotelBookingAnalysis.xlsx`.
3. Apply the custom theme via **View** -> **Themes** -> **Browse for themes...** -> Select `HotelBookingAnalysis_PowerBI_Theme.json`.
4. Build the charts (Line Chart for Monthly Revenue, Donut Chart for Hotel Type, Pie Chart for Market Segment, Bar Chart for Country Analysis).
