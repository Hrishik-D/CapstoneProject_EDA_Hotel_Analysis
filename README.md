# Hotel Bookings Exploratory Data Analysis

The project contains the real world data record of hotel bookings of a city and a resort hotel containing details like bookings, cancellations, guest details etc. from 2015 to 2017. In this project we are going to analyze Hotel Booking Data in order to find out valuable insights and give suggestions to increase revenue of hotels.

Programming Language : Python

Libraries used : Pandas, Numpy, Matplotlib, Seaborn

NoteBook : Google Colab

Dataset Source : Provided by Almabetter.


## Problem Statement
The main objective is to explore the given dataset and discover the factors which govern the bookings. The dataset will be analyzed and from the conclusions drawn from it will be used to recognize the missteps taken by the manager. With this information, hotels will be equipped to improve their performance.

## Dataset
We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.

```
- hotel: Name of hotel ( City or Resort)
- is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
- lead_time: time (in days) between booking transaction and actual arrival.
- arrival_date_year: Year of arrival
- arrival_date_month: month of arrival
- arrival_date_week_number: week number of arrival date.
- arrival_date_day_of_month: Day of month of arrival date
- stays_in_weekend_nights: No. of weekend nights spent in a hotel
- stays_in_week_nights: No. of weeknights spent in a hotel
- adults: No. of adults in single booking record.
- children: No. of children in single booking record.
- babies: No. of babies in single booking record. 
- meal: Type of meal chosen 
- country: Country of origin of customers (as mentioned by them)
- market_segment: What segment via booking was made and for what purpose.
- distribution_channel: Via which medium booking was made.
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for 
                     Yes)
- previous_cancellations: No. of previous canceled bookings.
- previous_bookings_not_canceled: No. of previous non-canceled bookings.
- reserved_room_type: Room type reserved by a customer.
- assigned_room_type: Room type assigned to the customer.
- booking_changes: No. of booking changes done by customers
- deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
- agent: Id of agent for booking
- company: Id of the company making a booking
- days_in_waiting_list: No. of days on waiting list.
- customer_type: Type of customer(Transient, Group, etc.)
- adr: Average Daily rate.
- required_car_parking_spaces: No. of car parking asked in booking
- total_of_special_requests: total no. of special request.
- reservation_status: Whether a customer has checked out or canceled,or not showed 
- reservation_status_date: Date of making reservation status.
```

- Total number of rows in data: 119390
- Total number of columns: 32

## Data Cleaning and Feature Engineering

### (1) Removing Duplicate rows
All duplicate rows were dropped.

### (2) Handling null values
- Null values in columns `company` and `agent` were replaced by 0.
- Null values in column `country` were replaced by 'others'.
- Null values in column `children` were replaced by the mean of the column.
  

### (3) Converting columns to appropriate data types

- Changed data type of `children`, `company`, `agent` to int type.
- Changed data type of `reservation_status_date` to date type.

### (4) Removing outliers

- One outlier was found in the `adr` column. Simply dropped it.

### (5) Creating new columns
- Created new column `total_stay` by adding `stays_in_weekend_nights`+`stays_in_week_nights`.
- Created new column `total_people` by adding `adults`+`children`+`babies`.


## Exploratory Data Analysis

Performed EDA and tried answering the following questions:

```
   1. What is the Percentage of bookings in each hotel?
   2. What is the percentage of cancellation ?
   3. How adr varies with total stays and finding the outlier ?
   4. How  ADR varies with Arrival Month Which are the most busy months? 
   5. Which agent makes the most no. of bookings?
   6.From which country most of the guests are coming ?
   7. Which room type is in most demand and which room type generates the  highest adr?
   8. which is the most liked meal ?
   9. Which hotel generated highest ADR ?
   10. Which distribution channel makes highest booking ?
   11. Number of cancellation for different hotel
   12. Which distribution has highest cancel percentage ?
   13. Does a  longer waiting period or longer lead time causes the cancellation of bookings?
   14.Are the guest returning after stay ?
   15. How does different parameter depend on each other which can help in business ?
    

Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:
   - Bar Plot.
   - Histogram.
   - Scatter Plot.
   - Pie Chart.
   - Line Plot.
   - Heatmap.
   - Box Plot.
   - Pair Plot.
   - KDE plot
  
```
## Challenges and Suggestion

```
Attract Longer Guest Stays: To encourage longer guest stays, consider offering competitive pricing for extended durations, such as weekly or monthly rates. Provide special packages or discounts for guests who book longer stays, making it economically attractive for them to stay longer.

Differentiate Services for Resort and City Hotels: Resort hotels should focus on enhancing recreational activities and services to attract more customers seeking leisure and relaxation. City hotels should continue providing high-quality services to maintain their competitiveness in urban markets.

Optimize Resource Allocation: Utilize historical cancellation data to allocate resources like staff and inventory more efficiently, especially during periods of lower occupancy. Implement dynamic pricing strategies to adjust room rates based on occupancy and demand, which can help maximize revenue.

Reduce Cancellations: Investigate reasons for reservation cancellations, and use this information to adjust pricing strategies, offer promotions, or revise policies to minimize cancellations. Develop customer retention strategies, such as loyalty programs, referral incentives, and special offers for returning customers.

Utilize ADR for Revenue Estimation: Continuously monitor Average Daily Rate (ADR) trends throughout the year to estimate revenue potential for different seasons. Use ADR insights to create budgets and financial plans that align with expected revenue fluctuations.

Partner with Travel Agents and Tour Operators: Collaborate with travel agents (TAs) and tour operators (TOs) to increase bookings, especially if they have an established customer base. Negotiate mutually beneficial partnerships with TAs and TOs, offering them competitive rates and special deals to attract more bookings.

Identify Top-Performing Agents: Identify the most successful travel agents and build strong relationships with them. Co-market with these agents, create special promotions, and provide exclusive deals to increase bookings through their channels.

Target High-Booking Countries: Identify countries with the highest number of bookings and focus marketing and expansion efforts in those regions. Allocate resources efficiently, such as offering customer support in commonly booked languages to enhance the guest experience.

Include Breakfast Options: Offer a Bed and Breakfast (B&B) option, as it can attract more guests looking for a convenient and cost-effective way to start their day. Promote this option prominently on your booking platforms and website.

Understand Booking Cancellation Patterns:

While the waiting period may not significantly affect booking cancellations, continue monitoring and analyzing booking data to identify other factors influencing cancellations.
Adapt cancellation policies and strategies accordingly to further reduce cancellations.

```

## Challenges
```
(1) Lot of null values were present in the dataset.
(2) Data type of some Data was in wrong format.
(3) Lot of duplicate data.
(4) Which visualization techniques to use was a challenge?

```
