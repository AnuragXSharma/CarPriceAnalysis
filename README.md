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
We use three algorithm to develop our models and see which value suits the data best. Three algorithm used are 
Ridge regression
Laso regression
# Model Evaluation
We then measure model performance based on MAE & R2 values and found out that Ridge Regression is better suited though though all the values are almost similar. However, under same MAE and R2 score Ridge regression is preferrable due to Overfitting & Multicollinearity Prevention

# Recommendations & Findings
Here are the key strategic recommendations we can make to help them optimize their inventory and pricing strategies:
Business Meaning: The features we tracked (manufacturer, age, odometer mileage, engine cylinders, fuel type, etc.) explain 61.9% of the overall variance in used car prices.
**Top Drivers Maximizing Vehicle Price (What Consumers Value)**
     1. Luxury & Exotic Brand Equity: Brands like Ferrari (+$51,820), **Morgan** (+$$51,820), **Morgan** (+$24,473), Aston-Martin (+$22,405), and **Tesla** (+$$22,405), and **Tesla** (+$15,731) hold significant value premiums.
     2. Vehicle Capability & Utility: Pickups (+$3,984) and **Trucks** (+$$3,984) and **Trucks** (+$3,548) carry substantial body-type utility premiums.
     3. Cars with larger 12-cylinder engines command a premium of around +$4,595.
**Top Drivers Minimizing Vehicle Price (What Lowers Valuation)**
Power Source / Fuel Type: Compared to diesel options, electric vehicles (-$17,293) and **gasoline cars** (-$$17,293) and **gasoline cars** (-$13,936) carry strong negative price associations in the secondary market.
Low-Performance or Smaller Engines: Small 3-cylinder engines reduce the estimated price by **-$10,620**. * **Specific Brand Penalties**: Brands like **Harley-Davidson** badged vehicles (-$$10,620**. * **Specific Brand Penalties**: Brands like **Harley-Davidson** badged vehicles (-$14,261) and Fiat (-$10,410) carry steep negative pricing adjustments.
**Strategic Action Plan for Your Dealership:**
Focus on Trucks and Pickups: These body styles carry robust premiums regardless of brand.
Manage EV/Gas Inventory Wisely: Diesel and hybrid models hold strong margins, whereas electric vehicles face steep depreciation factors in this dataset.
Use the $6,000 Baseline: Train your acquisition team to use this automated baseline pricing to avoid overpaying for inventory.
