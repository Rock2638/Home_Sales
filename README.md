# Home_Sales

### **Home_Sales Challenge**

#### Overview: 

In this challenge, I use my knowledge of SparkSQL to determine key metrics about home sales data. Spark is used to; create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

----------

#### Preparation: 
 - The repository called Home_Sales is created and cloned to my computer.
 - The Starter_Code folder is downloaded.
 - The file 'Home_Sales_starter_code.ipynb' found in the Starter_Code folder is renamed as 'Home_Sales.ipynb'. 
 - The necessary PySpark SQL functions for this assignment are imported.
 - The 'home_sales_revised.csv' data in the starter code is read into a Spark DataFrame.
 - A temporary table called 'home_sales' is created.
----------

#### A query to answer each of the following question is written using SparkSQL:  
 -   What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
    
-   What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
    
-   What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
    
-   What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

----------

#### The following are then performed as required: 
1.  Cached the temporary table 'home_sales'. 
    
2.  Checked if the temporary table is cached.
    
3.  Using the cached data, ran the query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determined the runtime and compared it to uncached runtime.
    
4.  Partitioned by the "date_built" field on the formatted parquet home sales data.
    
5.  Created a temporary table for the parquet data.
    
6.  Ran the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determined the runtime and compared it to uncached runtime.
    
7.  Uncached the 'home_sales' temporary table.
    
8.  Verified that the 'home_sales' temporary table is uncached using PySpark.
    
9.  Downloaded the 'Home_sales.ipynb file and uploaded it into my "Home_Sales" GitHub repository.

----------

#### **Runtime conclusions:**

-   **Cached Data:** Use caching for the fastest query execution, especially when the same data is queried multiple times.

-   **Parquet Format:** Use Parquet for efficient storage and moderately fast query execution, especially when working with large datasets that benefit from column storage.

-   **Regular DataFrame:** Expect the longest runtimes here, as Spark needs to process the data from scratch for each query.
