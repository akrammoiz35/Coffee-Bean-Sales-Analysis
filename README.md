# Coffee-Bean-Sales-Analysis
Business Problem Statement:
The primary objectives include identifying top customers, tracking coffee-type sales trends, and analyzing sales by country. The dashboard should enable customer engagement and loyalty strategies, optimize product offerings, and support geographical expansion efforts.
Data Overview
Data on coffee bean sales are divided into 3 separate sheets:

Sheet Name	Column Names
Orders	Order ID (Primary Key)
Order Date
Customer ID
Product ID
Quantity Ordered
Customers	Customer ID (Primary Key)
Customer Name
Email
Phone Number
Address Line 1
City
Country
Postcode
Loyalty Card
Products	Product ID (Primary Key)
Coffee Type
Roast Type
Size
Unit Price
Price Per 100g
Profit
Step By Step Changes
Data Gathering and Cleaning:
To create a comprehensive table encompassing all details related to product orders, and to enhance the usability of the data for subsequent analysis, various columns from the Customers and Products tables have been combined within the Orders table. These combined columns facilitate a more cohesive representation of the information pertaining to product orders, allowing for more effective analytical processes.

Columns selected are:

Customers Sheet
Customer Name
Email
Country
Products Sheet
Coffee Type
Roast Type
Size
Unit Price
The techniques employed to retrieve data from the Customers Table involve the utilization of the VLOOKUP formula. Meanwhile, a combination of the INDEX and MATCH functions is applied to extract information from the Products Table. This approach ensures that a uniform formula can be adapted and applied across every column within the table, enabling the extraction of data in a consistent manner.

Column Treatment and Adjustments:

Email Column: The missing values in the Email column were replaced with an empty cell using an IF statement.
Sales Column: To populate the sales column, a multiplication between Quantity and Unit Price was done
Coffee Type Name Column: Recognizing that the Coffee Type column exclusively contains abbreviations such as Rob, Exc, Ara, and Lib, a supplementary column titled Coffee Type Name has been established. To map the abbreviations to their respective full names, a Nested IF function has been implemented. This function systematically converts "Rob" to "Robusta", "Exc" to "Excelsa", "Ara" to "Arabica", and "Lib" to "Liberica", thereby enhancing the comprehensibility of the coffee types.
Roast Type Name Column: A similar approach was extended to the Roast Type Name column. Employing a comparable technique, abbreviations were replaced with their corresponding full roast-type names. Specifically, "M" was transformed to "Medium", "L" denoted "Light", and "D" was indicative of "Dark".
Order Date Column: To mitigate potential confusion arising from varying date formats across different regions, a strategic adjustment was made. The month component, previously represented as a numeric value, has been transformed into a categorical value.
Size Column: The Size column lacked metric value notation. As a solution, the unit "kg" was uniformly appended to each row within this column.
Unit Price and Sales Column: Changed to currency and $ symbol was added.
Loyal Card: Added a new column that checks whether the customer has a loyalty card or not.
Extra Adjustments

Examined for duplicate variables across all columns in the Data Tab, and no instances of duplicate entries were detected.
Before moving to plot Pivot charts and tables, a step was taken to convert the entire data range into a table format named “Orders”. This transformation holds the advantage of ensuring that any future alterations in the dataset will seamlessly reflect in the pivot table and graphs, eliminating the need for manual adjustments. This dynamic synchronization enhances the efficiency and accuracy of data analysis processes.
Pivot Table And Dashboard:

Total Sales Sheet:

A pivot table titled "TotalSales" was generated with the purpose of visually representing the aggregate sales across different time periods. However, an issue emerged wherein the data was initially grouped by years. To address this, a modification was made by reorganizing the data into monthly and yearly groups. This adjustment enables more detailed visualization of sales trends over time, facilitating a finer granularity for analysis.
Proceeded by adding the "Coffee Type Name" and "Sales" columns to the column list and values respectively of the pivot table. These columns will be utilized along the Y-axis for plotting against the date. This aims to provide insights into the quantity of sales recorded on specific dates, while also considering the different coffee types involved.
Inserted a 2D Line Chart and formatted it to my satisfaction.
Inserted a Timeline feature from the PivotChart Analyzer. This Timeline tool offers the capability to analyse specific segments of the timeline under consideration. By utilizing this feature, one can dynamically narrow down the timeframe of interest within the pivot chart, thereby enhancing the precision of the analysis and facilitating the exploration of particular time intervals in a more focused manner.
Inserted 3 Slicers, Size, Roast Name Type, and Loyalty Card.
Country Bar Chart Sheet:

Added a new bar graph to represent the countries with the highest sales figures in descending order.
Top 5 Customers:

Added a new bar graph and added customer names to the axis category, sorted the whole data in descending order, and then applied the top 5 filter.
Bar Chart Sheet:

Created a new sheet named “Dashboard”, where the interactive visuals will be presented.
Lastly, established connections between all the slicers and the various visual elements present. This linkage ensures that whenever filters are applied through the slicers, the resultant changes are seamlessly reflected across all associated graphs and visual representations.
