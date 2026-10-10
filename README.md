# CarPriceAnalysis
Analyse the car prices based on dataset containing information of 426 k cars from Kaggele and understand what factors impact prices of car

# Following the CRISP DM method. Here are key takeaways

# Business understanding
Provide information based on data to car dealers on what factors determine price of car so that they can make informed decision on their car inventory
# Data Understanding & Data Preparation
After considering the business understanding, we want to get familiar with our data. 
Step 1: Find the missing values in data set and drop the data which has high missing percentage insufficient to make analyis
Step 2: Dropping Irrelevant Identifiers like VIN# and ID
        Dropping regions and state to reduce noise
        Filtering Outliers like price $500 and more than $100K ; odometer less than 100 and more than 300K; Remove rows where vehcile manufacturer year is missing        
Step 3: Handling Remaining Missing Categorical Data: Rather than dropping missing records, categorical missing values in features like manufacturer, model, condition, cylinders, fuel, title_status, transmission, drive, type, and paint_color were imputed with a placeholder label: 'unknown'. This preserves sample size for training models.

# Data Modeling
