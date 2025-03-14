# MIST4610
# MIST_4610 Project 1
Group name:
61608 Group 3


Database name: ha_group3_crn61608
## Team Members
1. Cavanaugh, Rory
2. Chadha, Jasmine
3. McNally, Owen
4. Mulnix, Hayden
5. Nguyen, Timmy
## Problem Discription
Our Starbucks Database is designed to enhance the quality and efficiency of service at our local college coffee shop. It provides a comprehensive view of key operations, including ingredients used in food and beverages, menu offerings, sales transactions, and employee performance. This database enables us to generate valuable insights for improving sales revenue, tracking employee performance, and implementing targeted marketing strategies. With this system, Starbucks management can optimize operations, streamline service, and maximize overall efficiency.


## Data Model
This database models Starbucks' operational efficiency by tracking food and drink sales, ingredient usage, and employee performance. Ingredients are linked to both food and drink entities through a many-to-many relationship, as a single ingredient in inventory can be used in multiple food and drink items. This relationship forms the weak entities food_ingredients and drinks_ingredients, which associate each food or drink item with its corresponding ingredients.


For example, both a Caramel Cold Brew and a Caramel Frappuccino contain sugar and caramel. By structuring the database this way, we enable inventory tracking and supply chain analysis, allowing Starbucks to optimize ingredient management.


Similarly, the receipt entity records food and drink transactions, creating a many-to-many relationship between food and drink items and their sales. The weak entities food_sold and drink_sold capture the food or drink ID and the corresponding receipt(s), enabling the analysis of sales frequency and item demand.


Additionally, the receipt entity is linked to employees through a one-to-many relationship, as one employee can handle multiple sales, but each sale is attributed to a single employee. This structure supports performance evaluation by tracking individual employee contributions to sales. Employee data, including tenure and position, can further be used for workforce analysis.


By leveraging SQL queries, key business insights can be extracted, such as best-selling items, peak sales times, and ingredient consumption patterns, all of which help Starbucks streamline operations and maximize efficiency.
![final_data_model](https://github.com/user-attachments/assets/02b19181-5384-462e-a551-1a46e1444fc7)


## Data Dictionary
<img width="746" alt="image" src="https://github.com/user-attachments/assets/8a8fa056-2902-4572-879e-777e2027e773" />
<img width="745" alt="image" src="https://github.com/user-attachments/assets/3dfe4002-9985-41ea-94ea-b2d4186693ed" />
<img width="745" alt="image" src="https://github.com/user-attachments/assets/8165c274-1f61-4c3b-ab1e-df2434e19206" />
<img width="749" alt="image" src="https://github.com/user-attachments/assets/9aff2883-4c9f-4cf9-9d0e-e9d97bd85366" />
<img width="743" alt="image" src="https://github.com/user-attachments/assets/6b269516-9a1e-45b0-88fb-6233ad32ba10" />


## Simple Queries
## 1
Query 1 displays the receipt ids, total sale value, date of transaction, time of transaction, and employee ids
<img width="317" alt="image" src="https://github.com/user-attachments/assets/c0962d92-e129-44d4-8e05-67310397302f" />


This query provides management insight on transactions during a specified date. Management can analyze how sale price fluctuates throughout the day, as well as the success or failure of certain employees during the day.




## 2
This query displays the total revenue of the Starbucks


<img width="353" alt="image" src="https://github.com/user-attachments/assets/5a520fca-10ec-4f74-953c-07b80bca7eb2" />


Management is able to use this query as a flat numerical value to judge their performance, which can be useful on a broad scale.




## 3
This query lists the foods Starbucks has to offer, order by price in descending order.
<img width="407" alt="image" src="https://github.com/user-attachments/assets/85dac5a9-6055-462c-a5fd-c7a41dd85588" />


This is helpful to management as they are able to identify which products would generate the most revenue. This allows managers to create target promotions to push high priced item.




## 4
This query lists each food item offered, and the ingredients included in that food.
<img width="588" alt="image" src="https://github.com/user-attachments/assets/7a869950-73c8-411a-b5b8-5bd6207c6b95" />


Managers will be able to use this information to track ingredient usage, and ultimately reduce waste. This could also be used to forecast supply needs, as some ingredients may belong to 10+ items versus another ingredient might only belong to 1 or 2.




## Complex Queries
## 1
This query displays the highest sold food item with the most ingredients.


<img width="789" alt="image" src="https://github.com/user-attachments/assets/b15f4bbd-4c64-4347-8c6d-172673c77761" />


This can be useful for management as they are able to clearly identify which food item is their best seller, but is costing them the most in terms of ingredients usage. This could lead management to search for alternative ingredient options that would allow for less waste and a greater profit margin.




## 2
This query displays side by side the food versus drink revenue.


<img width="618" alt="image" src="https://github.com/user-attachments/assets/0b62881e-eca8-45dc-88f3-e3a957072479" />


By breaking down revenue into food sales and drink sales, it allows management to compare performance between these categories.This query is a simple yet powerful tool for Starbucks management to track sales performance, optimize inventory, and improve marketing strategies by analyzing the contribution of food and drinks to overall revenue.


## 3
This query displays the drink name and the corresponding total time it has sold


<img width="672" alt="image" src="https://github.com/user-attachments/assets/fa89290d-a619-4158-ad47-4cb1ef8be3b8" />


By counting the number of times each drink has been sold and organizing the results in descending order, management can quickly identify the most and least popular beverages. This insight helps in menu optimization, allowing decision-makers to determine which drinks should be promoted, discounted, or potentially removed from the menu


## 4
This query displays the employees name and id as well as how long they have worked at the starbucks and the total sales they have generated.


<img width="1045" alt="image" src="https://github.com/user-attachments/assets/74ffd196-0d4c-4bab-8732-811e963d1228" />


This query would prove to be beneficial to Starbucks management as it provides valuable insights into employee performance and experience. By displaying each employee's total sales alongside their tenure, managers can assess how experience correlates with sales performance. Employees with longer tenure may be expected to generate higher sales due to their familiarity with products and customer service skills. However, if newer employees are performing equally well or better, it could indicate strong training programs or highlight high-performing individuals who may be suited for leadership roles


## 5
This query specifically retrieves the total revenue generated by each employee from food sales on March 10, 2024 and ranks them in descending order.


<img width="655" alt="image" src="https://github.com/user-attachments/assets/2fe9da71-dde9-4acb-9a94-caee72580cdc" />


While this specific example is limited to March 10, 2024 the query can be edited to pull up any date of operations. The query also identifies the maximum revenue earned by an employee on a given day, making it a clear easy process to highlight top performers and optimize staffing decisions based on revenue contribution.


## 6
This query shows the total number of hours worked, sales made, revenue acquired, and average revenue per sale for each hour in a given day.


<img width="868" alt="image" src="https://github.com/user-attachments/assets/0bd00d52-88af-405d-9dff-07ba59687ea8" />


This query would help Starbucks identify peak and slower hours, allowing them to prepare for better staffing and inventory management. By identifying and understanding hourly sales trends, the Starbucks on Alps can optimize scheduling and promotions to maximize revenue.


## Database Information
<img width="1051" alt="image" src="https://github.com/user-attachments/assets/d3ebd29d-7bf0-438b-a4ef-cdcca6793564" />
