# Project Title

# Amazon Sales Report



## Report Overview
The Amazon Sales Dashboard provides a comprehensive overview of sales performance, focusing on key metrics such as total sales, sales count, and sales units. This interactive report is designed to enable businesses to analyze their performance across multiple dimensions, such as status of orders, geographic distribution of sales, and product categories.

## Skills used
- Data tranformation
- Dashboard designed
- Tooltip
- Use of bookmarks


## Processes
- Data Tranformation

- Creation Dax measures and Calculated columns

- Data Modelling

#### Data Transformation

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor 
- Step 3 : Performed data transformation on both tables imported

![Transformation_1](https://github.com/user-attachments/assets/a895064d-c5ca-40b8-81cb-478513a6ce2a)

![Transformation _2](https://github.com/user-attachments/assets/7a577845-7382-4551-a912-0de611aa7d35)

- Step 4 : Then closed and applied changes.

#### Dax Measures
- Step 1 : Created a data table for "Sales" and " Unit"
![DataTable](https://github.com/user-attachments/assets/988fcf72-d2a5-42a7-b121-8597446e7218)
- Step 2 : Created neccessary Dax measures to visual KPI for the report such as Total sale,Sales count and Sales

Below are some the Dax measures created

      Filter_sale = 
      VAR _select = SELECTEDVALUE(Sale_Option[Type])
      RETURN IF(_select ="1",[Sale_Amount],[Sale_Units])
        

     All_Overall_sale = 
    CALCULATE([Filter_sale],ALL('amazon-fashion - YT'[Category])) 


     Seller_Count = 
     var val = CALCULATE(COUNT('amazon-fashion - 
     YT' [seller_name]),CONTAINSSTRING(Amazon[Status],"Delivered"))
     return IF(val=BLANK(),"0",val)

      
     
           

#### Dax Modelling    
        
- Created connections between tables to create and interactive report.

![DataModelling](https://github.com/user-attachments/assets/9b92af29-b0b7-4265-ad1e-5de077f1e4a8)


#### Data Visualization

- Created page navigation button on all pages of the report for ease of navigation between pages of the report
  
  ![Page navigation ](https://github.com/user-attachments/assets/86a9edaf-f5bf-4609-bdbe-8501abc07d23)
 
 - Also created an in page navigator button for users interact with the numbers of sales and unit 

 ![In page Navigation](https://github.com/user-attachments/assets/02703861-1335-4086-9632-9552013d6952)

# Snapshot of Dashboard (Power BI Service)


The report was then published to Power BI Service.
 
 
![Amazon service report](https://github.com/user-attachments/assets/b8027c70-7db8-4a77-ab3b-d0ddae384bb2)



#  Snapshot of all report pages (Power BI DESKTOP)
![Overview page](https://github.com/user-attachments/assets/4881e211-7497-4ca1-b766-84823cab9441)

![Product Page](https://github.com/user-attachments/assets/1a657815-4450-4b40-9ece-4db6cd48eae7)

![Product view Page](https://github.com/user-attachments/assets/7a38a5dc-37e2-4431-990f-a05ba0faaf6d)
