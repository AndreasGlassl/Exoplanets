# Exoplanets
Steps to finding planets which maybe inhabitable for humans:

    1.Get a dataframe on exoplanets from the Nasa API. Also downloaded a CSV from exoplanet.eu, which contains information about exoplanets gathered from several European institutions. Writing the file to a csv file in the "data/nasa" folder.

    2. Retrieving the descriptions for the column names of the nasa data via web-scraping and then putting it into a json dictionary file for later use.

    3.Retrieving the information about the exoplanet temperatures from nasa, which is done in a seperate API request and later merged with the current DataFrame. 

    4. Due to connotation differences, before merging the tables on the planet name, there were some replacements within the strings, as far as found helpful. Left joining the tables and saving it into the "data/combined" folder.

    5. Filtering for Temperatures: If there is temperatures within the nasa part of the DataFrame, which are NaN, they will be replaced with the according cell of the temperatures from the EU. (that way, the missing values - if there - can be added to the temperature column which is to be kept after)

    6. Adding some more columns, such as converting the distance to km, getting the travel time in years for a car, a plane and a rocket.

    7. using the dictionary from step 2 to change the names of the columns left for better readability.

    8.Thinking of 2 ways to find life:

        a)If there is a star similar to our sun and the period in which the planet revolves around it, the distance between the star and the planet will be similar to ours. Therefore the conditions for life might be met. Although we have not yet considered density, g-force etc.
    
        b)For life to exist as we know it, there must be a certain range of temperatures. This means, that we can filter for temperatures simply and then take into account all options which are in a certain range of distance. 
