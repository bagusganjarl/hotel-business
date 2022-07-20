# **Investigate Hotel Business using Data Visualization**

## **Work Environment**
**Tools**                   : Jupyter Notebook<br>
**Programming Languange**   : Python<br>
**Libraries**               : NumPy, Pandas<br>
**Visualization**           : Matplotlib, Seaborn<br>
**Dataset**                 : [Hotel Bookings](https://github.com/bagusganjarl/hotel-business/blob/7d63a180c4a151c8b22b177eafae24d047ca383f/hotel_bookings_data.csv)

## **Introduction**
A mini project of [Rakamin Academy](https://www.rakamin.com/) from an expert tutor. In this project, as a **Data Scientist** from hotel company has responsibility analyze customer behavior of bookings hotel, cancellation bookings and interprete using Python visualization.

## **Problem Statement**
Business performance in hotel company.

## **Objective**
Investigate hotel business performance to gain insights.

## **Preprocessing**
1. First of all, I do a descriptive statistics. This dataset contains information of hotel bookings by customer.
   <p align="center">
    <img width="485" alt="Descriptive Statistics of Hotel Bookings" src="https://user-images.githubusercontent.com/103989278/179944979-b00638e8-0ccb-469e-a007-2a0a0dd92d1e.png"> <br>
    Figure 1: Descriptive Statistics of Hotel Bookings Dataset
   </p>
   The dataset has 119390 rows and 29 columns with various data type float64(4), int64(16), object(9).
2. Check missing values. After overviewing the dataset, I checked the values of each columns.
   <p align="center">
    <img width="349" alt="Missing Values" src="https://user-images.githubusercontent.com/103989278/179947510-a956c1aa-e66e-459d-834e-332cdf4067cb.png"> <br>
    Figure 2: Missing Values of Hotel Bookings Dataset
   </p>
   There are missing values in `company` (94.30%), `agent` (13.68%), `city` (0.40%) and `children` (0.003%) columns. I impute all the missing values with '0' for numericals and 'Unknown' for categoricals.
3. Handle odd value. `meal` column had the unique values Breakfast, Full Board, Dinner, No Meal, Undefined. Undefined values
   indicates same definition to No Meal. So, I replaced the the Undefined value to No Meal. 
4. Handle unnecessary values. I found that some guest are 0 based on the order so in the future I need to analyze the
   guest > 0 only. I make a copy of dataset onto new variable.

## **Analysis**
1. **Monthly Hotel Booking Analysis Based on Hotel Type**
   Observe and analyze growth based on monthly hotlel bookings on hotel type. Both of hotel type tend to be increase in the holiday season. However, amount of City Hotel booking looks decrease on August to September.
   <p align="center">
    <img width="969" alt="Screenshot Monthly Hotel Bookings" src="https://user-images.githubusercontent.com/103989278/179950901-e36d3e4c-f60f-4f6b-9617-998847f5764d.png"> <br>
    Figure 3: Distribution of Monthly Hotel Booking Based on Hotel Type
   </p>
2. **Annual Product Category Quality Analysis**
   Analyze correlation between stay duration towards cancellation hotel rates. City hotel was the highest cancel bookings rate than the Resort Hotel, almost 100%. However, Resort Hotel had the percentage less 50%.
   <p align="center">
    ![Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates Visualization](https://user-images.githubusercontent.com/103989278/179948576-c80250a9-119a-467c-afdc-d5aacece6011.png)<br>
    Figure 3: Distribution of Monthly Hotel Booking Based on Hotel Type
   </p>
3. **Annual Payment Type Usage Analysis**
   Analyze corelation between lead time towards cancellation rates. Increase of lead time City Hotel will affect to cancellation bookings. Besides, Resort Hotel had fluctuative distribution.
   <p align="center">
    ![Impact Analysis of Lead Time on Hotel Bookings Cancellation Rate Visualization](https://user-images.githubusercontent.com/103989278/179948770-387c08fe-c473-4b4a-87ad-eb141f5d7e3a.png)<br>
    Figure 3: Distribution of Monthly Hotel Booking Based on Hotel Type
   </p>