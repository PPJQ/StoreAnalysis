# StoreAnalysis

In this project we are going to review and analyze the information of a supermarket.

This dataset contains captures of detailed transactions from a supermarket, including product categories, unit prices, quantities, and gross income. It also records customer demographics like gender, payment method, and membership type.

We are going to analyze the following points: 

* Sale trends
* Customer behavior
* Revenue performance

In this dataset we have the following columns description:

   * **Invoice ID**: A unique identifier for each transaction or purchase. This is typically a string or alphanumeric code.

   * **Branch**: Indicates the specific branch of the supermarket where the transaction took place. This could be categorical (e.g., "A", "B", "C").

   * **City**:The city where the supermarket branch is located. This is also categorical and helps in geographic analysis.

   * **Customer Type**: Defines the type of customer (e.g., "Member" or "Normal"). This could be useful for segmentation and understanding purchasing behavior.

   * **Gender**: The gender of the customer (e.g., "Male" or "Female"). This can be useful for demographic analysis.

   * **Product Line**: Specifies the category of products purchased (e.g., "Groceries", "Clothing", "Electronics"). This helps in product performance analysis.

   * **Unit Price**: The price of a single unit of the product. This is a continuous numerical value.

   * **Quantity**: The number of units purchased in a single transaction. This is also a continuous numerical value.

   * **Tax 5%**:The amount of tax applied to the purchase, calculated as 5% of the total before tax. This is a continuous numerical value.

   * **Total**: The total amount paid by the customer, including tax. This is a continuous numerical value.

   * **Date**:The date of the transaction, which can help in time series analysis. Format is typically in YYYY-MM-DD.

   * **Time**:The time of the transaction, which can be used to analyze peak shopping hours.

   * **Payment**:The method of payment used (e.g., "Cash", "Credit Card", "Debit Card"). This is categorical and provides insights into payment preferences.

   * **COGS**: Cost of Goods Sold, representing the total cost of producing the goods sold. This is a continuous numerical value.

   * **Gross Margin Percentage**: The percentage difference between sales and the cost of goods sold, indicating the profitability of sales.

   * **Gross Income**:The income remaining after deducting the cost of goods sold from total sales. This is a continuous numerical value.

   * **Rating**:The customer’s rating of the product or service, usually on a scale (e.g., 1 to 5). This can help in understanding customer satisfaction.

## Sale Trends

According with the analysis we find the next results:

* The most popular Product Line of the store is `Electronic Accessories` with 971 product sales.

![Product Line Trends](./datasets/images/Product%20Line%20Trends.png)

For each store branch these are the most popular Product Line: 

* Store A: `Home and Lifestyle` (371 purchases) and `Sport and Travel` (333 purchases)
* Store B: `Sports and Travel` (322 purchases) and `Health and Beauty` (320 Purchases)
* Store C: `Food and Beverages` (369 purchases) and `Fashion Accessories` (342 purchases)

![Branch Product Trends](./datasets/images/Branch%20Product%20Trends.png)

A long the period of the dataset we find: 

* In January the product line with more sales was `Sports and Travel` with 375 purchases.
* In February the product line with more sales was `Food and Beverages` with 349 purchases.
* In March the product line with more sales was `Home and Lifestyle` with 364 purchases.

![Product Line Purchases Per Month](./datasets/images/Product%20Line%20Purchases%20Per%20Month.png)

## Customer Behavior

According with the results in the analysis we find the following behaviors:

### Customer Type Per Gender

* Female customer buy more products in both schemes (`Normal` and `Member`) that the Male customers.
* Male customers are more likely to be under the `Normal` scheme
* Female customers are more likely to be `Members` of the store

| Gender | Customer Type | Purchases | Members |
|--------|---------------|-----------|---------|
| Female | Member        | 1492      | 261     |
| Female | Normal        | 1377      | 240     |
| Male   | Member        | 1293      | 240     |
| Male   | Normal        | 1348      | 259     |


![Customer Type Per Gender](./datasets/images/Customer%20Type%20Per%20Gender.png)

### Product Line Preferences Per Customer Gender And Type

* Female customers are more used to buy `Fashion Accessories` and `Food And Beverages` products
* Male customers are more used to buy `Health and Beauty` and `Electronic Accessories` products

![Product Line Tendency Per Customer Gender](./datasets/images/Product%20Line%20Tendency%20Per%20Customer%20Gender.png)

* Normal customers are more used to buy `Electronic Accessories` products
* Member customers are more used to buy `Food and Beverages`, `Sport and Travel` and `Home and Lifestyle` products

![Product Line Tendency Per Customer Type](./datasets/images/Product%20Line%20Tendency%20Per%20Customer%20Type.png)

### Customer Behavior Per Date

In the analysis, we find that the female customer has more purchases in January and the male customer has more purchases in March, but both reduce purchases in February.

![Customer Purchases Per Month And Gender](./datasets/images/Customers%20Purchases%20Per%20Month%20And%20Gender.png)
![Customer Purchases Per Date And Gender](./datasets/images/Customer%20Purchases%20Per%20Date%20And%20Gender.png)

### Customer Purchases Per Month And Product Line

For each month each customer gender buys the following products lines:

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Product Line</th>
      <th>Electronic accessories</th>
      <th>Fashion accessories</th>
      <th>Food and beverages</th>
      <th>Health and beauty</th>
      <th>Home and lifestyle</th>
      <th>Sports and travel</th>
    </tr>
    <tr>
      <th>Month</th>
      <th>Gender</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="2" valign="top">January</th>
      <th>Female</th>
      <td>149</td>
      <td>197</td>
      <td>169</td>
      <td>96</td>
      <td>198</td>
      <td>210</td>
    </tr>
    <tr>
      <th>Male</th>
      <td>184</td>
      <td>139</td>
      <td>156</td>
      <td>158</td>
      <td>144</td>
      <td>165</td>
    </tr>
    <tr>
      <th rowspan="2" valign="top">February</th>
      <th>Female</th>
      <td>191</td>
      <td>185</td>
      <td>190</td>
      <td>140</td>
      <td>96</td>
      <td>149</td>
    </tr>
    <tr>
      <th>Male</th>
      <td>122</td>
      <td>110</td>
      <td>159</td>
      <td>126</td>
      <td>109</td>
      <td>77</td>
    </tr>
    <tr>
      <th rowspan="2" valign="top">March</th>
      <th>Female</th>
      <td>148</td>
      <td>148</td>
      <td>155</td>
      <td>107</td>
      <td>204</td>
      <td>137</td>
    </tr>
    <tr>
      <th>Male</th>
      <td>177</td>
      <td>123</td>
      <td>123</td>
      <td>227</td>
      <td>160</td>
      <td>182</td>
    </tr>
  </tbody>
</table>
</div>

#### Female Customers: 

* January: `Sport and Travel` products with 210 purchases.
* February: `Electronic Accessories` products with 191 purchases.
* March: `Home and Lifestyle` products with 204 purchases.

![Female Purchases Per Product Line and Month](./datasets/images/Female%20Purchases%20per%20Product%20Line%20and%20Month.png)
#### Male Customers: 

* January: `Electronic Accessories` products with 184 purchases.
* February: `Food and Beverages` products with 159 purchases.
* March: `Health and Beauty` products with 227 purchases. 

![Male Purchases Per Product Line and Month](./datasets/images/Male%20Purchases%20per%20Product%20Line%20and%20Month.png)

## Revenue Performance

After reviewing the revenue behavior of distinct segments we find the following behavior:

### Revenue Per Product Line And Branch

The product line with more revenue for each branch are:

* Branch A: `Home and Lifestyle` with $1,067.49
* Branch B: `Sport and Travel` and `Health and Beauty` with $951.00
* Branch C: `Food and Beverages` with $1,131.76

![Revenue Per Product Line And Branch](./datasets/images/Revenue%20Per%20Product%20Line%20and%20Branch.png)

The branch with more revenue is the "C" branch with $5,265.18.

![Revenue Per Branch](./datasets/images/Revenue%20Per%20Branch.png)

### Revenue Per Product Line And Month

* The product line `Sports and Travel` has the most revenue in January with $1,031.76.
* The product line `Food and Beverages` has the most revenue in February with $952.40.
* The product line `Home and Lifestyle` has the most revenue in March with $996.80.

![Revenue Per Product Line and Month](./datasets/images/Revenue%20Per%20Product%20Line%20and%20Month.png)

### Revenue Per Customer Type And Gender

* Female customers has the most revenue with $7,994.43, which:
  * Members has $4,197.47
  * Normal has $3,796.95
* Normal Male customers has the most revenue that Member Male customers with $3,762.25

![Revenue Per Customer Type And Gender](./datasets/images/Revenue%20Per%20Gender%20and%20Customer%20Type.png)

### Revenue Per Month And Branch

January was the month with most revenue with $5,537.00.

![Revenue Per Month](./datasets/images/Revenue%20Per%20Month.png)

For each branch January was the month with more revenue:

* Branch A: $1,841.96
* Branch B: $1,770.29
* Branch C: $1,925.46

![Revenue Per Month And Branch](./datasets/images/Revenue%20Per%20Month%20And%20Branch.png)

## Conclusions

According with the results in this analysis we find the following behavior: 

The product line more popular for each branch coincides with the product line with most revenue:

* Branch A: The Product Line with more sales is `Home and Lifestyle` with 371 sales and have a revenue of $1,067.49
* Branch B: The Product Line with more sales is `Sports and Travel` with 322 sales and have a revenue of $951.00
* Branch C: The Product Line with more sales is `Food and Beverages` with 369 sales and have a revenue of $1,131.76

January was the month with more sales with 1,965 sales and a revenue of $5,537.71. The sales decrease in February with 1,654 sales and a revenue of $4,629.49. And lastly in March the sales increase with 1891 sales and a revenue of $5,212.17.

For each month the product line with more sales were: 

* January: `Sports and Travel` with 375 sales and a revenue of $1,031.76
* February: `Food and Beverages` with 349 sales and a revenue of $952.40
* March: `Home and Lifestyle` with 364 sales and a revenue of $996.80

* The data contains almost the same amount of Female and Male customers:
  * Female users: 501
  * Male users: 499
* Female customer buy more products in both schemes ("Normal" and "Member") that the Male customers
  * Normal: 1,377 sales in total
  * Member: 1,492 sales in total
* Male customers are more likely to be under the "Normal" scheme with 1,348 sales in total
* Female customers are more likely to be "Members" of the store with 261 users
* Female Customers are more used to buy `Fashion Accessories` products with 530 purchases and `Food And Beverages` products with 514 purchases
* Male Customers are more used to buy `Health and Beauty` products with 511 purchases and `Electronic Accessories` products with 483 purchases
* Normal Customers are more used to buy `Electronic Accessories` products with 542 purchases.
* Member Customers are more used to buy `Food and Beverages` (506 purchases), `Sport and Travel` (493 purchases) and `Home and Lifestyle` (490 purchases) products.
* For each month, Female customers buys: 
  * January: `Sport and Travel` products with 210 purchases.
  * February: `Electronic Accessories` products with 191 purchases.
  * March: `Home and Lifestyle` products with 204 purchases.
* For each month, Male customers buys: 
  * January: `Electronic Accessories` products with 184 purchases.
  * February: `Food and Beverages` products with 159 purchases.
  * March: `Health and Beauty` products with 227 purchases. 
