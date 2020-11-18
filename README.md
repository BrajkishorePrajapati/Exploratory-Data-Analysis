This repository consists of Exploratory Data Analysis and Hypothesis testing notebooks on different competitions of Kaggle and Analystics Vidhya.<br>
The files in this repository will provide an effective way of performing EDA and Hypothesis testing in Real time projects and helps to get a better intuition
of the data.<br>
This Exploratory data analysis helps to get important insights from the data and can make the better decsion based on this and also helps to get some preprocessing ideas,
which ultimately improve the model performance.

# 1. Introduction to problem statement
## Sales Prediction for Big Mart Outlets:
The data scientists at BigMart have collected 2013 sales data for 1559 products across 10 stores in different cities. Also, certain attributes of each product and store have been defined. The aim is to build a predictive model and predict the sales of each product at a particular outlet.<br>

Using this model, BigMart will try to understand the properties of products and outlets which play a key role in increasing sales.<br>

Please note that the data may have missing values as some stores might not report all the data due to technical glitches. Hence, it will be required to treat them accordingly.<br>

## **2. Hypothesis generation with respect to problem statement.**

1. Item weight might effect a sales of the product.
2. Sales of the product may be depends on the items fat content.
3. More Item_Visibility of a particular product may be costlier than other products.
4. Item type could have an effect on the sales.
5. Are the items with more MRP have more item outlet sales.
6. Are the stores which have established earlier have more sales.
7. Size of the stores could have an effect on the item sales at a particular store.
8. Location of the stores might depends on the Item outlet sales.
9. Are the supermarkets have more sales than others.

After this successfully uploaded the dataset and did some variable identification and type casting needed. 

### **3 Numerical Features:**
* Item_Weight
* Item_Visibility
* Item_MRP
* Item_Outlet_Sales(Target Variable)

### **4ategorical Features**
* Item_Identifier
* Item_Fat_Content(Ordinal Feature)
* Item_Type
* Outlet_Itemtifier
* Outlet_Establishment_Year
* Outlet_Size(Ordinal Feature)
* Outlet__Location_Type(Ordinal Feature)
* Ootlet_Type(Ordinal Feature)

**Observations:**
* There are 4 float type variables, 1 integer type and 7 object type.
* We are considering Item_Establishment_Year as a categorical feature because it contains some fixed value but not converting its data type now will consider later.
* Item_Fat_Content, Outlet_Size, Outelet_Location_Type and Outlet_Type are ordinal features because these values can be arranged in some order.

## **5 Summary of Uniariate Analysis**

### **Important Observations:**
* Numerical<br>
    * The weight of the items lies in the range of 4 - 22 while the average weight of the items is 12.
    * There are some items that are not visible at all and the maximum visibility of the item is 33%.
    * The price of the items range in between Rs 31 - 265. The most expensive item in the stores is of Rs 266.89.
    * Most of the stores are established in year from 1985-1990 and 1995 to 2000.
    * From year 1990-1995 was ver bad time for people who wants to open the new store. No stores were established in between this period.
    * Most of the stores has a maximum sales in between 450 - 3900. Only few of the stores having sales more than 6000. 
  
* Categorical<br>
     *  Around 64% of the total items contains low fat while remaining contains regular fat.
     * More than 14%(ie more than 1200 items) are fruits & vegetables and snacks and foods.
     * Sale of breakfast and seafood type of items are very less.
     * All the stores are selling almost same number of items except the OUT010 and OUT019 stores.
     * 45% of the total number of items are sell from medium size store while only 15% items are sell from store which are very big.
     * 39% of the items sells from the stores laocated in Tier 3 cities, while 32% and 28% items are sells from the stores located in Tier 2 and Tier 1 cities.
     * 65% of the items are sell from Supermarket Type 1 whih is almost twice the other types of stores. i.e most of the customers prefer to buy the items from the Supermarket Type 1 stores.

* Missing Values
     * Since the percentage of missing values is very high so we can't drop these values otherwise we can miss some important information. Only way is to handle the missing values using some technique.

### **Things to investigate further in Bivariate Analysis.**
* Are the items with less visibility having more sales.
* Check whether the store Id OUT010 and OUT019 are recently opened store and if not then why they have sale the less number of items.
* Are the items contains low fat have more sales than the items contains regular fat.
* Are the stores with medium size have high sale than others.
* Are the stores located in Tier 3 cities have more sale than other.
* Are the Supermarket Type 1 type of stores have more sales than other type of stores.
* Do the missing values of Item weight have some relation with sales of the items or any other feature.
* Do the missing values of Outlet size have some relation with any other feature.

## **6 Summary of Bivariate Analysis**
* ### **Numerical- Numerical**
    * Item_MRP is somewhat correlated with Item_Outlet_Sales. So Item_MRP can be important feature for predicting Item_Outlet_Sales at particular store.
    * Increase in the item_visibility can decrease the item outlet sales because it is having negative correlation.
    * Item weight and Item_Establishment_Year does not have any realationship with Item_Outlet_Sales.

* ### **Numerical-Categorical**
    * There is no significance difference in the Item Outlet sales based on Item Weight so Item weight migh not be the much important for predicting sales. But there may be if be treat 'low fat' , 'LF' as 'Low Fat' and 'reg' as 'Regular'
    * The distribution of Item Fat Content is slightly right skew.
    * There is a significance difference in the Item Outlet sales of different item types. So this can be important for predicting Item Outlet sales.
    * Dairy products have the higher Item Outlet sales than others.
    * Yes there is a significance difference between Item Outlet Sales of stores with different Outlet Size.
    * Medium size stores have more Item Outlet sales than others, while the small size stores have the least Item Outlet sales.
    * Mean Item Outlet sales of the 'Medium' Outlet size is above 2500 while that of 'High' is below 2500 and 'Small' is of below 2000.
    * There is a significance difference between the Item Outlet Sales of stores of different Outlet Location Type.
    * Tier 2 cities have most sales while Tier 1 cities least sales. 
    * The average sale of Tier 2 cities is 2324 while that of Tier 2279.
    * * There is a significance difference between the Item Outlet Sales of stores of different Outlet Type.
    * No the supermarket Type 1 does not have the more sales than others
    * Supermarket type 3 have more sales than others and the average sales of the Supermarket Type 3 is 3694.
    * Grocery stores has the least Item Outlet sales.
    * There is a significance difference on the Item Outlet Sales of different stores based on store Id i.e Outlet Identifier.
    * Sales of OUT049 comes from the items whose average sales lies between 200-1000.

* ## **Missing values**
   * OUT027 and  OUT019 does not show the plot, so it is confirm that the missing information of Item Weught comes from the store ID OUT027 and OUT019.

Note - In this notebook, I have not perform Categorical- Categroical Analysis.


