# Module4 Zillow Best Zipcode
### Libraries used:
#### Pandas
#### Matplotlib
#### pyramid.arima
#### multiprocessing
#### fbprophet
#### sklearn
#### math
##  Methodology
###### 1. I used some Zillow API data to figure out which zipcodes in the whole country are the best to invest in.
###### 2. I processed the data using the very fast Pandas python library with all of its built-ins. I melted the data and removed a few zipcodes that did not have all the value information. The data is from 1996-2018 and in a monthly time series of the median home value per zipcode. 
###### 3. I sampled the top 5 best long term historical return percentage from each state because I could not run models on all the data.
###### 4. I used the FBprophet library that is used to build time series models quickly and easily. I used the parameters that are the defaults because I did not have enough computing resources or time to do more parameter searching. 
###### 5. I did cross validation splits at 60% training 40% test, 70% training 30% test, and 80% training 20% test. I calculated the Mean Squared Error from each train test split and stored the results into the results dictionary.
###### 6. I then ran a model on the whole dataset and predicted into the future 1 year, 2 years, and 4 years. I stored all of these in the results dictionary.
###### 7. Then I calculated if there was an uptrend from the current price to the end of the 4th year prediction. I did this to lower the risk. If there was no uptrend I removed the zipcode.
###### 8. I then deleted any zipcodes that didn't have a Mean Absolute Percent Error of less than 15%. This means that if the zipcode had a price of 100 and the average error was more than 15% or say from 80 - 120 then the error was too high.
###### 9. I calculated the profit for each time period predicted and stored that in the results dictionary. Then I filtered so that the best investments were at the top of the dictionary.
###### 10. I have a few graphs showing the best returns and the error rates. 
###### 11. A few extra things were that I tried multiprocessing but I couldn't get it to work. My conclusion on the project was that investing isn't that good or it is not an easy way to make a good return compared to other types of investments but that the top 5 zipcodes from my sample were not very good in my opinion.



## Be careful there is an error in the data, there are a few missing values in a few zipcodes. If you read the comments you can see where you will have to run items in the jupyter notebook out of order. It shouldn't be that much of a problem.





Thanks!
