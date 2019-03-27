## *JupyterNotebook for project*: https://gist.github.com/78d1ad441ab1f406ca636d4d7438d300

## Project report

_Introduction where you discuss the business problem and who would be interested in this project._


When planning to set a business, usually "local" information is required. FOr instance, such area is popular for coffee shops.
ANd it is usually learnt by hearing it from other people.
The aim of this project would be to be able to gather that info on which areas are more popular for a specific type of venue
A KNN clustering will be performed, being the venue type the response variable, and latitude and longitude the predicting variables.


_Data where you describe the data that will be used to solve the problem and the source of the data._
'''
This project will work with the City of Buenos Aires.
ITs coordinates are taken with geocode, and from them, venues searches are performed with the foursquare API.


Thus, the database will have the venues IDs, their category, their latitude & longitude. 
With the result, a predicted venue type will be included as well. 

'''



_Methodology section which represents the main component of the report where you discuss and describe any exploratory data analysis that
you did, any inferential statistical testing that you performed, and what machine learnings were used and why._

1. Select a city.
2. Obtain its centroid latitude and longitude
3. From those coordinates, use the foursquare API, exploring venues of two different categories.
4. Retrieve the results' coordinates, venue category, and store them in a df.
5. Perform a KNN on the df, being the predicting variables the coordinates and the response the venue category.
6. Graph & evaluate. 


_Results section where you discuss the results._
 - The first limitant was the foursquare limit: 50 different ids and it was not possible to specify a new query with different responses.
 - With that limited amount of entries, a train test split was not worth its deployment.
 - K was iterated from 1 to 11, and at 7 the highest accuracy was obtained: 70%, which is sufficiently high. 



_Discussion section where you discuss any observations you noted and any recommendations you can make based on the results._
- Hypothesis testing (parametric) could be performed as well
- The more data, the merrier



_Conclusion section where you conclude the report._
The accuracy was of 70%, which for a non-parametric is on the boundary for sufficient evidence to affirm the classiffication was 
justified. The next steps would be performing a general explore and obtain the distribution of distinct venues type, classifying them 
as well. 
