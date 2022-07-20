# **Investigate Hotel Business using Data Visualization**

## **Work Environment**
**Tools**                   : Jupyter Notebook<br>
**Programming Languange**   : Python<br>
**Libraries**               : NumPy, Pandas<br>
**Visualization**           : Matplotlib, Seaborn<br>
**Dataset**                 : [Hotel Bookings](https://github.com/bagusganjarl/hotel-business/blob/7d63a180c4a151c8b22b177eafae24d047ca383f/hotel_bookings_data.csv)

## **Introduction**
A mini project created by an expert tutor of [Rakamin Academy](https://www.rakamin.com/). In this project, as a **Data Scientist** from hotel company had responsibility analyze customer behavior of bookings hotel, cancellation bookings, and interprete the analysis using Python visualization.

## **Problem Statement**
Investigated hotel business performance with ability to reach the market **based on months**, **stays duration**, and **lead time** towards **cancellation bookings**.

## **Objective**
Created a **data-driven visualization** become **insights** for hotel business.

## **Preprocessing**
1. First of all, I did a **descriptive statistics**. This dataset contains information of hotel bookings by customer. The dataset
   has 119390 rows and 29 columns with various data type float64(4), int64(16), object(9).
   <p align="center">
    <img width="485" alt="Descriptive Statistics of Hotel Bookings" src="https://user-images.githubusercontent.com/103989278/179944979-b00638e8-0ccb-469e-a007-2a0a0dd92d1e.png"> <br>
    Figure 1: Descriptive Statistics of Hotel Bookings Dataset
   </p>
2. **Checked missing values**. After overviewing the dataset, I checked the values of each columns. There are missing values in
   `company` (94.30%), `agent` (13.68%), `city` (0.40%) and `children` (0.003%) columns. I impute all the missing values with '0' for numericals and 'Unknown' for categoricals.
   <p align="center">
    <img width="349" alt="Missing Values" src="https://user-images.githubusercontent.com/103989278/179947510-a956c1aa-e66e-459d-834e-332cdf4067cb.png"> <br>
    Figure 2: Missing Values of Hotel Bookings Dataset
   </p>
3. **Handled odd values**. `meal` column had the unique values **Breakfast**, **Full Board**, **Dinner**, **No Meal**,
   **Undefined**. **Undefined** values indicate same definition to **No Meal**. So, I replaced the the **Undefined** values to **No Meal**. 
4. **Handle unnecessary values**. I found that some guest are 0 based on the order so in the future I need to analyze the
   guest **> 0** only. I make a copy of dataset onto new variable.

## **Analysis**
1. **Monthly Hotel Booking Analysis Based on Hotel Type**<br>
   Observe and analyze growth based on monthly hotlel bookings on hotel type. Both of hotel type tend to be increase in the **holiday season**. However, amount of **City Hotel** booking looks decrease on **August to September**.
   <p align="center">
    <img width="969" alt="Screenshot Monthly Hotel Bookings" src="https://user-images.githubusercontent.com/103989278/179950901-e36d3e4c-f60f-4f6b-9617-998847f5764d.png"><br>
    Figure 3: Distribution of Monthly Hotel Booking Based on Hotel Type
   </p>
2. **Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates**<br>
   Analyze correlation between **stay duration** towards **cancellation hotel rates**. **City hotel** was **the highest** cancel bookings rate than the **Resort Hotel**, **almost 100%**. However, **Resort Hotel** had the percentage **less 50%**.
   <p align="center">
    <img width="935" alt="Stays of Duration" src="https://user-images.githubusercontent.com/103989278/179952444-3a2ee944-8a2d-4807-a475-562c2cc815d2.png"><br>
    Figure 4: Distribution of Stays Duration on Hotel Bookings Cancellation Rates 
   </p>
3. **Impact Analysis of Lead Time on Hotel Bookings Cancellation Rates**<br>
   Analyze correlation between **lead time** towards **cancellation rates**. Increase of lead time **City Hotel** will affect to **cancellation bookings**. Meanwhile, **Resort Hotel** had **fluctuative** distribution.
   <p align="center">
    <img width="842" alt="Screenshot Lead Time" src="https://user-images.githubusercontent.com/103989278/179953921-47f1c0b2-cdc8-468e-8dac-27976d3420dd.png"><br>
    Figure 5: Distribution of Lead Time on Hotel Bookings Cancellation Rates
   </p>