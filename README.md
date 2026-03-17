# Sales & Promotion Analysis Dashboard


### Dashboard Link : https://app.powerbi.com/links/5uKtYoD-D4?ctid=51697115-1ecd-42b5-b509-2d62c3919f76&pbi_source=linkShare

## Problem Statement

This dashboard analyzes sales performance to help businesses understand product profitability, sales trends, and discount impact. It identifies top and bottom performing products, compares performance across time periods, and highlights sales distribution across different cities. These insights help businesses make better decisions to improve revenue and profitability using interactive analysis built in Power BI.

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a Excel file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : The dataset contained four tables:

    Dim Customer

    Dim Product

    Dim Promotion

    Fact Table

The fact table contained several null values, which were handled by applying left joins with dimension tables to retrieve missing values where possible.

-Step 1: Loaded data from Excel into PowerBI.

Step 2: Performed data transformation in Power Query.

Step 3: Merged tables (Dim Customer, Dim Product, Dim Promotion) with Fact table using left join to handle null values.

Step 4: Filled missing values for "Price per Unit" and "Discount Price" using data from Product and Promotion tables.

Step 5: Created custom columns for Total Sales, Discount Value, Net Sales, and Profit.

Step 6: Built visuals to identify Top and Bottom 5 products by Sales, Profit, and Quantity Sold using filters.

Step 7: Developed interactive dashboards to analyze sales trends, profit distribution, and regional performance.

Step 8: Added slicers for dynamic filtering (Product, Date, Customer, Promotion).

Step 9: Designed report layout with multiple pages for overview, comparison, and detailed analysis.

Step 10: Developed interactive dashboard using Power BI with DAX-based measures (SUM of Net Sales, Total Profit, Total Quantity Sold) 

       
       Sum of Net Sales = CALCULATE(SUM('Fact Table'[Net Sales  ]),ALL('Date Table 1'),USERELATIONSHIP('Date Table 2'[Date],'Fact Table'[Date (dd/mm/yyyy)])) 

       Total Profit = CALCULATE(SUM('Fact Table'[Profit]),ALL('Date Table 1'),USERELATIONSHIP('Date Table 2'[Date],'Fact Table'[Date (dd/mm/yyyy)]))

       Total Quantity Sold = CALCULATE(SUM('Fact Table'[Units Sold]),ALL('Date Table 1'),USERELATIONSHIP('Date Table 2'[Date],'Fact Table'[Date (dd/mm/yyyy)]))
        
Step 11: The report contains four pages.

###  Overview Dashboard
- Sales by City (Map visualization)  
- KPI cards for key metrics  
- Average Discount by Promotion Category  
- Profit vs Net Sales analysis  
- Sales trends over time  

###  Top/Bottom 5 Analysis
- Identified top and bottom 5 products  
- Based on Sales, Profit, and Quantity Sold  

###  Comparison Analysis
- Compared Sales, Profit, and Quantity across categories  
- Identified high and low performance segments  

###  Interaction Control
- Customized visual interactions  
- Improved user experience  

###  Detailed Table View
- Tabular format for in-depth data analysis  
- Includes Sales, Profit, Discount, and Quantity  
Step 11: The report was then published to Power BI Service.
 
 
![Publish_Message](https://github.com/Chaithrakulal-23/Sales-Performance-Data-Analysis-Dashboard/blob/f77744214e09a5156b46a3b32bf1dab6da90ff4a/Publish.png)

# Dashboard Snapshots

##  Page 1: Overview
![Overview](https://github.com/Chaithrakulal-23/Sales-Performance-Data-Analysis-Dashboard/blob/4b00af71bcb162e010664516a8010e3a3d68d331/overview.png)

**Insight:** Sales show variation across cities, with certain locations contributing significantly to overall revenue. Profit increases with Net Sales, indicating a strong positive relationship.

---

##  Page 2: Top/Bottom 5 Analysis
![Top Bottom](https://github.com/Chaithrakulal-23/Sales-Performance-Data-Analysis-Dashboard/blob/a1ca9505476bd6d95dbab3065018147dd3268941/TopBottom5Analysis.png)

**Insight:** A small group of products drives the majority of sales and profit, while bottom-performing products contribute minimally and may require optimization or removal.

---

##  Page 3: Comparison Analysis
![Comparison](https://github.com/Chaithrakulal-23/Sales-Performance-Data-Analysis-Dashboard/blob/bd5784e77659ed5b07c0959d010f16a7926686d7/ComparisionSalesProfitQuantity.png)

**Insight:** Clear differences exist between product/category performance, helping identify high-performing segments and areas needing improvement.

---

##  Page 4: Interaction Control
![Interaction](https://github.com/Chaithrakulal-23/Sales-Performance-Data-Analysis-Dashboard/blob/c351e74df06986d3ea0e66b12dc1567758a7240c/Interaction.png)

**Insight:** Interactive filtering enables users to dynamically explore data, improving decision-making by focusing on specific segments.

---

##  Page 5: Detailed Table View
![Table](PASTE_IMAGE_LINK_5)

**Insight:** Provides granular-level data for deeper analysis, allowing validation of trends and identification of specific order-level patterns.
# Snapshot of Dashboard (Power BI Service)

![dashboard_snapo](https://user-images.githubusercontent.com/102996550/174096257-11f1aae5-203d-44fc-bfca-25d37faf3237.jpg)

 
 # Report Snapshot (Power BI DESKTOP)

 
![Dashboard_upload](https://user-images.githubusercontent.com/102996550/174074051-4f08287a-0568-4fdf-8ac9-6762e0d8fa94.jpg)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Customers = 129880

   Number of satisfied Customers (Male) = 28159 (21.68 %)

   Number of satisfied Customers (Female) = 28269 (21.76 %)

   Number of neutral/unsatisfied customers (Male) = 35822 (27.58 %)

   Number of neutral/unsatisfied customers (Female) = 37630 (28.97 %)


           thus, higher number of customers are neutral/unsatisfied.
           
### [2] Average Ratings

    a) Baggage Handling - 3.63/5
    b) Check-in Service - 3.31/5
    c) Cleanliness - 3.29/5
    d) Ease of online booking - 2.88/5
    e) Food & Drink - 3.21/5
    f) In-flight Entertainment - 3.36/5
    g) In-flight service - 3.64/5
    h) In-flight Wifi service - 2.81/5
    i) Leg room service - 3.37/5
    j) On-board service - 3.38/5
    k) Online boarding - 3.33/5
    l) Seat comfort - 3.44/5
    m) Departure & arrival convenience - 3.22/5
  
  while calculating average rating, null values have been ignored as they were not relevant for some customers. 
  
  These ratings will change if different visual filters will be applied.  
  
  ### [3] Average Delay 
  
      a) Average delay in arrival(minutes) - 15.09
      b) Average delay in departure(minutes) - 14.71
Average delay will change if different visual filters will be applied.

 ### [4] Some other insights
 
 ### Class
 
 1.1) 47.87 % customers travelled by Business class.
 
 1.2) 44.89 % customers travelled by Economy class.
 
 1.3) 7.25 % customers travelled by Economy plus class.
 
         thus, maximum customers travelled by Business class.
 
 ### Age Group
 
 2.1)  21.69 % customers belong to '0-25' age group.
 
 2.2)  52.44 % customers belong to '25-50' age group.
 
 2.3)  25.57 % customers belong to '50-75' age group.
 
 2.4)  0.31 % customers belong to '75-100' age group.
 
         thus, maximum customers belong to '25-50' age group.
         
### Customer Type

3.1) 18.31 % customers have customer type 'First time'.

3.2) 81.69 % customers have customer type 'returning'.
       
       thus, more customers have customer type 'returning'.

### Type of travel

4.1) 69.06 % customers have travel type 'Business'.

4.2) 30.94 % customers have travel type 'Personal'.

        thus, more customers have travel type 'Business'.
