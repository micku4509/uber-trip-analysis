Uber Trip Analysis – Power BI Project
Project Overview

This project focuses on analyzing Uber trip data using Power BI to uncover trends in booking patterns, revenue, and travel behavior.
The goal was to build a fully interactive dashboard that provides key insights into total bookings, trip distance, fare value, payment type, and time-based ride demand.
It demonstrates the complete Power BI workflow — from data cleaning and modeling to DAX calculations and visualization design.

Objectives

Understand total and average trip metrics (bookings, distance, and fare value)

Identify high-demand hours, days, and regions

Compare performance by vehicle type and payment method

Highlight top pickup/drop-off locations

Enable dynamic user interactions through DAX and bookmarks

Tools & Technologies Used

Power BI Desktop – for visualization and DAX-based modeling

Power Query – for data cleaning and transformation

Microsoft Excel – as the data source

DAX (Data Analysis Expressions) – for KPI calculations and logic building

Data Model

The data model follows a star schema with one fact table and multiple dimension tables:

Fact Table: Trip Details

Dimension Tables: Calendar Table, Location Table, Dynamic Measures Table

Relationships:

Trip Details[Pickup Date] → Calendar[Date] (Active)

Trip Details[PULocationID] → Location[LocationID] (Active)

Trip Details[DOLocationID] → Location[LocationID] (Inactive – used via USERELATIONSHIP)

DAX Measures Highlights

Total Bookings: COUNT('Trip Details'[Trip ID])

Total Booking Value: SUM('Trip Details'[Booking Value])

Avg Booking Value: DIVIDE([Total Booking Value], [Total Bookings])

Total Trip Distance: SUM('Trip Details'[trip_distance])

Farthest Trip: Finds max trip distance and returns pickup/drop-off locations

Trip (Day/Night): Categorizes trips by time of day

Dynamic Measures Table: Enables switching KPIs using slicers and bookmarks

Dashboard Features

KPIs for bookings, distance, and fare performance

Dynamic measure switching with slicers and DAX logic

Drill-through functionality for trip-level exploration

Interactive slicers for city, payment type, vehicle type, and time

Calendar table for weekday and hourly trend analysis

Navigation buttons (Home, Info, Refresh, LinkedIn) for smooth user experience

Key Insights

Total Bookings: ~103,700

Total Revenue: ~$1.6M

Average Trip: 3 miles, 16 minutes, $15 fare

Peak Hours: 6–9 AM and 5–8 PM

Payment Mode: Uber Pay used in 70%+ of transactions

Top Vehicle Type: UberX

Weekend Demand: 25% higher than weekdays

Files in Repository

Uber_Trip_Analysis.pbix → Power BI Dashboard

Uber_Trip_Analysis_Report.pdf → Full Project Documentation

Dashboard_Overview.png → Dashboard Screenshot

Business Impact

This dashboard helps business and operations teams:

Identify peak ride hours and plan driver schedules efficiently

Monitor revenue trends and optimize pricing

Track city-wise and vehicle-type performance

Improve decision-making through clear visual insights

Author

Himanshu Patra
Aspiring Data Analyst | SQL | Power BI | Excel | Python
📧 Email: himanshupatra3443@gmail.com

🔗 LinkedIn
https://www.linkedin.com/in/himanshu-patra-9569262575patra/

Live Preview / Download
You can download and explore the .pbix file directly from this repository.
The dashboard is built for learning and demonstration purposes.

## Dashboard Preview 1
![Uber Trip Dashboard](https://github.com/user-attachments/assets/e23a4849-2741-42ab-a907-4c4e5cc62d9f)
## Dashboard Preview 2
![Uber Trip Dashboard](https://github.com/user-attachments/assets/c7df9135-ac09-4bbc-b082-8f3aa062f82d)
## Dashboard Preview 3
![Uber Trip Dashboard](https://github.com/user-attachments/assets/9673de47-0b85-4145-9aa5-f16850af7f97)

