# **Investigate Hotel Business using Data Visualization**

## **Work Environment**
**Tools**                   : Jupyter Notebook
**Programming Languange**   : Python
**Libraries**               : NumPy, Pandas
**Visualization**           : Matplotlib, Seaborn           
**Dataset**                 : [Hotel Bookings](https://github.com/bagusganjarl/hotel-business/blob/7d63a180c4a151c8b22b177eafae24d047ca383f/hotel_bookings_data.csv)

## **Introduction**
A mini project of [Rakamin Academy](https://www.rakamin.com/) from an expert tutor. In this project, as a **Data Scientist** from hotel company has responsibility analyze customer behavior of bookings hotel, cancellation bookings and interprete using Python visualization.

## **Problem Statement**
Business performance in hotel company.

## **Objective**
Investigate hotel business performance to gain insights.

## **Preprocessing**
1. First of all, I do a descriptive statistics. This dataset contains information of hotel bookings by customer.
   <insert image>
   The dataset has 119390 rows and 29 columns with various data type float64(4), int64(16), object(9).
2. Check missing values. After overviewing the dataset, I checked the values of each columns.
   <insert image>
   There are missing values in `company` (94.30%), `agent` (13.68%), `city` (0.40%) and `children` (0.003%) columns. I impute all the missing values with '0' for numericals and 'Unknown' for categoricals.
3. Handle odd value. `meal` column had the unique values Breakfast, Full Board, Dinner, No Meal, Undefined.
    <insert image>
   Undefined indicates same definition to No Meal. So, I replaced the the Undefined value to No Meal. 
4. Handle unnecessary values. I found that some guest are 0 based on the order so in the future I need to analyze the
   guest > 0 only. I make a copy of dataset onto new variable.

## **Analysis**
1. **Monthly Hotel Booking Analysis Based on Hotel Type**
   Observe and analyze growth based on monthly hotlel bookings on hotel type. Both of hotel type tend to be increase in the holiday season. However, amount of City Hotel booking looks decrease on August to September. 
2. **Annual Product Category Quality Analysis**
   Analyze correlation between stay duration towards cancellation hotel rates. City hotel was the highest cancel bookings rate than the Resort Hotel, almost 100%. However, Resort Hotel had the percentage less 50%.
3. **Annual Payment Type Usage Analysis**
   Analyze corelation between lead time towards cancellation rates. Increase of lead time City Hotel will affect to cancellation bookings. Besides, Resort Hotel had fluctuative distribution.