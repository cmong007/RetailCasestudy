**<h1> Retail Case Study </h1>**


<h2><ins> Company Background: </ins></h2>

PetMind is a nationwide pet product retailer in the United States. With inflation hitting 41-year highs, the company is planning to reduce the cost of customer retention by improving brand loyalty. The first strategy is to launch a monthly pet box subscription in three months. The marketing team is preparing a list of popular products for the pet box subscription. The chief marketing officer wants to know whether the list should only include the products being purchased more than once.

<h3><ins> Questions: </ins></h3>

- How many products are being purchased more than once?
- Do the products being purchased again have better sales than others?
- What products are more likely to be purchased again for different types of pets?  

<h4><ins> Exploring the dataset </ins></h4>
<img src = 'https://github.com/cmong007/retailcasestudy/assets/135245393/0a2ed5cf-5d40-4ebc-a5ef-e911b113291b'/>

Looks like there are 879 records.

<br>  Columns:

-  "product_id" - unique identifier of product
-  "product_category" - 1 out of 11 product category
-  "sales" - the dollar amount of sales made last year
-  "price" - the price of product
-  "vendor_id" - unique identifier of vendor
-  "pet_size" - 1 out of 5 category of pet size
-  "pet_type" - 1 out of 4 type of pets : cat,dog,fish,bird
-  "rating" - customer's rating on a 10 point scale
-  "re_buy" - binary value indicating if there were repeated purchases for the same product

<br>  Data validation:

- Duplicate records:
<br  > <img src = 'https://github.com/cmong007/retailcasestudy/assets/135245393/e2a181ce-3eaf-45e4-9531-f71d97078f6a' >
- Missing values:
<br  > <img src = 'https://github.com/cmong007/retailcasestudy/assets/135245393/8dddace7-7956-47b8-bc36-ff78b7613f11' height="35%" width = "35%">
<br  > Noted that there are no duplicate records and no missing values in the dataset.
<br  > The data type of sales was still a string type. For computational sake, it has to be changed to a numeric type.

<br>  Data pre-processing:
- Removing "$" and "," to facilitate changing data type
<br  /> <img src = 'https://github.com/cmong007/retailcasestudy/assets/135245393/69ed9e61-0003-4f9f-976a-c6b02cbcaf56' height="35%" width = "35%">
- Removing other pet types as subrcription box are for cat,dog,fish,bird only.
<br  /> <img src = 'https://github.com/cmong007/retailcasestudy/assets/135245393/33b4a00b-e9c8-4d4e-9bc4-ca191653f722'>
<br  />Data is sufficiently prepped . Let's create some visualizations!

**<h2><ins> Product purchased more than once  </ins></h2>**
<img src = 'https://github.com/cmong007/retailcasestudy/assets/135245393/7d89cfda-5f6d-407a-82da-fee4b13e8801' height="35%"  width="35%">
<br  /> 
About 390 products were being purchased more than once in the stores last year which represents 46.8% of the total products sold.
<br  />
<br  />
Let's take closer look into the categories being repurchased.
<br  /> <img src = 'https://github.com/cmong007/retailcasestudy/assets/135245393/564a133a-499f-4693-a223-580130e1211b' height="75%"  width="75%" >
<br  />
Upon closer inspection, the top 5 repurchases were from the Equipment,Snack,Toys,Food and Medicine product categories. These values are based on absolute figures where the higher number of repurchases may be due to a higher volume in sales for that particular product category.
<br  />
<br  />
Let's take a look into the proportion of products being repurchased for each categories.
<br  /> <img src = 'https://github.com/cmong007/retailcasestudy/assets/135245393/c3563979-00b8-47ba-9fbe-886693780da2' height="75%"  width="75%" >
<br  />
Although the top 5 repurchases were Equipment,Snack,Toys,Food and Medicine categories . The top 5 highest proportions of repurchases are Bedding,Food,Medicine,Equipment and Accessory.
<br  />
**<h2><ins> Repurchase = better sales?  </ins></h2>**
In my opinion sales can be seen as the volume of sales and the total dollar amount of sale. In this section, we will investigate both factors to determine which has better sales.
<br  />
<br  />
<img src='https://github.com/cmong007/retailcasestudy/assets/135245393/ebd3c1fe-fbe8-4d8c-8133-e5e63efb0658'>
<br  />
It seems that those products being purchased again do not have a better overall dollar amount of sales. However, volume of sales should also be considered due to ticket sizes.
<br  />
<br  />
For now, let's look at the dollar amount separated by each product category.
<img src = 'https://github.com/cmong007/retailcasestudy/assets/135245393/a4fd9a02-15c5-4589-ab4c-74ac937f4937' height="30%" width="50%" >
<br  />

The chart above shows the total sales separated by each product category sorted by the highest to lowest repurchases. 
  - The top 5 total sales with repurchases are Equipment,Snack,Toy,Medicine and Food
  - However, the total sales for Snacks and Toys (rank 2nd and 3rd) are worse than the non-repurchases.

<br  />
Due to the volume in sales, the total dollar amount in sales may not be representative when comparing which is better. The average sales may be a better metric to represent the efficiency in making a sale.
<br  />
Hence, the comparison of average sales between repurchases and non-repurchases should be made.
<br  />
<img src='https://github.com/cmong007/retailcasestudy/assets/135245393/b8de215a-6e6e-4a61-8d98-4e8d210c9a5e' >
<br  />
When volume of sales were considered, the repurchased products seems to be doing better.
<br  />
<br  />
Taking a closer look:
<br  />
<img src = 'https://github.com/cmong007/retailcasestudy/assets/135245393/35a5483f-b50a-457b-bc32-c5a9c0d1b3e8' width="50%">
<br  />

The chart above shows the total average sales separated by each product category. 
  - The top 5 repurchases with the highest average sales were Accessory,Equipment,Housing,Bedding and Grooming. 
  - Out of these products, the average sales of repurchases for Accessory,Equipment and Housing products were substantially higher as compared to non-repurchases for the same product types.  

**In Summary:**

Sales could better in terms of higher volume of sale or the higher value per sale. 
  - The products with repurchases seems to be doing better in sales based on the average sales figure, particularly in Accessory,Equipment and Housing. This suggests an opportunity to increase sales through these products.
  - On the other hand, the products with non-repurchases are doing better in sales based on the volume of sale, particularly in Snacks and Toys.

**<h2><ins> Products likely to be repurchased for different pets?  </ins></h2>**
<img src = 'https://github.com/cmong007/retailcasestudy/assets/135245393/0999449d-1b79-42d4-a1cf-5523f483dc49' width="55%">
<br  />

The chart above shows the volume of repurchases for each product category and each pet type.
  - For pet type bird, the product categories Equipment,Toys and Snack had a tie in number of repurchases.
  - For pet type cat,the product category Equipment was also repurchased most.
  - For pet type dog,the product category Equipment was repurchased most.
  - For pet type fish,the product category Snack was repurchased most.

<br  />

<img src = 'https://github.com/cmong007/retailcasestudy/assets/135245393/f4503151-c4bb-4ac4-8e2c-902d4c4463c1' width = "55%">
<br  />

The chart shows the proportion of repurchases for each product category and pet type.
  - For the pet type bird, the product categories Medicine,Supplements,Bedding,Clothes,Accessory and Housing all had the same proportion of repurchases.
  - For the pet type cat, the product category Food has the highest proportion of repurchases.
  - For the pet type dog, the product category Bedding has the highest proportion of repurchases.
  - For the pet type fish, the product category Housing has the highest proportion of repurchases. However, there was only 2 sales.

<br  />

**<h3>In Summary:</h3>**

  - A high number of repurchases and proportion could indicate a high likelihood of repurchase.
  - For the pet type bird, both **<ins>Snack** and **<ins>Toy** are likely to be purchased again as they have the same number of repurchases and proportion.
  - For the pet type cat, **<ins>Equipment** is likely to be purchased again as it has the highest number and proportion of repurchases.
  - For the pet type dog, **<ins>Medicine** and/or **<ins>Equipment** is likely to be purchased again as it ranks either 3rd and 2nd or 1st and 4th in number and proportion of repurchases.
  - For the pet type fish, **<ins>Snack** is likely to be purchased again as it has the highest number of repurchases and ranks 3rd in proportion. The 1st and 2nd ranks of proportion was not chosen due to the the small number of sale. 


