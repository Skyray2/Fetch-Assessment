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

Then, I decided to develop a one-page website using HTML. This website provides basic information about the data and then asks the user to select the
month for which they want to obtain the predicted data for the year 2022. It also at the bottom shows the overall graph with the data predicted
which is concatenated with the graph from the year 2021. 

Then, I made a .py file called app.py which allows the ML model to be mounted on to website. For this file to run I had to call the functions of the 
LSTM model from another .py file titled MyLSTM.py. 

# Instructions for Running the Files


## Docker pull Instructions: 

Make sure that you have opened the Dockerhub. Open the terminal or command prompt in your system and type:

docker pull sbaskar2/fetch-assessment-final:0.0.1.RELEASE

After the container is pulled type the below command in the terminal:

docker container run -d -p 1000:5000 sbaskar2/fetch-assessment-final:0.0.1.RELEASE

Press enter after you have typed this. Now, open your browser and type: localhost:1000

You'll be able to view the website now. 

If you get an error saying the port is already allocated then try a different number instead of 1000 like 2000 or 3000 or any other 4 digit number, for ex:

docker container run -d -p 2000:5000 sbaskar2/fetch-assessment-final:0.0.1.RELEASE 

and follow the same instruction above of opening the browser and typing in localhost:????. The number that you have chosen to replace 1000. 

## Alternate Method

If the files are directly downloaded from the GitHub repository then, make sure that all the downloaded files are in the same directory. 
Open app.py and run the file. You'll be able to find the URL for the website in the terminal that would be hosted as a local host.




