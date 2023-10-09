# Fetch-Assessment
This repository contains all the files that were required for the completion of the Fetch Assessment. 

Initially, this task was tried using various ML models to check how the result would appear. Out of the traditional ML models, Random Forest
Regressor was the best-performing model and gave decent enough results. So, it was decided that this was the model that should be chosen and
it was written from scratch as it can be found in the RandomForestReg.ipynb file. 

In this code, random forest regression was implemented from scratch with the use of decision tree as its base, and further GARCH was used to 
smoothen the and get a more accurate result. However, this did not provide satisfying results and the computational time was too large as well
hence, I decided that I should try some other methods.

I then tried different statistical models and wrote them from scratch as well. The main model that was giving results was ARIMA, the code
for both the model written using the library and the one written from scratch can be found in this repository named Arimalib.ipynb and 
ARIMA_scratch.ipynb. 

But the result obtained from the code written from scratch didn't provide results similar to the stats model and I then decided to venturer into
Neural Networks. I tried out various CNN architectures and finally settled on LSTM. This model was giving out good results and unlike random 
forest, its computational time was low.




