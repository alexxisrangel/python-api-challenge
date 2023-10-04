# python-api-challenge


## Background 

Data's true power is its ability to definitively answer questions. So, let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What is the weather like as we approach the equator?"
Now, we know what you may be thinking: “That’s obvious. It gets hotter.” But, if pressed for more information, how would you prove that?



### Before You Begin (Requirements)

Create a new repository for this project called python-api-challenge. Do not add this homework to an existing repository.

Clone the new repository to your computer.

Inside your local Git repository, create a directory for this assignment. Use a folder name that corresponds to the Challenges, such as WeatherPy.

Inside the folder you just created, add the files called api_keys.py, WeatherPy.ipynb, and VacationPy.ipynb that you will find in the starter code ZIP file provided. These will be the main scripts to run for each analysis.

Before you push your changes to GitHub, add a .gitignore file.

Add a .gitignore File
For this assignment, you will need to add a .gitignore file to your repo. Doing so will prevent the api_keys.py file that contains your API key from being shared with the public. If you skip this step, anyone using GitHub could copy and use your API key, and you may incur charges as a result.

To get started, type git status in the command line to see a list of all the untracked files that you have created so far.

To add only the WeatherPy.ipynb file to GitHub, for example, type git add WeatherPy.ipynb. Keep in mind that you would have to add each file individually when adding or updating a file. A more efficient solution is to add all of the files that you don't want to track to the .gitignore file.

Before adding your files to GitHub, add api_keys.py to the .gitignore file by following these steps:

Open your python-api-challenge GitHub folder in VS Code.

Open the .gitignore file and type the following code on the first line:

# Adding config.py file.
api_keys.py
In the command line, type git status and press Enter. The output should indicate that the .gitignore file has been modified and the api_keys.py file is untracked.


#### Instructions

This activity is broken down into two deliverables, WeatherPy and VacationPy.


##### WeatherPy Deliverable 

In this deliverable I vizualizes over 500 cities varying distances near the equator. I used  citipy Python library and the OpenWeatherMap API in order to obtain the neccessry data required. 

Importing dependencies 

/var/folders/w9/1qf67rw90dgbqv7rkw546lvh0000gn/T/TemporaryItems/NSIRD_screencaptureui_9TJDFj/Screenshot 2023-10-03 at 2.41.09 PM.png

Generating Citites List with the citipy Library 

/var/folders/w9/1qf67rw90dgbqv7rkw546lvh0000gn/T/TemporaryItems/NSIRD_screencaptureui_hbdeGU/Screenshot 2023-10-03 at 2.42.42 PM.png

 
 Creating connection to API 
/var/folders/w9/1qf67rw90dgbqv7rkw546lvh0000gn/T/TemporaryItems/NSIRD_screencaptureui_IT4aql/Screenshot 2023-10-03 at 2.46.02 PM.png


Creating loop in order to extract nececessry data and adding it to my city_data list
/var/folders/w9/1qf67rw90dgbqv7rkw546lvh0000gn/T/TemporaryItems/NSIRD_screencaptureui_DfzIVK/Screenshot 2023-10-03 at 2.47.22 PM.png

After converting data into a DataFrame, I was able to create the following plots: 


Latitude vs. Temperature

<img width="690" alt="Screenshot 2023-10-03 at 2 50 36 PM" src="https://github.com/alexxisrangel/python-api-challenge/assets/129305054/266ca687-5a23-4dec-85f3-1971ff2e398e">


Latitude vs. Humidity

/var/folders/w9/1qf67rw90dgbqv7rkw546lvh0000gn/T/TemporaryItems/NSIRD_screencaptureui_PVnRJh/Screenshot 2023-10-03 at 2.52.01 PM.png

Latitude vs. Cloudiness

![Uploading Screenshot 2023-10-03 at 2.52.23 PM.png…]()


Latitude vs. Wind Speed

![Uploading Screenshot 2023-10-03 at 2.52.44 PM.png…]()


Linear Regression 

/var/folders/w9/1qf67rw90dgbqv7rkw546lvh0000gn/T/TemporaryItems/NSIRD_screencaptureui_duZnPO/Screenshot 2023-10-03 at 3.01.26 PM.png



After reviewing linear regression for each relationship I noticed that the r-value was not very high for most relationships. The highest correlation I found was for Temperature vs. Lattitude for the Northern Hemisphere. It had an r-value of 0.7. What we can see from the reationship is that temperatures tend to drop the closer we get to lattitude 100 and we see higher temeperatures the closer we get to 0. 


VacationPy Deliverable
In this deliverable I used my weather data in order to plan future vacations using Jupyter notebooks, the geoViews Python library, and the Geoapify API.

Creating Map 
After importing my dependecies and creating a DataFrame from my ciites.csv I created a map that displayed a point for every city in my DataFrame. The size of each point reflects the humidity for each city. 

/var/folders/w9/1qf67rw90dgbqv7rkw546lvh0000gn/T/TemporaryItems/NSIRD_screencaptureui_XZWl4f/Screenshot 2023-10-03 at 3.21.34 PM.png

Narrowing Search 
I narrowed down my cities to the ideal conditions I would like while being on vacation /var/folders/w9/1qf67rw90dgbqv7rkw546lvh0000gn/T/TemporaryItems/NSIRD_screencaptureui_wxjYSk/Screenshot 2023-10-03 at 3.23.06 PM.png


Geoapify API 

I used the geoapify API in order to get a list of hotels within the city limits of my ideal weather conidtions. For this step I created a loop thats iterates through the API, looksd for hotels within 10000 m of my city and logs the results for me
/var/folders/w9/1qf67rw90dgbqv7rkw546lvh0000gn/T/TemporaryItems/NSIRD_screencaptureui_O10DT3/Screenshot 2023-10-03 at 3.25.00 PM.png


Hover Message displaying Hotel Name and country 











