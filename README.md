# Module-12-Challenge
The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. This challenge will serve to evaluate some of the ratings data in order to help their journalists of the food magazine food magazine, Eat Safe, Love and food critics decide where to focus future articles.

In this challenge I will work with NoSQL Databases using MongoDB instance and the libraries of PyMongo , Pretty Print and Pandas in Jupyter notebook. First I will import my data in json format from my terminal with the help of the path "C:\mongoimport.exe --type json -d uk_food -c establishments --drop --jsonArray establishments.json" and then I will develop the analysis.

The challenge will be divided into 3 parts and with two deliverables:

* Part 1: Database and Jupyter Notebook Set Up
* Part 2: Update the Database
* Part 3: Exploratory Analysis 

Deliverables 
* Deliverable 1: A Jupyter notebook containing code that imports the data and sets up and updates the uk_food database.
* Deliverable 2: A Jupyter notebook containing code that performs the exploratory analysis queries in the database.


# Part 1
Afer having imported my database through my terminal , imported the liberties PyMongo and Pretty Print (pprint) and having created the instance of Mongo Client port=27017 , I will :
* List the databases I have in MongoDB. Confirm that uk_food is listed.
* List the collection(s) in the database to ensure that establishments is there.
* Find and display one document in the establishments collection using find_one and display with pprint.
Finally I will assign the establishments collection to a variable to prepare the collection for use.

# Part 2
In this part I will update my database becuase one new restaurant have to be added to the analysis. For this I will begin by create a dictionary for the new restaurant data and insert the new restaurant into the collection.Then I will find the BusinessTypeID for "Restaurant/Cafe/Canteen" returning only the BusinessTypeID and BusinessType fields and I will update the new restaurant with the BusinessTypeID found.

Because the magazine is not interested in any establishments in Dover, I will check how many documents contain the Dover Local Authorit and I will remove it from the database. 

Finally I will do the excercise of convert longitud and latitudes stored values as strings to numbers.

# Part 3
In this exploratory part I will answer the following questions 
* Which establishments have a hygiene score equal to 20?
* Which establishments in London have a RatingValue greater than or equal to 4?
* What are the top 5 establishments with a RatingValue rating value of '5', sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
* How many establishments in each Local Authority area have a hygiene score of 0?

In this part I will use the method of aggregation to merge queries in a pipeline as well as $regex and $gte in order to delimite my search criteria. 

All the results of this section will be converted to Pandas DataFrame.


# References
UK Food Standards Agency (2022). UK food hygiene rating data API. https://ratings.food.gov.uk/open-data/en-GB. Contains public sector information licensed under the Open Government Licence v3.0
Accessed Sept 9, 2022 and Sept 12, 2022 with the establishment settings as follows: longitude=51.5072, latitude=-0.1276, maxdistancelimit=4567, pagesize=10000, sortoptionkey=distance, pagenumber=(1,2,3,4,5,6,7,8).
