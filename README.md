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
