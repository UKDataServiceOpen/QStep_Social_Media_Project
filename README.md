![UKDS Logo](./images/Logo.png)<br>
<br>
# Q-step project and supporting materials
This repository is under construction. Work is being done to ensure that the data associated with project is shared correctly in compliance with the terms, conditions and best practice for data sharing. 

## Topics 
Reproducibility details for the QStep 2021 Social Media Project. In this project we needed to collect data across multiple cities during "Veganuary 2019". We chose to cover Manchester, London and Preston.
Researchers - Sima Aykin and Rumeysa Piskin
Supervisors - Dr. Jools Kasmire and Joseph Allen

## Materials
### code 
Collect tweets
```
twarc2 search --archive --start-time "2019-01-01" --end-time "2019-01-30" '(vegan OR plant-based OR "plant based" OR veganism) point_radius:[-0.127758 51.507351 5mi]' londonGeoPointRadius.jsonl
twarc2 search --archive --start-time "2019-01-01" --end-time "2019-01-30" '(vegan OR plant-based OR "plant based" OR veganism) place:london' londonGeoPlace.jsonl
twarc2 search --archive --start-time "2019-01-01" --end-time "2019-01-30" '(vegan OR plant-based OR "plant based" OR veganism) point_radius:[-2.242631 53.480759 5mi]' manchesterGeoPointRadius.jsonl
twarc2 search --archive --start-time "2019-01-01" --end-time "2019-01-30" '(vegan OR plant-based OR "plant based" OR veganism) place:manchester' manchesterGeoPlace.jsonl
twarc2 search --archive --start-time "2019-01-01" --end-time "2019-01-30" '(vegan OR plant-based OR "plant based" OR veganism) point_radius:[-2.703440 53.757729 5mi]' prestonGeoPointRadius.jsonl
twarc2 search --archive --start-time "2019-01-01" --end-time "2019-01-30" '(vegan OR plant-based OR "plant based" OR veganism) place:preston' prestonGeoPlace.jsonl
```
these are then converted into .csvs with the following:
```
twarc2 csv londonGeoPointRadius.jsonl londonGeoPointRadius.csv
twarc2 csv londonGeoPlace.jsonl londonGeoPlace.csv
twarc2 csv manchesterGeoPointRadius.jsonl manchesterGeoPointRadius.csv
twarc2 csv manchesterGeoPlace.jsonl manchesterGeoPlace.csv
twarc2 csv prestonGeoPointRadius.jsonl prestonGeoPointRadius.csv
twarc2 csv prestonGeoPlace.jsonl prestonGeoPlace.csv
```
These tweets then go through a tidying process, as seen in the data tidying notebook.

Statistical Analysis
We used Google Collab to make our analysis reproducible. As such the analysis for each city are as follows:
London Analysis
Manchester Analysis
Preston Analysis

### data 
The data for this project will be stored in the `/data` folder. Currently, there is nothing there as the data is being evaluated for data sharing rules. 

The data collected was tweets with following fields:
ID
created_at - time the tweet was created
text
user id
username
screenname
location
follower count
tweet created at
geolocation
retweet count
favorite count 

The collected data was restricted to the selected locations, dates, limits per day, and to original tweets, not replies or retweets.

### slides
### other materials

## Data sources and licenses

Data Acquisition
This data was all collected with the Twitter API, at the academic tier.
We made use of the Twarc package to collect our data. 

## images
## Further Information
