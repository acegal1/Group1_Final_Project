# **UFO Sightings in Arizona**

![arizona ufo](/images/ufo%20arizona%202018.jpg)

## Group 1 Team Members: 
- Connie Aceves
- Angelica Rosario
- Jordan Peterson
- Katie Bernstein
***

# **Overview**
This respository includes the dataset, source code, images and other relevants documents for the Arizona UFO Sightings and Predictions project.

## Topic Rationale
Arizona is one of the top tourist destinations in the world for UFO sightings due to the high number of sightings over the last 50 years - totalling over 4600 sightings. As residents of Arizona, we selected this topic as a fun and interesting way to show the data visualization, machine learning, database and other data analytic skills we have learned throughout the bootcamp.

## Data Questions
* Does the amount of UFO sightings in Arizona increase at a similar rate as the population growth in Arizona cities?

***

# **Project Outline:** 

## Datasets

__UFO Sightings Data Source:__ https://www.kaggle.com/datasets/sadeghjalalian/ufo-sightings-in-usa

 Full text and geocoded UFO sighting reports from the National UFO Research Center (NUFORC). The National UFO Research Center (NUFORC) collects and serves over 100,000 reports of UFO sightings. This dataset contains the report content itself including the time, location duration, and other attributes in both the raw form as it is recorded on the NUFORC site as well as a refined, standardized form that also contains lat/lon coordinates. (source: kaggle.com)

__City and Population Data Source: US Census Bureau:__ https://data.census.gov/cedsci/

__World Population Review__ https://worldpopulationreview.com/

United States Census data was utilized to determine proper city naming conventions along with gathering population data for each year of the project scope (2000 to 2022) to allow us to analyze the growth of the cities in relationship to the number of sightings in each city.
***


### Data Cleaning (Extract, Transform, Load):
- The raw kaggle dataset was initally loaded into a jupyter notebook in Python

### Database
- Utilizing the Kaggle and population datasets, the data was loaded into a SQL database in PGAdmin and then exported into Python to be cleaned utilizing the ETL code created and then exported back into SQL. After the clean data for Arizona was imported back into SQL, the clean data table was then joined with the clean population table which held the Arizona cities and population data from the year 2000 to 2022. The table created can then be utilized to run the machine learning models. 
- We utilized a local instance of PGAdmin and a connection string using SQLAlchemy to connect to Python to demonstrate our team's database knowledge. Amazon Web Services (AWS) could be utilized for this process to hold the raw data files and the database and a connection string using SQLAlchemy to connect to Python/Google Colab for all team members to connect remotely and the provide the link to others outside the team as a longer term solution. 

SQL Database ERD (Entity Relationship Diagram)
![UFO AZ ERD](/images/UFO%20Final%20Project%20ERD%20Chart.png)

### Machine Learning Model 
We evaluated our data using the following models:
- Unsupervised K-means Clustering - we used this method because we had to convert all the labels to numbers 
- Google Colab - PySpark with Pandas
- SK Learn Module - Clustering
- ![Clustering](/images/UFO_3D_Clustering.png)
- Plotly
- ![plot](/images/UFO_Elbow.png)
- Matplotlib
- ![matplotlib](/images/UFO_Clusters.png)
- HV Plot
- ![plot](/images/UFO_Scaled.png)



### Presentation

Link to Presentation Slides

Power BI Slides

### Future Analysis and Recommendations
__National UFO Reporting Center Recommendations:__
- Less free form answers – more drop down options to reduce the amount of non-sense data or variability in the data. 
- Sighting Validation – new column or area of data where NUFORC can add their feedback that either approves or denies the sightings. Currently it is listed in the comment box. 

__Additional Datasets to include:__
- Weather Patterns
- Locations of Government Testing Sites, Military Bases and other business locations that might effect the data.
