# A. Introduction


**Problem statement:**  
The given data was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios, including the destination, current time, weather, and passengers. It then asks whether the driver will accept the coupon.

**Motivation for choosing this project:**    
Businesses frequently use targeted marketing strategies, with coupons serving as a common incentive to boost customer engagement and sales. The effectiveness of these coupons, however, depends on factors such as the customer's location, time of day, company, and personal preferences. By understanding the factors that influence a customer's decision to accept a coupon in various situations, businesses can optimize their promotional efforts.

**Our objective:**    
We aim to build a classification model to predict whether the coupon will be accepted or not in various driving scenarios based on customer and situational features. 

**Information on the dataset:** 

- Dataset Characteristics - Multivariate
- Subject Area            - Business
- Associated Tasks        - Classification
- Feature Type            - Categorical, Integer
- Instances in dataset    - 12684
- Features in dataset     - 25
- Has Missing Values?     - Yes
- Currency                - $ (USD)



**Information on the features:** 

**Note:** We use the original feature names from the dataset for consistency, even if they contain spelling errors (e.g., 'passanger' instead of 'passenger'). Additionally, monetary values in the dataset are represented with '$', but we use 'USD' in the comments to avoid Jupyter Notebook formatting issues.

- `destination` : No Urgent Place, Home, Work
- `passanger` : Alone, Friend(s), Kid(s), Partner (feature meaning : Who are the passengers in the car?)
- `weather` : Sunny, Rainy, Snowy
- `temperature` : 30, 55, 80
- `time` : 7AM, 10AM, 2PM, 6PM, 10PM
- `coupon` : Restaurant( < 20 USD), Coffee House, Carry out & Take away, Bar, Restaurant(20-50 USD)
- `expiration` : 1d, 2h (feature meaning : The coupon expires in 1 day or in 2 hours?)
- `gender` : Female, Male
- `age` : below21, 21, 26, 31, 36, 41, 46, 50 plus
- `maritalStatus` : Unmarried partner, Single, Married partner, Divorced, Widowed
- `has_Children` : 1, 0 (feature meaning : Do you have children? Yes = 1, No = 0)
- `education` : Some college - no degree, Bachelors degree, Associates degree, High School Graduate, Graduate degree (Masters or Doctorate), Some High School
- `occupation` : Unemployed, Architecture & Engineering, Student, Education&Training&Library, Healthcare Support, Healthcare Practitioners & Technical, Sales & Related, Management,  Arts Design Entertainment Sports & Media, Computer & Mathematical, Life Physical Social Science, Personal Care & Service, Community & Social Services, Office & Administrative Support, Construction & Extraction, Legal, Retired, Installation Maintenance & Repair, Transportation & Material Moving, Business & Financial, Protective Service, Food Preparation & Serving Related, Production Occupations, Building & Grounds Cleaning & Maintenance, Farming Fishing & Forestry
- `income` : Less than 12500, 12500-24999, 25000-37499, 37500-49999, 50000-62499, 62500-74999, 75000-87499, 87500-99999, 100000 or More (in USD)
- `car` : Car that is too old to install Onstar, crossover, do not drive, Mazda5, Scooter and motorcycle
- `Bar` : never, less1, 1-3, 4-8, gt8 (feature meaning : How many times do you go to a bar every month?)
- `CoffeeHouse` : never, less1, 1-3, 4-8, gt8 (feature meaning : How many times do you go to a coffeehouse every month?)
- `CarryAway` : never, less1, 1-3, 4-8, gt8 (feature meaning : How many times do you get take-away food every month?)
- `RestaurantLessThan20` : never, less1, 1-3, 4-8, gt8 (feature meaning : How many times do you go to a restaurant with an average expense per person of less than 20 USD every month?)
- `Restaurant20To50` : never, less1, 1-3, 4-8, gt8 (feature meaning : How many times do you go to a restaurant with average expense per person of 20-50 USD every month?)
- `toCoupon_GEQ5min` : 1 (feature meaning : Is the driving distance to the restaurant/bar for using the coupon greater than 5 minutes? Yes = 1)
- `toCoupon_GEQ15min` : 1, 0 (feature meaning : Is the driving distance to the restaurant/bar for using the coupon greater than 15 minutes? Yes = 1, No = 0)
- `toCoupon_GEQ25min` : 1, 0 (feature meaning : Is the driving distance to the restaurant/bar for using the coupon greater than 25 minutes? Yes = 1, No = 0)
- `direction_same` : 1, 0 (feature meaning : Whether the restaurant/bar is in the same direction as your current destination? Yes = 1, No = 0)
- `direction_opp` : 1, 0 (feature meaning : Whether the restaurant/bar is in the same direction as your current destination? Yes = 1, No = 0)

- **Information on target variable:**

- `Y` : 1, 0 (Whether the coupon is accepted? Yes = 1, No = 0)

**References used:** 
- Dataset from the repository:
  In-Vehicle Coupon Recommendation from UCI Machine Learning Repository. https://doi.org/10.24432/C5GS4P
- More information about the dataset, referred from the paper:
  Wang, Tong, Cynthia Rudin, Finale Doshi-Velez, Yimin Liu, Erica Klampfl, and Perry MacNeille.
  'A Bayesian framework for learning rule sets for interpretable classification.'
  The Journal of Machine Learning Research 18, no. 1 (2017): 2357-2393. https://www.jmlr.org/papers/volume18/16-003/16-003.pdf

**Important note:**    
Depending on the user's laptop configuration, this notebook may take 10-25 minutes to run.

- 
