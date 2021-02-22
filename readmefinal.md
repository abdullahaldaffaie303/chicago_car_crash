##### Phase 3 Project #####

# Chicago Car Crashes

## Traffic Crashes - Crashes Data 
Dataset&Columns Description can be found here 
[https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if]

## -Columns in Traffic Crashes - Crashes Data

Column Name&Description	

- CRASH_RECORD_ID	
This number can be used to link to the same crash in the Vehicles and People datasets. This number also serves as a unique ID in this dataset.

- RD_NO	
Chicago Police Department report number. For privacy reasons, this column is blank for recent crashes.

- CRASH_DATE_EST_I	
Crash date estimated by desk officer or reporting party (only used in cases where crash is reported at police station days after the crash)

- CRASH_DATE	
Date and time of crash as entered by the reporting officer

- POSTED_SPEED_LIMIT	
Posted speed limit, as determined by reporting officer

- TRAFFIC_CONTROL_DEVICE	
Traffic control device present at crash location, as determined by reporting officer

- DEVICE_CONDITION	
Condition of traffic control device, as determined by reporting officer

- WEATHER_CONDITION	
Weather condition at time of crash, as determined by reporting officer

- LIGHTING_CONDITION	
Light condition at time of crash, as determined by reporting officer

- FIRST_CRASH_TYPE	
Type of first collision in crash

- TRAFFICWAY_TYPE	
Trafficway type, as determined by reporting officer

- LANE_CNT	
Total number of through lanes in either direction, excluding turn lanes, as determined by reporting officer (0 = intersection)

- ALIGNMENT	
Street alignment at crash location, as determined by reporting officer

- ROADWAY_SURFACE_COND	
Road surface condition, as determined by reporting officer

- ROAD_DEFECT	
Road defects, as determined by reporting officer

- REPORT_TYPE	
Administrative report type (at scene, at desk, amended)

- CRASH_TYPE	
A general severity classification for the crash. Can be either Injury and/or Tow Due to Crash or No Injury / Drive Away

- INTERSECTION_RELATED_I	
A field observation by the police officer whether an intersection played a role in the crash. Does not represent whether or not the crash occurred within the intersection.

- NOT_RIGHT_OF_WAY_I	
Whether the crash begun or first contact was made outside of the public right-of-way.

- HIT_AND_RUN_I	
Crash did/did not involve a driver who caused the crash and fled the scene without exchanging information and/or rendering aid

- DAMAGE	
A field observation of estimated damage.

- DATE_POLICE_NOTIFIED	
Calendar date on which police were notified of the crash

- PRIM_CONTRIBUTORY_CAUSE	
The factor which was most significant in causing the crash, as determined by officer judgment

- SEC_CONTRIBUTORY_CAUSE	
The factor which was second most significant in causing the crash, as determined by officer judgment

- STREET_NO	
Street address number of crash location, as determined by reporting officer

- STREET_DIRECTION	
Street address direction (N,E,S,W) of crash location, as determined by reporting officer

- STREET_NAME	
Street address name of crash location, as determined by reporting officer

- BEAT_OF_OCCURRENCE	
Chicago Police Department Beat ID. Boundaries available at https://data.cityofchicago.org/d/aerh-rz74

- PHOTOS_TAKEN_I	
Whether the Chicago Police Department took photos at the location of the crash

- STATEMENTS_TAKEN_I	
Whether statements were taken from unit(s) involved in crash

- DOORING_I	
Whether crash involved a motor vehicle occupant opening a door into the travel path of a bicyclist, causing a crash

- WORK_ZONE_I	
Whether the crash occurred in an active work zone

- WORK_ZONE_TYPE	
The type of work zone, if any

- WORKERS_PRESENT_I	
Whether construction workers were present in an active work zone at crash location

- NUM_UNITS	
Number of units involved in the crash. A unit can be a motor vehicle, a pedestrian, a bicyclist, or another non-passenger roadway user. Each unit represents a mode of traffic with an independent trajectory.

- MOST_SEVERE_INJURY	
Most severe injury sustained by any person involved in the crash

- INJURIES_TOTAL	
Total persons sustaining fatal, incapacitating, non-incapacitating, and possible injuries as determined by the reporting officer

- INJURIES_FATAL	
Total persons sustaining fatal injuries in the crash

- INJURIES_INCAPACITATING	
Total persons sustaining incapacitating/serious injuries in the crash as determined by the reporting officer. Any injury other than fatal injury, which prevents the injured person from walking, driving, or normally continuing the activities they were capable of performing before the injury occurred. Includes severe lacerations, broken limbs, skull or chest injuries, and abdominal injuries.

- INJURIES_NON_INCAPACITATING	
Total persons sustaining non-incapacitating injuries in the crash as determined by the reporting officer. Any injury, other than fatal or incapacitating injury, which is evident to observers at the scene of the crash. Includes lump on head, abrasions, bruises, and minor lacerations.

- INJURIES_REPORTED_NOT_EVIDENT	
Total persons sustaining possible injuries in the crash as determined by the reporting officer. Includes momentary unconsciousness, claims of injuries not evident, limping, complaint of pain, nausea, and hysteria.

- INJURIES_NO_INDICATION	
Total persons sustaining no injuries in the crash as determined by the reporting officer

- INJURIES_UNKNOWN	
Total persons for whom injuries sustained, if any, are unknown

- CRASH_HOUR	
The hour of the day component of CRASH_DATE.

- CRASH_DAY_OF_WEEK	
The day of the week component of CRASH_DATE. Sunday=1

- CRASH_MONTH	
The month component of CRASH_DATE.

- LATITUDE	
The latitude of the crash location, as determined by reporting officer, as derived from the reported address of crash

- LONGITUDE	
The longitude of the crash location, as determined by reporting officer, as derived from the reported address of crash

- LOCATION	
The crash location, as determined by reporting officer, as derived from the reported address of crash, in a column type that allows for mapping and other geographic analysis in the data portal software

# -Business problem 

Chicago, on Lake Michigan in Illinois, is among the largest cities in the U.S.
Chicago Vehicle Safety Board interested in reducing traffic accidents in the city.
The provided dataset consist of a large amount of collision data recorded over many years in the Chicago city. This dataset also provides various information which are some related to the cause of the crash.

# -Data Cleaning & Pre-Processing

This dataset is obtained from Chicago Data Portal and usually any dataset obtained will not be in a clean format, it will always contain some missing values and some irrelevant data. This dataset too consist of a lot of missing values and useless data. so before further processing the data it is important to clean the dataset.

- Cleaning Binary columns. 
- Cleaning categorical columns.
- Cleaning columns with a lot of missing values and not useful and irrelevant for Predicting     of our model.
- Drop irrelevant columns to predict our model.

# -Data exploration 

 Exploring the columns and their values and finding the best way organize them. 
 The dataset was very large which made it Difficult to navigate through it. In the 
 First notebook I decided to drop lots of columns so I do not run into issue such as 
 Memory size, computer slowing down and categorizing the column's values. I noticed 
 Lots of the Binary columns had missing data, and the categorical columns had lot 
 of similar Variables I can group.
 

# - visualization

![Primary Crash Cause vs Number of Crashes](images/1.png)

![Primary Crash Cause Vs injuries](images/2.png)

![Primary Crash Cause Vs Fatal](images/3.png)

![Weather Conditions Vs Number of Crashes](images/4.png)

![Light conditions Vs Number of Crashes](images/5.png)

# - Cleaning categorical Columns 

- First notebook since I was worried about the computer slowing down because of the large
  data, I thought i would be good idea to group the variables in the categorical columns
  and narrow them down to two variables, and the second reason i decided to use this way 
  because i thought by narrowing down the variables that would help my model accuracy.
  
  For Binary variables I decided to full their missing data with NOs, and switched the 
  YESs to 1 and NOs to 0 since machine learning algorithms works with Digits. I decided to 
  use this approach because most of the Binary columns were Relevant to the model prediction 
  and they had lots of missing data and i wanted to avoid dropping NAn. 
  
  For the target column I organized the variables from the top 5 primary cause of crash, 
  I listed the variables with the least data all together under others.
  

- Second notebook I decide to add more columns to help with my model accuracy.
  and did not group the categorical columns variables.

# -Modeling

- I used [ Decision Tree, Random Forest Classifier, Logistic Regression ]



- Conclusion
  
  Initially, The classifiers had an prediction accuracy of 39%, however, upon going back   to the data preparation and taking additional fields in the dataset improved the overall       accuracy of all models.
  The accuracy of the classifiers is ok, i.e.0.59% . This means that the model has              trained better this time around and fits the training data and performs well on the testing set as well as the training set. We can conclude that this model can predict the primary cause of the crashes in Chicago with an Accuracy of 60%.
  
  

jupyter nbconvert --to markdown notebookname.ipynb


```python

```
