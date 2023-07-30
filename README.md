# nosql_challenge (MongoDB)

I used VS Code for this challenge, which included the evaluation of ratings of restaurants across the UK. I imported the data from the establishments.json file by typing the following command onto my terminal.  

mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json.

The database on my computer was named uk_food, and the collection was named establishments. Steps involved in analysis:

1. pandas, Pymongo, and pprint were imported into the VSCode.

2. An instance of Mongoclient was created.

3. Information about a new restaurant was added to the database, and its BusineeTypeID was changed to BusinessTypeID for Restaurant/Cafe/Canteen.

4. Documents for Dover as the Local Authority were deleted as they were not needed for the analysis.

5. Latitude and longitude values were converted from string to decimal.

6. Queries were written to answer the following questions:
   
     a. Which establishments have a hygiene score equal to 20?

     b. Which establishments in London have a RatingValue greater than or equal to 4?

     c. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

     d. How many establishments in each Local Authority area have a hygiene score 0? Sort the results from highest to lowest, and print out the top ten local authority        areas.

   The results from these queries were changed to pandas Dataframes.
