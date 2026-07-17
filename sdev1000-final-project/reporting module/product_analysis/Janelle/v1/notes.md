JUST NOTES

User inputs any of the other columns AS choice

if choice == revenue
	product name | ***total revenue

if choice == date 
#IF DATE, NOT SURE IF USER WOULD INPUT SPECIFIC DATE OR IF WE DO TOP 5 FOR EACH DATE
	product name | ***

if choice == category 
#IF CATEGORY, NOT SURE IF USER WOULD INPUT SPECIFIC OR TOP 5 FOR EACH CAT
	category | Product name | ***

if choice == quantity
	Product name | ***total quantity

if choice == price
	Product name | ***total price

if choice == discount applie 
	Product name | ***total discount applied

if choice == total price
	Product name | ***Total total price



SPECIAL CONSIDERATIONS

Product ID and  Product Name  won't produce ranked values... (top 5 products by product id will always be just have 1 rank...)

Date and Category aren't aggregatable. So if user choses top 5 by date or category, it will show top 5 products for every instance.


EDGE CASE

if two product names have same totals? How are those ranked?? (1, 2, 2, 4, 5?)


