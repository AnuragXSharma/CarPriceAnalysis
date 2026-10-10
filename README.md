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
Linear regression 
Ridge regression
Laso regression
# Model Evaluation
We then measure model performance based on MAE & R2 values and found out that Ridge Regression is better suited though though all the values are almost similar. However, under same MAE and R2 score Ridge regression is preferrable due to Overfitting & Multicollinearity Prevention

# Receomendtion & Findings
Here are the key strategic recommendations we can make to help them optimize their inventory and pricing strategies:

**Highlight of Positive Price Drivers (What to Buy/Stock)**
Vehicle Age (Year of Manufacture): The year variable has a strong positive coefficient, indicating that newer vehicles command significantly higher prices. For every year newer a car is, its price rises predictably.
Engine Configuration (Cylinders): Vehicles with more cylinders (such as cylinders_8 cylinders or cylinders_10 cylinders) generally have high positive coefficients. Stocking high-displacement trucks, SUVs, or sports cars represents a higher-revenue segment.
Four-Wheel/All-Wheel Drive (drive_4wd): 4WD and AWD options significantly boost a vehicle's value compared to front-wheel drive (drive_fwd). Dealers should prioritize buying 4WD configurations, especially in markets prone to winter weather.
Fuel Type: Diesel vehicles (fuel_diesel) typically carry a high positive premium compared to standard gasoline cars due to their towing capabilities and longevity.
**Highlight of Negative Price Drivers (What to Avoid or Price Conservatively)**
High Mileage (odometer): Odometer has a strong negative coefficient. Every mile added directly chips away at a car's value. Dealers should be wary of high-mileage trade-ins unless they are heavily discounted.
Title Status Limitations: Vehicles without a clean title (such as title_status_salvage, title_status_rebuilt, or title_status_parts only) have massive negative coefficients. These cars dramatically reduce resale value and turn off the majority of consumers.
Manual Transmissions: In modern markets, automatic or other advanced transmissions are generally preferred over standard manual options (transmission_manual), which often lower the average selling price of mainstream vehicles.
**Actionable Strategic Summary for Dealers:**
Target Inventory: Maximize profit margins by acquiring newer, low-mileage vehicles with 4WD, diesel engines, or V8 configurations.
Sourcing Caution: Be extremely cautious when bidding on vehicles with rebuilt/salvage titles or manual transmissions unless they are priced well below trade-in value, as these features severely depress the vehicle's retail potential.
