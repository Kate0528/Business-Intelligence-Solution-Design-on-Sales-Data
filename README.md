# Business-Intelligence-Solution-Design-on-Sales-Data

## Introduction

This is a business case from Business Intelligence System course. The objective of this project is to help the target sales company better understand their sales history through some interactive visualizations and reports. We are trying to solve the following business questions and put forward some suggestions to improve sales.

1. Overall sales performance.
2. Give an overall assessment of store number 10, and 21 sales.
 - How are they performing compared to target? Will they meet their 2014 target?
 - Should either store be closed? Why or why not?
 - What should be done in the next year to maximize store profits?
3. Assess product sales by day of the week at stores 10 and 21. What can we learn about sales trends?
4. Should any new stores be opened? Include all stores in your analysis if necessary. If so, where? Why or why not?

## Dashboard 1: Overall Sales Performance

Here we built a dashboard as follows. This dashboard contains five worksheets covering general performance on product profitability, sales quantity, sales amount, profit by month, sales quantity by month etc.

![jpg](Dashboard_1.jpg)

**Product Profitability**

In this worksheet, different colors representing product categories such as accessories and children's apparels, and different shapes shows product types under these categories. The y-axis is the unit profit margin, which is calculated as (Price – Cost ) / Price. The x-aixs represents the unit price, which is equal to Price - Cost.

***Design Note*** This graphic was built from the Product dimension and is used to show the profit of a single unit of a product, rather than the total profit of what was sold.

We know that the profit margin is an indication of the financial success and viability of a particular product or service. The higher the percentage, the more the company retains on each dollar of sales to service its other costs and obligations. It is often used by businesses that are looking for ways to boost their revenue, want to evaluate a product or service or simply want to take an inventory of what they’re spending versus what they’re making. In this graph, we may find that most of the current product types have a gross profit margin larger than 0.5, but Denim Jeans and Spider man T-shirt both have a relatively low profit margin. We may use that kind of graph to conduct product margin analysis to figure out the best solution. For example, if the overall sales are steady, but one product’s sales have seen a decline in recent months. After figuring out the profit margin for that particular produce line, the company might decide that it’s within its best interest to discontinue the product.

**Product Sales Qty vs. Target**

***Design Note*** This graphic was built using the Sales Fact table and the Target Fact table and represented the total sales of all product sold compared to the target for the month.

In this worksheet, we compared actual sales quantity and the target quantity, then we sorted the products in order of highest sales at the top. The green lines represent target sales quantity. As before, different colors representing product categories, so that we may identify which product sales quantity doesn't meet the target sales quantity in which product category. For example, we may find that most of the product sales quantity doesn't meet the target quantity, but they are very close to the target quantity, instead of Girl's dress. Next, analysts could dig into Girl's dress sales performance among diffrent sales channels, locations and days of week to figure out the reason.

**Profit by Month**

***Design Note*** This graphic was built using the Sales Fact table and represented the total profit of all products sold.  

The overall profit by month is steady instead of November and December, which is due to the original data lacks these two months in 2014. We may also find a trend that the sales increases a little bit in Summer and Autumn, while may hit the trough in January and February. It may happens because most discounts happened in November and consumers tend to purchase a lot in these months, and don't need much more in the following month, which is February.

**Sales Amount vs. Target by Month**

***Design Note*** This graphic was built using the Sales Fact table and the Target Fact table and represented the total sales amount of all product sold compared to the store sales amount target for the month.

As before, the green line represents the target amount and the blue bar represents the actual sales amount in each month. Since December, 2014 and November, 2014 were missing, we just focus on previous ten months for now. As we expected, this graph also shows that the actual sales amount seems a little worse in Winter, compared to in Summer. The gap between the actual amount and target amount is not big except January. The analyst could gather more data to see if the target sales amount in January we set is reasonable or not. For example, if in the past five years, the performance in January is as good as the other months, which indicates the target sales in 2013/2014 January is reasonable, we need to figure out if there's unexpected things happened in 2013 and 2014.

According to this graph, store 10 would meet 2014 target, but store 21 might not meet 2014 target. The company could consider to close store 21 if its performance continue to be worse than the other stores.

**Sales Qauntity by Month**

***Design Note*** This graphic was built using the Sales Fact table and represented the total sales quantity of all products sold.  

Compared with the Profit by Month graph, we may find an interesting thing in March and April. The sales quantity in March and April is close to the quantity in May to July, but the profits in March and April are relatively lower than the other months. That may because consumers tend to purchase more products which have a relatively low product profit in these two months. However, we need more evidence to correlate this situation with the product sales in these two months.

## Dashboard 2: Overall Assessment of Store Number 10, and 21 sales

Here we build a dashboard representing the sales amount vs. target amount bar graph, monthly target completion rate chart, quarterly target completion rate bar graph and best selling products.

![jpg](Dashboard_2.jpg)

**Actual Sales Amount vs. Target Amount**

***Design Note*** This graphic was built using the Sales Fact table and the Target Fact table and represented the total sales amount of all product sold compared to the store sales amount target for the month, and keep store 10 and store 21 only. Pink bars represents store 10's actual sales amount, while green bars represents store 21's sales amount. The yellow line shows target amount for each year in store 10 and store 21. Since we lack the data in December and November 2014, we made a rough estimation using the build-in prediction functions in Tableau. The gray bars represent our sales amount predictions.

We may find notice store 21 had a worse performance in 2013 than in 2014. However, we can identify that the sales company decreased store 21's target sales amount in 2014. Actually, there isn't a big diffrence in 2013 and 2014 for store 21. The sales amount is relatively steady over these two years. When we compare these two stores from a vertical perspective, store 10's performance seems much better than store 21 in both years. In most of the months, store 10 hit the target amount in 2013, therefore, the sales company increased the target amount in 2014. Even though the targets has increased, store 10 completed the target amount successfully in 2014 as well.

**By Month Sales Target Completion Rate**

***Design Note*** This graphic was built using the Sales Fact table and the Target Fact table and represented the total sales amount of all product sold compared to the store sales amount target for the month, and keep store 10 and store 21 only. The completion rate is calculated by Sales Amount / Target Amount.

As we expected, store 10 had a better performance than store 21. The overall completion rate for store 10 dropped a little bit from 2013 to 2014, which might because we increased the target amount for store 10 in 2014. Meanwhile, the overall completion rate for store 21 increased from 63% to 76% might because we decreased the target amount for store 21.

**By Quarter Sales Target Completion Rate**

***Design Note*** This graphic was built using the Sales Fact table and the Target Fact table and represented the total sales amount of all product sold compared to the store sales amount target for the month, and keep store 10 and store 21 only.

As before, we may find store 10 had a better performance than store 21. Each bar represents the sales target completion rate by quarter. We could identify that store 10 had a relatively steady performance over quarters, but store 21 had a larger fluctuation in these quarters. The best performance quarter for store 21 is quarter 2 in 2014, whereas store 10 seemed always complete the target amount in these two years.

**Best Selling Product**

***Design Note*** This graphic was built using the Sales Fact table. Different colors represent products. We use highest sales quantity to indicate the best selling products.

In this graph, store 10's best selling product was Buttondown Shirt and the worst selling product was Blue Onesie Pajamas. In store 21, the best selling product was Blouse and the worst selling product was Blue Onesie Pajamas as well. This graph is useful for the company to make decisions on product purchase and stock amount. However, sales quantity only reflect the quantity of sales for these products. It'd be better if the analyst could combine this chart with the product profit margin graph to make decisions. To maximize store profits, the company should consider to purchase more on the best selling product and less on the worst selling product.

## Dashboard 3: Product Sales by Day of the Week at Stores 10 and 21

Here we build a dashboard representing the sales per day of the week per product, sales per product per day of the week, 12 months forecast and store geography with maps.

![jpg](Dashboard_3.jpg)

**Sales Per Day of the Week per Product**

***Design Note*** This graphic was built using the Sales Fact table. As before, pink represents store 10 and green represents store 21. Here we used sales amount in the y-axis to indicate the sales performance. 

With tooltips in Tableau, we could identify that the best selling products per day of the week in store 10 and store 21 are different. For example, Dress is the best selling product in Tuesday, Wednesday, Saturday and Sunday in store 10. The best selling product in other days of the week is Strapless Dress in store 10. For store 21, the best selling product is always blouse, no matter in which day of the week.

**Sales per Product per Day of the Week**

***Design Note*** This graphic was built using the Sales Fact table. As before, pink represents store 10 and green represents store 21. Here we used sales amount in the y-axis to indicate the sales performance. We chose line plot to show the sales trend over days of the week.

While most products sales trends are flat, dress, strapless dress and blouse are not stable in store 10. Dress and strapless dress are not stable in store 21 as well.

**12 Months Forecast**

***Design Note*** This graphic was built using the Sales Fact table. As before, pink represents store 10 and green represents store 21. Here we used sales amount in the y-axis to indicate the sales performance. We chose line plot to show the sales trend over months from 2013 to 2015.

We made 12 months forecast based on Jan 2013 to Oct 2014 sales data. The dash line represents the trend and the colored region represent the confidence interval of our forecast. From this graph, we may identify that store 10 might get better performance in the next 12 months, while store 21 may get the same or even worse performance than the current. This made us more conviced that the company might need to consider to close store 21 later.

**12 Months Forecast**

***Design Note*** This graphic was built using the Sales Fact table and the Location Dimension table. Pink represents store 10 and green represents store 21. The circle size represents the sales amount in these two stores.

We used map to show the locations of these two stores. We may find that these two stores are not too far away from each other. There're also some other stores nearby, which may indicate that if we close store 21, some customers may go to other nearby stores.


## Dashboard 4: Sales Amount with Location Info

Here we build a dashboard representing the sales amount chart, sales amount with locations, sales amount by months and store geography with maps.

![jpg](Dashboard_4.jpg)

**Store Sales Amount**

***Design Note*** This graphic was built using the Sales Fact table and the Location Dimension table. The number here indicates the sales amount in different stores.

We may find that stores in Georgia and Mississippi have good performance. Store in Arkansas seems to have more space to improve. However, that also depends on other external information such as the state population number, etc.

**Stores Loaction vs. Sales Amount**

***Design Note*** This graphic was built using the Sales Fact table and the Location Dimension table. Different colors represent U.S. states, and the circle size indicates sales amount in these stores. The number marks indicates the sales amount target completion rate in each store.

Based on this graph, stores in Indiana and Mississippi both did a good job in the past two years. The completion rate in these two states are close to or more than 100%. Besides, the sales amount in these stores seems much more than the others. Stores in Missouri's and Atlanta's target completion rate seems great as well, but the overall sales amount is not as much as stores in Indiana and Mississippi. As in the Store Sales Amount chart represented, stores in Arkansas need to improve more. Both the sales amount and the target completion rate seem not good.

**Sales Amount by Month vs. Target Amount**

***Design Note*** This graphic was built using the Sales Fact table and the Location Dimension table. The x-axis shows months from 2013 to 2015, and the y-axis represents the sales amount in these months. Dark blue bars indicates the historical sales amount, whereas shallow blue bars are our pedictions for next 12 months. Yellow lines represents the target amount (historical target in 2013 and 2014, and predictive target in 2015).

Store 5 and store 39 seems to be the best in terms of historical sales amount. Both stores also indicates an increase trend in our predictive sales amount, especially store 39. The company might even need to adjust the target sales amount for store 39, since the current target amount seems easy for them to reach in 2015. Store 10's and store 34's sales amount seemed steady over years, and the target amount seemed reasonable for them as well. In terms of growth potential, store 10 seems a little better than store 34, since our prediction of store 10's sales amount shows a slightly increase trend in 2015. Neither Store 8 or store 21 reached the target amount in 2013, and the gap seemed big. After the company decreased their target sales amount in 2014, we may find that both stores got much closer to the target amount. However, in our prediction, store 21 may not reach to the target amount in 2015, and there's a prediction decrease trend in store 21 as well. Therefore, if we need to close a store, we might consider to close store 21 first.

**Sales Amount by Month vs. Target Amount**

***Design Note*** This graphic was built using the Sales Fact table and the Location Dimension table. As before, different colors represent U.S. states. The y-axis shows total sales amount in these two years. Blue line is the target sales amount.

We find that stores in Georgia and Mississippi reached the target sales amount, so we recommend Georgia and Mississippi open a new store to handle these sales. For these two stores, Mississippi near Jackson City has the priority because store 39 would have a large increase in our predictive sales. One possible choice is to open in Alabama, which is n between these two states. However, it has a higher sales tax than the other two states so the trade-off counts.
