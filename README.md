Final Project: Online Store Inventory Management System 

Team Size: 3-4 students 
Weight: 30% of Final Grade 

Project Overview 

You will design and develop an Inventory Management System for a fictional online retailer. The system will handle inventory tracking, sales processing, and generating sales reports. This project will assess your understanding of all course outcomes, including logical thinking, flowcharting, mathematical analysis, algorithm application, and pseudocode development. 

The final submission will include: 

Documented problem analyses and decompositions. 

Flowcharts representing various system processes. 

Pseudocode demonstrating algorithmic solutions. 

Statistical analysis of sales data. 

Justifications for algorithm choices and optimizations. 

A 5-10 minute recorded presentation showcasing your solution 

Only the project-submission.docx and the presentation video files will be graded. Any other files uploaded will not count towards your graded. 

The presentation video must be a single file, not a collection of individual videos. 

Refer to the course syllabus about Academic Integrity for this assessment. 

Project Requirements 

Your system must include the following modules and meet all outlined requirements. Where applicable, provide flowcharts, pseudocode, and justifications for algorithm selection. 

1. Inventory Management Module 

The Inventory Management Module is responsible for handling all product details in the store's inventory and is accessible by employees. No authentication is required. This module allows employees to add, update, and remove products from the inventory, which requires the searching and sorting of items. Users can perform as many operations as they want until they decide to quit. 

Include a detailed problem decomposition and analysis, identify necessary modules, provide a detailed flowchart of the entire process, and write modular pseudocode. Make use of the search and sort functions you write in these operations as necessary and include appropriate validations (valid productID, positive values, etc.). The search and sorting algorithms do not need to be part of the flowchart, but must be implemented in pseudocode. 

The Inventory Management module requires the following functionality: 

Accept inputs for adding new products with the following fields: 

Product ID (Unique identifier, alphanumeric) 

Product Name (String) 

Category (String, e.g., Electronics, Clothing, Books, etc.) 

Price (Decimal, representing the price of the product) 

Quantity (Integer, representing stock level) 

Allow updates to existing products including: 

Modifying price, quantity, or category. 

Removing products from the inventory. 

Provide search functionality to locate products in inventory: 

By Product Name. Return a single item, the product. Implement the Binary Search algorithm for this functionality. 

By Category. Return all products of a particular category. Implement the Linear Search algorithm for this functionality. 

By Product ID. Return a single item, the product. Implement either the Linear Search or Binary Search algorithm for this functionality. Justify your decision. 

Provide sorting functionality to sort products in inventory: 

Alphabetically by Product Name. Implement the Merge Sort algorithm for this functionality. 

By Category. Implement the Bubble Sort for this functionality. 

By Price. Implement either Merge Sort or Bubble Sort for this functionality. Justify your decision. 

 

2. Sales Processing Module 

The Sales Processing module is responsible for handling an entire customer transaction. It should handle the addition of as many items as the customer wishes to purchase, applying the discount while the items are processed. The customer must be prompted to move to the payment stage of the sales processing, at which point a detailed receipt will be generated. 

Include a detailed problem decomposition and analysis, identify necessary modules, provide a detailed flowchart of the entire process, and write modular pseudocode for each of the required functionalities. 

The Sales Processing module requires the following functionality: 

Accepting product IDs and quantities to process a purchase. 

Adjusting inventory quantities accordingly. 

Handling insufficient stock situations with appropriate messages. 

Generating receipts including: 

Product Names, Quantities, and Prices of each purchased item. 

Total Cost of the transaction. 

Applying a 10% discount on individual products when the customer purchases over 5 of that product. For example, if they purchase 6 apples, there is a 10% discount applied to the apple subtotal, not the entire order. 

Note: You can assume that the product ID that is entered is always valid and the quantity entered will never be negative. 

3. Reporting Module 

The Reporting Module is responsible for generating statistical analysis and reports using the provided dataset (sales_data.csv).  

The dataset simulates a history of transactions for an online store and includes the following columns: 

OrderID: Unique identifier for each order. An order may consist of multiple line items. 

Date: The date of the transaction. 

Product ID: Unique identifier for each product sold. 

Product Name: Name of the product sold. 

Category: Product category (e.g., Electronics, Accessories, Wearables, Books). 

Quantity: Number of units sold for a particular product. 

Price: Unit price of the product. 

Discount Applied: Discount rate applied to the transaction (e.g., 0.1 for 10%). 

Total Price: Total price for the line item, including any applied discounts. 

You do not have to implement functionality that loads data from the csv. You can assume a function called loadSalesData() is called and returns a list of entries with the appropriate columns. 

Note: Only the Statistical Analysis and Product Analysis sections require pseudocode. 

Your reporting must include the following: 

Statistical Analysis 

Total Revenue: 

Write the pseudocode necessary to perform this calculation for any input. 

Provide the total revenue from all transactions based on sales_data.csv. 

Average Transaction Value:  

Write the pseudocode necessary to perform this calculation for any input. 

Provide the average value of transactions across all orders in sales_data.csv. 

Product Analysis 

Most Popular Products:  

Write the pseudocode necessary to find the top 5 products for any input. 

Identify the top 5 products based on total quantity sold in sales_data.csv. 

Least Popular Products:  

Write the pseudocode necessary to find the bottom 5 products for any input. 

Identify the bottom 5 products based on total quantity sold in sales_data.csv. 

Correlation Analysis 

Price-Quantity Correlation: Calculate and interpret the correlation between product price and quantity sold. Describe what the correlation represents in the context of the sales data. 

Probability Analysis 

Probability of Sale: Calculate the probability of a particular product being sold on any given day based on the date range in the sales data. 

Make sure to include the full date range, including days where nothing was sold (these would be missing from the csv) 

Trend Analysis 

Compare sales quantity by date to identify peaks and declines.  

Group sales quantity by category to determine which types of products are performing best. 

Report Generation Requirements 

Provide visual representations where appropriate (e.g., bar charts, line graphs). 

Include justifications and explanations of findings. 

Compare and contrast findings across different categories or time periods. 

4. Algorithm Implementation & Justification 

Searching Algorithms: Explain the Linear Search and Binary Search algorithms written in Part 2. Include the time complexity. Provide a justification for each algorithm’s suitability in the program. 

Sorting Algorithms: Explain the Bubble Sort and Merge Sort algorithms written in Part 2. Include the time complexity. Provide a justification for each algorithm’s suitability in the program. 

Optimization: Suggest at least two optimizations to improve efficiency of the entire system. If you have already implemented these in your design, explain why your choices are optimal. 

5. Presentation Requirements 

Provide a recorded presentation of your project. The presentation should be broken into the following portions: 

Inventory Management Module: 

Problem analysis and decomposition 

Flowchart of the process 

Pseudocode summary 

Sales Processing Module: 

Problem analysis and decomposition 

Flowchart of the process 

Pseudocode summary 

Reporting Module - Statistical Analysis 

Provide the total revenue and the average transaction values 

Show how you arrived at those numbers 

Provide a visual representation (Bar graph, pie chart, etc.) illustrating revenue distribution or transaction value trends. 

Reporting Module - Product Analysis 

Provide the most popular (top 5) products by quantity sold. 

Provide the least popular (bottom 5) products by quantity sold. 

Show how you arrived at those numbers 

Provide a visual representation (e.g. bar chart) comparing sales across different products. 

Reporting Module - Correlation and Probability Analysis 

Provide the correlation value between the Price and the Quantity. 

Provide the probability of sales for each product. 

Show how you arrived at those numbers 

Visual representation of the correlational coefficient (e.g. Scatter Plot) and the probability of sales for each number. 

Algorithm Implementation & Justification 

Explain the algorithms you implemented in your solution (search and sort). 

Explain the benefits and drawbacks of each algorithm. 

Optimization 

Provide descriptions of optimizations you implemented or could implement in the future. 

Submission Requirements 

Problem analysis document (explaining how the problem was broken down into modules). 

Flowcharts representing system processes. 

Pseudocode for each module, including algorithm selection and justification. 

Statistical analysis demonstrating applied mathematical techniques, including: 

Total Revenue Calculation 

Average Transaction Value Calculation 

Product Analysis: Identification of most and least popular products. 

Correlation Analysis: Calculation and interpretation of correlation between product price and quantity sold. 

Probability Analysis: Estimation of the probability of specific products being sold on a given day. 

Trend Analysis: Analysis of sales volume over time to identify patterns and trends. 

Written justification of selected algorithms and any applied optimizations. 

A brief presentation (5–10 minutes) showcasing your solution, including visual representations (e.g., bar charts, line graphs) of your findings. 

Assessment Rubric 

The project will be graded out of 100 marks according to the following criteria: 

Component 

Inventory Management Module 

Sales Processing Module 

Reporting Module 

Algorithm Implementation & Justification 

Presentation 

Total 

 
