# witcher
Witcher is an automated, driverless tool to build an errorfree machine learning application.


Witcher is an automated AI application designed to speed up the data processing phases.
The current witcher's magical-recommender-system will provide you with a comprehensive product recommendation using product popularity, product similarity and user similarity models.
 
Magical data processing, predictive, and deep learning models will be joining witchers functions very soon :)

hope you will enjoy using the witcher library

Thank you. 

Babak.EA


How to run : 

<b> using Jupyter notbook </b> 

import witcher

witcher.recommender_system()

needs 3 dataset including:

df_C_Per_Product

ProductCode	ProductName	product_category 	CustomerCount

0	a	SPL Credit Life Insurance		INSURANCE	85613

1	b	Scotia Plan Loan				BORROWING	83512

2	c	SPL Credit Health Insurance		INSURANCE	79696

3	d	Savings Account					DAYTODAY	62850

4	e	Everyday Banking 				DAYTODAY	5840


<hr>

df_C_NPS_Extend

CustomerID	ResponseDate	CustomerScore	StatedIncome	CustomerSinceDate

User1		2020-02-01		10					10000		2008-01-01

User1		2020-04-01		8					2000		2008-01-01

User1		2020-01-01		7					1500		2008-01-01

User1		2019-02-01		9					1000		2008-01-01

<hr>


df_C_NPS_Product

CustomerID	RewardDollarValue	ProductCode	ProductName	product_category 

0	User1	0.00		d	Small Business CMS			DAYTODAY

2	User1	130000.00	y	Small Business Term Loan	BORROWING

3	User1	23870.00	y	Small Business Term Loan	BORROWING

4	User1	172017.00	y	Small Business Term Loan	BORROWING

5	User2	160960.00	y	Small Business Term Loan	BORROWING

<hr>
<hr>

Generate the model : 

Model_Generator(df_C_Per_Product,df_C_NPS_Product,df_C_NPS_Extend)


### recommender system 
help(Product_Recommender)

Product_Recommender(userId) like 

product=Product_Recommender("user1")


product.report: is a JSON API file provides a comprehensive vision 


Model_Generator(
        "df_C_Per_Product=Dataset including Product information like Id, name, domain, popularity, count",
        "df_C_NPS_Extend: dataset including user raw's information, user ID, product ID",
 |      "df_C_NPS_Products: user info , Income, and rating"
 |      ProductCode, Customer_ID are columns name to help the AI to read the dataset,
 |      CustomerCount: count product, group by customer ID,
 |      pr_category: what category products belong like small business, daytoday, ..., 
 |      limit=0.8: the ratio for the similarity between products 
 |      ,knn_neighbors=100: number of similar users based on products and activities)



class Product_Recommender(builtins.object)
 |  Product_Recommender(USER_ID, Customer_ID='USER_ID', Model_path='./model/', Report_path='./report/', Limit=0.8)






source code : github

https://github.com/BabakEA/witcher


PyPi : https://pypi.org/project/witcher/0.0.1/
pip install witcher
