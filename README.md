# CouponAcceptancePredictor
## This ML project aims at predicting if a particular customer will accept the coupon if he is the driver.

### The dataset was obtained from Kaggle 
(https://www.kaggle.com/mathurinache/invehicle-coupon-recommendation).

This data was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver.

This project uses Random Forest Classifier for prediction.(All classification algorithms like Naive Bayes, Logistic Regression, XGBoost, Support Vector Regression, etc. were used, but the best accuracy was from Random Forest(77.6%)

Following are the columns in the dataset:

1. destination: No Urgent Place, Home, Work
2. passanger: Alone, Friend(s), Kid(s), Partner (who are the passengers in the car)
3. weather: Sunny, Rainy, Snowy
4. temperature:55, 80, 30
5. time: 2PM, 10AM, 6PM, 7AM, 10PM
6. coupon: Restaurant(<$20), Coffee House, Carry out & Take away, Bar, Restaurant($20-$50)
7. expiration: 1d, 2h (the coupon expires in 1 day or in 2 hours)
8. gender: Female, Male
9. age: 21, 46, 26, 31, 41, 50plus, 36, below21
10. maritalStatus: Unmarried partner, Single, Married partner, Divorced, Widowed
11. hasChildren:1, 0 
12. education: Some college - no degree, Bachelors degree, Associates degree, High School Graduate, Graduate degree (Masters or Doctorate), Some High School 
13. occupation: Unemployed, Architecture & Engineering, Student, Education&Training&Library, Healthcare Support, Healthcare Practitioners & Technical, Sales & Related,     Management, Arts Design Entertainment Sports & Media, Computer & Mathematical, Life Physical Social Science, Personal Care & Service, Community & Social Services, Office & Administrative Support, Construction & Extraction, Legal, Retired, Installation Maintenance & Repair, Transportation & Material Moving, Business & Financial, Protective Service, Food Preparation & Serving Related, Production Occupations, Building & Grounds Cleaning & Maintenance, Farming Fishing & Forestry 
14. income: $37500 - $49999, $62500 - $74999, $12500 - $24999, $75000 - $87499, $50000 - $62499, $25000 - $37499, $100000 or More, $87500 - $99999, Less than $12500 
15. Bar: never, less1, 1~3, gt8, nan4~8 (feature meaning: how many times do you go to a bar every month?) 
16. CoffeeHouse: never, less1, 4~8, 1~3, gt8, nan (feature meaning: how many times do you go to a coffeehouse every month?) 
17. CarryAway:n4~8, 1~3, gt8, less1, never (feature meaning: how many times do you get take-away food every month?) 
18. RestaurantLessThan20: 4~8, 1~3, less1, gt8, never (feature meaning: how many times do you go to a restaurant with an average expense per person of less than $20 every month?) 
19. Restaurant20To50: 1~3, less1, never, gt8, 4~8, nan (feature meaning: how many times do you go to a restaurant with average expense per person of $20 - $50 every month?)
20. toCouponGEQ15min:0,1 (feature meaning: driving distance to the restaurant/bar for using the coupon is greater than 15 minutes)
21. toCouponGEQ25min:0, 1 (feature meaning: driving distance to the restaurant/bar for using the coupon is greater than 25 minutes) 
22. directionsame:0, 1 (feature meaning: whether the restaurant/bar is in the same direction as your current destination)
23. direction_opp:1, 0 (feature meaning: whether the restaurant/bar is in the same direction as your current destination)
24. Y:1, 0 (whether the coupon is accepted) -- Dependent variable
