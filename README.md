# HomeValueAI

The dataset utilized for this project was sourced from Zameen.com, Pakistan's premier online real estate marketplace. Leveraging Microsoft SQL Server, we conducted comprehensive data cleaning and analysis to extract pertinent insights. Python served as the primary tool for data preprocessing, feature engineering, and data mining, leveraging key libraries such as Pandas, NumPy, Matplotlib, and Seaborn for effective data wrangling and visualization.

Following meticulous data preparation, the refined dataset underwent machine learning modeling. Employing a repertoire of tools including Scikit-learn, TensorFlow, and Keras, we delved into predictive analytics. Given the regression nature of the dataset, a suite of algorithms including XGBoost, Linear Regression, and Artificial Neural Networks (ANN) were deployed. Remarkably, XGBoost emerged as the optimal choice, exhibiting unparalleled performance with a test accuracy surpassing 90%, thereby outperforming alternative models.

This meticulous process reflects our commitment to delivering robust insights and predictive models in real estate analytics, underscoring our dedication to excellence in data-driven decision-making.

#Libraries/Dependencies:
1. Pandas
2. Numpy
3. Matplotlib
4. Seaborn
5. Plotly
6. Sklearn
7. os

# About Dataset:

#### Property id: The unique value of each Property.
#### Location id: The unique value of each location is based on the subcategory of the city.
#### Page URL: The URL of the page where the property was published.
#### Property type: In this section we have six different types:
1. House
2. FarmHouse
3. Upper Portion
4. Lower Portion
5. Flat
6. Room

#### Price: Price is dependent feature/parameter in this dataset.
#### City: In this dataset total number of cities are five:
1. Lahore
2. Karachi
3. Faisalabad
4. Rawalpindi
5. Islamabad

#### Province: Provice parameter is about the state of the city
#### Location: It is about the different kind of location in each city.

Lastly, Latitude and Longitude of the Cities.



# Step Involved:<br>
1. Statical Analysis<br>
  i. Data Types<br>
  ii. Level of Measurement<br>
  iii. Mean, Standard Deviation, Min, Max<br>
2. Data Cleaning<br>
  i. Filling null values<br>
  ii. Drop the duplicate values<br>
  iii. Correcting the datatypes<br>
  iv. Outliers detection<br>
3. EDA<br>
  i. Seaborn<br>
  ii. Matplotlib<br>
  ii. plotly<br>
4. Model Building<br>
  i. Libraries:<br>
    i.i. Sklearn<br>
    i.ii. pickle <br>
  ii. Models list<br>
    ii.i. Linear Regression<br>
    ii.ii. Decision Tree<br>
    ii.iii. Random Forest<br>
    ii.iv. KNN<br>
    ii.v. XG Boost<br>
    ii.vi. Gradient Boost<br>
    ii.vii. Ada boost<br>
  iii. Select the best that was KNN with 90% accuracy.<br>
  iv. Save it inot pickle file


## SQL
1. Uses Microsoft SQL sever for:<br>
    i. Data Cleaning<br>
    ii. Data Analysis<br>
    
## Visualization:
1. In this section I use Power BI for making graphs.


# Screen Shots

### Application:
<img width="1470" alt="Screenshot 2024-08-30 at 6 47 12 PM" src="https://github.com/user-attachments/assets/c033ec10-1797-4951-a6b6-bd28fbedece6">



### EDA

![newplot (2)](https://user-images.githubusercontent.com/104086680/229906408-2b94758c-00d8-47dd-89f5-9e97c6575898.png)


### Data Analysis in SQL:
![Capture2](https://user-images.githubusercontent.com/104086680/230314514-8d18cf89-db19-410f-bfa6-f772164aec3d.PNG)


### Visualization in SQL:

![Capture1](https://user-images.githubusercontent.com/104086680/230315216-5c182b39-f085-47e5-960c-f62060dba447.PNG)
