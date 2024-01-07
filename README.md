# Restaurants Sales Analysis

## Author: Chao Gao

Git-hub repository at: 
https://github.com/Chaoccz/RestaurantsSalesAnalysis

- Jupyter notebook: **Restaurants Sales During COVID.ipynd**
- Data Set: Top250.csv, Independence100.csv, Future50.csv, Food_Supply_Quantity_kg_Data.csv

  ![28](images/28.png)

# Table of contents
1. [Introduction](#introduction)

2. [Feature Engineering](#sec2)
     1. [Null Values Checking](#sec2p1)
     2. [Renaming Columns, Casting](#sec2p2)
     3. [Making Category Feature](#sec2p3)

3. [EDA Data Visualization](#sec3)
     1. [Year on Year Distribution](#sec3p1)
     2. [Correlation with Sales](#sec3p2)
     3. [Year on Year Sales Indicator](#sec3p3)
     4. [Restaurant Category and Sub Category](#sec3p4)
     5. [Category Sales Indicator](#sec3p5)

4. [Top Resturants in Best Category](#sec4)
     1. [Pizza](#sec4p1)
     2. [Burger](#sec4p2)
     3. [Varied Menu](#sec4p3)
     4. [Family](#sec4p4)
     5. [Meat](#sec4p5)
     6. [Mexican](#sec4p6)
     7. [Cafe](#sec4p7)
     8. [Sandwich](#sec4p8)
     9. [Chicken](#sec4p9)
     10. [Drinks](#sec4p10)

5. [Top 50 Future Restaurants](#sec5)
     1. [Overview](#sec5p1)
     2. [Franchising Or Not](#sec5p2)
     3. [Franchising Or not/Sales](#sec5p3)
     4. [Correlation with YoY Sales](#sec5p4)

6. [Relationship between Diet and Corona](#sec6)
     1. [Correlation](#sec6p1)
     2. [Confirmed Cases and Veg products](#sec6p2)
     3. [Vegan vs Animal](#sec6p3)
     4. [PairGrid](#sec6p4)

7. [Conclusion](#sec7)

## 1. Introduction <a name = 'introduction'></a>
The data was obtained by means of web scraping, i.e. data download with the use of programming code based on the website code. In this case, the "rvest" package from the R programming language was used along with the "SelectorGadet" browser add-on to facilitate work with the website.

The data was downloaded from www.restaurantbusinessonline.com on January 30, 2021 with three plants describing 3 rankings: top 250, top 100 indenents and future 50 thus creating 3 tables, where the restaurant is described by several variables in each row.

The data can be used to tell the story of what 2020 was like for restaurants, what was hot, what could be more popular soon, or what the difference is between large companies and smaller businesses. I am curious what useful information can be obtained from this data!

We will try through theses datasets to know how restaurants act during Covid-19, what makes difference with sales during covid, peoples food behaviour during 2020 and how it's affecting on future restaurants

## 2. Feature Engineering <a name = 'sec2'></a>
In this section, I will be doing **Feature Engineering** on the dataset. That includes Adding, Deleting, Combining, Mutating and Handling missing data. Here is a brief information of the dataset: 

![1](images/1.png)
### 2.1 Null Values Checking <a name = 'sec2p1'></a>
As we can see, there's no missing values in the dataset:

![2](images/2.png)

### 2.2 Renaming Columns, Casting <a name = 'sec2p2'></a>
I renamed Units to Branches, Segment_Category to sub_category, Converted percentags(YOY_Sales, YOY_Units) to floats, Checked there is no independence restaurant in top 250:

![3](images/3.png)

### 2.3 Making Category Feature<a name = 'sec2p3'></a>
I made a new column called category according to the column sub_category, that way, the category is more concise and accurate:

![4](images/4.png)

## 3. EDA Data Visualization <a name = 'sec3'></a>
In this section, we will try to figure out what happend to Top Resturants Sales During 2020 and Extracting Imformative insights
### 3.1 Year on Year Distribution <a name = 'sec3p1'></a>
These Distributions shows us that year on year sales percentage no more than 40%:

![5](images/5.png)

### 3.2 Correlation with Sales <a name = 'sec3p2'></a>
Sales High Correlated with Branches: 

![6](images/6.png)

### 3.3 Year on Year Sales Indicator <a name = 'sec3p3'></a>
Although the restaurants were on the best list during the year, about 35% of restaurants had negative indicators:

![7](images/7.png)

### 3.4 Restaurant Category and Sub Category <a name = 'sec3p4'></a>
Sunburst shows that quick-service subcategory always get high sales:

![8](images/8.png)

### 3.5 Category Sales Indicator <a name = 'sec3p5'></a>
Varied menu, sandwiches and sports bar had negative indicators more than positive:

![9](images/9.png)

## 4. Top Resturants in Best Category <a name = 'sec4'></a>
In this section, we will continue exploring top resturants in each categories using EDA

### 4.1 Pizza <a name = 'sec4p1'></a>

![10](images/10.png)

### 4.2 Burger <a name = 'sec4p2'></a>

![11](images/11.png)

### 4.3 Varied Menu <a name = 'sec4p3'></a>

![12](images/12.png)

### 4.4 Family <a name = 'sec4p4'></a>

![13](images/13.png)

### 4.5 Meat <a name = 'sec4p5'></a>

![14](images/14.png)

### 4.6 Mexican <a name = 'sec4p6'></a>

![15](images/15.png)

### 4.7 Cafe <a name = 'sec4p7'></a>

![16](images/16.png)

### 4.8 Sandwich <a name = 'sec4p8'></a>

![17](images/17.png)

### 4.9 Chicken <a name = 'sec4p9'></a>

![18](images/18.png)

### 4.10 Drinks <a name = 'sec4p10'></a>

![19](images/19.png)

## Insights

1. Number Branches is The Highest Correlated With Sales
2. 35% YOY for Top Restaurants are Negative
3. Burger Restaurants is the highest Sales in 2020
4. Quick Service is an optimal solution to get high sales
5. Sports Bar and Sandwich Restaurants face Big losses

## 5. Top 50 Future Restaurants <a name = 'sec5'></a>
In this section, we will explore the top 50 future restaurants and extract information from the plots

### 5.1 Overview <a name = 'sec5p1'></a>
Here is a brief information of the dataset:

![20](images/20.png)

### 5.2 Franchising Or Not <a name = 'sec5p2'></a>
58% of the restaurants are a franchise, and 42% are not a franchise:

![21](images/21.png)

### 5.3 Franchising Or not/Sales <a name = 'sec5p3'></a>
Restaurants that are a franchise have more sales than non-franchise ones:

![22](images/22.png)

### 5.4 Correlation with YoY Sales <a name = 'sec5p4'></a>
Year on Year Sales is not highly correlated with other attributes:

![23](images/23.png)

## 6. Relationship between Diet and Corona  <a name = 'sec6'></a>
**Is diet Related to your Infection with Corona?** 

Now we are trying to find if there is a relationship between some food products and the high rates of infection with the Coronavirus

### 6.1 Correlation <a name = 'sec6p1'></a>

![24](images/24.png)

### 6.2 Confirmed Cases and Veg products <a name = 'sec6p2'></a>
we will notice here the negative correlation between confirmed cases and veg_product:

![25](images/25.png)

### 6.3 Vegan vs Animal <a name = 'sec6p3'></a>
We note here that vegan products have an inverse relationship with the number of Confirmed cases (-0.5) , unlike animal products(+0.6), and this is a logical explanation for why evergreens restaurant was the most increase in sales rates during the Corona pandemic:

![26](images/26.png)

### 6.4 PairGrid <a name = 'sec6p4'></a>

![27](images/27.png)

## 7. Conclusion <a name = 'sec7'></a>
1. During The corona pandemic, The Most were eating organic food
2. Restaurants That rely on gatherings have faced significant losses
3. Number of branches forms a big difference in sales, it helps to provide Quick Services
4. It is worth relying on franchising for its high potential in achieving high sale
5. Going Vegan Can Reduce Severity Of COVID-19

![29](images/29.png)
